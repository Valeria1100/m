INTRODUCCIÓN
Este proyecto tiene como propósito calcular el daño final de una bala en función del material con el que choca. Dependiendo del tipo de material (Madera, Metal o Concreto), el daño sufrido por la bala será diferente y tendra una reduccion de porcentajes diferentes. El programa está disponible en dos versiones: una en Python y otra en C++.
INSTALACIÓN
Instalación de Python
1. Asegúrate de tener Python instalado en tu sistema. Puedes descargarlo desde la página oficial de este mismo, o usar visual studio code, el que te permitirá usar diferentes lenguajes, pero para este caso desde el mismo, visual studio descargas Python y sus extensiones.
2. Una vez instalado, abre una terminal con la tecla F1(en el caso de visual studio code) y verifica que Python esté correctamente instalado con el siguiente comando:
Python --version, que más allá de mostrarte que se encuentra instalado te dira en que versión se encuentra
Instalación de C++
1.	Si deseas ejecutar el código en C++, puedes usar también visual studio code, descargando compilador de c++ en la misma aplicación y después de esto descargas MinGW, a lo que siguiendo las instrucciones te quedara listo para poder usarlo.
1.	Verifica que tienes un compilador de C++ en tu sistema usando el siguiente comando en la terminal 
g++ o g++ --version 
GUIA DE USO
Usar el programa en Python
1.	Guarda el archivo en la ruta que desees preferiblemente crea una carpeta.
2.	Abre una terminal, en el caso de visual studio code con la tecla F1, que te llevara a la ruta donde guardaste el código y en la consola se ejecutara todo.
3.	Para el problema de la bala de COD el programa pedirá que ingreses el daño de la bala y el tipo de material (1 para Madera, 2 para Metal, 3 para Concreto). Luego, mostrará el daño final calculado según el material elegido.
Usar el programa en C++
1.	Guarda el archivo en la ruta que desees preferiblemente crea una carpeta.
2.	Abre una terminal, en el caso de visual studio code con la tecla F1, que te llevara a la ruta donde guardaste el código y en la consola se ejecutara todo.
3.	Al igual que en el programa Python, el programa pedirá que ingreses el daño base y el tipo de material, y luego mostrará el daño final.

4. Documentación Técnica
Estructura del Proyecto
Este proyecto está compuesto por dos archivos principales:
•	.py: Contiene el código en Python que calcula el daño final de la bala en función del material.
•	.cpp: Contiene el código en C++ con la misma funcionalidad que el código Python.
Descripción del Código
Python:
1.	Se solicita al usuario ingresar el daño base y el tipo de material.
2.	El programa calcula el daño final dependiendo del material (con diferentes porcentajes de reducción).
3.	Si el tipo de material es inválido, se muestra un mensaje de error.
4.	Si es válido se ejecuta el material seleccionado y se muestra el resultado final
C++:
1.	Similar al código en Python, se solicita al usuario el daño base y el tipo de material.
2.	Se utiliza un switch para aplicar los diferentes porcentajes de daño según el material.
3.	Si se ingresa un material no válido, se muestra un mensaje de error.
4.	Si es válido se ejecuta el material seleccionado y se muestra el resultado final

5. Ejemplos de Código
Ejemplo en Python:
PYTHON
```
# Entrada
dano_base = float(input("Ingresa el daño de la bala: "))
tipo_material = int(input("Ingresa el tipo de material (1 = Madera, 2 = Metal, 3 = Concreto): "))

# Cálculo del daño final
dano_final = -1  # En caso de error
if tipo_material == 1:  # Madera
    dano_final = dano_base * 0.70  # Reduce un 30%
elif tipo_material == 2:  # Metal
    dano_final = dano_base * 0.50  # Reduce un 50%
elif tipo_material == 3:  # Concreto
    dano_final = dano_base * 0.30  # Reduce un 70%
else: 
    print("Tipo de material no válido")
```
# Solo si el material es válido
if dano_final != -1:
    print("Daño Final es", round(dano_final, 2))
Ejemplo en C++:
CPP
```
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    /* Entrada */
    double DanoB;
    int material;

    /* Salida */
    double DanoF;
    cout << fixed << setprecision(2);
    cout << "Digite el daño base del material: ";
    cin >> DanoB;
    cout << "Digite el material: ";
    cin >> material;

    switch(material) { 
        case 1: /* Madera */
            DanoF = (DanoB * 0.70); /* Reduce el 30% */
            break;
        case 2: /* Metal */
            DanoF = (DanoB * 0.50); /* Reduce el 50% */
            break;
        case 3: /* Concreto */
            DanoF = (DanoB * 0.30); /* Reduce el 70% */
            break;
        default:
            DanoF = -1; /* En caso de error */
    }

    if (DanoF == -1) {
        cout << "Los datos ingresados no son válidos" << endl;
    } else { /* Solo si el material es válido */
        cout << "El Daño final es " << DanoF << endl;
    }

    return 0;
}
```
6. Errores Comunes
•	Entrada incorrecta de material: Asegúrate de ingresar un número entre 1 y 3 para el material.
•	Error en los cálculos: Si el resultado del daño final no es correcto, revisa que los valores ingresados sean válidos y que el programa esté recibiendo los datos en el formato adecuado.
7. Contribuciones
Si deseas contribuir al proyecto, se puede permitir que contribuyan haciendo que el desarrollo del código sea más eficaz, también se pueden incluir más materiales, o también organizando mejor el código.
8. Licencia
Licenciado bajo Python Softwate Foundation License (PSFL).
C++ no tiene una licencia pero las bibliotecas que usa si la tienen como, la Licencia Pública General GNU o la Licencia MIT.

