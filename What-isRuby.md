<img src="ruby.png" alt="ruby" width="30" align="right">

# Que es Ruby?

<div style="margin-top: 30px; ">
</div>

Ruby es un lenguaje interpretado, como javascript **(JS)** pero en este caso tambien es mas orientado a objetos **(POO)** , quiere decir que todo es un objeto.

Es dinamico quiere decir que no necesita agregar los _data types_ a los mismos , el interprete entiende el tipo de dato, aunque puede ser cambiadas en tiempo de ejecucion. Es claro como [Python](https://www.python.org/) pero fuerte en cuando a la creacion de proyectos y legible.

<div style="margin-top: 30px; "></div>

---

<left>
<div style="margin-top: 10px; "></div>

## Variables

Las variables, ya sabes son lugares o espacio en memoria donde guardar un valor para ser utilizado, usando un nombre caracteristico y que pueden guardar un tipo de valor, por ejemplo:

```ruby
miVariable = 10
miVariableText = "Hola Mundo"
```

<div style="margin: 30px; "></div>

### **Variables de Instancia :**

Son variables que pertenecen a una instancia de una clase, y se utilizan datos de esa instancia. Las de instancia se definen usando el **@**

```ruby
class Persona
  def initialize(nombre, edad)
    @nombre = nombre
    @edad = edad
  end
end

# Crear una nueva instancia de la clase Persona y asignarle valores a sus variables de instancia
juan = Persona.new("Juan", 25)

```

<div style="margin: 30px; "></div>

### **Variables de Clase :**

Son variables que pertenecen a una clase en su conjunto y se pueden compartir entre todas las instancias de ESA CLASE, y aqui se usan **@**

```ruby
class Persona
  @@total_personas = 0

  def initialize(nombre, edad)
    @nombre = nombre
    @edad = edad
    @@total_personas += 1
  end

  def self.total_personas
    @@total_personas
  end
end

# Crear dos instancias de la clase Persona
juan = Persona.new("Juan", 25)
maria = Persona.new("Maria", 30)

# Acceder a la variable de clase desde fuera de la clase
puts "Total de personas creadas: #{Persona.total_personas}"
juan = Persona.new("Juan", 25)

```

<div style="margin: 30px; "></div>

### **Variables de Globales :**

Son variables que pueden accederse desde cualquier parte desde cualquier parte del programa , incluye si estan dentro de funciones y clases (_no recomendable_ ), este es un ejemplo

```ruby
# Crear una variable global y asignarle un valor
$nombre_app = "Mi aplicación"

# Acceder a la variable global desde cualquier parte del programa
def imprimir_nombre_app
  puts "El nombre de la aplicación es: #{$nombre_app}"
end

imprimir_nombre_app # El nombre de la aplicación es: Mi aplicación


```
