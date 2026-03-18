# PRIMERO

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
    



# Class estudiante
class Estudiante:
    def __init__(self, nombre, nota, definitiva):
        self.nombre = nombre
        self.nota = nota
 
    
    def clasificar(self):
        definitiva = self.calcular_definitiva()
        return clasificar(definitiva)
    
    def calcular_definitiva(notas):
        return sum (nota)/ len (nota)
    
    def calcular_clasificar(self):
        if self.nota == 5:
            return "Excelente"
        elif self.nota >= 3:
           return "Aprobado"
        else:
           return "reprobado"
        
def validar_nota:
        nota >=0 and <=5:


while True:
    nombre = input("Nombre (o 'salir'): ")
    if nombre.lower() == 'salir': 
        break
    print("\n-Resultado- ")
    for i in range(3):
   num = float(input("i+1"))
   if validar.nota
    print(f"{i.nombre}: {i.nota}, {i.calcular_clasificar()}")
