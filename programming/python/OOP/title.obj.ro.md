## programare OOP. Obiecte și clase

---

* Să presupunem că ni s-a dat o clasă


```python
class Title:
  pass
```

* care este un șablon pentru obiecte de tip „titlu” (nume de cărți, articole, pagini)
* ESTE NECESAR sa:
   1. Adăugați un constructor la clasă - astfel încât să poată seta proprietatea **text** transmisă în momentul creării unui nou obiect (```__init__(...)```), de exemplu. ```t1 = Title("Programming in Python 3")```
   2. Adăugați o metodă pentru conversia titlului în șir **```__str__(...)```** care la momentul tipăririi unui obiect de tip titlu va da următorul rezultat
    ```
     -= PROGRAMMING IN PYTHON 3 =-
    ```

class Title:
    def __init__(self, text):
        self.text = text

    def __str__(self):
        return f"-= {self.text.upper()} =-"


t1 = Title(input("your text: "))
print(t1)  
