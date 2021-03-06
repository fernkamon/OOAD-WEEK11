# OOAD-WEEK11
State Diagram
##ส่งการบ้าน

### State Diagram

ภาพที่ 1  การเปิดคอมพิวเตอร์

 ```
@startuml
title turn on COMPUTER

[*] --> OFF
OFF : switch shut down
OFF -r-> ON
ON : turn on computer

ON -d-> Boot : computer work
Boot : loading System

Boot -l-> Ready : boot computer into works
Ready : computer available
Ready --> [*]
@enduml
 ```
 
 ![](https://github.com/fernkamon/OOAD-WEEK11/blob/master/1.png)


 ภาพที่2 เครื่องคิดเลข
 
  ```
 @startuml
title Calculator

[*] --> OFF
OFF : Calculator closed
OFF -r-> ON : Press on
ON : turn on Calculator

ON -r-> Number1 : Press Number set 1
Number1 : Number 0 - 9
Number1 -d-> OP : Press Operator
OP : Operators is + - * /

OP -l-> Number2 : Press Number set 2
Number2 : Number 0 - 9

Number2 -l-> resalt : Press resalt
resalt : Opertor =

resalt -d-> Clear : Press Clear
Clear : clear monitor with space
Clear --> Number1 : reset to operands
Clear -r-> [*]
@enduml
 ```
 
 ![](https://github.com/fernkamon/OOAD-WEEK11/blob/master/2.png)
 
 ภาพที่3 การกดปุ่ม ATM
 
  ```
  @startuml
title  ATM
[*] -r-> keypad : wait press keypad
keypad : keypad 0 -9
keypad -d-> AddedValue : press keypad
AddedValue : Press the button to \ncomplete the set.
AddedValue -d-> keypad : Unexpired
AddedValue -l-> Transaction 
Transaction : Deposit, withdraw and transfer money
Transaction -l-> [*]
@enduml

   ```
 ![](https://github.com/fernkamon/OOAD-WEEK11/blob/master/3.png)
 

ภาพที่ 4 ตู้เติมเงินออนไลน์

 ``` 
@startuml
title  Online Top Up
[*] -r-> keypad : wait press keypad
keypad : keypad 0 -9
keypad --> AddedValue : press keypad
AddedValue : Press the button 10-digit dialing
AddedValue --> keypad : Unexpired
AddedValue -r-> topUp 
topUp : Deposit money As needed
topUp -r-> Coin : insert Coin
Coin : Coin stated
Coin -d-> System : calculations
System -l-> network :Send data 
network -d-> telephone : Prepaid service users
network : Mobile networks of users
telephone : telephone User
telephone -d-> telephone : Check money
telephone -l-> [*]
@enduml

 ```
 
 ![](https://github.com/fernkamon/OOAD-WEEK11/blob/master/4.1.png)
 
 ภาพที่ 5 การพิมพ์งาน
 
 ```
 @startuml
title  use Microsoft office Word
[*] -r-> Program : into program
Program : program Word
Program -r-> FirstPage : into first page
FirstPage : Page for printing
FirstPage -r-> framework : Opening Page Setup
framework : Page Setup
framework --> FirstPage : Back to work
FirstPage --> insert : To add photos
insert : photos graph etc.
FirstPage --> printer : finish
printer --> printer :  Make sure the print.
printer --> [*]
@enduml
 ```

![](https://github.com/fernkamon/OOAD-WEEK11/blob/master/5.png)

### Activity Diagram
 
ภาพที่ 1 การกดสวิตซ์แล้วไฟติด

 ```
@startuml
title Press the switch and light
(*) --> "Input operation"

if "If the press switch" then
  -->[true] "LED stick"
    -r-> [Ending \nprocess](*)
else
  ->[false] "LED OFF"
  -->[Ending process] (*)
endif

@enduml
 ```
 
 ![](https://github.com/fernkamon/OOAD-WEEK11/blob/master/Activity1.png)

ภาพที่ 2 การเปิดหลักสูตรการเรียน

 ```
@startuml
title registration
(*) -r->  [registration create\ncurriculum]curriculum

curriculum -d-> [Choose a course \nthat will teach]Subject
curriculum --> [Requiring teachers \nin each subject]Teacher
if "If All subjects \nthen, define" then
  -r->[true \n create] "Student Guide"
  -->[send]"book center"
"Student Guide" --> [send] "student"  
else
  -l->[false] Teacher

endif
"book center"  --> "Open registration"
"student"  --> "Open registration"
  --> (*)
@enduml
 ```
 
 ![](https://github.com/fernkamon/OOAD-WEEK11/blob/master/Activity2.png)
 
 ภาพที่ 3 การสมัครสมาชิก

```
 @startuml
title Subscriptions
(*) -r->  [data entry]"Candidate information"

if "If Enter your information" then
  -r->[true] "Register"
  -d->[send]"e-mail"
"e-mail" -l-> [send] "number member"  
else
  -l->[false] "Candidate information"
"number member"    --> (*)
endif

@enduml
 ```
 
 ![](https://github.com/fernkamon/OOAD-WEEK11/blob/master/Activity3.png)
 
 ภาพที่ 4 ระบบร้านกาแฟ
 
 ```
 @startuml

(*) -r->  "make Coffee"
 "make Coffee" --> "Check Coffee"
if "If Check Coffee complete" then
  -r->[true] "Send order"
else
  -l->[false] "make Coffee"
"Send order"--> (*)
endif

@enduml
 ```
 
 ![](https://github.com/fernkamon/OOAD-WEEK11/blob/master/Activity4.png)
 
 ภาพที่ 5 ระบบเช็คสินค้า
 
  ```
  @startuml

(*) -r->  "recive"
 "recive" --> "Check product"
if "Count the number \nof products available" then
  -r->[count complete] "keep storehouse"
else
  -l->[not complete] "Check product"
"keep storehouse"--> (*)
endif

@enduml
   ```

![](https://github.com/fernkamon/OOAD-WEEK11/blob/master/Activity5.png)
