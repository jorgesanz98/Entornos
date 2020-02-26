```mermaid
classDiagram
      Persona <|-- Empleado
      Persona <|-- Cliente
      Directivos"0*" -- "0*"Empleado : subordinado
      Empleado *-- Directivos
      Cliente"0* clientes" --o "1*"Empresas
      Empleado"1* empleados" --* "1*"Empresas
      

      class Persona{
          +age : Integer
          +name : String
          +mostrar()
      }
      class Cliente{
          +String telefono_de_contacto
          +mostrar()
      }
      class Empleado{
          +int sueldo_bruto
          +mostrar()
          +calcular_salario_neto()
      }
      class Directivos{
          +String categoria
          +mostrar()
      }
      class Empresas{
          +mostrar()
      }