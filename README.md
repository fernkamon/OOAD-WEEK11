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
