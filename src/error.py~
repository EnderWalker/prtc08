#! /usr/bin/python
#!encoding: UTF-8

#Importamos el módulo mod_pi.
import mod_pi

#Definimos una función destinada a la detección de errores.

def error (n, t, umbral):
    sol = 0.0
    warn = 0.0
# ref = mod_pi.f(n)
    ref = mod_pi.f(n)
    for j in range (t):
        pi = mod_pi.f(n)
        if (abs(pi - ref) > umbral):
            warn += 1
    return (warn/t) * 100

#Cuerpo de comprobaciones del módulo.

if (__name__ == "__main__"):
    #Importamos la librería sys para permitir el uso de sys.argv.
    import sys
    if (len(sys.argv) != 4):
        n = int(raw_input("Introduzca el número de intervalos utilizados para aproximar pi: "))
        t = int(raw_input("Introduzca el número de ejecuciones del programa: "))
        umbral = float(raw_input("Tolerancia: "))
    else:
        n = int(sys.argv[1])
        t = int(sys.argv[2])
        umbral = float(sys.argv[3])
    answer = error(n, t, umbral)
    print "\nEl porcentaje de errores detectados ha sido del %.4f %%.\n" %answer
    