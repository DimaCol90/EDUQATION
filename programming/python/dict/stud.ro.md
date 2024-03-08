## Lucrul cu dict / reusita studentului

1. Creați un dicționar numit student care să conțină următoarele chei: firstname, lastname, age, grade_1, grade_2 și grade_3. Valorile asociate cheilor pot fi orice număr întreg, cu excepția cheii nume și prenume, care ar trebui să fie un șir de caractere.

2. Utilizați o buclă for pentru a parcurge dicționarul și a afișa fiecare cheie și valoare pe un rând separat. Asigurați-vă că valorile asociate cheilor grade_1, grade_2 și grade_3 sunt afișate cu 2 zecimale.

3. Adăugați o funcționalitate pentru a calcula media celor 3 note și afișați-o în consolă. Asigurați-vă că media este afișată cu 2 zecimale.

4. Adăugați o funcționalitate pentru a verifica dacă fiecare student a trecut examenul (adică are o medie de cel puțin 5.00). Afisati intr-un mesaj daca fiecare student a trecut sau nu.



student = {
    "firstname": "Dima",
    "lastname": "Colesnicov",
    "age": 33,
    "grade_1": 10,
    "grade_2": 9,
    "grade_3": 7,
    "english_grade": 7.8
}
total_g=0
count=0
for key, value in student.items():
    if "grade" in key and (type(value) == float or type(value) == int):
        print(f"{key}: {value:.2f}")
        total_g+=value
        count+=1
    else:
        print(f"{key}: {value}")

avg=total_g/count
print(f"average grade of student{student['firstname']} is {avg:.2f}")

if avg>=5:
    print(f"student {student['firstname']} {student['lastname']} has passed the exam ")
else:
    print(f"student {student['firstname']} {student['lastname']} has not passed the exam ")    
