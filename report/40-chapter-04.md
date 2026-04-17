# Capítulo IV: Product Design

## 4.1. Style Guidelines

### 4.1.1. General Style Guidelines

### 4.1.2. Web Style Guidelines

## 4.2. Information Architecture

### 4.2.1. Organization Systems

### 4.2.2. Labeling Systems

### 4.2.3. SEO Tags and Meta Tags

### 4.2.4. Searching Systems

### 4.2.5. Navigation Systems

## 4.3. Landing Page UI Design

### 4.3.1. Landing Page Wireframe

### 4.3.2. Landing Page Mock-up.

## 4.4. Web Applications UX/UI Design

### 4.4.1. Web Applications Wireframes

### 4.4.2. Web Applications Wireflow Diagrams

### 4.4.3. Web Applications Mock-ups

### 4.4.4. Web Applications User Flow Diagrams

## 4.5. Web Applications Prototyping

## 4.6. Domain-Driven Software Architecture

### 4.6.1. Design-Level Event Storming

### 4.6.2. Software Architecture Context Diagram

### 4.6.3. Software Architecture Container Diagrams

### 4.6.4. Software Architecture Components Diagrams

## 4.7. Software Object-Oriented Design



### 4.7.1. Class Diagrams

```plantuml
@startuml
'//---ENUM---//
enum Gender{
- FEMALE
- MALE
}

enum DeviceStatus{
- ON
- OFF
- MAINTENANCE
}

enum FollowUpStatus{
- ACTIVE
- COMPLETED
- CANCELLED
}

enum PaymentStatus{
- PENDING
- PAID
- EXPIRED
- CANCELLED
}

enum NotificationType{
- CRITICAL_ALERT
- REMINDER
- SYSTEM_INFO
}





'//---ENTITIES---//
entity Parents{
* idParents: UUID
- name: String
- phoneNumber: String
- email: String
- babies: List<baby>
- subscription: UserSubscription
---
+ addBaby(baby: Baby): void
+ getActiveSubscription(): UserSubscription
}

entity Baby{
* idBaby: UUID
- name: String
- birthday: LocalDate
- gender: Gender
- parent: Parents
- device: Device
- records: List<HealthRecord>
---
+ calculatedAge(): int
+ getLastRecord(): HealthRecord
}

entity Medic{
* idMedic: UUID
- name: String
- phoneNumber: String
- email: String
- followUps: List<FollowUp>
---
+ createdAlertRange(config: AlertRange): void
}

entity Device{
* idDevice: UUID
- model: String
- status: DeviceStatus
- firmwareVersion: String
---
+ syncData(): void
+ checkBattery(): int
}

entity HealthRecord{
* idHealthRecord: UUID
- temperature: Double
- weight: Double
- oxygenSaturation: Double
- observation: String
- createdAt: LocalDateTime
- baby: Baby
- device: Device
- appliedRange: AlertRange
---
+ isCriticValue(): boolean
}

entity HealthReport{
+ idReport: UUID
- baby: Baby
- generatedAt: LocalDateTime
- summary: String
- pdfURL: String
- avgTemperature: Double
- weightGain: Double
---
+ generatedPDF(): void
+ calculatedStats(record: List<HealthRecord>): void
}

entity AlertRange{
* idAlertRange: UUID
- type: String
- maxValue: Double
- minValue: Double
- description: String
- createdBy: Medic
---
+ getMaxValue(): Double
+ getMinValue(): Double
}

entity SubscriptionPlan {
* idPlan: UUID
- name: String
- price: Double
- feature: String
---
+ getPlanDetails(): String
}

entity UserSubscription {
* idUserSub: UUID
- parents: Parents
- plan: SubscriptionPlan
- startDate: LocalDateTime
- endDate: LocalDateTime
- status: PaymentStatus
---
+ isValid(): boolean
+ renewSubscription(): void
}

entity FollowUp {
* idFollow: UUID
- baby: Baby
- medic: Medic
- status: FollowUpStatus
- startAt: LocalDateTime
- endAt: LocalDateTime
---
+ updateStatus(newsStatus: FollowUpStatus): void
+ getDurationInDays(): int
}

entity Notification {
* idNotification: UUID
- type: NotificationType
- title: String
- description: String
- sendAt: LocalDateTime
- readAt: LocalDateTime
- isRead: boolean
- parents: Parents
- medic: Medic
- record: HealthRecord
---
+ markAsRead(): void
+ send(): void
}

'//---RELATIONSHIPS---//

' Relaciones de Composición (Ciclo de vida dependiente)
Parents "1" *-- "1..*" Baby
Baby "1" *-- "0..*" HealthRecord
Baby "1" *-- "0..*" HealthReport

' Relaciones de Asociación y Agregación
Parents "1" -- "1" UserSubscription
UserSubscription "n" -- "1" SubscriptionPlan
Baby "1" o-- "0..1" Device
Medic "1" -- "0..*" FollowUp
FollowUp "n" -- "1" Baby
Medic "1" -- "0..*" AlertRange
HealthRecord "n" -- "0..1" AlertRange
Device "1" -- "0..*" HealthRecord

' Relaciones con ENUMS (Uso de tipos)
Baby ..> Gender : <<use>>
Device ..> DeviceStatus : <<use>>
FollowUp ..> FollowUpStatus : <<use>>
UserSubscription ..> PaymentStatus : <<use>>
Notification ..> NotificationType : <<use>>

' Relaciones de Notificación
Notification "n" -- "0..1" Parents
Notification "n" -- "0..1" Medic
Notification "n" -- "0..1" HealthRecord
@enduml
```


## 4.8. Database Design

Antes de crear una base de datos, se debe de modelar el sistema considerando las necesidades del proyecto o negocio a realizar. La finalidad de esto es mostrar entidades, atributos y las relaciones que tienen dichas entidades (IBM, s.f.).

### 4.8.1. Database Diagram

```plantuml

@startuml
'//---Users---//
entity Parents{
*idParents: String <<PK>>
---
name: String
phoneNumber: String
email: String
}
entity Medic{
*idMedic: String <<PK>>
---
name: String
phoneNumber: String
email: String
}





'//---IoT Hardware---//
entity Device {
  *idDevice: String <<PK>>
  --
  model: String
  status: String
  firmwareVersion: String
  idBaby: String <<FK>>
}





'//---Subscription---//
entity SubscriptionPlan{
*idPlan: String <<PK>>
---
name: String
price: Double
features: String
}
entity UserSubscription{
*idUserSub: String <<PK>>
---
startDate: LocalDateTime
endDate: LocalDateTime
paymentStatus: String
idParents: String <<FK>>
idPlan: String <<FK>>
}





'//---To Business---//
entity Notification{
*idNotification: String <<PK>>
---
type: String
read: Boolean
description: String
readAt: LocalDateTime
sentAt: LocalDateTime
idParents: String <<FK>>
idMedic: String <<FK>>
idHealthRecord: String <<FK>>
}
entity AlertRange{
*idAlertRaNge: String <<PK>>
---
type: String
maxValue: Double
minValue: Double
description: String
idMedic: String <<FK>>
}





'//---Related to the baby's health---//
entity Baby{
*idBaby: String <<PK>>
---
name: String
birthday: LocalDateTime
gender: String
idParents: String <<FK>>
}
entity HealthRecord {
  *idHealthRecord: String <<PK>>
  --
  temperature: Double
  weight: Double
  oxygenSaturation: Double
  createdAt: LocalDateTime
  idBaby: String <<FK>>
  idDevice: String <<FK>>   
}
entity FollowUp{
*idFollow: String
---
status: String
startAt: LocalDateTime
endAt: LocalDateTime
idBaby: String <<FK>>
idMedic: String <<FK>>
}





'//---Dashboard---//
entity HealthReport{
*idReport: String <<PK>>
---
generatedAt: LocalDateTime
summary: String
pdfURL: String
avgTemperature: Double
weightGain: Double
idBaby: String <<FK>>
}





'//---Relationship---//
Parents ||--|{ Baby
Parents ||--|| UserSubscription

UserSubscription ||--|{ SubscriptionPlan
Baby ||--o| HealthReport

Baby ||--o| HealthRecord
Baby ||--o{ FollowUp

Medic ||--o{ FollowUp
Parents ||--o{ Notification

Medic ||--o{ AlertRange
Medic ||--o{ Notification

Baby ||--o|Device
HealthRecord ||--o{ Notification

Device ||--|{ HealthRecord
@enduml

```

- Descripción de entidades
    - Parents
        - Usuario y tutor legal dentro de la aplicación.
        - Un 'Parents' solamente tiene una suscripción.
        - Un 'Parents' puede monitorear 1 a muchos 'Baby'.
        - Un 'Parents' puede estar recibiendo 0 a muchas notificaciones.
    - SubscriptionPlan
        - Son todos los planes que existen en la aplicación.
    - UserSubscription
        - Es la suscripción asociada al usuario 'Parents'.
        - Necesita el plan seleccionado y al usuario que tiene el plan.
    - Baby
        - Objeto de observación.
        - Es necesario que se guarde la información del 'Parents' al que pertenece un 'Baby'.
    - Device
        - Representación del dispositivo IoT.
        - La información conseguida se debe relacionar a un 'Baby'.
    - HealthRecord
        - Registro historico de los signos vitales.
        - Guarda el 'Device' que obtiene informacion.
        - Guarda el 'Baby' al que pertenecen los 'Device'.
    - HealthReport
        - Consolidado de datos procesados para visualización en el Dashboard.
        - Facilita la interpretación de tendencias de crecimiento y salud sin necesidad de consultar registros individuales.
    - Notification
        - Encargado de mensajes para 'Parents' y 'Medic'.
        - Necesita el 'Parents' y 'Medic' que recibiran las notificaciones.
    - FollowUp
        - Entidad intermedia de 'Baby' y 'Medic'.
    - Medic
        - Usuario profesional con privilegios altos.
        - Visualiza al 'Baby' y gestiona los 'AlertRange'
    - AlertRange
        - Configuración hecha por un medico o puesta de manera estándar.