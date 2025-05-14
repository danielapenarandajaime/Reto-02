# Reto-02
## Agendamiento de citas
classDiagram
     Cita "1" -- "1" Receta : genera
    Paciente "1" -- "*" Cita : agenda
    Doctor "1" -- "*" Cita : atiende
    Receta : +String resumen
    Receta : +list<String> medicamentos
    Receta : +list<String> examenes
    Receta: +reclamar_medicamentos()
    class Cita{
      +int fecha
      +seleccionar_especialidad()
      +seleccionar_doctor()
      +programar()
      +cancelar()
    }
    class Paciente{
      -String nombre
      +double peso
      +double altura
      +dar_sintomas()
    }
    class Doctor{
      +String nombre
      +String especialidad
      +examinar()
      +diagnosticar()
    }
