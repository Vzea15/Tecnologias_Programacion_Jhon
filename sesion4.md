<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4

# 1
# def calculadora(n1,n2,op):
#     resultado = 0
#     if op == '+':
#         resultado = n1 + n2
#     elif op == '-':
#         resultado = n1 - n2
#     elif op == '*':
#         resultado = n1 * n2
#     elif op == '/':
#         resultado = n1 / n2
#     return resultado
# 
# num1 = int(input("Ingrese el primer numero: "))
# num2 = int(input("Ingrese el segundo numero: "))
# op = input("Ingrese el operador: ")
# x = calculadora(num1,num2,op)
# print(x)


# 2
# def contar_vocales(palabras):
#     contador = 0
#     palabras = palabras.lower()
#     for vocales in palabras:
#         if vocales in 'aeiou':
#             contador += 1
#     return contador
# 
# palabras = input("Ingrese una o más palabras: ")
# resultado = contar_vocales(palabras)
# print("Número de vocales:", resultado)

# 3
# def es_primo(num):
#     if num <= 1:
#         return False
#     elif num <= 3:
#         return True
#     elif num % 2 == 0:
#         return False
#     else:
#         for i in range(3, int(num**0.5) + 1, 2):
#             if num % i == 0:
#                 return False
#         return True
# 
# numero = int(input("Ingrese un numero: "))
# resultado = es_primo(numero)
# if resultado:
#     print(f"{numero} es primo.")
# else:
#     print(f"{numero} no es primo.")


# 4
# def contar_palabras(cadena):
#     palabras = cadena.split()
#     return len(palabras)
# 
# cadena = input("Ingrese una o más palabras: ")
# resultado = contar_palabras(cadena)
# print("Número de palabras:", resultado)

# 5
# def potencia(base, exponente):
#     resultado = base ** exponente
#     return resultado
# 
# numBase = 2
# numExponente = 3
# resultado = potencia(numBase, numExponente)
# print(f"{numBase} elevado a la {numExponente} es igual a {resultado}")
# 
# def potencia(base, exponente):
#     resultado = base ** exponente
#     return resultado
# 
# numBase = 2
# numExponente = 3
# resultado = potencia(numBase, numExponente)
# print(f"{numBase} elevado a la {numExponente} es igual a {resultado}")



<!-- Su documentación aquí -->






