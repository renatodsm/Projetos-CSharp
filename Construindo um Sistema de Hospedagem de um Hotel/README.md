# Análise de Requisitos do Sistema de Reserva de Hotel

Este documento apresenta uma análise de requisitos para um sistema simples de reserva de hotel, baseado no código C# fornecido.

## Requisitos Identificados

### 1. Classe Pessoa (Guest):
   - **Atributos**:
     - `nome: string` - Representa o nome do hóspede.

### 2. Classe Suite:
   - **Atributos**:
     - `tipoSuite: string` - Representa o tipo de suíte (por exemplo, Premium).
     - `capacidade: int` - Representa o número máximo de hóspedes que a suíte pode acomodar.
     - `valorDiaria: decimal` - Representa a taxa diária da suíte.

### 3. Classe Reserva:
   - **Atributos**:
     - `diasReservados: int` - Representa o número de dias para os quais a reserva foi feita.
   - **Associações**:
     - `suite: Suite` - Representa a suíte reservada.
     - `hospedes: List<Pessoa>` - Representa a lista de hóspedes associados à reserva.

## Diagrama de Classe UML Simplificado

```plantuml
@startuml
class Pessoa {
    nome: string
}

class Suite {
    tipoSuite: string
    capacidade: int
    valorDiaria: decimal
}

class Reserva {
    diasReservados: int
    - suite: Suite
    - hospedes: List<Pessoa>
}

Pessoa --> "*" Reserva
Reserva "1" --> "1" Suite
@enduml
Este diagrama de classe UML simplificado representa a estrutura básica do sistema e as associações entre as classes identificadas nos requisitos.

