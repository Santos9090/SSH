# SSH

Ejercicio 1
```bash
#!/bin/bash

echo "Ingrese un número entero: "
read num

if [ $num -gt 0 ]; then
  echo "El número ${num} es positivo"
else
  echo "El número ${num} no es positivo"
fi

```
Ejercicio 2
```bash
#!/bin/bash

echo "Ingrese un número entero: "
read num

if [ $num -lt 0 ]; then
  echo "El número ${num} es negativo"
else
  echo "El número ${num} es positivo"
fi

```
Ejercicio 3
```bash
#!/bin/bash

echo "Ingrese un número entero: "
read num

if [ $num -eq 0 ]
then
  echo "El número  ${num} es igual a cero"
else
  echo "El número  ${num} no es igual a cero"
fi

```
Ejercicio 4
```bash
#!/bin/bash

echo "Ingrese un numero entero: "
read num

if [ $num -gt 0 ]; then
  echo "El numero ${num} es positivo"
elif [ $num -lt 0 ]; then
  echo "El numero ${num} es negativo"
else
  echo "El numero ${num} es cero"
fi

```
Ejercicio 5
```bash
#!/bin/bash

if [ $# -eq 3 ]
then
  echo "El número de parámetros introducido es correcto"
else
  echo "Error: el número de parámetros introducido es incorrecto"
fi

```
Ejercicio 6
```bash
#!/bin/bash

if [ $# -ne 2 ]; then
  echo "Error: Se requieren dos parámetros para realizar la suma"
else
  echo "La suma de los dos números es: $(($1 + $2))"
fi

```
Ejercicio 7
```bash
#!/bin/bash

if [ $# -ne 3 ]; then
  echo "Error: Se requieren 3 parámetros"
  exit 1
fi

if [[ ! $1 =~ ^[0-9]+$ ]] || [[ ! $2 =~ ^[0-9]+$ ]]; then
  echo "Error: Los dos primeros parámetros deben ser números"
  exit 1
fi

if [ $3 == "+" ]; then
  echo $(($1 + $2))
elif [ $3 == "-" ]; then
  echo $(($1 - $2))
elif [ $3 == "x" ]; then
  echo $(($1 * $2))
elif [ $3 == "/" ]; then
  echo $(($1 / $2))
else
  echo "Error: El tercer parámetro debe ser uno de los siguientes símbolos: + - x /"
  exit 1
fi

```
Ejercicio 8
```bash
#!/bin/bash

# Comprobamos si el fichero existe
if [ -f $1 ]; then
  echo "El fichero existe"
else
  echo "El fichero no existe"
fi

```
Ejercicio 9
```bash
#!/bin/bash

if [ -d "$1" ]; then
  echo "$1 es un directorio"
elif [ -f "$1" ]; then
  echo "$1 es un fichero"
else
  echo "$1 no es un directorio ni un fichero"
fi

```
Ejercicio 10
```bash

#!/bin/bash

echo "Introduce la ruta del fichero: "
read ruta

if [ -f $ruta ]; then
    permisos=$(stat -c "%a" $ruta)
    echo "Permisos del fichero: $permisos"
    echo "Lectura: $(($permisos/100%10))"
    echo "Escritura: $(($permisos/10%10))"
    echo "Ejecución: $(($permisos%10))"
else
    echo "El fichero no existe"
fi

```
Ejercicio 11
```bash
#!/bin/bash
for(i=0;i<50;I++){
echo "HOLA";
}

```
Ejercicio 12
```bash
#!/bin/bash

for(i=0;i<10;i++){
    echo "Ingrese una palabra:"
    read palabra
    echo "La palabra ingresada es: $palabra"
}

```
Ejercicio 13
```bash
#!/bin/bash

numero=$#

for(i=0;i<numero;i++){
  echo "hola"
}

```
Ejercicio 14
```bash
#!/bin/bash

if [ $# -eq 0 ]
then
  echo "No se ha pasado ningún parámetro"
else
  for i in $(seq 0 $1)
  do
    echo $i
  done
fi

```
Ejercicio 15
```bash
#!/bin/bash

n=$1

suma=0

for i in $(seq 1 $n); do
  suma=$((suma + i))
done

echo "La suma de los números entre 1 y $n es $suma"

```
