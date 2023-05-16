## Dependency Relations in Detail
### Core Arguments
Our annotation guidelines encompass all UD core argument relation types. iobj is rare (formerly unused), since Hebrew does not have core marking for indirect objects, but can rarely use the object marker et (recipients and similar arguments are mostly mediated by the preposition ל and are therefore attached regularly as obl. 

We also distinguish the commonly used nsubj:pass and csubj:pass for subjects of passive voice verbs.


#### nsubj

This function label is used for the syntactic subject of a clause, be it a finite verb’s subject, which typically agrees in number and gender with the finite verb, or the subject of a nominal sentence, either marked by a copula, or without an overt copula. These three most common constructions are illustrated below:

-	Finite verb subject:

tree

-	Overt copula (same analysis also with forms of היה, ADJ predicates, etc.)

tree

-	No copula:

tree

The nsubj label is also used for existential predication (יש\אין) as well as possessive constructs (יש ל\אין ל).

tree

This holds true for יש את as well (with its past or negative אין את, היה את), as in Modern Hebrew the את here does not mean the accusative, e.g.

פה בסיפור הזה אין ויכוחים בין המשרדים, יש פה את משרד החינוך.

The construct is a similar one on both parts of the sentence - the only difference is it's negative and indefinite at the start, positive and definite at the end. 


The את does not change משרד החינוך into an object on its own, in an otherwise obvious subject construct.

את is (mostly) required for a definite existential or possessive construct in Modern Hebrew (פה בסיפור אין הוויכוחים*).


The את is depreled case, with no Case=Acc feature. 
 ~~(for יש ל see obl, for יש את see obj).~~



In nested predicates where the nesting predicate is in a copula clause with its subject, two nsubj relations are possible for the same head. For example:

tree

#### nsubj:pass

This label is used for subjects of finite passives as well as predications with passive participles:

tree

tree

#### obj

The obj label is given to direct objects not mediated by a preposition, as well as definite direct objects mediated by the object marker את, which is attached to the head of the object phrase as case.

-	Direct object without את:

tree

-	Object with את:

tree

Note that pronominal objects with forms of את + suffix pronouns are analyzed in the same way:

tree

~~Additionally, accusative marked objects of the possessive construction are marked with the obj relation, unlike indefinite existentials which are labeled nsubj (see nsubj for יש + noun phrase).~~

Note that יש את is not tagged obj; see nsubj.

#### iobj
The iobj label is used very sparingly, since Hebrew doesn’t incorporate a clear indirect object marking, which is usually mediated by a preposition (obl). 
It is marked in some limited usage, with the same object position marker את, only when the regular object position itself is also marked (i.e. only when there is another object or ccomp):

לימדתי אותו את השיר   -  Since the direct object position is saturated, we mark the indirect as iobj

לימדתי את משה שאין מה לעשות לגבי זה the clausal ccomp in the object position,the PN in the iobj


Note: cognate objects (מושא פנימי) are not to be tagged as such, but with obl:npmod:

לימדתי את משה את הלימוד  -  halimud is cognate, and is obl:npmod, so moshe is obj. npmod,obj

These constructs are quite peculiar to Hebrew (and other languages) and behave a bit differently than regular objects, more of an echo or emphasis to the subject, i.e. they should not be treated as true objects, as conflicting with regular syntax theory that two direct objects are impossible. Further discussion is here - https://github.com/UniversalDependencies/docs/issues/832.

For guidelines for distinguishing obj, obl:npmod from plain obj, iobj, see obl:npmod section.

#### csubj

The csubj relation is used analogously to the nsubj relation in cases where the subject is a clause, for example an infinitive clause, a complementizer ש clause (less common) or a plain finite clause (rare). If the predicate is a passive verb or participle, see the csubj:pass relation instead.

tree

When in doubt about complement clause (ccomp) vs. subject clause status, consider whether the corresponding question could be posed with ‘את’, or whether it could be replaced by “את זה”:

-	מה היה נדמה? שדיסני עלתה שוב על הסוס
-	*את מה היה נדמה? שדיסני עלתה שוב על הסוס
-	*היה נדמה את זה

note that ADV can also govern a `csubj`, in case of -

- אל לרגש לגבור על השכל

The token אל is tagged ADV (Polarity=Neg) and govern רגש through `obl` and לגבור through `csubj`.

#### csubj:pass

This relation is analogous to csubj, except that the predicate is a passive finite verb or predicative passive participle (בינוני פעול). This does not include possible ‘mediopassives’ (Voice=Mid) where an action is not truly passive, but uses a reflexive binyan to indicate benefactivity or self-interest of the agent (for example נמאס is usually not a true passive). A common test for passive as opposed to medium forms is the possibility of introducing a by-agent (על ידי…, e.g. * נמאס על-ידיי לעבוד is odd, but הוא נרצח על ידיהם is grammatical, i.e. a true passive). See the Voice feature under Morphology for more details.

 Some examples of csubj:pass:

tree

tree

tree

#### ccomp

The label ccomp is used for complement clauses, often of speech or psych verbs which take content clause arguments:

tree

This label is not used for complement clauses of nominals (e.g. deverbal nouns) which are instead labeled acl (see acl).
ccomp is also used for mid and pass verbs, but not in the subject position (see csubj).

Note: when the object position is already saturated, we cannot tag an objectival ccomp again.
This has limited consequences, e.g. שם לב כי זה קרה since lev is obj, we tag the clause advcl.

#### xcomp

The label xcomp (external or ‘open’ complement clause) is used for non-finite complements of verbal or adjectival predicates which structurally lack an overt subject, but whose subject is inferred to be an argument of their dependency parent. The most typical cases involve subject or object control (PRO control in classic Government and Binding theory), where the unexpressed subject of the xcomp infinitive is coreferent with the subject, or more often object of the superordinate verb. For example:

-	Direct object as external subject: (object of מכריח is the subject of לנסוע)

tree

-	Subject sharing: (subject of רצו is also the subject of להמשיך)

tree

-	Prepositional object: (the subject of ‘ללכת סביב’ is ‘מטוס’, the prepositional object of the parent verb, למנוע)

tree

Care should be taken not to label plain infinitival adverbial clauses (purpose clauses) as xcomp - these should be advcl. A common test is ability to insert כדי: 

tree

Additionally, the xcomp label is used for the secondary predicate of verbs meaning ‘become’ or similar, which do not take true objects (and are incompatible with את), for example:

tree

Note how in this example, it is not possible to say “היא נעשית את מורה”. Use of the label xcomp in such cases in UD is based on an analysis (originally from the LFG literature) which interprets ‘become’ predicates as involving a secondary predication with coreferring subjects, viz. “[she becomes - [she is a teacher]]”. Also note that this analysis is not applied to ‘become’ verbs with overt PP secondary predicates, which are analyzed as obl using the usual guidelines:

tree

Additionally, the `xcomp` label is used for the structures בשם and מסוג (the tokens שם and סוג govern through `xcomp`)

- ילד בשם דני
- צהבת נגיפית מסוג הפטיטיס


### Non-Core Dependents
#### advcl

This label is used for all oblique clausal dependents, including adverbial clauses proper, whether finite or non-finite (temporal כש, locative היכן ש, purpose כדי, conditional etc.), and oblique argument clauses, due to the lack of an argument/adjunct distinction in UD (e.g. אני מחכה לכש...). As with all UD clausal dependents, attachment proceeds from head to head, from the governing predicate head to the subordinate predicate head. 

-	Plain finite adverbial clause:

tree

-	Infinitival adverbials clause:

tree
  

Typical advcl constructions are introduced by the following subordinators (not an exhaustive list; see also mark):

-	Conditional: אם, אילו, לו
-	Temporal: כש, כאשר
-	Causal: בגלל ש, כיוון ש, היות ש, הואיל ו
-	Purpose: כדי, כדי ש, על מנת ש
-	Concessive: למרות ש, אף על פי ש
-	Manner/means: כך ש, בלי ש
-	Extent:	ככל ש

Note that advcl is not used for infinitival complement clauses which take the xcomp relation (see xcomp).

#### advmod

This label is used for adverbial modifiers, including modifiers of VERBs, ADJ and ADV heads (the latter two typically for intensification), and, rarely, NOUNs. Note that according to UD guidelines advmod dependents may only be tagged ADV, unless they are the head of a multiword expression connected via the fixed relation (and therefore we assume the multiword expression as a whole functions as advmod).

Typical examples:
-	VERB modifier:

tree

-	ADJ modifier:

tree

-	ADV modifier:

tree

-	Less frequently, NOUN modifier - most cases involve NP modification with semantics like ‘also’, ‘only’ etc.:

tree

Note also in particular that advmod is used for most forms of negation:

tree

#### aux

This label is given to tense and modality auxiliaries of predicates, but not to impersonal modals which are themselves a main predicate. 

Tense auxiliary example:

tree

Modal auxiliary example:

tree

Note that in both of the above cases, the auxiliary is not the main lexical predicate, but rather serves to add tense or mood to a lexical predicate. This is not the case with the independent impersonal modals. Modal predicates which are not auxiliary:

tree

tree


Note that the infinitive attached to impersonal modals is typically a subject clause:

-	אי אפשר לדעת (.To know something is impossible = What is impossible? To know)

#### cop

This label is used for copulas, including tensed forms of היה as a copula (זה היה טוב), but not as a tense auxiliary (היא היתה הולכת). It is also used for pronominal copulas such as זה and הוא:

tree

Note that the copula can precede the subject, so care must be taken to identify and distinguish the subject from the copula:

tree

#### discourse

This label is used for interjections (היי), fillers (אה) and non-adverbial discourse markers (phatic כאילו). For clausal modifiers, attachment is to the clause root, but for phrasal phatic markers (כאילו, יעני) and fillers attachment is to the modified head, which usually follows the marker. For example:

-	Clausal modifier of root:

tree

-	Filler:

tree

-	Phatic adnominal dependent:

tree

It is also used for appellative particles in combination with a vocative, e.g.:

tree

#### dislocated

This relation is used for a right or left dislocated verbal argument, which is used in addition to the regular mention of that argument, as in the following example:

tree

Note that the dislocated argument is identified as the one that is farther from the verb, with the usual pattern being a heavy noun phrase being extraposed (either before the main clause, or postponed until after the verb), with the same argument being realized ‘redundantly’ as a pronoun in the canonical subject or object position. If the pronoun and lexical NP are realized on opposite sides of the VERB, we assume that the dislocated argument is the lexical one, which is usually set apart by a comma in writing. For example:

-	מוטי, הכרתי אותו (מוטי=dislocated)
-	הוא נחמד, מוטי (מוטי=dislocated)
-	אותו לא הכרתי, את מוטי (מוטי=dislocated)

Also note that in the bare hanging topic construction, the topic head is labeled dislocated  despite not bearing overt marking of the same function (as in the repetition of את in the last example). For example:

-	מוטי, אחותו נחמדה (מוטי=dislocated)

Here the dislocated mention is not explicitly marked as a possessor, though the second mention in canonical position serves a possessive function.

#### expl

The expl relation marks the placeholder expletive זה when it takes the position of a dislocated argument, usually a subject clause labeled csubj.

tree

Note that this construction can be identified by the possibility of omitting זה:

-	לא נכון שבישראל הוא היה סרסור

#### mark

This label is used for the subordinator (a.k.a. Complementizer, tagged SCONJ) in subordinate clauses, both finite and infinitival, most commonly ש or כי and multiword expressions (with fixed) headed by ש. It is attached to the subordinate clause head (usually a VERB or nominal predicate).

-	Finite argument clause:

tree

-	Infinitival adverbial clause:

tree

-	Multiword example (see also fixed):

tree

#### obl

This label is used to attach dependent nominals of verbs, adjectives and adverbs which have a preposition (i.e. a case dependent), as well as dependents of nouns if they are actually modifying an entire nominal sentence, rather than the noun in the narrow sense. The most common cases of prepositional modifications to verbs and adjectives are analyzed as follows:

-	PP modifiers of VERB:

tree

-	PP modifiers of ADJ/ADV:

tree

The more unusual case of modifying a nominal predication follows the pattern in the following example. Note that here the modifier is not actually modifying the noun, as in the subsequent example, which uses the nmod relation:

-	The obl relation attached to a predicate NOUN, indicating that the modifier belongs to the predication itself (‘being important’ is according to mulsim traditions; there is no noun phrase “בעל חשיבות גם לפי חלק מהמסורות...”)

tree

-	Normal nmod of a NOUN which happens to be a predicate (i.e. there is a noun phrase “מחווה למדענית”)

tree


To distinguish between these last two variants (which are only confusable for PP modifiers of copula predicate nouns), we can consider the possibility of movement for the PP modifier. Compare:

-	* למדענית שמו של השבב החדש הוא מחווה
-	גם לפי חלק מהמסורות המוסלמיות הסלע המזוהה כאבן השתייה הוא בעל חשיבות

The infelicity of the first example demonstrates that the modifier belongs in a single noun phrase with the noun מחווה, and therefore the usual adnominal nmod relation should be used.

This label is also used for adjectives or verbs that govern `case`s as כ and ב, for example: כ+ראוי, כ+רגיל, ב+רגיל. When it is governed by a predicate the anaysis is:

`obl`(**_predicate_**, ragil)

`case`(ragil, ka)

Additionally, obl is used for the possessor in predicative possessives when the possessor is marked with ל (this is in fact not an exception, but rather an application of the normal rule that prepositional dependents of VERBs are labeled obl). The direct object, marked by את, is labeled obj (but note that indefinite plain existentials are labeled nsubj; see nsubj):

tree

#### obl:tmod

This label is used for temporal modifiers of VERBs, ADJ and ADV which are not mediated by a preposition (e.g. extent: dance two hours, temporal: arrived 1992, etc.). Typical items taking this label include יום, שנה, דקה, שעה, שבוע, חודש, שנייה and year numbers or other date expressions without a preposition.

Examples:

-	Time of predicate:

tree

-	Extent:

tree

-	Temporal frequency:

tree

Note that temporal modifiers with prepositions are regular obl, and that temporal moidifiers of nominals (NOUN, NUM) are nmod:tmod:

tree

#### obl:npmod

This label is used to tag any oblique not mediated by a preposition (as well as obl:desc until it is implemented). The nominal equivalent is nmod:npmod. These tend to be adverbial, but also nominal and adjectival.

#### obj or obl:npmod?

Some את marker mediated words aren’t actual objects, but are cognate objects (מושא פנימי).
Sometimes appearing in pairs (i.e. one true object, one cognate), the distinction between a cognate object (obl:npmod), and a true object (obj), can further determine if we tag iobj or obj (iobj is only tagged when another obj appears, if it’s obl:npmod, the counterpart is a plain obj).

For intransitives, consider הוא רץ ריצה מהירה. The “fast running” is already implied by “ran”, and so “fast running” is a kind of addition for emphasis, which happens to be in an object position.
It is not truly dependant on “ran”, and can be its own NP - הוא רץ, [זו] ריצה מהירה with no problem.
Thus even הוא רץ את הריצה המהירה mediated by את, is a cognate object, tagged obl:npmod.

Transitives, though, are prone to mark objects by nature, and it’s harder to distinguish a true, dependant, complement like object, from a standalone addition in the object position (cognate). 

I baked the bread a thorough baking - It’s easy to see a thorough baking is its own NP.  
In שאלתי אותו שאלה חשובה - again שאלתי already conveys שאלה, which is standalone.

In האכלתי תינוקות דייסה it seems an obj,iobj case, as both are arguments truly licensed in a special way by the verb’s valency, not being able to be added to just everything.   
Such is the case with לימדתי אותו את השיר, while may seem השיר is an unrequired addition to לימדתי - it’s not the case. Both are again true objects, therefore a true obj, iobj case.  
The complement is השיר, a truly valent object by its verb, not standalone, as well as אותו.

See iobj section for additional discussion, as well as here - https://github.com/IAHLT/UD_Hebrew/issues/63#issuecomment-1126328193 and here - https://github.com/UniversalDependencies/docs/issues/832.

Further examples:
להטיל נטל כבד יותר על מערכות הביטחון הסוציאלי  obj - a collocation, but "lehatil" is still transitive

פוגע פגיעה קשה בזכותו החוקתית cognate npmod, notice "pogea oto" is bad, since not a transitive 


#### vocative

This label is used to denote direct appellation of an addressee, either in conjunction with an imperative, or as a non-argument mention of the addressee. For example:


tree

Note also that appellative discourse particles tagged INTJ (יא, הו) are attached to the vocative via the discourse relation.

### Nominal Dependents
#### acl

The label acl is used for all adnominal clauses that are not nominal clauses, including infinitive and finite clauses. Object clauses of deverbal nouns are also labeled acl (and not ccomp):

-	Adnominal infinitive clause:

tree

-	Finite adnominal complement clause, also labeled acl (and not ccomp, per UD guidelines)

tree

This label is only used if there is no possibility of introducing a resumptive pronoun, which would indicate that this is a relative clause.

#### acl:relcl

This label is given to the head (predicate) of a relative clause, whether it is introduced by an explicit relative pronoun (ש, אשר, ה labeled mark) or not (zero relative).

-	Explicit relative marker:

tree

-	The same, but note the non VERB predicate:

tree

-	Zero relative (note the possibility of inserting ש):

tree

A special construction which deserves mention is free relatives. In free relatives, a single word (the node word, usually an interrogative pronoun) serves a double role in both the main clause and a subordinate relative clause. In these cases, both functions cannot be annotated in a simple tree (though they are represented in Enhanced UD trees), and we therefore prioritize the matrix clause function, while allowing the word to govern the subordinate clause as acl:relcl. The following examples illustrate this:

-	Node word in predicate position:

tree

-	Node word in object position:

tree


To understand this analysis, we can consider what would happen if both functions of the node word would be separated into two words:
-	אז זה בדיוק הדבר שעשיתי אותו
-	לדעת את הדרך שבה יפעל וייראה התוצר הסופי

These paraphrases illustrate the existence of the two functions: in the first example, מה is replace by דבר (realizing the predicate function of מה) and אותו (its function as the object of עשיתי). Similarly for איך, the paraphrase reveals that it is both the object of ‘knowing’ and the oblique manner PP of ‘how the product will work’.

Note that this analysis does not apply to polar object clauses (i.e. “whether” clauses), marked by ‘האם’ or ‘אם’, which are seen as ccomp (i.e. אני יודע אם הוא בא is analyzed like אני יודע שהוא בא).

#### amod

This is the label given to adjectival modifiers of nouns, e.g.:

tree

Note that when the NP is definite, the second agreement article is attached to its adjective as det.

#### appos

This label is used for appositional nouns, which expand on an existing noun without adding an additional argument or participant to the clause (the appositive fills the same role as the noun it expands on). Apposition is expected to be reversible, i.e. we can say NP1 NP2, or NP2 NP1, though in practice this will sometimes sound odd. 

Example:

tree

Note we could say:
-	בן היישוב שנפטר לאחר מאבק ממושך במחלת הסרטן, חן שמיר

In cases of double or triple apposition, all appositive heads are attached to the first, argument function bearing head. In:

-	הרמטכ"ל, אביב כוכבי, איש קרית ביאליק…

The appositive heads אביב and איש would both be dependents of רמטכ”ל.

The following expressions are all examples of appos:

-	העיר חיפה
-	התוכנה בבילון
-	המילה “פופיק”
-	השנה 1990
-	האדון כהן (only with a definite article; אדון כהן would be flat)
-	השחקנית פאר

Note that common titles and appellations such as מר, גברת are analyzed as part of the name, tagged PROPN and taken as the first part of a flat relation if and only if they occur without an article. For items that can occur with or without an article, such as אדון כהן vs האדון כהן, the construction without an article is taken to be flat, but the construction with the article is taken to be appos.

The “city, state” construction is also conventionally analyzed as appos, in keeping with other UD languages:

-	בוסטון, מסצ'וסטס
-	פראג, צ'כיה

#### case

This label is used to mark prepositions, tagged ADP, which are attached to a nominal, indicating the lexical type of a prepositional phrase. Note that if the head of the phrase is verbal or forms a complete nominal predication, what would otherwise by a preposition will be tagged SCONJ and attached as mark instead. 

Compare:

-	Plain nominal head with the preposition בלי (tagged ADP):

tree

-	Nominal is actually part of a predication marked with the SCONJ complementizer בלי:

tree

For multiword prepositions, the POS tags can be ignored (i.e. they do not all need to be ADP) and the first word in the fixed chain is always the one attached as case regardless of any opinions about the possible internal structure of the multiword preposition.

tree

#### det

The label det is given to determiners of nominal heads, most often the article ה (except when used as a relative marker, see mark), and some other quantifiers, which crucially do not form a separate referring expression (see below for counterexamples). The most common Hebrew determiners are: 
-	ה, זה
-	כל, כמה, הרבה
-	שום, אף
-	אותו (אותו אחד)

Examples

-	Simple article:

tree

-	Compound article: (סמיכות)

tree

-	Quantifier:

tree

-	Postposed demonstrative:

tree

Agreement articles on attributive adjectives are also attached as det to their respective adjectives:

tree

This also applies to postposed demonstratives with an agreement article, resulting in ‘det of det’:

tree

Orthographically unexpressed articles are not attached via det, and their prepositions are attached via case as usual, though the morphological features of the ADP will express Definite=Def in such cases (see Definite). For example:

tree

Finally note that partitive or other referring expressions with a determinative sense are not labeled as det, in particular when they form part of a prepositional phrase, both the head and dependent in which could be referred back to with a pronoun. Compare:

-	No internal preposition, single referring expression:

tree

-	Preposition phrase, two referring expressions:\

tree

In the first example, the head is מירוצים, and only one referring expression is formed (a pronoun הם could only refer back to the entire כמה מירוצים, which creates exactly one participant in the sentence). In the second example, the head is כמה, which has an nmod prepositional phrase dependent, מהמירוצים. In this latter case a subsequent pronoun הם could refer back either to all races (המירוצים), or only to several races (כמה מהמירוצים), indicating that we are dealing with two full (but nested) NPs.

#### nmod

The label nmod is given to prepositional phrase dependent nominals of other nominals (adnominal PPs). These are prepositional phrases which are embedded in a noun phrase, for example:

tree

Note that it is not impossible to have an obl dependent of a NOUN, specifically when the NOUN is the predicate of a nominal sentence (see obl for more discussion):

tree

#### nmod:poss

This is a special subtype of nmod which is given to possessor phrases of two kinds: prepositional possessors with a case dependent של, and suffixal clitic possessor pronouns.

-	Prepositional possessor:

tree

-	Clitic possessor:

tree

This also applies for cases that are not really possessive, but contain של, like מהירות של 50 קמ”ש.

#### nmod:tmod

This label is used for temporal modifiers of nominals, not introduced by a preposition (for which we use the regular nmod). For example, years in dates are nominal modifiers, but not introduced by a preposition:

tree

#### nummod

This label is used for numerical dependents which indicate the quantity of a head nominal, regardless of how the numeral is expressed (spelled out, Arabic numeral, Roman numeral, Hebrew letters, etc.). 

tree

Numbers which commonly create a construct state with their enumerated noun are still analyzed as nummod:

tree

As compound numbers are not analyzed using the compound relation, in some cases, chains of nummod may be possible, for example:

tree

Note that not all Arabic numeral tokens are nummod.

tree

### Other
#### cc

This label is given to explicit coordinators, such as ו, או, אבל etc. They are attached the coordinate conjunct head following them, i.e. pointing backwards.

tree

#### compound:affix

This label is used for a set of prefixes forming complex words, but only when they are spelled apart. Some essential prefixes are:

-	בין, תת, דו, חד, תלת, פרו, קדם, אנטי, סופר, נאו, מולטי, מיני, אקס, כלל, פוסט, טרום, כל/כול, היפר, היפו, על, רב, פרה, אין

Some rarer prefixes can appear in more technical/specific contexts, and should be applied the Prefix=Yes feature, if the compound:affix deprel is appropriate. 
The above list is therefore not an exhaustive one.

Example:

tree


Note that compound:affix modifiers are usually tagged ADV (very rare exceptions are numerals in a prefix position, tagged NUM).

#### compound

This label (formerly called compound:smixut, now shortened to compound) is given to all non-head construct state dependents (סומך). For example:
-	Simple construct state:

tree

-	Nested construct state:

tree

This label is also used for left-headed compound adjectives:

מאכל מזרח תיכוני

`amod`(maaxal, tixoni)

`compound`(tixoni, mizrax)

Definite=Cons should be assign for those cases that are underlyingly smixut:

נוף בית ספרי

`amod`(nof, sifri)

`compound`(sifri, beit) BEIT\Definite=Cons

If the dependent is originally a PROPN (Tel Aviv - PROPN + PROPN) it should be tagged PROPN:

הטרילוגיה התל אביבית

`amod`(trilogia, avivit)

`compound`(abibit, tel) TEL\PROPN

#### conj

This label is given to the head of each coordinate conjunct after the first in a coordination. All non-initial conjuncts are attached to the initial one, creating a ‘fountain’ shape, rather than a chain - in “A, B and C”, both B and C will be attached to A. Any coordinating conjunctions will be attached to their conjunct heads as cc. Examples:

-	Plain coordination

tree

-	Multiple conjuncts (‘fountain’ shape)

tree

It is also possible to have nested coordination, in which case nested conjuncts may attach to the second conjunct (because they are not coordinate with the first in the chain):

tree


Note that `conj` is possible even when there is no `cc`, if you can insert 've':

בואו נעשה

`conj` (bou, naase)

#### dep

A dependency can be labeled as dep when it is impossible to determine a more precise relation. This may be because of a weird grammatical construction, or a construction for which none of the existing guidelines apply, with the understanding that we may want to go back and devise guidelines for such cases. The use of dep should be avoided as much as possible.

#### fixed

This label is given to multiword fixed expressions, and the dependency always proceeds from the first word of the expression to all subsequent words in a ‘fountain’ shape.

tree

The following fixed expressions are recognized:

**Prepositional** (`case`)

אל תוך | באשר ל | בהתבסס על | בהתחשב ב | בהתייחס ל | בהסתמך על | חוץ מ | מחוץ ל | חוץ ל | מחוצה ל | לבד מ | למעלה מ | מעבר ל | מעל ל | עד כדי | עד ל | קודם ל | על אודות | על אף (אף – ADV) | על גבי (גב – NOUN) | על ידי (יד – NOUN) | על פי (פה – NOUN) | על פני (פנים – NOUN) | תוך כדי | ב דומה ל | ב שונה מ | מעבר ל | מתחת ל | ב יחס ל | ב קשר ל | ב נוגע ל | יחד עם | ב יחד עם | נכון ל (נכון - ADJ) | מסביב ל | כש ל | ל כש | החל מ | כלה ב | על מנת (מנה – NOUN) | ב סמוך ל | לחלק ב (לחלק - VERB) | 
לחלק ל (לחלק - VERB) | פרט ל

**Conjunctions** (`mark`)

אם כי | אף על פי ש | אף ש | בגלל ש | כדי ש | כפי ש | כשם ש | לפני ש | למרות ש | מאחר ש | מפני ש | משום ש | על אף ש | עד ש | כך ש | היות ו | היות ש | היה ו | לאחר ש | בעוד ש | מבלי ש | בלי ש | על מנת ש | תוך ש | כל אימת ש | בלבד ש | לא בלבד ש | עד כדי ש | מכיוון ש | כיוון ש | ל כש | על אחת כמה וכמה ש | ה גם ש | הואיל ו | מה גם ש | אלא אם כן | כ כל ש\ה | אלא אם | כל עוד

**Coordinations** (`cc`)

ו אולם | ו אילו | כי אם 

**Adverbial** (`advmod`)

יותר מ | פחות מ | כל כך | אם כי | בבת אחת | על אחת כמה וכמה 


#### flat

This label is given to multiword names without a clear head structure (for example first+last name), tagged PROPN, with a ‘fountain’-like structure, in which the first token governs all subsequent tokens. Examples:

tree

Compositional names should not receive this analysis, and are analyzed based on the underlying syntax, though the PROPN POS tags still indicate that they are names:

tree

Non-compound complex names do use the flat relation, for example:

-	המכללה תל חי

In this case we can tell that the relation is not compound due to the definite article on the first word, and we connect מכללה to תל as flat (תל חי itself is compound). Note that in such cases the flat expression is itself a name, not an apposition (compare the following cases, which are appos: העיר חיפה, התוכנה בבילון, המילה “פופיק”, השנה 1990)

Common titles and appellations such as מר, גברת are analyzed as part of the name, tagged PROPN and taken as the first part of a flat relation if and only if they occur without an article. For items that can occur with or without an article, such as אדון כהן vs האדון כהן, the construction without an article is taken to be flat, but the construction with the article is taken to be appos.

#### goeswith

This label is given to incorrectly split-off tokens, which should actually be one word in correct orthography. It always proceeds from the first token-part to all subsequent parts. For example:

tree

#### orphan

This rare dependency replaces the relationship between an elided coordinate predicate with multiple dependents and its secondary dependents, by promoting its primary dependent to take its place. 

Based on the UD rules of promotion (see General Principles: Elliptical Promotion), when an elided head has multiple dependents, its primary dependent is taken to fill the role of the predicate (usually conj). However when there are multiple dependents, it is odd, for example, for a promoted conj subject to govern a direct object. In such cases, the secondary dependents are attached to the promoted token as orphan. For example:

tree

In this example, the elided second repetition of the VERB זקוקים triggers the promotion of its subject, משפחותיהם, which is now conj to the first זקוקים. The adverbial clause head לתמוך cannot be attached as such to משפחותיהם, since it is an adverbial clause which should attach to the missing VERB. The indirect relationship between the primary dependent (משפחותיהם, which is the highest ranked dependent of the ellipsis) and the secondary dependent (לתמוך) is therefore expressed via the orphan relation.

#### parataxis

The parataxis relation is used for two distinct scenarios: when two independent trees, usually full sentences, stand next to each other in the same orthographic sentence without an explicit coordination, and in the case of parentheticals, which do not belong to the superordinate syntactic structure. 

-	Coordinating (sentential) parataxis:

tree

-	Parenthetical parataxis:

tree

Note that the adverb אז can appear as a loose coordinator between sentences, but since it is not analyzed as cc, this case also triggers a parataxis analysis:

tree

Note that unlike coordination, parataxis is not considered transitive, and does not form ‘fountain’ shaped dependencies. Instead, multiple paratactic structures are arranged in a ‘chain’ shape, i.e. S1 -> S2 -> S3, where the head of each paratactic sentence is joined to the next (and not all to the first).

#### punct

This label is given to any and all tokens tagged as PUNCT (see PUNCT), which are generally punctuation marks which have no pronunciation (for pronounced symbols, see SYM). quoteאנרAttachment of punctuation in Universal Dependencies follows the following principles, but need not worry annotators due to its automation (see below):

1.	punct tokens always attach to content words (except in cases of ellipsis) 
2.	punct can never have dependents 
3.	punct separating coordinated units is attached to the following conjunct (to B in A, B)
4.	punct preceding or following a dependent unit is attached to that unit.
5.	Within the relevant unit, punct is attached at the highest possible node that preserves projectivity (i.e. avoiding crossing edges)
6.	Paired punctuation marks (e.g. quotes and brackets, sometimes also dashes etc.) should be attached to the same word unless that would create non-projectivity. This word is usually the head of the phrase enclosed in the paired punctuation.

Because punctuation attachment is so robotic, we generally apply the official Udapi FixPunct block to parsed and also manually treebanked output, in order to avoid meaningless variation in punctuation attachment. As a result, annotators can generally leave punctuation marks as attached by the parser, though care must be given to token mistagged as punctuation, or incorrectly not tagged as punctuation.

#### reparandum

The label reparandum is given to the highest possible head of an aborted phrase (e.g. due to disfluency, typos, etc.) and is attached to the head word or head of phrase seen as its replacement. For example in a plain repetition, the first instance is considered aborted, and the second instance is its replacement.

tree

If an aborted phrase has multiple words, they are analyzed as usual until the head of the aborted phrase is reached, which is then attached as reparandum.

##### root

The root label is a special label reserved for the unique dependency root of each sentence. There is exactly one root per sentence, and its head is always set to 0 (not dependent of any other token). The root token is generally the head of the predicate phrase (predicate VERB, ADJ, head NOUN of a nominal predicate, etc.) or the highest node in a non-predicate fragment sentence (e.g. head NOUN in a plain NP sentence, or the INTJ token in an utterance consisting solely of an interjection.

Nesting predicates in which a copula construction predicates a second predication also take the normal top level matrix VERB (or other predicate word) as their root. This can lead to situations in which a single root token is the predicate of two different subjects, from the nesting and nested predication, for example:

tree



### Confusing cases

#### obj or xcomp?

Only transitive verbs can govern accusative objects (including forms that get the explicit definite accusative object because of colloquial-origin language changes – יש לי את ה..., בא לי את ה...). Middle and passive verbs don't govern objects: the middle is a reflexive category with the mention of only one argument (which is a syntactic subject – it comes no explicit syntactic object). In a passive clause what is usually expressed by the object (or sometimes another argument) is now expressed by the subject.


The best way to check if a token is governed through `obj` is to apply the את ה... test:

השאלה נשארה פתוחה

*השאלה נשארה את הפתוחה


If an element can’t be modified by את ה... and there is no possibility to rephrase the sentence to make it work, this is not an `obj`. In this particular case the deprel is `xcomp`(nishara, ptuxa). In xcomps, there is always an implicit secondary predication: in this example, the question is both that which remains and that which is open; in other words, פתוחה is a secondary predicate which also applies to the same subject, שאלה

It should be noted that there are also active verbs that can fail this test:

הוא מרגיש חולה

*הוא מרגיש את החולה

`xcomp`(margish, xole)

Some dictionaries, like Even Shoshan, indicate if verbs are transitive or intransitive. They could be used as another auxiliary tool.


#### ccomp or csubj[:pass]?

While both `ccomp` and `csubj[:pass]` are often governed by speech or psych verbs which govern content clause arguments, `ccomp` is a content clause, mostly in the object position, and `csubj` is actually in the subject position, when used in the impersonal (i.e. no further subject position is saturated - הוא שוכנע כי אין צורך is ccomp):

Example for verbs that govern `obj` or `ccomp`:

הוא אמר [את דברו] – `obj`(amar, dvar)

הוא אמר [שמחירי הדלק עלו שוב] – `ccomp`(amar, alu)



טענתי [טענות דומות] - `obj`(taanti, teanot)

טענתי [שרוב הלקוחות שלי מרוצים] - `ccomp`(taanti, merutsim)



היא ציינה [זאת] - `obj`(tsiena, zot)

היא ציינה [שגישתו של שינדלר לבטהובן הייתה רומנטית מדי] - `ccomp`(tsiena, romantit)




Example for verbs that govern `nsubj` or `csubj` or `csubj:pass` (which are impersonal):

Note: in contrast to the next two examples, there are cases that aren’t impersonal and have a clause. Since the subject position is saturated (הוא שוכנע שמחירי הדלק יעלו) ccomp is used for the clause, even though it is not in the traditional object position (passive verbs don’t have objects).

 [קדיש] נאמר לרוב על ידי שליח הציבור– `nsubj:pass`(neemar, kadish)
 
 עוד נאמר [כי מחירי הדלק עלו שוב] - `csubj:pass`(neemar, alu)
 
 
 
[טענות דומות] נטענו בעבר - `nsubj:pass`(nitanu, teanot)

נטען [שרוב לקוחות החברה מרוצים] - `csubj:pass`(nitaan, merutsim)




בחוזה צוין [איסור על בעלי חיים] - `nsubj:pass`(tsuyan, isur)

לעיתים קרובות צוין [שגישתו של שינדלר לבטהובן הייתה רומנטית מדי] - `cusbj:pass`(tsuyan, romantit)



התבררה [התמונה המלאה] - `nsubj`(hitbarera, tmuna)

התברר [שהמצב לא טוב] - `csubj`(hitbarer, tov)



Illustrating the relationship between `ccomp` governors and impersonal `csubj[:pass]` governors:
|     `ccomp` governor    |     `csubj` or `csubj:pass` governor    |
|-------------------------|-----------------------------------------|
|     אמר ש...            |     נאמר ש...                           |
|     כתב ש...            |     נכתב ש...                           |
|     טען ש...            |     נטען ש...                           |
|     דיווח ש...          |     דוּוח ש...                           |
|     סיפר ש...           |     מסופר ש...                          |
|     קבע ש...            |     נקבע ש...                           |
|     ציין ש...           |     צוין ש...                           |
|     סיכם ש...           |     סוּכם ש...                           |
|     ראה ש...           |     נראה ש...                           |
|     ידע ש..., הודיע ש...            |     נודע ש...                           |
|     -                   |     התברר ש...                          |
|     -                   |     נדמה ש...                           |

#### AUX+aux or AUX+cop?

As per issue https://github.com/IAHLT/UD_Hebrew/issues/48, the following tagging, features and deprel should be followed:

- If we have אינו/הינו before nominal predicates (NOUN, ADJ), the upos is AUX, the deprel cop, 
and the features are as follows (AUX+cop):

Gender=Masc, Number=Sing, Person=3, Polarity=Neg, VerbType=Cop, lemma=אינו

Gender=Masc, Number=Sing, Person=3, Polarity=Pos, VerbType=Cop, lemma=הינו

Examples:

אנשים שאינם עובדי חברות כוח אדם

אנשים שהינם עובדי חברות כוח אדם






- If we have אינו/הינו before VERB and AUX (modals), the upos is AUX, the deprel aux, 
and the features are as follows (AUX+aux):

Gender=Masc, Number=Sing, Person=3, Polarity=Neg, Tense=Pres, lemma=אינו

Gender=Masc, Number=Sing, Person=3, Polarity=Pos, Tense=Pres, lemma=הינו

Examples:

העובדים אינם מועסקים בחברות כוח אדם

העובדים הינם מועסקים בחברות כוח אדם

העובדים אינם צריכים להגיש את המסמכים הבאים

העובדים הינם צריכים להגיש את המסמכים הבאים




- If we have להיות from lemma היה before nominal predicates (NOUN, ADJ), the upos is AUX, the deprel cop, 
and the features are as follows (AUX+cop):

HebBinyan=PAAL, VerbForm=Inf, VerbType=Cop, lemma=היה

Example:

העובדים היו אמורים להיות במקום העבודה


- If we have להיות from lemma היה before VERB, the upos is AUX, the deprel aux, 
and the features are as follows (AUX+aux):

HebBinyan=PAAL, VerbForm=Inf, lemma=היה

Example:

העובדים היו אמורים להיות מוזמנים לוועדה



### Open Questions
Please list new annotation questions in this section AND add a comment, mentioning each person who should chime in on this using “@” (so those people get a notification to answer):
-	Example: should a Hindi word in a sentence be tagged as X? 

#### Aspect

●	In the new Wikipedia data, we have a new morphological feature, which I assume is added by the newly improved automatic parser. The feature is Aspect=Prog, akin to the English progressive tenses. Here’s the relevant page on the UD website.

An example for this feature is the following construction, where the beinoni is accompanied by the past derivations of היה as AUX.


מגדה הייתה חברתה ללימודים של ליזה, אחותו של ארלוזורוב, והייתה מיודדת גם עם 
חיים ארלוזורוב, והרצח נועד לטשטש את היחסים הקרובים שהיו בינו למגדה.

The beinoni in this instance actually has Tense=Past, instead of the usual Tense=Pres, presumably to relay the past progressive meaning.



18	הייתה	היה	AUX	AUX
	Gender=Fem|Number=Sing|Person=3|Polarity=Pos|Tense=Past	19	aux	_	_

19	מיודדת	יודד	VERB	VERB	Aspect=Prog|Gender=Fem|HebBinyan=PUAL|Number=Sing|Person=3|Tense=Past|
VerbForm=Part	5	conj	_	_

This is not the best example, since מיודדת is probably better tagged as ADJ with the lemma מיודד. But assuming we leave it as a beinoni VERB, is this a feature we should add from now on to such constructions?

#### Dates
●	Why do we use the obl deprel from day to month in Hebrew Dates, like the one below? Is it solely because of the preposition? Shouldn’t nmod be more suitable, considering the day is not strictly a numeral, but a shorthand for “the 25th day”, that is, a nominalized numeral?


```
המאמר פורסם בעיתון "מאמענט", שראה אור בוורשה שבפולין, ב-25 ביוני 1933.

19	ב	ב	ADP	ADP	_	21	case	_	_
20	-	-	PUNCT	PUNCT	_	21	punct	_	_
21	25	25	NUM	NUM	_	11	obl	_	_
22	ב	ב	ADP	ADP	_	23	case	_	_
23	יוני	יוני	PROPN	PROPN	_	21	obl	_	_
24	1933	1933	NUM	NUM	_	21	nmod:tmod	_	SpaceAfter=No
```
