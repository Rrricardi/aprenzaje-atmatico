# aprenzaje-atmatico
import random
#primer punto
def es_entero_valido(x):
    try:
        return int(x)
    except ValueError:
        return None
while True:
    entrada = input("Ingrese un número entero menor o igual a 12: ")
    numero = es_entero_valido(entrada)

    if numero is None:
        print("No es un número entero. Intente de nuevo.")
        continue  

    if numero <= 12:
        print(f"¡Perfecto! Ingresaste: {numero}")
        break     
    else:
        print("El número debe ser menor o igual a 12. Intente de nuevo.")
        continue 
A=[]
B=[]
#segundo punto
while len(A) < numero:    # aqui se crea la lista A
    entrada = input("Ingrese un número entero para la lista A: ")
    numero_ingresar = es_entero_valido(entrada)
    if numero_ingresar is None:
        print("No es un número entero. Intente de nuevo.")
    else:
        A.append(numero_ingresar)  
# tercer punto
for j in range(1,numero+1):
    B.append(random.randint(1,20)) #tercer punto
#puntos 4,5,6,7.
def suma_pares(x):
    suma_pares = 0
    for i in x:
        if i % 2 == 0:
            suma_pares += i
    return suma_pares
def promedio(x):
    return sum(x) / len(x)
def suma_lista(x,y):
    suma=[]
    for h in range(0,numero):
        suma.append(x[h] + y[h])
    return suma
def producto_lista(x,y):
    producto=[]
    for h in range(0,numero):
        producto.append(x[h] * y[h])
    return producto
#punto 8
C=[]
def crear_lista_C(x,y):
    for h in range(0,numero):
        C.append(x[h])
        C.append(y[h])
    return C
#punto 9
def mayor(x):
    mayor = x[0]
    for i in x:
        if i > mayor:
            mayor = i
    return mayor, x.index(mayor)
print("la lista A es: ", A)
print("la lista B es: ", B) 
print("la suma de las dos listas es: ", suma_lista(A,B))
print("el producto de las dos listas es: ", producto_lista(A,B))
print("la suma de los enteros pares de la lista A es: ", suma_pares(A))
print("el promedio de los elementos de la lista B es: ", promedio(B))
print("el mayor elemento de la lista C es junto con su posicion: ", mayor(C))
