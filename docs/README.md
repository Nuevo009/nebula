```puml
@startuml
title Case 1: Good handshake

!pragma teoz true
skinparam sequenceMessageAlign center

actor "Initiator" as i
actor "Responder" as r

-> i: tun rx
i -> i: Stage 0: Prepare handshake
i -> r: stage 1 packet

r -> r: Stage 1: Stand up tunnel

r -> i: Stage 2 packet
i -> i: Stage 2: Stand up tunnel
@enduml
```