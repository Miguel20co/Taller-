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
