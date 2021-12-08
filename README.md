# Satzmetzer
Split German text to sentence! Uses TRIE-Regex to filter ordinal numbers (23.04., 2.5. ...), roman numbers, (II., XI. ...) 15,000 abbreviations (z.B., Abk. ...) , about 7,500 second-level domains (.com.br, ac.at ...), 1500 file name filename extensions (hallo.docx, tabelle.xlsx)   

Before writing this class, I had tested about 20 classes, modules, functions, and methods to split German text to sentences. I wasn't happy with any of the results, so I wrote this class here! It doesn't use any AI, just old school Regex! 


It is very simple to use! Here is everything you need to know:

```
textzumsplitten ='''Hallo, ich bin ein Text. Zerhack mich bitte! Ich halte es nicht mehr aus. Wenn du mich bis zum 23.04. nicht zerhackst, rufe ich Papst Hackerpeter X. an und schicke ihm das Dokument erhatmichnichtzerhackt.docx, er wird z. B. sehr böse auf dich sein! Darauf kannst du einen lassen!'''

from satzmetzger import Satzmetzger
losgehts = Satzmetzger()
textfertig = losgehts.zerhack_den_text(textzumsplitten, debug=False)
for indi, zerhacktersatz in enumerate(textfertig):
    print(indi, end='\t\t')
    print(zerhacktersatz)
```

```
#Output:
#0		Hallo, ich bin ein Text.
#1		Zerhack mich bitte!
#2		Ich halte es nicht mehr aus.
#3		Wenn du mich bis zum 23.04. nicht zerhackst, rufe ich Papst Hackerpeter X. an und schicke ihm das Dokument erhatmichnichtzerhackt.docx, er wird z. B. sehr böse auf dich sein!
#4		Darauf kannst du einen lassen!
```
