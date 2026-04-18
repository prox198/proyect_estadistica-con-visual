# proyect_estadistica-con-visual
explicaion en el readme

¿Es conveniente graficar?
Sí,se considero que si por que Una tabla con 276 números no permite apreciar el comportamiento del clima a simple vista.



Por que un histograma?
Tenemos demasiados datos diferentes.
Al medir la temperatura con decimales (como 23.4°C o 25.1°C), es casi imposible que los valores se repitan exactamente. Si usáramos una gráfica de pastel, tendríamos 276 rebanadas delgaditas y no entenderíamos nada. 
Si usáramos barras simples, tendríamos una fila infinita de palitos que no nos dirían nada.

el historgrama Agrupa: En lugar de ver cada dato por separado, 
los mete en "cajones/intervalos" de 1 grado (ejemplo: todos los que están entre 23°C y 24°C).
convierte los 276 datos en una montaña que es facil de leer donde la parte más alta nos dice cuál es el clima más frecuente del verano.



Proceso ; Para armar el histograma, lo que hicimos fue un proceso de agrupación por "cajones/intervalos"













1.
 Definir el Rango TotalPrimero necesitas saber qué tanto espacio vas a cubrir.
 Es la distancia entre el valor más alto y el más bajo.Fórmula: Rango = Máximo - Mínimo ,Ejemplo: 
Si tu máxima es 28°C y tu mínima es 21°C, tu rango es de 7 grados.

1.2.no usamos exactamente la regla de stugles para determinar k por que los intervalos quedaria en decimos lo cual no es tan entendible 
[21.34°-22.18°]
El programa resta el valor máximo menos el mínimo y crea tantos cajones como grados de diferencia haya. 
Por ejemplo, si el rango es de 21°C a 29°C, el programa crea automáticamente 9.

y si se sigue stungles queda 9.11  asi que igual es aprox de 9 intervalos 




1.2.Calculo de la amplitud: ya que sabemos cuanto espacio tenemos el rango y cuantas barras vamos a querer osea (K)
 rango/k
pero forzamos la amplitud a 1 o que siempre sea un entero para que los limtes queden limpios y no queden numeros con munchos decimales 
se uso los metodos . ceil al maximo y (floor) al minimo 

Define el ancho fijo: Al usar números enteros para los índices del arreglo (int indice = (int) Math.floor(v) - minInt;),asi que agrupo todos
cualquier dato como 23.1 o 23.9 se quedan en el mismo intervalo 


-----------------------------------------------




luego buscamos los límites. 
Vimos cuál era la temperatura más fría (Mínimo) y la más calurosa (Máximo).
Ejemplo, si tu mínimo fue 21.2°C y tu máximo 28.7°C, decidimos crear cajones de 1 grado de ancho para que sea fácil de leer:

Cajón 1: De 21°C a 22°C

Cajón 2: De 22°C a 23°C 
y 24 a 25 etc


2.Luego, tomamos cada uno de los 276 datos y lo lanzamos al cajón/intevalo que le corresponde.

¿Salió un 23.4°C? Va para el cajón de [23-24].

¿Salió un 23.8°C? También va para el mismo cajón.

Al final, contamos cuántos datos cayeron en cada cajón. Ese número es la Frecuencia  (EL EJE X)



3.La altura (o largo, en nuestro caso) de la barra representa cuántos datos hay en ese rango.

Si en el cajón de [24-25°C] cayeron 50 días, esa barra será muy larga.

Si en el de [21-22°C] solo cayeron 4 días, esa barra será cortita.



El histograma esta acostado solo se invirtieron los papeles el eje Y es el intervalo y el x es el numero de datos 
en ese intervalo 
