## Segmentation

> **_NOTE:_** **SHIRA** to update this section.



### Complex expressions NOT to segment
The following expressions are not segmented and retrained as single tokens:

-	היום, החודש, השנה, השבוע (in the temporal adverbial sense "this year" etc)
-	באמת, בדיוק, בדיעבד, בהכרח, בוודאי, ביותר, בכלל, בלבד, במיוחד, במפורש, בעיקר, בפרט, במקביל, בראשונה
-	לבסוף, למעשה, למשל, לעולם, לפחות, לפיכך, לראשונה, לשעבר
-	כאמור, כיום, כמעט, כמובן, כנראה, כעבור
- מחדש

### Similar complex expressions that ARE segmented
-	כרגיל, כראוי - both are ADP+ADJ governed through `obl`
- note that when למחרת is in nismax position, and only when it's in nismax position, it is segemented - ל+מחרת ה+יום, ל+מחרת ה+חקירה. In these cases, מחרת is tagged NOUN (Gender=Fem, lemma=מחרת), governed through `obl` and it governs the next NOUN through `compound`. When it doesn't take `compound`, it stays as unsegmented ADV - למחרת. 
