"Escribe un programa que genere un numero aleatorio del 1 al 10."
"Le debes pedir al usuario que adivine un maximo de 3 intentos."
"Si el usuario adivina el numero, imprimir un mensaje de felicitaciones."
"Si el usuario no logra adivinar el numero, imprimir un mensaje que indique que no lo logro."

"Para manejar numeros aletorios vamos usar la biblioteca random"
"De random la funcion randint() que genera un numero entero, recibe como parametro 2 numeros separados por coma, el minimo y el maximo del rango"


from random import randint

# Declaracion de variables
count = 0 # vale 0 pero cuando llega a while empieza a valer 1 
numero_usuario = int(input("Ingrese un valor: "))
numero_random = randint(1, 10)



if 0 < numero_usuario <= 10: # no usamos mayor o igual en el 0 pq sino lo incluye, y es del 1 al 10 solamente 
    while count < 2: # sin el igual y uno menos porque suma uno de mas
        count += 1 # a while count le suma 1 hasta que llegue a 3
        if numero_usuario is numero_random:
               print("Felicitaciones has adivinado")
               break    
        elif numero_usuario > numero_random:
                print("Igresaste un valor mayor")
                numero_usuario = int(input("Ingrese un valor: "))
        else:
            print("Ingresaste un valor menor")
            numero_usuario = int(input("Ingrese un valor: ")) # se lo vuelvo a pedir porque sino la operacion se va al else de abajo
    else:
        print("No has adivinado el numero")

else:
     print("Ingresaste un valor fuera de rango")


print(numero_random) # imprime el numero que era correcto



# control + c, convertir indentacio en tabulacion, de casualidad si pasa algun error mal indentando


# Conjuntos: son una coleccion de datos de valor unico no ordenados

conjunto = {}
conjunto_vacio = set () # si el conjunto esta vacio va con set (), sino le decimos a python que son diccionarios 


# ADD es una funcion de los conjuntos: 

numeros = {1, 2, 3, 4}
numeros.add(5) # es igual al append de las listas 
print(numeros)


# UPDATE sirve para añadir varios elementos a un set 

numeros = {1, 2, 3, 4}
numeros.update([5, 6, 7])
numeros.update(range(8, 11))
print(numeros)


# LEN

numeros = {1, 2, 3, 4}
print(len(numeros))

# DISCARD elimina un elemento del set, si el item a remover no exite, lo igora
# REMOVE es igual a discard, pero si el item a remover no existe, nos indica un error

# POP en conjuntos

mi_conjunto = {1, 2, 3} # no se puede hacer slicing en conjuntos pq son desordenados!!!
while mi_conjunto: # es como decir while True
    print("Se esta borrando...", mi_conjunto.pop()) # borra todo a diferencia del pop en las listas 



conjunto = {"rojo", "blanco", "azul"}
conjunto.add("violeta") # un solo elemento
conjunto.update(["celeste", "dorado"])
# update va entre listas o tuplas, porque me permite agregar varios elementos iterables
 # update acepta una lista iterable, es decir, agrega varios elementos
print(conjunto)

conjunto = {"verde", "naranja", "azul"}
conjunto.discard("verde") # hay que hacerlo de a uno 
print(conjunto)
# si yo pongo remove y borro algo que no hay me tire error


lista_1 = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
lista_2 = [1, 3, 5, 7]
# transformamos las listas a conjuntos
conjunto_1 = set(lista_1)
conjunto_2 = set(lista_2)
# aca se hace una interseccion entre el conjunto 1 y 2, y en el 3 trae los valores que tienen en comun 
conjunto_3 = conjunto_1.intersection(conjunto_2)
print(conjunto_3)


# Diccionarios, son mutables

diccionario = {"nombre": "Valentin"}
                #clave    #valor
print(diccionario)


# trayendo valor de una clave 
colores = {"amarillo", "azul"}
colores = ["amarillo"]
print(colores)

# DEL, elimina un elemento del diccionario sin modificar el resto
