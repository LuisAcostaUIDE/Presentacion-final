# Presentacion-final
 # 1. Registrar usuario
print("EL juego del Ahorcado")
nombre = input("Por favor, ingresa tu nombre: ")
print(f"Hola, {nombre}. Buena suerte!")

# 2. Seleccionar palabra secreta
palabra_secreta = "ciberseguridad".lower()
palabra_mostrada = ["_"] * len(palabra_secreta)
intentos_restantes = 6

print("\n¡Comencemos el juego!")
print(" ".join(palabra_mostrada))

# 3.Comienza el juego
while intentos_restantes > 0:
    # Adivinar letra
    letra = input("\nAdivina una letra: ").lower()
    
    if letra in palabra_secreta:
        print("Correcto!")
        # Actualizar las posiciones de las letras adivinadas
        for i in range(len(palabra_secreta)):
            if palabra_secreta[i] == letra:
                palabra_mostrada[i] = letra
    else:
        print("Incorrecto. Pierdes un intento.")
        intentos_restantes -= 1
 # Mostrar progreso
    print(" ".join(palabra_mostrada))
    print(f"Intentos restantes: {intentos_restantes}")
    
    # Comprobar si se completó la palabra
    if "_" not in palabra_mostrada:
        print("\nFelicidades, ganaste!")
        break
else:
    print("\nLo siento, has perdido :c.")
    print(f"La palabra secreta era: {palabra_secreta}")

EXPLICACION DE LA FUNCIONALIBILIDAD DEL CODIGO

Parte 1: Bienvenida al Juego

"Primero, nuestro programa da la bienvenida al jugador y le pide que escriba su nombre. Para esto usamos la función print para mostrar el mensaje, y input para que el usuario escriba su nombre. Todo lo que el jugador escribe se guarda en una variable llamada nombre. Después, saludamos al jugador usando algo llamado f-strings, que nos permite insertar el nombre directamente en una frase."

nombre = input("Por favor, ingresa tu nombre: ")
print(f"Hola, {nombre}. Buena suerte!")

Parte 2: Preparación del Juego

"El siguiente paso es preparar el juego. Aquí definimos una palabra secreta, que en este caso es 'ciberseguridad'. Luego, creamos una lista llamada palabra_mostrada que contiene guiones bajos para representar las letras aún no adivinadas. Así, el jugador puede ver su progreso."

(Ejemplo del código)



palabra_secreta = "ciberseguridad".lower()
palabra_mostrada = ["_"] * len(palabra_secreta)
intentos_restantes = 6
"También definimos intentos_restantes para controlar cuántas veces el jugador puede fallar antes de perder."

Parte 3: Ciclo Principal del Juego

"El corazón del programa está en un ciclo while. Este ciclo se repite mientras el jugador tenga intentos disponibles. Cada vez, el programa pide al jugador que adivine una letra."

"Si la letra que el jugador adivina está en la palabra secreta, el programa la coloca en su posición correcta. Para esto usamos un for que revisa cada letra de la palabra secreta. Si la letra no está, el programa resta un intento y le muestra al jugador cuántos intentos le quedan."

if letra in palabra_secreta:
    for i in range(len(palabra_secreta)):
        if palabra_secreta[i] == letra:
            palabra_mostrada[i] = letra
else:
    intentos_restantes -= 1

Parte 4: Final del Juego

"El juego termina cuando el jugador completa la palabra o cuando se quedan sin intentos. Si completan la palabra, el programa felicita al jugador. Si no, muestra un mensaje diciendo que perdió y revela la palabra secreta."


if "_" not in palabra_mostrada:
    print("¡Felicidades, ganaste!")
else:
    print("Lo siento, has perdido.")

"Ahora, ejecutemos el programa para ver cómo funciona. Ingreso mi nombre, intento adivinar la palabra letra por letra y observo cómo el programa actualiza la palabra mostrada y los intentos restantes. Finalmente, vemos qué pasa si gano o pierdo."


