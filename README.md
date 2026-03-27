# Nivel 1:

def edad():
    user_edad = input("Ingresa tu edad: ")
    print("Tu edad es:", user_edad, "años")

def suma():
    n1 = float(input("Ingresa el primer número: "))
    n2 = float(input("Ingresa el segundo número: "))
    print("La suma es:", n1 + n2)

    def num_aleatorio():
    secreto = random.randint(1, 100)
    intento = int(input("Adivina el número (1-100): "))
    if intento == secreto:
        print("¡Felicitaciones, adivinaste el número!")
    elif intento < secreto:
        print("Es mayor que", intento)
    else:
        print("Es menor que", intento)





        


# Nivel 2:

def palindromo(palabra):
    palabra = palabra.lower()
    if palabra == palabra[::-1]:
        return True
    else:
        return False

def calcular_potencia(base, exponente):
    resultado = base ** exponente
    print("El resultado de la potencia es:", resultado)

def calcular_media(lista):
    total = sum(lista)
    cantidad = len(lista)
    media = total / cantidad
    print("La media de los elementos es:", media)


# Nivel 3:

def invertir_cadena(cadena):
     return cadena[::-1]


def mayor_de_tres_numeros(numero1, numero2, numero3):
    return max(numero1, numero2, numero3)



def calcular_area(radio, altura):
    area = (2 * math.pi * radio * altura) + (2 * math.pi * radio**2)
    return area



def buscar_palabra(cadena, palabra):
    if palabra in cadena:
        return True
    else:
        return False




        


# Nivel 4:
def promedio(*numeros):
    if not numeros:
        return 0
    return sum(numeros) / len(numeros)


def multiplicar_lista(lista, numero):
    nueva_lista = [elemento * numero for elemento in lista]
    return nueva_lista


def mayor_de_varios_numeros(*numeros):
    if not numeros:
        return None
    return max(numeros)


def calcular_mediana(*numeros):
    lista = sorted(numeros)
    n = len(lista)
    if n == 0:
        return None
    medio = n // 2
    if n % 2 != 0:
        return lista[medio]
    else:
        return (lista[medio - 1] + lista[medio]) / 2


def contar_ocurrencias(cadena, palabra):
      return cadena.count(palabra)





      


# Class estudiante
class Estudiante:
    def __init__(self, nombre, notas):
        self.nombre = nombre
        self.notas = notas 

    def calcular_definitiva(self):
     if not self.notas:
            return 0
     return sum(self.notas) / len(self.notas)

    def clasificar(self):
        promedio = self.calcular_definitiva()
        if promedio == 5:
            return "Excelente"
        elif promedio >= 3:
            return "Aprobado"
        else:
            return "Reprobado"

def validar_nota(nota):
    return 0 <= nota <= 5

while True:
    nombre = input("\nNombre del estudiante (o 'salir'): ")
    if nombre.lower() == 'salir': 
        break
    
    notas_temporales = []
    i = 0
    while i < 3:
        try:
            num = float(input(f"Ingrese nota {i+1} (0-5): "))
            if validar_nota(num):
                notas_temporales.append(num)
                i += 1
            else:
                print("Error: La nota debe estar entre 0 y 5.")
        except ValueError:
            print("Error: Ingrese un número válido.")

   estudiante = Estudiante(nombre, notas_temporales)
    definitiva = estudiante.calcular_definitiva()
    estado = estudiante.clasificar()
    
    print("-" * 20)
    print(f"Estudiante: {estudiante.nombre}")
    print(f"Definitiva: {definitiva:.2f}")
    print(f"Resultado: {estado}")
    print("-" * 20)






# Medicamento

class Medicamento:
   def __init__(self,nombre, formula medica, cantidad, precio unitario):
       self._nombre = nombre
       self._formula medica = formula
       self._cantidad = cantidad
       self._precio unitario = unitario
    
    def get_nombre(self):                return self._nombre
    def get_formula_medica(self):        return self._requiere_formula
    def get_cantidad(self):              return self._cantidad
    def precio_unitario(self):           return self._precio
         
    def __str__(self):
        formula = "Si" if self._formula_medica
        else
          "No"
        return (f"{medicamento] {self._nombre}"
                f"formula: {formula}"
                f"cantidad: {self._cantidad"}
                f"precio: {preio_unitario"}
    
    def vender(self,cantidad_vendida):
        if cantidad_vendida <= 0:
            print("invalidad")
            return 0
        if cantiadad_vendidad > self.cantidad:
            print(f"no hay suficiente"
                  f"disponible:")
            
            
        self._cantidad -= cantiadad_vendida:
                return cantiada_vendida * self.precio
            
        else:
            return 0
    
    print(f"insuficiente")
          elf.cantidad -= cantiadad_vendida:
                return cantiada_vendida * self.precio




# Clases basicas

class Persona:
    def __init__(self, nombre, edad):
        self._nombre = nombre
        self._edad = edad
    
    def saludar(self):
        print("hola mi nombre es {self.nombre} y tengo {self.edad} años")







# Herencia
class Vehiculo:
    def __init__(self, marca, modelo, info):
        self._marca = marca
        self._modelo = modelo
        
    def info(self):
        return print(f"vehiculo: {self.marca} {self.modelo}")
    
class Coche(Vehiculo):
    def __init__(self, puertas, modelo, marca):
        super().__init__(marca, modelo)
        self._puertas = puertas
    
    def info(self):
        mensaje = super().imfo()
        return f"{mensaje}, puertas: {self.puertas}"

        
    





# Clases y archivos
class Libro:
    def __init__(self, titulo, autor):
        self._titulo = titulo
        self._autor = autor
        
    def __str__(self):
        return f"{self._titulo}, {self._autor}"
    
    
class Biblioteca:
    def __init__(self,nombres):
        self._nombre = nombre
        self._libros = []
        
    def agrear(self,titulo, autor):
        nuevo_libro = libro(titulo, autor)
        self.libros.append(nuevo_libro)
    
    def listar(self):
        for libro in self.libros:
            print(f"titulo:{libro.titulo}, Autor{libro.autor}")
            
    def guardar(self):
        archivo = open("lista_libros")
        for libro in self.libros:
            archivo.escribir(f"{libro.titulo},{libro.autor}\n")
        archivo.cerrado()
        print("archivo guardado")
        
    def cargar (self):
        archivo = open("lista_libro")
        for line in archivo:
            datos = linea.strip().split(",")
            self.agregar(datos[0], datos[1])
        archivo.close()
        print("Archivo cargador.")

  
  
  
  
  
  
  # Clase Empaque
    class Empaque:
    def __init__(self,material, color, resistencia):
        self.color = color
        self.material = material
        self._resistencia = resitencia
        
    def mostrar_info(self):
        print(f"Empaque de {self.material}, color: {self.capacidad}")
        
    def obtener_resistencia(self):
        return f"aleacion especial: {self._resistencia}"

class caja(Empaque):
    pass

class bolsa(Empaque):
    pass

Caja = caja("madera,15kg")
Bolsa = bolsa("plastico, 50gr")





# Clase Vehiculo
class vehiculo:
    def __init__(self,marca, color, modelo):
        self.marca = marca
        self.color = color
        self._modelo = modelo
        
    def mostrar.info():
        print(f"vehiculo:{self.marca} , color:{self.color}")
        
    def obteer_modelo(self):
        print(f"el modelo es: {self._modelo}")
        
class Moto(Vehiculo):
    pass
class Camioneta(vehiculo):
    pass

moto = Moto("Bera, azul , trxcb")
camioneta = Camioneta ("Ram, negra, Trx")



# Clase planta
class Planta: 
    def __init__(self, tipo):
        self.tipo = tipo

class Arbol(Planta):
    def __init__(self, especie, edad, id_forestal):
        super().__init__("frondoso")   
        self.especie = especie        
        self.edad = edad              
        self.__id_forestal = id_forestal 

    def crecer(self):                
        print(f"El {self.especie} ha crecido un poco más.")

    def oxigenar(self):               
        print("Produciendo oxígeno...")


araguaney = Araguaney("Araguaney", 10, "ABC-789")  

araguaney.crecer()

