## Appendix: Notes on HTB Conversion

The following notes document the main changes undertaken in the HTB for use as a training basis in the tools used to produce new IAHLT Hebrew data.
### Tokenization
During conversion, ‘inserted’ tokens, such as unexpressed definite articles after prepositions, were removed, and replaced with a definiteness feature where relevant (see Removal of reconstructed articles and של/את above).

#### Notes:
-	The majority of cases of inserted tokens have leading/trailing underscores as shown above – these were relatively easy to identify, though fixing them was quite complex in terms of realigning tokens to supertokens
-	In some cases, the fused token takes the lemma form of the pronoun (e.g. אנחנו), but not always (sometimes נו) - normalized to match text form (נו)
-	A further subset of cases was identified with no leading/trailing underscores – these were recognized based on implausible sequences of POS tags/lemmas (e.g. supertoken containing NOUN followed by של and PRON)

### Morphology
-          Added definiteness and article feature to elided article subtokens:

#### OLD:
```
22-24    	לעובדים  	_           	_           	_             	_           	_           	_           	_             	_
22         	ל           	ל           	ADP     	ADP             	_           	24         	case      	_             	_
23         	ה_         	ה           	DET     	DET             	Definite=Def|PronType=Art    	24             	det        	_           	_
24         	עובדים    	עובד       	NOUN  	NOUN             	Gender=Masc|Number=Plur    	20             	nmod    	_           	_
```
#### NEW:
```
22-23    	לעובדים  	_           	_           	_             	_           	_           	_           	_             	_
22         	ל           	ל           	ADP     	ADP             	Definite=Def|PronType=Art         	23         	case             	_           	_
23         	עובדים    	עובד       	NOUN  	NOUN             	Gender=Masc|Number=Plur    	20             	nmod    	_           	_
24         	מתחת     	מתחת     	ADP     	ADP             	_           	26         	case      	_             	_
```

Note that adding the features on prepositions, rather than nouns, is consistent with treatment of regular definiteness, since where a normal ה is present, definiteness is marked on the article, not the noun (so we should not mark it on the noun here either).

#### Other changes:
-	Poss=Yes was added for fused possessive pronouns, added this since it can be automated easily.

#### Lemmatization
-	Added missing lemmas for items formerly lemmatized “__” (e.g possessed אח)
-	Normalized final letter lemmas like ח"ך -> ח"כ and bizarre wrong lemmas (e.g. הכול was consistently lemmatized to הכיל in HTB…)
-	Lemmatized חצי to חצי (was consistently: חץ)
-	Lemma of הכול was consistently wrong as ‘הכיל’, fixed to be itself
-	All cardinal numbers lemmatized to unmarked feminine form
-	All demonstrative pronouns lemmatized to זה except זהו/זוהי (lemma=זהו) and הללו (lemma=הללו, since it is not segmented, but actually corresponds to הזה, which is segmented, and not to זה)

#### POS tags
-	HTB oddly annotates the interrogative pronouns מי and מה as ADV, except for the forms מיהו and מהו which are lemmatized to מי and מה but tagged PRON. These forms receive normal grammatical function labels, such as nsubj or obj, and it is not clear why they should be considered adverbs – they were therefore changed to be PRON whenever they do not have the deprel advmod.
-	Tagged חצי as NUM, not NOUN.
-	ה used to introduce a relative clause is mark, so it cannot be tagged DET; changed to SCONJ as per the UD guidelines.
-	Some questionable POS tagging conventions from HTB were kept (in some cases since they are consistent and difficult to change automatically):
-	Nominalized participles are often tagged as VERB, for example consistently so for חולים in בית חולים - the VERB tag was retained and also used in new gold data for consistency with the original HTB decision, but this may be something to review in the future. In new data, lexicalized nominalized participles for which HTB does not have a convention were generally tagged as NOUN.
-	Copulas in HTB are often VERB, which is invalid in current UD validation, so they were changed to AUX. However, for the forms הוא, היא etc., it seems more plausible to tag them as PRON, which is also allowed as a copula POS tag, so this practice was changed to PRON. 

#### Dependencies
-	Fixed recurring invalid attachment to auxiliaries (should connect to VERB), e.g. for mark:

tree

-	Reattach cc dominated by cc to intervening parent of conj (HTB conversion error?)

tree

-	Change PRON advmod to nmod or obl as appropriate

tree

-	Change אחד, חלק and similar words labeled as PRON/det (which is invalid) to be the head of  the phrase (note this is also more correct for entity recognition and agreement, since the phrase is singular and both the ‘אחד’ and the plural noun are separate referring expressions (relevant also for entity tagging)

OLD: (invalid)

tree

NEW:

tree

#### Removal of some subtypes
As discussed, case subtypes such as case:gen and case:acc for של and את respectively were removed, as well as the subtype mark:q for האם and שמא.

#### Addition of passive with nsubj:pass
This subtype was added based on the morphological Voice feature of the head of an nsubj relation.

Corrupted text
HTB seems to have an odd inversion of textual numbers, spelled ‘right to left’:
28-29   ב01  	_      	_      	_      	_        	_      	_      	_      	_
28    	ב      	ב      	ADP	ADP	_        	30    	case 	_      	_
29    	01    	01    	NUM   NUM   _        	30    	nummod      	_      	_
30    	אלפים   אלפים   NUM   NUM        	Gender=Masc|Number=Plur  27        	obl   	_      	SpaceAfter=No
Corrected these cases to:
27-28   ב10  	_      	_      	_      	_        	_      	_      	_      	_
27    	ב      	ב      	ADP	ADP	_        	29    	case 	_      	_
28    	10    	10    	NUM   NUM   _        	29    	nummod      	_      	_
29    	אלפים   אלפים   NUM   NUM        	Gender=Masc|Number=Plur  26        	obl   	_      	SpaceAfter=No
 Opened issues in UD_Hebrew:
https://github.com/UniversalDependencies/UD_Hebrew-HTB/issues/26 
But the correction was heuristic and based on the supertoken text – this might be worth letting someone go over manually/by comparing with the original TB, since some inverted numbers might be present which were not part of supertokens (so there is no record of their correct textual representation in the data).
Similar problems show up with mangled final letters and some other inserted tokens which are incorrectly reconstructed, opened issues with examples here:
https://github.com/UniversalDependencies/UD_Hebrew-HTB/issues/27
https://github.com/UniversalDependencies/UD_Hebrew-HTB/issues/28 
Data fixed heuristically in our new version (fixed manually for the cases in issue #28).
