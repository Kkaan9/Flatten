# Flatten

1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

output: [1,'a','cat',2,3,'dog',4,5]
Eleman eğer listin içindeyse listeden çıkarmak için tekrar fonksiyon çalışıyor değilse yeni oluşturduğumuz listeye elemanı ekliyor.


list_new=[]

def flatten(x):
    for i in x:
        if isinstance(i, list):
            flatten(i)
        else:
            list_new.append(i)

flatten(input)
print(list_new)
