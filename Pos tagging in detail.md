
## POS Tagging in Detail
This section goes over the Universal POS tags and their assignment for Hebrew text, taking into account UD HTB practices and guidelines for data from the Web, and in particular User Generated Content. For confusing cases, consult the subsections of Confusing Cases, which are headed “TAG1 or TAG2” in alphabetical order of tags (e.g. NOUN or VERB). 

Note that some categories are closed class, meaning that no words should receive those tags if they are not already attested with these tags in gold data. Lists of words within closed classes should be kept up to date if new words are ever added when encountering new cases in text.

### Open classes
#### ADJ

The ADJ category encompasses words with variable gender and number which may modify nouns as adjectival modifiers (see deprel amod) or stand as predicates. In both cases, they are inflected to match the described entity.

The ADJ category inflects for the morphological feature categories Gender and Number.

Tests for being an adjective include:
-	Inflection: גדול/גדולה/גדולים/גדולות
-	Definiteness agreement: ה בית ה גדול (the word גדול agrees in definiteness -> ADJ)
-	Comparison: יותר גדול

Typical adjectival formations appear in the pattern qatil (e.g. בהיר) and by formation with the suffix -י often from nominal stems (e.g. חתולי). 

Compound adjective bases are also tagged ADJ and take a dependent with the deprel compound, for example:

חסר/ADJ אחריות/NOUN

For adjectival/adverbial prefixes such as בלתי, תת see compound:affix.

#### ADV
The tag ADV is given to oblique modifiers of VERB and intensifiers of ADJ tokens when the ADV head is not modified by a preposition (otherwise, see NOUN and the deprel obl). These modifiers typically specify spatio-temporal, manner and purpose for VERB parents (אז, שם, כך, לפיכך), and degree (מאוד, פחות) for ADJ parents. Only ADV tokens (or equivalent multiword expressions chained via the deprel fixed) may carry the advmod deprel.

This class includes untokenized fixed prepositional phrases and definite adverbials, such as היום, לעיתים etc. which are treated as one token in segmentation. Note that similar expressions which are segmented would not be labeled ADV, but rather receive a compositional analysis as NOUN, e.g.
ב/ADP מהירות/NOUN

Negation is also treated as an adverbial modification, e.g. 
לא/ADV שמעתי/VERB

The most common Hebrew adverbs include:

לא, גם, יותר, רק, אולי, אתמול,שם, אז, כך, ביותר, כבר,דווקא

For adjectival/adverbial prefixes such as בלתי, תת see compound:affix.

#### INTJ

The tag INTJ is given to interjections, interpreted fairly broadly: this category is used for exclamative sounds and hesitation markers (אה), as well as pleasantries or insults that do not saturate a syntactic participant role in the sentence (e.g. בבקשה, חרא). The same items are typically attached via the deprel discourse. 

Particles accompanying vocatives and imperatives also fall into this category, e.g. 

נא/INTJ לבוא/VERB
הו/INTJ שוטה/NOUN 

#### NOUN

The tag NOUN is given to all common nouns, including abstract and concrete references to people, places, things and ideas, as well as deverbal nouns (שמות פעולה). Note that proper nouns (i.e. names) are given the separate tag PROPN. 

NOUNs carry the Gender and Number morphological features. Nominalized participles (בינוני) which carry an article or serve an argument structure role as a participant in a predication are tagged NOUN as well, whereas predicate participles are tagged as VERB (see also NOUN or VERB?).

#### NUM

The NUM tag is given to numerals, whether spelled in Arabic numerals or as words, as well as other types, such as Roman numerals etc. Note that ordinals do not constitute NUM, but are typically tagged as ADJ (e.g. ראשון, שני).


#### PROPN

The tag PROPN is given to proper nouns, which are nouns referring to named, typically uniquely identifiable entities, such as דינה, גוגל, צרפת. 
Note that in the original HTB, transparent common noun components of institutional names are tagged NOUN, e.g. 

אוניברסיטת/NOUN בוסטון/PROPN

We revise this to:
אוניברסיטת/PROPN בוסטון/PROPN

Note that lemmatization does revert transparent morphological inflection even on PROPNs, meaning that the lemma will be אוניברסיטה, not אוניברסיטת.

More generally, within each span of tokens designating a name, any token that is otherwise a NOUN will be tagged PROPN, but all other POS tags are retained unchanged. More examples:

-	רמת/PROPN גן/PROPN
-	קיבוץ/NOUN עין/PROPN ה/DET שלושה/NUM

Function words inside names are tagged as usual (not PROPN). Dependency relations for syntactically transparent name constructions are analyzed compositionally (for names with opaque syntax, see flat).


#### VERB

The tag VERB is given to morphological verbs in Hebrew which can express tense, including participles when used as a present tense form (see NOUN or VERB?). It does not include a specific subset of auxiliaries (see AUX) or verbs used as a copula (see COP). It additionally includes some non-morphological predicate forms listed below.

Normal tensed verbs carry the morphological features Tense, Voice, Number, Gender, Mood, VerbForm and Person. Additionally, the Hebrew-specific category HebBinyan expresses the morphological paradigm that a verb belongs to, using one of the seven traditional pattern names (e.g. PAAL, PIEL, etc., see HebBinyan).

Modal and copula verbs are assigned with the morphological features VerbType=Mod and VerbType=Cop, respectively.
 
In addition to these, the following items are tagged as VERB:

-	Absolute existentials יש, אין and inflected forms ישנו, איננה etc.
-	The otherwise auxiliary modals (see AUX) when used as a main predicate, i.e. when they are not auxiliary to anything else. For example:

tree

### Closed classes
Note: UD also uses a tag PART for particles, which is not currently in use in UD HTB. If we want to use this tag, we can consider adding guidelines for it.

#### ADP

The tag ADP is used for adpositions, which in Hebrew designates either simple (i.e. single token) prepositions or complex (multi-token) ones, whose components are attached to the first word in the complex expression. The preposition is attached to the head of its phrase with the deprel case. The following list is based on HTB’s contents and is intended to be exhaustive, though further prepositions which are not listed yet can potentially be added after careful consideration.

List of single token prepositions:
|     אחרי      |     אל         |     אצל      |     את       |     ב         |
|---------------|----------------|--------------|--------------|---------------|
|     באוזני    |     באמצעות    |     בגדר     |     בגין     |     בטרם      |
|     בידי      |     בין        |     בלי      |     במקום    |     במשך      |
|     בעקבות    |     בפני       |     בקרב     |     בתוך     |     בתוככי    |
|     דרך       |     החל        |     חרף      |     כ        |     כגון      |
|     כדי       |     כלפי       |     כמו      |     כנגד     |     ל         |
|     לאור      |     לאורך      |     לאחר     |     לבין     |     ליד       |
|     ללא       |     למען       |     למרות    |     לעבר     |     לעומת     |
|     לפי       |     לפני       |     לרבות    |     לרגל     |     לשם       |
|     לתוך      |     מ          |     מאשר     |     מבין     |     מבלי      |
|     מול       |     מחמת       |     מלבד     |     מן       |     מעבר      |
|     מפני      |     מתוך       |     מתחת     |     נגד      |     נוכח      |
|     ע"ש       |     עד         |     על       |     עם       |     פי        |
|     של        |     תוך        |              |              |               |

In complex prepositions, components derived from other POS tags retain their original tags, while the entire expression is attached using the deprel case.

tree

#### AUX

The AUX category is used for four main kinds of words: verbal copulas attached with the deprel cop, tense auxiliaries, assertive auxiliaries (negation with אינו), and modals attached to a lexical predicate with the deprel aux. Note that independent modals (e.g. צריך+NOUN) are not tagged as AUX, but as VERB. Pronominal copulas should be tagged PRON.

Typical copula cases follow this pattern:

tree

Tense auxiliaries include forms of היה forming a past progressive or counterfactual conditional (irrealis) together with a participle, for example:

tree

Assertion auxiliaries of the type אינו\איננו are analyzed as follows

tree

Finally, modal auxiliaries include items such as יכול, צריך, רוצה etc. which modify a lexical head VERB to indicate modality. Note that in keeping with other UD treebanks, impersonal modals with subject infinitive clauses are analyzed differently (אפשר, אסור and also צריך without an experiencer subject); see the deprel csubj for more details and examples.

tree

The following lemmas may be AUX:
-	יכול, צריך, חייב, מוכרח, מסוגל
-	אינו, אין, הינו, היה
-	מוכן, רשאי, זכאי, צפוי
-	עשוי, עתיד, אמור, עלול

#### CCONJ

This tag is given to coordinating conjunctions, most commonly ו, או, אבל and similar words. The first conjunct governs all subsequent ones as conj, while the coordination is governed by its immediate successor head as cc and given the POS tag CCONJ.

tree

The following lemmas may be tagged as CCONJ:

-	אך, אבל, אולם
-	או, ו
-	אלא (לא X אלא Y)

#### DET

The tag DET is given to determiners which specify (in)definiteness (ה, כמה) or quantification (כל, הרבה) for a single noun phrase, usually attached as det. The following lemmas may serve as DET:
-	ה
-	כל, כמה, מִדֵי ('מִדֵי יום')
-	רוב, שאר, הרבה 
-	אף, שום
-	מספיק, מספר

Note that those items which can appear in construct or absolute state, the absolute state rendition implies separate noun phrases for the quantifier and the quantified phrase. In keeping with other corpora, DET items are still tagged DET in such cases, but are no longer given the deprel det, i.e. הרבה תלמידים is det, but הרבה מהתלמידים is regular PP modification (nmod). In both cases, הרבה is tagged DET.

#### PRON

The PRON tag is given to several kinds of pronouns, including personal pronouns (אני, הן), demonstrative pronouns (זה, אלו), interrogative pronouns (מי, מה) and copula pronouns (א הוא ב). A complete list of lemmas which are allowed to take the PRON tag:

-	הוא (incl. forms אני, את, הם…)
-	זה
-	כך
- כן
-	עצמו (note: not segmented, per HTB conventions)
-	אותו (unsegmented and tagged PRON only in the sense the same one)
-	זהו
-	מי
-	מה
-	כלשהו
-	דנן
-	איזה

Note that the word כךis tagged as PRON only when it is accompanied by a preposition; when appearing by itself, it is tagged ADV. The pronominal adverbs, incl. Interrogatives, are tagged ADV (איכשהו, איפשהו, מתי, איך, איפה)

Copula pronouns are tagged PRON as usual and given the deprel cop:

tree

Pronouns carry Gender, Number, Person (where relevant), and PronType morphological features.

#### SCONJ

The tag SCONJ is given to subordinating conjunctions which mark the function of the clause they introduce, including adverbial clauses, direct speech and relative clauses. Note that this includes uninflected relative markers (ש, אשר) and the article-like conjunction ה when introducing a relative clause, typically with a participial (beinoni) modifier, for example:

tree

Note that the main criterion for identifying this construction, as opposed to an ADJ with an agreeing article (ה as DET and not SCONJ), is the substitutability with ש - for example in:

-	כל הדרישות החשובות לכם

The embedded predicate חשובות is not a VERB, but we still attach it as acl:relcl, and tag ה/SCONJ, since it is equivalent to “כל הדרישות שחשובות לכם”. That said, in some archaic/elliptical constructions, substitution with ש is not possible and we still assign SCONJ to ה, specifically the “whosoever” type construction in:

-	כל המציל נפש בישראל… (=כל מי ש)
-	הבנה בסיסית של המתרחש (=מהשמתרחש)


The following simple lemmas are allowed as SCONJ:
-	ש, אשר, ה
-	כי, אם
-	כפי, ככל, כשם
-	אם, שמא
-	באם, האם
-	כש, מש, לכש, כאשר
-	ו' (במקרה ו... הלוואי ו... ייתכן ו...)
-	במקום
-	בטרם
-	בעוד
-	ב, כ, מ
-	משום, כיוון, מכיוון

Note that in multiword expressions serving as SCONJ, constituent tokens will receive their regular POS tags, though they will be attached to the first token in the SCONJ expression with the deprel fixed.

tree

### Special symbols and other cases
#### PUNCT

The tag PUNCT is used for non-alphabetic tokens which delimit text, such as commas, parentheses, periods, etc. Similar symbols which are pronounced, such as currency symbols, hyphens meaning ‘to’ (between numbers), measurement units, etc. are not PUNCT, but SYM.

#### SYM
The tag SYM is given to non-alphabetic tokens which are pronounced and serve some function in the sentence, for example hyphens meaning ‘to’ (between numbers), currency symbols, etc.

#### X

The tag X is used for words that cannot be assigned a real or ‘linguistic’ part-of-speech category, either because we do not know it (garbled text, gibberish), or because it is not in Hebrew. The latter category encompasses only cases of true “code switching” or foreign text cited verbatim within Hebrew data; it does not include syntactically integrated use of loan words.

### Confusing cases
#### ADJ or NOUN?

Nouns are sometimes used within adjective-like constructions, such as comparison. For such cases we retain the NOUN tag based on the underlying morphological category of the word, rather than the syntactix usage:

מי יותר גבר/NOUN?

For uncertain NOUN/ADJ cases in which a possible noun exhibits gendered forms

Specific lemmas which are conventionally analyzed as ADJ even when not used as amod include: אחר, קיים

#### AUX or VERB?

Strong uses of היה to indicate pure existence or possession are tagged VERB, not AUX (e.g. היה אוכל; היה לי כלב).

Impersonal modals are VERB, not AUX (אפשר, אסור), while modals which can be impersonal are only VERB in that construction. Strong modals (with nominal object) are VERB (note they can take accusative objects marked by את):

-	AUX: אני צריךללכת
-	VERB: צריךללכת
-	VERB: אני צריך את המטריה

#### DET or SCONJ?

The definite article DET is used to modify nominals, including nouns and adjectives, while SCONJ is used to modify relative clause heads, typically VERBs and most often present tense forms. A test for SCONJ status is substitutability with ש as a relative marker. Compare:

tree

tree

In the first example, it would be very odd to replace ה with ש, (cf. הגרעין שמייסד?), but in the second example it is possible to retain the same sense with ש (cf. הודעת תנחומים שממוענת…).

#### NOUN or NUM?

For nominalized ordinal numbers, we use the NOUN category, based on the the logic that ordinals are generally ADJ and not NUM, and so the usual treatment of nominalized ADJ applies:

-	מקבעים את אבני השפה אחת/NUM בצמוד לשנייה/NOUN

In this example, אחת is a cardinal number, and therefore tagged NUM. Howeverשנייה is an ordinal functioning as a NOUN (the equivalent for ‘one’ would be ראשונה ‘the first’, which in this context would also be tagged NOUN, and generally as ADJ).

#### NOUN or VERB?

One of the trickier places to distinguish NOUN and VERB is in participles (בינוני) where predicative cases should be tagged VERB, while argument structure participants should be tagged NOUN. The easiest subtypes to resolve are:

-	If a participle carries a definite article or similar determiner, it is a NOUN (but note that the relative marker ה where it is interchangeable with ש does not constitute a determiner for this purpose)
-	If a participle has a subject dependent, it is likely a VERB. An exception to this rule occurs when the predication is actually a form of equative nominal clause, in which case a copula can typically be inserted (for example in יוסי מדריך “Yossi is a guide”, the participle is a NOUN, because we can insert יוסי הואמדריך)

#### PUNCT or SYM?

The main criterion for identifying SYM is pronunciation - PUNCT is generally not read out as a word. Some things that are SYM: $, ₪, / (pronounced “קו נטוי” or “או”), “-” in “3-4” and emoticons/emoji.

The following are PUNCT and not SYM: “-” in “בית - דין” or in “- היא אמרה- ”, the symbol “*” separating paragraphs in a story or unpronounced separators inside a phone number.

#### X or NOUN/PROPN?

The category X is not used for syntactically integrated loanwords, even if they are spelled in foreign characters:

-	אין לי מניות ב-SpaceX/PROPN
