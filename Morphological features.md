## Morphological Features
In the following section, we outline the morphological features for each POS tag, as they pertain to Hebrew.

### Concentrated Table of features

<table>
    <tr>
        <td>POS Tag</td>
        <td>Feature</td>
        <td>Values</td>
        <td>Selected Examples (Invented and from HTB)</td>
    </tr>
    <tr>
        <td>NOUN</td>
        <td>Gender</td>
        <td>Fem</td>
        <td>מנהלת</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Masc</td>
        <td>אצן</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Fem,Masc</td>
        <td>עובדים/ות</td>
    </tr>
    <tr>
        <td></td>
        <td>Number</td>
        <td>Sing</td>
        <td>עבודה</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Plur</td>
        <td>כדורים, עובדות, מעצבים/ות</td>
   </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Dual</td>
        <td>Only when the paradigm includes three values:
שעה, שעתיים, שעות
יום, יומיים, ימים
דלת, דלתיים, דלתות
If the paradigm includes two values, these values are sorted only to singular and plural:
עין, עיניים/plur
שן, שיניים/plur
</td>     
   </tr>
    <tr>
        <td></td>
        <td>Definite</td>
        <td>Cons</td>
        <td>Construct State Forms: ילדי הגן</td>
    </tr>
    <tr>
        <td></td>
        <td>Abbr</td>
        <td>Yes</td>
        <td>יו"ר, מנכ"ל, ח"כ</td>
    </tr>
    <tr>
        <td>PROPN</td>
        <td>Abbr</td>
        <td>Yes</td>
        <td>שב"כ, ימ"מ, צה"ל</td>
    </tr>
    <tr>
        <td>ADJ</td>
        <td>Gender</td>
        <td>Fem</td>
        <td>בכירה</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Masc</td>
        <td>מהיר</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Fem,Masc</td>
        <td>גדול/ה</td>
    </tr>
    <tr>
        <td></td>
        <td>Number</td>
        <td>Sing</td>
        <td>קרוב</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Plur</td>
        <td>רחוקים</td>
    </tr>
    <tr>
        <td></td>
        <td>Definite</td>
        <td>Cons</td>
        <td>יפי נפש יפה = Lemma</td>
    </tr>
    <tr>
        <td></td>
        <td>Abbr</td>
        <td>Yes</td>
        <td>תנ"כי</td>
    </tr>
    <tr>
        <td></td>
        <td>NumType</td>
        <td>Ord  </td>
        <td>Ordinal numbers (ראשון, שני, שלישי, etc.) are tagged ADJ (default Lemma = Masc): זה היה שערו החמישי העונה בליגה. Also for Arabic numerals as ADJ: שחר פאר סיימה במקום ה-3 בעולם.</td>
    </tr>
    <tr>
        <td>ADP</td>
        <td>Case</td>
        <td>Gen</td>
        <td>Only for Genitive preposition: של</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Acc</td>
        <td>Only for Accusative preposition: את</td>
    </tr>
    <tr>
        <td></td>
        <td>Definite</td>
        <td>Def</td>
        <td>For cases of hidden definiteness: יצאתי לטייל בחצר</td>
    </tr>
    <tr>
        <td></td>
        <td>PronType</td>
        <td>Art</td>
        <td>For cases of hidden definiteness: יצאתי לטייל בחצר</td>
    </tr>
    <tr>
        <td>DET</td>
        <td>PronType</td>
        <td>Art</td>
        <td>Only for the definite article ה</td>
    </tr>
    <tr>
        <td></td>
        <td>Definite</td>
        <td>Def</td>
        <td>Def is only for the definite article ה</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Cons</td>
        <td>Cons is relevant for רוב, מעט, שאר, יתר, כול</td>
    </tr>
    <tr>
        <td>PRON</td>
        <td>PronType</td>
        <td>Prs  </td>
        <td>Personal Pronouns = היא, הם, אתן (Lemma: הוא) היא הודיעה כי הוועדה תגבש הצעת חוק בנושא העובדים הזרים.   Reflexive Pronouns (with ADP and in oblique position) = עצמה, עצמן, עצמכם (Lemma: עצמו) קשה להבין כיצד מנהיגים אלה לא שאלו את עצמם שאלה יסודית אחת.   As determiners, meaning the same one, morphologically similar to accusative pronouns, but unsegmented; Lemma:אותו ): היא מבוססת על אותו קרב המגננה שבו אירעו מעשי גבורה עילאיים, ועל קבלת החלטות קשות בתנאי קרב.  Other forms used as determiners meaning the whole/entire one (Lemma: כולו): למכבי תל אביב אין גם כיום שחקן שתמיד יצר את הפער בינו לליגה כולה.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Dem</td>
        <td>Demonstrative Pronouns = זו, אלה (Lemma: זה) טיעונים כאלה, שפעם היו מקובלים בין ליברלים בארה"ב, לא שמעתי כבר הרבה זמן.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Int  </td>
        <td>Interrogative Pronouns = מי, מה   Main clause: במקום שבו שרים, חברי כנסת ואנשי ציבור משמיעים את אמרותיהם, מי זקוק לסאטירה.   Subordinate clause: מקסוול דרש לדווח לו מי הדליף את הנתונים הכספיים של ההוצאה לתקשורת.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Ind  </td>
        <td>Indefinite Pronouns = כלשהו, איזושהי   במאה הזו נבחרו שני סנאטורים לנשיאים, ושלושה נשיאים אחרים כיהנו בסנאט בזמן כלשהו של הקריירה שלהם .   אין ספק כי יש כאן איזושהי אמירה מטאפיסית של היקום על מות האמת.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Emp  </td>
        <td>Emphatic Pronouns (No ADP; in `nmod:npmod` position) = עצמה, עצמן, עצמכם (Lemma: עצמו) גבולות מדיניים מפרידים בין ארצות, וגבולות אתניים מפרידים בתוך הארצות עצמן.</td>
    </tr>
    <tr>
        <td></td>
        <td>Case</td>
        <td>Gen</td>
        <td>Gen for possessive clitic pronouns: ילדיה = הילדים שלה</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Acc</td>
        <td>Acc for accusative clitic pronouns: להכשילם = להכשיל אותם</td>
    </tr>
    <tr>
        <td></td>
        <td>Definite</td>
        <td>Def</td>
        <td>Mainly for examples like ילדיה. Since we do not assign this feature to the nominal, we must mark somehow that the entire phrase is definite.   Accusative pronouns used as determiners meaning the same one: מדוע לפחות אין הם מפרסמים התנצלות והסברים, באותו תקציב שבו הם משתמשים כדי ליצור תדמית ציבורית חיובית?   Other forms used as determiners meaning the whole/entire one: אחרי עיתונאים יהיו אלה הפוליטיקאים , השוטרים והשופטים , והדבר יביא לקריסת המרקם החברתי כולו.</td>
    </tr>
    <tr>
        <td></td>
        <td>Gender</td>
        <td>Fem</td>
        <td>יתר-על-כן, הריבית בישראל במיוחד על משכנתאות היא מהנמוכות ביותר בעולם, אם לא הנמוכה שבהן.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Masc</td>
        <td>זהו כישלונו היחיד עד כה של המפכ"ל , שנגרם רק בגלל העובדה שהוא סמך יותר מדי על קציניו הבכירים.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Fem,Masc</td>
        <td>The delimiter may vary or be missing altogether: אתם/ן מוזמניםות לפנות אליי בכל נושא. [Forms without explicit reference should not be assigned Gender, e.g., אליי here.]</td>
    </tr>
    <tr>
        <td></td>
        <td>Number</td>
        <td>Sing</td>
        <td>רק אחר-כך נמצא כרטיס ביקור, ובו שמו ותוארו של גרוסבורד כמנהל מפעל פרטי.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Plur</td>
        <td>על פי כל הדיווחים חלה בעשורים האחרונים ירידה תלולה בתמיכה בעבודות מחקר במדעי החברה שאין להן יישום מעשי מידי.</td>
    </tr>
    <tr>
        <td></td>
        <td>Poss</td>
        <td>Yes</td>
        <td>For possessive clitic pronouns: כלכלתה היתה שקועה במיתון קשה, בשעה שרוב המדינות האחרות בארה"ב נהנו משגשוג חסר תקדים.</td>
    </tr>
    <tr>
        <td></td>
        <td>Person</td>
        <td>1</td>
        <td>לשם איזון הנושא, עליי לציין כי אני נמנה על ההורים שהביעו את הסכמתם לקיום הטיול.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>2</td>
        <td>אם בכל זאת אתם רוצים סבסוד למחשבותיכם ולמעשיכם, עליכם להשיג אותו בדרך המיושנת.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>3</td>
        <td>מתקבל הרושם שהיחידים במדינה הזו שאינם צריכים לחשוש מתוצאות מעשיהם הם הפוליטיקאים.</td>
    </tr>
    <tr>
        <td></td>
        <td>Reflex</td>
        <td>Yes</td>
        <td>Coreference with the subject: היא עשתה זאת בעצמה   Coreference with the object: הוא אמר לה לעשות זאת בעצמה   The emphatic pronouns also receive this value: הקרב עצמו נמשך שעות   No explicit reference (predicate-embedded): תראו בעצמכם.</td>
    </tr>
    <tr>
        <td>ADV</td>
        <td>Prefix</td>
        <td>Yes</td>
        <td>Modifying an ADJ: דו-קוטבי, תלת-ספרתי, רב-לאומית ADV: חד-חד-ערכי  VERB: אי אפשר Noun: אנטי-קומוניסט, מולטי-מיליונר</td>
    </tr>
    <tr>
        <td></td>
        <td>Polarity</td>
        <td>Pos</td>
        <td>Positive: כן, אני מסכים</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Neg  </td>
        <td>Negative Adverbs: בלתי חוקי הוא לא התכוון לכך</td>
    </tr>
    <tr>
        <td>NUM</td>
        <td>Gender</td>
        <td>Fem</td>
        <td>צעד זה של קופת חולים הכללית נעשה במסגרת המאמץ להחזיר אליה חברים שעזבו אותה בחמש השנים האחרונות.   Ambiguous forms – acc. to the context: שיעור האבטלה מתקרב לשמונה אחוזים.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Masc  </td>
        <td>איני יכולה שלא להתריס בפניו על משפט אחד בקטע הפתיחה של הכתבה.   Ambiguous forms – acc. to the context: כל רצוני היה שיאפשרו לי לאחר התמסרות של שמונה שנים לנתח גם במרכז חורב.</td>
    </tr>
    <tr>
        <td></td>
        <td>Number</td>
        <td>Sing</td>
        <td>Numerals are considered singular only when they have a contrast with a plural form. They should not receive this feature if no such contrast exists: זו אחת הסיבות לכך שמענקי מקארתור מבוקשים כל כך. (cp. אחדות)</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Plur</td>
        <td>Clear contrast (אלף-אלפים,מאה-מאות, עשר/ה-עשרות, מיליון-מיליונים)), Cp. Singular, מדיווח שהגיע אתמול למשרד התיירות בירושלים, ישתתפו במשלחת כמאה מראשי הקהילה . vs. Plural, משום כך, ראשית כל עליך לחשוב על קבלת תפקיד חשוב באחד ממאות הגופים הללו.</td>
    </tr>
    <tr>
        <td></td>
        <td>Definite</td>
        <td>Cons</td>
        <td>Some numerals have overt CS forms שני הילדים (שתיים = Lemma) אלפי המפגינים (אלף = Lemma) Cp. שלושת הכדורים with a distinct CS form (Lemma = שלוש) vs. שלוש המנהלות which has the same form as the bare numeral, but different pronunciation (shalosh vs. shlosh)</td>
    </tr>
    <tr>
        <td></td>
        <td>NumType</td>
        <td>Card</td>
        <td>Cardinal numbers (אחת, שתיים, שלוש, etc.) are tagged NUM (default Lemma = Fem): נשיא אירלנד נבחר לשבע שנים. But not for Arabic numerals as NUM: לפני שהפסידה במשחק הרביעי, היא ניצחה ב-3 משחקים ברציפות.</td>
    </tr>
    <tr>
        <td>AUX      </td>
        <td>VerbType</td>
        <td>Cop</td>
        <td>Forms of היה: אתה מתבונן בנושא שיהיה בעל ערך לגיטימי למחקר, ובו בזמן יכבוש את דמיונו של פקיד התוכנית.   The inflected forms of הִנֵּה (הינו, הינה, הינם, הינן): מרכיב חשוב ביותר בתהליך קבלת החלטות הינו המידע. Inflected forms of אין only as pure copulas: תחנת הקלפי אינה מקום ההצבעה ההכרחי היחיד.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Mod</td>
        <td>האם אתם יכולים להתעלות על כך?   שום קרן או חברה מסחרית לא תהיה מוכנה לתת לו מימון אם ייוודעו פרטיו.</td>
    </tr>
    <tr>
        <td></td>
        <td>Polarity</td>
        <td>Pos</td>
        <td>The inflected forms of הִנֵּה (הינו, הינה, הינם, הינן): דיווח אמין הינו ערך יסודי חיוני ומקודש במשרד המשטרה.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Neg</td>
        <td>Assertion auxiliaries: האשמה אינה בשיטה או במדגם.</td>
    </tr>
    <tr>
        <td></td>
        <td>Gender</td>
        <td>Fem</td>
        <td>מורשת הקרב שצה"ל אימץ כתוצאה מהקרב על מנזר סן סימון איננה מיתוס.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Masc</td>
        <td>אם אתה מעדיף לפעול בלי איש ביניים, אתה יכול להקים ארגון משלך שלא למטרות רווח.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Fem,Masc</td>
        <td>את.ה יכול/ה להקים ארגון משלך שלא למטרות רווח.</td>
    </tr>
    <tr>
        <td></td>
        <td>Number</td>
        <td>Sing</td>
        <td>תחנת הקלפי שוב אינה מקום ההצבעה ההכרחי היחיד.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Plur</td>
        <td>הדמוקרטים היו באווירת אופוריה, והניחו שמועמדם דוקאקיס לא יצטרך אפילו לרוץ לבית הלבן .</td>
    </tr>
    <tr>
        <td></td>
        <td>Person</td>
        <td>1</td>
        <td>מסתבר שהייתי תמים.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>2</td>
        <td>עם הרבה עץ, מכונת אספרסו עתיקה כמעט ושטח גן מקסים, הוא מסוג המקומות הפשוטים והמזמינים שהייתם מצפים למצוא בין גבעות טוסקאנה.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>3</td>
        <td>זו הייתה התרברבות לא-דיסקרטית, ואין ספק שיימנע ממנה השנה.</td>
    </tr>
    <tr>
        <td></td>
        <td>Tense</td>
        <td>Past</td>
        <td>הביקור הקצר היה רווי מתח ודרמטי .</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Present</td>
        <td>Inflected forms of אין only as pure copulas: תחנת הקלפי אינה מקום ההצבעה ההכרחי היחיד.  The inflected forms of הִנֵּה (הינו, הינה, הינם, הינן): תחנת הקלפי הינה מקום ההצבעה ההכרחי היחיד</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Fut</td>
        <td>מצב קופת ההתאחדות לספורט בהחלט יהיה פחות טוב, אם למרות הכל יממש ללקין את נסיעתו לאוסטרליה.</td>
    </tr>
    <tr>
        <td>VERB</td>
        <td>Gender</td>
        <td>Fem</td>
        <td>תופעה זו התבררה אתמול בוועדת העבודה והרווחה של הכנסת, שדנה בנושא העסקת עובדים זרים.  The inflected forms of יש (ישנו, ישנה, ישנם, ישנן):  בארצות הברים ישנן חבילות של מבחנים ומבדקים שנקבעו מראש.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Masc</td>
        <td>החלטתי לקחת יוזמה ולטפל בבעיה בעצמי. We should not assign this feature when it is impossible to figure out the gender from the context.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Fem,Masc</td>
        <td>Overt mixed reference: א.נשים בחברה דיווחו שהםן מרוצים/ות.</td>
    </tr>
    <tr>
        <td></td>
        <td>Person</td>
        <td>1</td>
        <td>כהיסטוריון, הוא בוודאי רוצה שנתעד, נלמד ונשתדל להבין את הרקע שהוליד את התופעה הנאצית.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>2</td>
        <td>אבל אל תטרחו לדווח לשלטונות המקומיים.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>3  </td>
        <td>איש לא התכוון לכך .</td>
    </tr>
    <tr>
        <td></td>
        <td>Number</td>
        <td>Sing</td>
        <td>בחודש הבא, הוא יבקר את בני משפחתו בצרפת.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Plur  </td>
        <td>עמדנו בתור במשך שעות.  The inflected forms of יש (ישנו, ישנה, ישנם, ישנן):  ישנם ויכוחים רבים על דרכי הטיפול ויעילותן</td>
    </tr>
    <tr>
        <td></td>
        <td>Tense</td>
        <td>Pres</td>
        <td>Present (same form as Participles): הם מקבעים את אבני השפה אחת בצמוד לשנייה.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Past</td>
        <td>Past: בתקופה זו שימשה כמנהלת המחלקה לביטחון מידע.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Fut</td>
        <td>Future: בסוף השנה יעלה לאקרנים סרטו התשיעי הבמאי קוונטין טרנטינו.</td>
    </tr>
    <tr>
        <td></td>
        <td>Voice</td>
        <td>Act</td>
        <td>Active voice refers to an action that the subject is performing or a state that the subject is in: היא למדה באוניברסיטת בוסטון.  בקצהו עומד מנזר "יוחנן במדבר".  יוסי בישל פסטה.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Mid</td>
        <td>Middle voice refers to reciprocal or reflexive actions, and often when no external agent is understood or implied: אבל השיטים נזכרת בספר במדבר (*על-ידי כותבי המקרא). הפסטה התבשלה (*על-ידי יוסי).</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Pass</td>
        <td>Passive voice refers to an action that is performed on the subject, e.g., נגד רביב הוגש בסופו של דבר כתב אישום (על-ידי הפרקליטות). הפסטה בושלה ע"י יוסי.</td>
    </tr>
    <tr>
        <td></td>
        <td>Mood</td>
        <td>Imp</td>
        <td>Reserved for Imperatives, which in Hebrew appear only in the 2nd person (sing or plur), e.g. קח אותו החוצה. צאו לטייל ברחבי הארץ. תן לי את הלחם.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Irr</td>
        <td>Reserved for beinoni, in contra-factual constructions. No Tense feature should be assigned to the beinoni in this case, but the AUX (היה) should get Tense=Past even though it doesn't semantically refer to the past, e.g., היינו רגועים יותר, לו הצבא האמריקאי היה מעדכן את צה"ל בכל הנוגע לתכונותיו של הצבא העיראקי , בכוויית ובעיראק עצמה.</td>
    </tr>
    <tr>
        <td></td>
        <td>Aspect</td>
        <td>Prog</td>
        <td>Reserved for beinoni, in past progressive meaning. No Tense feature should be assigned to the beinoni in this case, e.g.,  אחת לכמה שבועות הייתי נקלע לאסיפת המונים שכינס במרכז ירושלים.</td>
    </tr>
    <tr>
        <td></td>
        <td>VerbForm</td>
        <td>Part  </td>
        <td>Present Participles (beinoni): היא כיתבה את השרה הממונה על ניהול משבר הקורונה.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Inf  </td>
        <td>Infinitive forms (In all verbal templates but passives PUAL and HUFAL): בני משפחת מנגיסטו דרשו מהצלב האדום לסייע להחזיר את בנם ארצה. The first infinitive לסייע is Active in HebBinyan = PIEL The second infinitive להחזיר is also Active in HebBinyan = HIFIL    הוא השאיר את הפסטה על הכיריים להתבשל  The infinitive להתבשל is Middle in HebBinyan = HITPAEL</td>
    </tr>
    <tr>
    </tr>
    <tr>
        <td></td>
        <td>VerbType</td>
        <td>Mod</td>
        <td>חלק גדול מהסצנות מרגישות לא מלוטשות, הניראות הכללית של המשחק מרגישה מיושנת, ולא בטוח שגם שדרוג החומרה שלכם יצליח לגרום לעובדה הזאת להשתנות. [VERB+csubj = בטוח←יצליח]</td>
    </tr>
    <tr>
        <td></td>
        <td>Polarity</td>
        <td>Pos</td>
        <td>Forms of יש (existential): הם פשוט תהו, נזכר לנקובסקי, "למי יש רעיונות מעניינים?"</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Neg  </td>
        <td>Negative existential forms: אין ביניהם אנשי ציבור הרצים לכנסת בשם פתרונותיהם.</td>
    </tr>
    <tr>
        <td></td>
        <td>HebBinyan (Universal Features)</td>
        <td>PAAL</td>
        <td>היא אמרה כי שירות התעסוקה הציע להביא עובדים מדרום לבנון, אך תנועת המושבים סירבה.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>PIEL</td>
        <td>היא הודיעה כי הוועדה תגבש הצעת חוק בנושא העובדים הזרים.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>HIFIL</td>
        <td>רייזמן מציע שהממשלה תסבסד מחצית מעלות העסקתם של העולים בקטיף .</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>HUFAL</td>
        <td>הרבה כסף הוקדש להגות על מדינות העולם השלישי .</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>PUAL</td>
        <td>תשדירי הבחירות שלו תוארו כשנונים ביותר בארה"ב .</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>NIFAL</td>
        <td>אנו, נפגעי המשכנתאות, נקלענו למצבנו הקשה לא בגלל ריבית נמוכה, אלא בגלל האינפלציה וההצמדה.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>HITPAEL</td>
        <td>כך או כך, שמו של בורחס יצטרף מעתה לרשימה הארוכה של הסופרים שהפרס נמנע מהם.</td>
    </tr>
</table>

### Nominal Features
#### Gender
Hebrew inflects nominals (NOUN, PRON), predicates (VERB, AUX) and modifiers (ADJ, NUM) for Gender. We distinguish between the values Fem, Masc and Fem,Masc standing for feminine, masculine and overt mixed reference respectively. 

Morphologically Masculine nominals and verbs, referring to a mixed group (males and females) receive the value Masc. It is based on conventions from other TBs where this occurs:

המסירות הבלתי-נלאית של מיקרוסופט והחיבור המוצלח עם גוגל יבטיחו את המשך שיתוף הפעולה ביניהן.

If the gender cannot be determined, it might be better to assign Fem,Masc. In cases where Gender cannot be determined from the context, we will not assign this feature. In cases where it is clearly referring to a specific Gender (Fem or Masc), then we should annotate accordingly.     

Some examples:
האצן המהיר.
both the NOUN אצן and the ADJ מהיר receive the feature Gender=Masc;
המנהלת הבכירה. 
both the NOUN מנהלת and the ADJ בכירה receive the feature Gender=Fem;
דרושים/ות עובדים/ות למשרה נחשקת. 
both the VERB דרושים/ות and the NOUN עובדים/ות receive the feature Gender=Fem,Masc.

#### Number
Hebrew inflects nominals (NOUN, PRON), predicates (VERB, AUX) and modifiers (ADJ, NUM) for Number. We distinguish between the values Sing and Plur standing for singular and plural respectively. 
Some examples:
הגשם הראשון.
Both the NOUN גשם and the ADJ ראשון receive the features Number=Sing and Gender=Masc. (The ADJ ראשון should also receive NumType=Ord, see NumType).
עבודה קשה.
Both the NOUN עבודה and the ADJ קשה receive the features Number=Sing and Gender=Fem;
כרישים נצפו קרוב לחופי הים התיכון. 
Though the NOUN כרישים refers to a group of sharks comprising of males and females, and the VERB נצפו is morphologically shared for both Genders, we follow other TBs conventions in assigning both Number=Plur and Gender=Masc.

### Lexical Features
#### Definite
Definiteness is expressed in Hebrew using a definite article in the form of the morpheme ה attached to nominals (not to be confused with the relative clause marker ה preceding participles (beinoni) and standing for ש/אשר). We assign the definite article, tagged DET, the values Definite=Def and PronType=Art. Adjectives modifying a definite Noun also require a repetition of the definite article. Therefore, in the phrase הילדה החכמה, both articles receive these features.

In cases of hidden definiteness, as in prepositions ב, ל, e.g., הלכתי לבית, נסענו באוטובוס, we do not introduce pseudo-tokens by segmenting the phrase to ל_ה_בית, but rather indicate the definiteness on the preposition itself by assigning both Definite=Def and PronType=Art.

Construct State (CS henceforth) forms are special forms of nominals (and some modifiers) when appearing in compound (smixut) constructions. In the phrase משרתי המלכה, the first nominal משרתים appears in its CS form. A definite article is implicit before משרתי when the second nominal is definite, due to definiteness spreading from the second nominal, מלכה. 
As stated above, we do not introduce pseudo-tokens by segmenting the nominal משרתי as המשרתים_של_. Instead, we indicate this special form by assigning it the feature Definite=Cons. The article attached to the second nominal (המלכה) receives the features Definite=Def and PronType=Art. 

Please note the difference between these two values: while not strictly definite per se, Definite=Cons allows us to differentiate the CS form (e.g., ליצנֵי) from the bare noun (e.g., ליצנים). Definite=Def is the value we assign the definite article attached to the bare noun (e.g., הליצנים) to render some non-specific jesters into specific, definite ones. The phrase ליצני חצר, then, is not definite, but rather equivalent semantically to some generic court jesters, ליצנים של חצר. Nevertheless, we need to indicate that the surface form of ליצנים is different, i.e., the CS one. UD or HTB decided to assign the value Cons under the Definite feature.
The phrase ליצני החצר, however, is definite, by virtue of definiteness spreading from the second nominal (החצר). Therefore, it is semantically equivalent to some specific court jesters, הליצנים של החצר. The value Definite=Cons assigned to ליצני in both cases to simply indicate the morphological CS form, does not make the entire phrase definite.

#### Poss
When we have a nominal with a clitic possessive pronoun, as in תלמידיה,  it is essentially equivalent to the phrase התלמידים שלה. Since we do not introduce pseudo-tokens, as stated above, and we do not mark definiteness on the nominal itself, we indicate definiteness by marking Definite=Def and Poss=Yes on the clitic pronoun (in addition to other features, to be stated below). Note that we do not indicate PronType=Art in this case, since it is actually a personal pronoun and requires the feature PronType=Prs.

At the moment, indicating possession with the deprel nmod:poss and the morphological feature Poss=Yes seem redundant. However, this is the convention in other TBs. We also have the double genitive construction in Hebrew, תלמידיו (היקרים) של המורה, which, though superfluous,  requires two nmod:poss relations, one within the phrase תלמידיו and another between תלמידי and מורה, but only the former receives the Poss=Yes feature.

We assign this feature to the pronoun in segmented possessive pronouns:
התלמידים שלה ← ה|תלמידים של|ה 

#### PronType
There are several pronominal types which are relevant to Hebrew:
-	The definite article ה and prepositions with hidden definiteness (ב, ל) receive PronType=Art (see Definite).

-	The personal pronouns (PronType=Prs) inflect based on Gender, Number and Person. 

The 1st person pronouns אני and אנחנו (as well as the less common forms אנוכי and אנו) refer to singular and plural speakers, respectively. Their Gender may be left unassigned in the absence of clear reference.

The 2nd person pronouns (את, אתה, את/ה | אתן, אתם, אתם/ן) refer to singular and plural addressees with Gender Fem, Masc and Fem,Masc respectively. 

The 3rd person pronouns (היא, הוא, הוא/היא | הן, הם, הם/ן) refer to singular and plural third parties with Gender Fem, Masc and Fem,Masc respectively. Note that the pronominal copulas have the same form but they do not receive PronType=Prs. Rather, they receive Polarity=Pos (see Polarity).

Their default Lemma is הוא.

As Omer & Shira suggested, I recommend segmenting the forms שנינו, שניכם, שניהם | שתינו, שתיכן, שתיהן, instead of referring to them as frozen forms to address two entities. Since this is possible, in theory, with other numerals (שלושתכן, ארבעתכם, etc.), we might want to treat all these forms as a NUM+PRON with deprel nummod from the PRON to the NUM. The NUM in these cases have the Definite=Cons feature solely based on its morphologically CS form (שני+הם, שלושת+ן, ארבעת+כן, etc.)

-	Some pronouns can be used as determiners in the sense of “the same one”. They are morphologically identical to the accusative pronouns (אותו, אותה, אותם, אותן), but unlike the latter, we leave them unsegmented. They are tagged PRON with deprel det, e.g.,
הוא ימשיך להתגלגל, לאו דווקא באותן השיטות. 
Here we assign the following features to אותן (default Lemma is אותו):
Definite=Def | Gender=Fem | Number=Plur | Person=3 | PronType=Prs

-	As Omer suggested, we might want to add to this list the forms of כולו (Lemma=כולו; Inflection: כולו, כולה, כולם, כולן) when they function as determiners in the sense of “the whole/entire one”. Just as above, they should not be segmented. I suggest tagging them PRON with deprel det, e.g.,
למכבי תל אביב אין גם כיום שחקן שתמיד יצר את הפער בינו לליגה כולה.
Here we assign the following features to כולה (default Lemma is כולו):
Definite=Def | Gender=Fem | Number=Sing | Person=3 | PronType=Prs

Alternatively, we may want to introduce PronType=Tot for Total/Collective pronouns, adjectives and determiners, since they have full inflection for Number and Gender.

That said, we should distinguish the above forms from the nominalized usage of כולם which is unsegmented and tagged NOUN.

-	The demonstrative pronouns (PronType=Dem) refer deictically to a third party entity:
זה, זהו, זו, זוהי, זאת | אלה, אלו. 

Note that זאתי is not considered grammatical. If it appears in the data, add Typo=Yes and CorrectForm=זאת (see under Additional Features). The plural forms are interchangeable and refer to either Gender.

The default Lemma is זה (Person=3).

-	The reflexive pronouns (PronType=Prs and Reflex=Yes) refer anaphorically to an entity in the subject position (whether explicit or not, as in תראו בעצמכם) or object/oblique position and they are preceded by a preposition. They inflect for Gender, Number and Person:
The 1st person reflexive pronouns, e.g.,
 ראיתי את עצמי במראה.
 הצענו את עצמנו כמתנדבים אפשריים.
 היא אמרה לי לעשות זאת בעצמי.

The 2nd person reflexive pronouns, e.g.,
 אתה יכול למצוא את הפתרון בעצמך.
 אתן חייבות להקדיש זמן לעצמכן.

The 3rd person reflexive pronouns, e.g.,
 אילו היה עושה זאת, הוא היה עלול להביך את עצמו.
 אך לפני הכל ארה"ב חייבת להבהיר לעצמה לשם מה הקימה את העולם על רגליו.
 אבל הן גם יצטרכו עכשיו לממן בעצמן את ההוצאות שלהן.

The default Lemma is עצמו.

-	The emphatic pronouns (PronType=Emp and Reflex=Yes) appear in the bare forms of עצמו and they follow an entity in subject or an object/oblique position to emphatically refer back to them: 
הקרב עצמו נמשך שעות. 
הגשתי למרצה את הטיוטה עצמה בצירוף מספר נספחים. 

We refer to them as emphatic pronouns, because they can be left out while keeping the sentence grammatical, unlike the reflexive pronouns above.

The default Lemma is עצמו.

-	The indefinite pronouns (PronType=Ind) refer to an indefinite third party: מישהו, כלשהו, איזשהו, מישהי, איזושהי, כלשהי, כלשהם, כלשהן. While they can be thought of as segmented to מי_ש_הוא, as mentioned above, we will not introduce pseudo-tokens, and instead leave them unsegmented.
מישהו יכול לפנות לפתרון בעיה כלשהי ולהיתקל באיזשהו מכשול בדרך.

The default Lemma for each will be its Masc.Sing.3 variant, i.e., מישהו, כלשהו, איזשהו in the above example.
  
-	The interrogative pronouns (PronType=Int) are those used to introduce either a main question or a subordinate one: מי, מה, למה, איך, איזו, איזה, אילו

Main question: 
מה פשר המושג הזה?
באיזו מידה יכול אדם להשתנות?
Subordinate question:
אני לא יודע מה יקרה.
לימדת אותי איך לחשוב בצורה ביקורתית.
While the POS tag of the above examples is not always PRON (e.g., איך is tagged ADV), they all carry the feature PronType=Int.

#### Case
Case is generally a nominal feature. Languages rich in morphology have several conjugations for each noun based on case (Nominative, Accusative, Genitive, Dative, etc.). However, Hebrew nouns are invariant and we indicate case using certain prepositions.

#### Case
Case is generally a nominal feature. Languages rich in morphology have several conjugations for each noun based on case (Nominative, Accusative, Genitive, Dative, etc.). However, Hebrew nouns are invariant and we indicate case using certain prepositions.

Genitive case indicates some form of relation, ownership or possession. When the preposition של precedes a nominal, it carries the feature Case=Gen.
התלמידים היקרים של המורה  

Note that we segment the possessive pronouns to their components:
התלמידים שלה ← ה|תלמידים של|ה

The preposition receives Case=Gen and the clitic pronoun receives the features 
Gender=Fem | Number=Sing | Person = 3 | Poss=Yes | PronType=Prs 

In the equivalent form תלמידיה, we assign the clitic possessive pronoun the feature Case=Gen, in addition to those mentioned before (see Definite & Poss):
Case=Gen | Definite=Def | Gender=Fem | Number=Sing | Person=3 | Poss=Yes | PronType=Prs

Accusative case indicates the direct object, often the patient participant in transitive constructions. In Hebrew the feature Case=Acc is marked on the preposition את before a definite nominal:
חברי התנועה המארגנים יבקשו לנצל את ההיתר הזה

Or before compound (smixut) phrases which are considered definite:
זו לא הריבית שסיבכה את מקבלי המשכנתאות

Also before nominals with clitic possessive pronouns:
אני נמנה על ההורים שהביעו את הסכמתם לקיום הטיול

In higher registers, verbs can have clitic accusative pronouns:
אבקשכן לשלוח אליי חומר זה ← אבקש את|כן לשלוח אליי חומר זה

Here the features of the clitic pronoun are:
Case=Acc | Gender=Fem | Number=Plur | Person=2 | PronType=Prs

#### Reflex
Reflexive and emphatic pronouns receive the feature Reflex=Yes, the former is of type PronType=Prs, the latter of type PronType=Emp (see above under PronType). 

#### NumType
Hebrew distinguishes between two types of numbers: Cardinal (NumType=Card) and Ordinal (NumType=Ord). While Cardinal numbers (אחת, שתיים, שלוש, etc.) are tagged NUM with a default Fem Lemma (e.g., ארבעה has the Lemma ארבע), the Ordinal numbers (ראשון, שני, שלישי, etc.) are tagged ADJ with a default Masc Lemma (e.g, הבעיות הראשונות has the Lemma ראשון).

As mentioned above (see under PronType), some cardinal numerals have overt CS forms (e.g., שני התלמידים, שתי הסטודנטיות, both with Lemma=שתיים). Some forms on the surface do not differ from the bare form (e.g., חתכתי לסלט את שלוש העגבניות vs. אכלתי את שלושת הממתקים שנשארו), but all of these forms receive the feature Definite=Cons solely based on their morphologically CS form.

We recommend assigning the Number feature to Cardinal numbers only when they have clear contrast between singular and plural morphology, e.g., אלף-אלפים, מאה-מאות, עשר/ה-עשרות, מיליון-מיליונים, etc. If no such contrast exists, we should not assign the Number feature, 
e.g., שתי סטודנטיות, שלושה כדורים, ארבע תחנות, etc.

Most Cardinal and Ordinal numbers do inflect for Gender. We should assign the Gender feature with values Masc or Fem based on the form , e.g., ארבעה כדורים receives Gender=Masc and ארבע תחנות receives Gender=Fem. 

We assign morphological features to Arabic numerals only when they are tagged ADJ, but not when they are tagged NUM: 
3 תחנות = No morphological features
3 כדורים  = No morphological features
המשחק ה-3 = Gender=Masc|NumType=Ord
התחנה ה-3 = Gender=Fem|NumType=Ord


Some numerals do not have a Gender contrast, עשרים עגבניות vs. עשרים תפוחים. In such cases, the Gender value will be determined by the modified NOUN. If it appears in isolation with no clear disambiguating context, it should not receive the Gender feature.

Most Ordinal numbers, as regular Adjectives, have clearer forms for Number and Gender (e.g., ראשון, ראשונה, ראשונים, ראשונות).

If the Gender is incorrect, assign the features according to the correct form (e.g., חמש כדורים receives the feature Gender=Masc). In those cases, we add CorrectForm=חמישה and Typo=Yes (see under Additional Features).

### Verbal Features
#### Tense
Hebrew finite verbs have three temporal conjugations, some of them complete for each verbal template: Past, Future and Present. Note that the Present forms are the same as those of participles. We do not assign Tense to infinitives (VerbForm=Inf) or to imperatives (Mood=Imp).

Verbs inflect for Gender, Number and Person. Some forms share Gender (e.g., present verbs for singular are the same for each person, and the same goes for plural; 3rd person plural forms in the past and future are the same for both genders). As mentioned before, if it is possible to determine the gender (Fem or Masc), then we should annotate accordingly. If it refers to a mixed group, we should follow other TBs and annotate Masc. If it is impossible to determine the gender from the context, we should not assign this feature.

Past:
לא שמעתי כבר הרבה זמן טיעונים כאלה.
Future:
הממשלה תסבסד מחצית מעלות העסקתם של העולים בקטיף.
Present & Participles:
הראש היהודי ממציא לנו פטנטים בדמות מתנדבים, המשולמים שכר מחפיר.

The first is a finite verb with the following features:
Gender=Masc | HebBinyan=HIFIL | Number=Sing | Person=3 | Tense=Pres | VerbForm=Part | Voice=Act

The second is a participle (following the SCONJ ה) with the following features:
Gender=Masc | HebBinyan=PUAL | Number=Plur | Person=3 | Tense=Pres | VerbForm=Part | Voice=Pass

#### Voice
Finite verbs, Imperatives, Infinitives and Participles carry the Voice feature. We distinguish in Hebrew between three possible values: Active, indicating that the subject is performing an action or is in a certain state; Passive, denoting that the subject is undergoing an action or is being acted upon; and Middle, which are rather trickier to figure out (see HebBinyan for more examples). A common distinction between Active, Passive and Middle respectively is to consider whether an external agent is mentioned in the sentence (or can be understood):

יוסי בישל פסטה
הפסטה בושלה ע"י יוסי
הפסטה התבשלה


Note that the following is ungrammatical:
*הפסטה התבשלה ע"י יוסי

We can demonstrate the difference with the HebRoot שני with examples from the HTB. The Active voice in transitive constructions requires two participants, one performing the action and one receiving it. Here, קופת חולים הכללית is termed the Agent; התעריף… is termed the Patient, the direct object.
Active →
קופת חולים הכללית שינתה את התעריף לשמירת זכויות החברות בקופה ליוצאים לתקופה ממושכת לחו"ל.
Gender=Fem | HebBinyan=PIEL | Number=Sing | Person=3 | Tense=Past | Voice=Act

The Middle voice generally denotes a reflexive meaning (the subject is the internal object of an action, or the subject is performing an action to their benefit). It can also refer to an action without an explicit, or even implicit, external agent. Here, המצב needs to change, and it is understood as a process that needs to happen without referring to some third party who will undertake this change.
Middle → 
המצב צריך להשתנות בהתאם (*ע"י החברה)
HebBinyan=HITPAEL | VerbForm=Inf | Voice=Mid

The Passive voice indicates that the subject is being acted upon. An Agent, if explicitly mentioned, often appears inside a by-phrase (על ידי/ע”י + nominal)
Passive → 
ב1945 שונה שמה של קניגסברג לקלינינגרד (ע"י ברית המועצות)

Gender=Masc | HebBinyan=PUAL | Number=Sing | Person=3 | Tense=Past | Voice=Pass


Shira recommended consulting this article on the connection between HebBinyan and Voice:
(עידית דורון) תרומתו של הבניין למשמעות הפועל

#### Mood
This feature is reserved in Hebrew for Imperatives, a form of command or strong request to addressees (2nd person singular or plural). We assign the value Mood=Imp to such examples as:
אנא דאג לנעילת הכניסה אל הגג.
קחו למשל את אריק ובנץ.
Note that these forms do not have Tense.

We also assign the value Mood=Irr, short for irrealis, to beinoni forms in contra-factual constructions. Note that the Tense feature should not be assigned to the beinoni in this case.

היינו רגועים יותר, לו הצבא האמריקאי היה מעדכן את צה"ל בכל הנוגע לתכונותיו של הצבא העיראקי, בכוויית ובעיראק עצמה.

#### Aspect
This value Aspect=Prog, short for progressive, is assigned to beinoni forms in the past progressive - structurally, even if we cannot make sure the semantic meaning is indeed progressive. Note that this is predominantly in constructions with derivations of היה. Note that the Tense feature should not be assigned to the beinoni in this case. Instead, the dependent AUX should carry the Tense.

אחת לכמה שבועות הייתי נקלע לאסיפת המונים שכינס במרכז ירושלים.

ניתן היה לעשות זאת

 Could be a simple past form (ניתן+past aux), irrealis (it could have been done), and not necessarily progressive, but we still mark it as such, because of its structure. 

#### Person
Verbs and Pronouns inflect for person: 1st person - speaker; 2nd person - addressee; 3rd person - third party. See PronType and Tense for examples.

#### VerbForm
We distinguish in Hebrew between three possible values: Part standing for Participles, Inf standing for Infinitives, and Vnoun for Infinite Absolute in clear adverbial constructions. 

Note that both Present finite verbs and Present Participles receive the features 
Tense=Pres | VerbForm=Part (see Tense).

Infinitives are non-finite verbal forms. They can stand as clausal subjects or follow finite verbs. 
They do not have Tense or Person, but they do carry Voice. 
Except Passive verbal templates (PUAL and HUFAL), all other templates have a unique infinitive form, e.g.,

PAAL → 
מדובר בקומץ אנשים שניסו למשוך אליהם כספי מענקים.
HIFIL →
ברצוני להדגיש משפט אחד בדבריה.
HITPAEL →
שגב החליט שלא להתייחס לכך בכתבתו.

The value VerbForm=Vnoun is assigned to infinitive absolute forms in adverbial clause constructions. We should distinguish between simple nouns, predominantly in smixut constructions, e.g., עד רדת הלילה, and clear adverbial clauses, 
e.g., ברדתו אל הבאר, מעד ונחבל בראשו.
 
We segment ב|רדת|ו in the following manner: ב is an SCONJ+mark; רדת is VERB+advcl with the features VerbForm=Vnoun|Voice=Act|HebBinyan=PAAL andLemma ירד; and the pronominal suffix ו is PRON+nsubj. 
Copular Vnoun forms, however, like היותו should be left unsegmented, consistent with היה-הייתן...

#### VerbType
Hebrew has two possible values for this feature: Cop standing for Copula, and Mod standing for Modal verbs and auxiliaries.
Only forms of היה receive the value VerbType=Cop (see Polarity):
זו הייתה התפילה הקשה ביותר בחיי.

Here הייתה, tagged AUX (with deprel cop), receive the following features:
Gender=Fem | Number=Sing | Person=3 | Polarity=Pos | Tense=Past | VerbType=Cop

The inflected forms of הִנֵּה (tagged AUX ;הינו, הינה, הינם, הינן), standing for a copula:
הרשת הינה בבעלותו של איש העסקים יהושע סטרויסקי.
Gender=Fem | Number=Sing | Person=3 | Polarity=Pos | VerbType=Cop | Tense=Pres.


Modal verbs and auxiliaries belong to a closed POS class (see list of possible Lemmas under AUX in POS tagging in Detail):
החברה שלנו צריכה להיות פתוחה יותר.

Here the root is the ADJ פתוחה. The nsubj is חברה in החברה שלנו.
We have two auxiliaries (tagged AUX):

The first is modal, צריכה, which receive the following features:
Gender=Fem | Number=Sing | Person=3 | VerbType=Mod

THE second, להיות, is an Infinitive functioning as a copula:
Polarity=Pos | VerbForm=Inf | VerbType=Cop

We attach the root to להיות with deprel cop, and to צריכה with deprel aux.

#### HebBinyan
All Hebrew verbs have unique conjugations based on verbal templates called Binyanim. The seven verbal templates can be (loosely) divided into three groups, based on Voice. We assign this feature under Universal Features (formerly under Misc Features):

Active → PAAL, PIEL, HIFIL
הוא קרא להפסקת התופעה.
הדבר סייע להכניס את הספר לרשימת רבי-המכר של "ניו יורק טיימס".

היא הודיעה כי הוועדה תגבש הצעת חוק בנושא העובדים הזרים.

Middle → NIFAL (often reciprocal, but may also be passive), HITPAEL (often in reflexive meaning, but may also be active)
בייקר נפגש אתמול עם נשיא צרפת.
הוא התגלח והתארגן לפני שיצא לעבודתו. 

Passive → PUAL, HUFAL
כל עובד ישראלי שיסכים לעבוד בענף החקלאות ישובץ לעבודה לאלתר.
עד סוף השנה לא תועסק בארץ אף אחות כעובדת זרה.

### Additional Features
#### Polarity
The feature Polarity has two possible values: Pos for positive and Neg for Negative. We assign 
Polarity=Pos to the following POS with specific tokens, as detailed below.

Pronominal copulas, tagged PRON (הוא, היא, הם, הן):
דיווח אמין הוא ערך יסודי, חיוני ומקודש במשרד המשטרה.
Note that these forms do not receive the feature PronType=Prs.

The inflected forms of הִנֵּה (tagged AUX ;הינו, הינה, הינם, הינן) are often used in place of a copula. While this use is not considered grammatical according to the Hebrew Academy, they are nonetheless prevalent, particularly in journalism and academic papers.
מרכיב חשוב ביותר בתהליך קבלת החלטות הינו המידע.
הרשת הינה בבעלותו של איש העסקים יהושע סטרויסקי.


All the forms of היה in copulative function receive this feature, tagged AUX (היה, היו, יהיה, יהיו):
הקרב היה אחד הקרבות הקשים והמפוארים בכל קרבות ישראל.
שנים אלו יהיו גורליות בכמה מישורים.
Note that the feature VerbType=Cop is assigned only to these forms, but not to the pronominal copulas.


We assign Polarity=Neg to the following POS with specific tokens, as detailed below.

Assertion auxiliaries, tagged AUX (e.g., איני, אינך, אינה, אינכם, אינם):
ההבחנות אינן ברורות.
We suggest adding Tense=Pres to these forms only when they function as pure copulas, but not when they negate a participle or a present tense verb, e.g.,:
"איני תומכת באף אחד מן הצדדים ", הכריזה.

Negation adverbs, tagged ADV (e.g., אי, לא, אין):
אין יודעים אם מדובר בהורה בודד, או בקבוצת הורים מסוימת.

Existential verbs (יש) receive the feature Polarity=Pos. They are contrastive to אין in existential meaning (more precisely the lack thereof) which receives the feature Polarity=Neg. E.g,

אין דרך אחת טובה, ולפעמים אנחנו מתכננים תוכניות והדרך משתנה.
באופן טבעי אנחנו מחפשים יזמים שאנחנו מאמינים שיש להם פוטנציאל לבנות ולהוביל חברות ענק.

#### Prefix
The feature for affixation, predominantly a prefix in Hebrew, is Prefix=Yes. 

When modifying a NOUN, a prefix is tagged ADJ:
אני שומע שאתם הולכים להצביע אי אמון בממשלה.

When modifying an ADJ, VERB or an ADV, it is tagged ADV.
ADJ:
בשנת 1984 עלתה לשלטון מפלגת העבודה וחוללה מהפך בלתי צפוי.

VERB:
אי אפשר להפריד בין כושר גופני ליכולת ריצה.
See the discussion on אפשר:  
מה אי אפשר לעשות? ← להפריד בין כושר גופני ליכולת ריצה.
In this construction, אפשר is the root and is tagged VERB (VerbType=Mod), להפריד is the csubj and is also tagged VERB (VerbForm=Inf), and אי is advmod tagged ADV with the features Prefix=Yes and Polarity=Neg (see VerbForm, VerbType & Polarity).
 
ADV:
פונקציה חד-חד-ערכית היא פונקציה המקבלת כל ערך פעם אחת לכל היותר.

#### Abbr
Some NOUNs, PROPNs, ADJs and ADP may appear in their abbreviated forms. Note that the Lemma should be the abbreviated form, not the unabbreviated one. In case we want to be extra diligent, we can add the unabbreviated lemma using the feature Gloss under Misc Features.
  

NOUNs:
יו"ר הוועדה, ח"כ אורה נמיר, טענה כי…
The features we assign here to both are Abbr=Yes | Gender=Fem | Number=Sing. Additionally, the feature Definite=Cons is assigned to יו”ר for being in a compound (smixut) phrase.

PROPNs:
המדינות האחרות בארה"ב נהנו משגשוג חסר תקדים.  

ADJs:
הדמות התנ"כית שממנה הוא שואב השראה היא דוד המלך.

ADPs:
מעריכים שהישיבה תנוהל ע"י שלום עצמו.

#### Typo
In cases where the data has an incorrect form we will assign the feature Typo=Yes under Misc Features. This goes hand in hand with the feature CorrectForm which is used to indicate the correct spelling of a token.

#### CorrectForm
We indicate the correct form of a token, wherever the data contain an incorrect spelling. This is done under Misc Features and is combined with the feature Typo=Yes.

#### Uncertain
When we are not sure of a feature we assigned to a token, or the choice of a POS tag, we should assign the feature Uncertain=Yes under Misc Features. 


### Confusing cases

#### Voice – Act or Mid?


Middle voice refers to reflexive actions, but with the mention of only one argument (and no external agent implied). 

התנועה התעכבה - middle

התנועה עוכבה – passive

In our scheme it refers also to reciprocal actions:

הם התכתבו – middle

הם כתבו אחד לשני – active

Note that the semantic volition and stative verbs are not related to the voice issue. 

Active verbs can be unintentional in nature: ספג, נפל, נפל, מעד, קיבל  


They can also be stative: חי, מת, ישב, עמד, שהה.


As for intransitive forms of HIFIL (הפשיר, האדים – הקרחונים הפשירו, הפנים האדימו), these forms are active since they are not reflexive – when we say הקרחונים הפשירו we don't mean the icebergs don't melt themselves or each other. The middle voice is marked by distinctive morphological forms, HITPAEL and NIFAL. Doron explained this in her article, תרומתו של הבניין למערכת הפועל:

![image](https://user-images.githubusercontent.com/90029994/147973335-1f9d2e5a-10db-4b0a-a5af-095a83fd8f3f.png)

![image](https://user-images.githubusercontent.com/90029994/147973349-266f40ce-222f-4b0f-a6ee-6d849ba9ffc1.png)
![image](https://user-images.githubusercontent.com/90029994/147973359-5d092f05-03ff-4b75-80a6-e9b5c6cc22e8.png)
