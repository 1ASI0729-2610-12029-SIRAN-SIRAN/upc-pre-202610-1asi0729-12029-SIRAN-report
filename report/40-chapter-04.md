# Capítulo IV: Product Design

## 4.1. Style Guidelines

### 4.1.1. General Style Guidelines
Branding:
Para el logotipo de **SIRAN**, se ha optado por un diseño protector y clínico que refleja la seguridad de la aplicación. El logotipo se compone de una tipografía sólida y moderna, acompañada de un icono que simboliza el cuidado neonatal y el monitoreo constante, así como un escudo de protección. Los colores utilizados son tonos azules y celestes, lo que refuerza la idea de confianza, salud y tranquilidad.

### Tipografía

La tipografía de nuestra aplicación será fácilmente legible y estética. Se utilizará la fuente **Poppins** para botones y títulos, mientras que para los textos se empleará **Roboto**.

El interlineado será de **1.15**, con un tamaño base de:
- **18px** en la versión web
- **16px** en la versión móvil

### Pesos y estilos

- **Heading 1**
    - Poppins, Bold, 18px, Negro (#000000)
    - Poppins, Normal, 18px, Blanco (#FFFFFF)

- **Heading 2**
    - Poppins, Normal, 16px, Rojo (#FF0000)
    - Poppins, Normal, 16px, SkyBlue (#87CEEB)

- **Heading 3**
    - Poppins, Normal, 14px, LawnGreen (#7CFC00)

- **Texto**
    - Roboto, Bold, 11px, Rojo (#FF0000)
    - Roboto, Normal, 9px, Blanco (#FFFFFF)


### Colores

Nuestra plataforma, al estar dirigida a centros de salud y atención neonatal, utiliza una paleta cromática que transmite confianza, cuidado y profesionalismo:

- **#E3EDFF (azul lavanda pálido):** aporta calma y cercanía en testimonios.
- **#FFFFFF (blanco):** representa limpieza y orden.
- **#F2F2F2 (blanco grisáceo):** permite diferenciar secciones con sutileza.
- **#4A7FF0 (azul brillante):** resalta elementos interactivos y fomenta la interacción.
- **#000000 (negro):** asegura legibilidad y formalidad en los textos.
- **#C0EEE3 (cian pastel):** transmite bienestar y armonía.
- **#CDEBFF (celeste pastel):** refuerza la serenidad y la seguridad visual en la experiencia del usuario.

---

## Spacing

El diseño de **SIRAN** destaca por un espacio amplio y regular que sirve como eje organizador. Esta apuesta por el “aire” entre elementos mejora la claridad informativa y proyecta una imagen de orden y estabilidad, haciendo que la interacción del usuario sea mucho más cómoda.

### Escala de Espaciado (Spacing System)

- **4px:** Micro-ajustes (iconos, etiquetas pequeñas).
- **8px:** Espaciado interno entre elementos muy cercanos (título y subtítulo).
- **12px:** Espaciado entre elementos de una lista o tarjetas pequeñas.
- **16px:** Relleno (padding) interno estándar para botones y tarjetas.
- **20px:** Espaciado entre bloques de texto cortos.
- **24px:** Margen entre elementos de un mismo grupo (botones de planes).
- **32px:** Espacio entre columnas o elementos secundarios.
- **40px:** Margen superior/inferior para secciones pequeñas de contenido.
- **48px:** Separación estándar entre secciones de información (testimonios).
- **64px:** Espaciado generoso para resaltar el hero (cabecera).
- **80px:** Margen de seguridad para respiración visual en dispositivos móviles.
- **96px:** Separación amplia entre secciones principales (precios y beneficios).
- **128px:** Margen superior/inferior para secciones de alto impacto visual.
- **160px:** Espaciado máximo para secciones con mucho aire (capturas de pantalla).
- **192px:** Margen de diseño para pantallas de escritorio extra anchas.
- **256px:** Espaciado para composiciones artísticas o cierres de página.



### Tono de Comunicación y Lenguaje

Para **SIRAN**, la comunicación se sitúa en un equilibrio entre la autoridad clínica y la empatía humana:

- **Serio:** El manejo de datos vitales de bebés exige rigor absoluto, transmitiendo precisión y responsabilidad.
- **Formal:** Uso de lenguaje profesional que respete la relación médico-paciente y la institucionalidad.
- **Respetuoso:** Reconoce la vulnerabilidad y preocupación de padres y personal médico.
- **Sereno:** Transmite calma, control y seguridad en momentos de tensión.



### Sustento de Principios y Orientación del Servicio

La página está orientada como una extensión digital de la confianza clínica. Inspirada en sistemas de diseño como **Carbon Health** o **Spectrum (Adobe)**, se basa en:

- **Claridad Operativa:** Reducción del ruido visual. La información crítica (alertas y signos) debe ser legible en segundos, priorizando la jerarquía visual para evitar fatiga cognitiva.
- **Empatía Silenciosa:** Uso de espacios en blanco y paleta de azules suaves para reducir la ansiedad del usuario.
- **Accesibilidad y Confiabilidad:** Enfoque en la consistencia, asegurando que iconos y mensajes sean predecibles y claros, eliminando ambigüedades.

---

> **"SIRAN se presenta como un ecosistema de vigilancia silenciosa y precisa, donde la tecnología se humaniza para ofrecer paz mental a través de una comunicación directa, experta y profundamente protectora."**


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

El Diseño de Software Orientado a Objetos (OOD) es una metodología que busca la definición de los objetos y la manera que se relaciona con otros objetos, con la finalidad de mantener un diseño coherente y eficiente, al momento de escalar (Schmidt, 2018).

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