## Operatii de baza cu listele.



* Sa presupunem ca vi se dau 3 liste cu numele persoanelor ce vor participa la un eveniment (fiecare lista vine dintr-o sursa diferita):

    ```python   
    guests_1 = [ "Bethaney Bain", "Kacey Johns", "Manpreet Saunders" ]
    guests_2 = [ "Elwood Curtis", "Diya Griffin", "Kacey Johns" ]
    guests_3 = [ "Tobey Weiss", "Kadie Barnes", "Diya Griffin" ]
    ``` 

* Se cere sa asamblati o lista finala a acestor participanti, eliminand valorile care se dubleaza.
  
  Algoritmul propus de solutionare este acesta:
    1. mai intai de toate concatenati toate listele in una (operatorul +)
    2. creati o lista goala - pentru rezultatul final
    3. pasiti iterativ (**for**) prin lista asamblata si "copiati" cate un element in lista finala NUMAI in cazul in care acesta NU EXISTA deja in lista finala (operatorul **in**)!
    * BONUS, dupa ce ati obtinut lista finala, sortati-o alfabetic inainte sa fie afisata!

guests_1 = ["Bethaney Bain", "Kacey Johns", "Manpreet Saunders"]
guests_2 = ["Elwood Curtis", "Diya Griffin", "Kacey Johns"]
guests_3 = ["Tobey Weiss", "Kadie Barnes", "Diya Griffin"]

guest_list = guests_1 + guests_2 + guests_3
final_list = []

for guest in guest_list:
    if guest not in final_list:
        final_list.append(guest)

final_list.sort() 

print(final_list)
