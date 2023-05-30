# Втора лабораториска вежба по Софтверско инженерство

Тамара Георгиева, бр. на индекс 213207

Control Flow Graph

![image](https://github.com/TamaraGeorgieva/SI_2023_lab2_213207/assets/128751939/122889d2-a79b-479f-b77c-ff7a3519ba3d)

Цикломатска комплексност

Ја добив со формулата v(G)=E-N+2

Во мојот Сontrol Flow Graph имам 34 edges и 25 nodes, што ставено во форулата би било 34-25+2=11.


Тест случаи според критериумот Multiple Condition
Multiple Condition критериумот за (user==null||user.getPassword()==null||user.getEmail()==null) можеме да го прикажеме со тебаела на вистинитост со 3 варијабли и да ги видиме можните резултати.

user==null | user.getPassword()==null | user.getEmail()==null | Multiple Condition 

     T       |             T          |           T          |        T           
     T       |             T          |           F          |        T           
     T       |             F          |           T          |        T           
     T       |             F          |           F          |        T           
     F       |             T          |           T          |        T           
     F       |             T          |           F          |        T           
     F       |             F          |           T          |        T           
     F       |             F          |           F          |        F   
     
Вака изгледа првичната табела според булова алгебра.
Но тука можеме да видиме дека овие 8 изрази можеме да ги доведеме до 4, и да ја добиеме точната табела:
user==null | user.getPassword()==null | user.getEmail()==null | Multiple Condition |
------------------------------------------------------------------------------------
     T     |             Х            |           Х           |          T           
     F     |             T            |           X           |          T                    
     F     |             F            |           T           |          T           
     F     |             F            |           F           |          F          
  
Ова ни покажува дека според Multiple Condition критериумот, ние би имале вистинит услов во 3 ситуации а само еднаш невистинит. Потребни ни се сите сегмети од условот да се неточни, за да имаме целосно теночен if, за програмата да продолжи, инаку ќе добиеме  RuntimeException.
