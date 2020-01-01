# Computer Science Unplugged

## TODO
- Revisar los libros que recomiendan en Bits&Books

## Números Binarios

TODO
Hay una actividad en Scratch que trata el tema de los números Binarios
https://code.google.com/archive/p/scratch-unplugged/downloads

Se le da un set de 5 tarjetas a cada alumno/a del aula: 1, 2, 4, 8, 16
Cada carta representa 2^0, 2x1, 2x2, 2x2x2, 2x2x2x2

Se comprueban los siguientes números usando las cartas:
00001 = 1
00010 = 2
00011 = 3
00100 = 4

Se compara con el sistema decimal en la pizarra:
01, 10, 11, 100. Donde cada "carta representa" 10 elevado

Se les pide que traduzcan los siguientes números en binario:
01001 (sol = 9)
10100 (sol= 20)
11100 (sol= 28)
00011 (sol= 3)
00101 (sol= 5)
01110 (sol= 14)
11001 (sol= 25)

Una vez corregido este ejercicio vamos a usar el código binario para ver las representaciones de los siguientes símbolos. Esto es importante porque ayuda a hablar de la representatividad del código binario. No se entrega ficha, se resuelve directamente en la pizarra con el proyector.

![binario](/csunplugged/binario1.png)

El siguiente ejercicio consiste en hacer el ejercicio inverso.
Se trata de decir los números binarios de los siguientes números decimales.

4 (sol = 00000)
7 (sol = 00111)
13 (sol = 01101)
18 (sol = 10010)
27 (sol = 11101)

00001 (sol = 1  = a)
11100 (sol = 28 = y)
11000 (sol = 24 = u)
00101 (sol = 5  = d)
00001 (sol = 1  = a)
00000 (sol = 0  = _ )
00001 (sol = 1  = a)
10111 (sol = 23 = t)
10101 (sol = 21 = r)
00001 (sol = 1  = a)
10011 (sol = 19 = p)
00001 (sol = 1  = a)
00101 (sol = 5  = d)
10010 (sol = 18 = o)

La última actividad consiste en construir un modem que envíe mensajes en binario.

``` python
# mensaje sin sentido

#################################
#Coded by La Verbena Electrónica#
#         Sonotrónica           #
#################################


# necesitamos un sonido de onda cuadrada y muy corto
use_synth :dpulse
use_synth_defaults release: 0.1

# definición de los valores del beep para 0 y 1
# Buscar en internet las frecuencias reales
zero = hz_to_midi(600)
one = hz_to_midi(1000)

# velocidad de transmisión
bps = 0.08

# mensaje aleatorio, cuatro palabras, cada una con 56 bits (7 bytes)
#4.times do
#  56.times do
#    play [zero, one].choose
#    sleep bps
#  end
#  sleep rrand_i(0.5,1.5)
#end

# Alfabeto traducido a binario
_ = [zero, zero, zero, zero, one]
a = [zero, zero, zero, zero, one]
b = [zero, zero, zero, one, zero]
c = [zero, zero, zero, one, one]
d = [zero, zero, one, zero, zero]
e = [zero, zero, one, zero, one]
f = [zero, zero, one, one, zero]
g = [zero, zero, one, one, one]
h = [zero, one, zero, zero, zero]
i = [zero, one, zero, zero, one]
j = [zero, one, zero, one, zero]
k = [zero, one, zero, one, one]
l = [zero, one, one, zero, zero]
m = [zero, one, one, zero, one]
n = [zero, one, one, one, zero]
ñ = [zero, one, one, one, one]
o = [one, zero, zero, zero, zero]
p = [one, zero, zero, zero, one]
q = [one, zero, zero, one, zero]
r = [one, zero, zero, one, one]
s = [one, zero, one, zero, zero]
t = [one, zero, one, zero, one]
u = [one, zero, one, one, zero]
v = [one, zero, one, one, one]
w = [one, one, zero, zero, zero]
x = [one, one, zero, zero, one]
y = [one, one, zero, one, zero]
z = [one, one, zero, one, one]


# mensaje con sentido
mail = [h,o,l,a,_,c,o,m,o,_,e,s,t,a,s,_]
long = 16

long.times do |letra|
  5.times do |digito|
    play mail[letra][digito]
    sleep 0.08
  end
end
```

Otro día vemos como se puede volver a traducir este audio en bits
