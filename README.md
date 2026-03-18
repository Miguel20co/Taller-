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
    
