# Втора лабораториска вежба по Софтверско инженерство

Тамара Георгиева, бр. на индекс 213207

Control Flow Graph

![image](https://github.com/TamaraGeorgieva/SI_2023_lab2_213207/assets/128751939/122889d2-a79b-479f-b77c-ff7a3519ba3d)

Цикломатска комплексност

Ја добив со формулата v(G)=E-N+2

Во мојот Сontrol Flow Graph имам 34 edges и 25 nodes, што ставено во форулата би било 34-25+2=11.


Тест случаи според критериумот Multiple Condition
Multiple Condition критериумот има 8 тест случаи за (user==null||user.getPassword()==null||user.getEmail()==null)
user==null | user.getPassword()==null | user.getEmail()==null | Multiple Condition |
------------------------------------------------------------------------------------
     T     |             T            |           T           |          T           
     T     |             T            |           F           |          T           
     T     |             F            |           T           |          T           
     T     |             F            |           F           |          T           
     F     |             T            |           T           |          T           
     F     |             T            |           F           |          T           
     F     |             F            |           T           |          T           
     F     |             F            |           F           |          F   
     
Вака изгледа првичната табела според булова алгебра.

user==null | user.getPassword()==null | user.getEmail()==null | Multiple Condition |
------------------------------------------------------------------------------------
     T     |             x            |           x           |          T           
     F     |             T            |           X           |          T                    
     F     |             F            |           T           |          T           
     F     |             F            |           F           |          F   

       
  
Ова ни покажува дека според Multiple Condition критериумот, ние би имале вистинит услов во 7 ситуации а само еднаш невистинит. Потребни ни се сите сегмети од условот да се неточни, за да имаме целосно теночен if, за програмата да продолжи, инаку ќе добиеме  RuntimeException.
