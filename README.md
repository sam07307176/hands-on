# hands-on-on3/20
# Sentence Extractor
***
方便分析日語分析句子的主詞、動詞、受詞。
===
***
```python
def parsing(textLIST):
    count=0
    while count < len(textLIST):
        print ("Line" + str(count+1) + " = " + textLIST[count])
       
        #search subject
        index1 = textLIST[count].find("が")
        print ("Subject = " + textLIST[count][0:index1])
    
        #search object
        index2 = textLIST[count].find("を")
        print ("Object = " + textLIST[count][index1+1:index2])
    
        #search verb
        index3 = textLIST[count].find("す")
        print ("Verbs = " + textLIST[count][index2+1:index3])
    
        print ("===========================================")
        count += 1
    
   
with open("./inputSTR.txt", mode='r', encoding="Utf-8") as f:
    inputLIST = f.readlines() 
    print(inputLIST)
