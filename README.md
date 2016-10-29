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

![]()
 
