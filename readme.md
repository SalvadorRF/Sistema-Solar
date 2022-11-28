# Sistema Solar
Se creó un pequeño sistema solar, el cual consiste en 3 cuerpos celestres, sol, tierra y luna, para generar una rotación sobre sí mismo y sobre su astro padre.

## Texturas
Las texturas fueron obtenidas de 
https://www.solarsystemscope.com/textures/

## Scripts
Rotate.cs

    using  System.Collections;
    using  System.Collections.Generic;
    using  UnityEngine;
    
    public  class  Rotate  :  MonoBehaviour
    {

	    public  float speed =  1.0f;

	    void  Start()
	    {
	    
	    }
	    
	    void  Update()
	    {
	    transform.Rotate(Vector3.up,  speed  *  Time.deltaTime);
	    }
    
    }

Este script servirá para transformar la rotación sobre el eje y de cada objeto aplicado.

**Variables**
speed → caracterizará la velocidad que esperamos tome la rotación. (modificable desde la GUI)

**Metodos**
Update() → se ejecutará cada vez que se modifique el tiempo.

**Funcion transform**
Usaremos el método Rotate, del objeto transform que es nativo, le pasaremos como primer parámetro Vector3.up el cual le indica al método que modificaremos de un vector de 3 posiciones, la posición correspondiente a las Y en una posición positiva (https://docs.unity.cn/ScriptReference/Vector3-up.html), como segundo parámetro indicaremos el valor de la transformación (rotación) deseada, colocando el producto de la velocidad y deltatime (la modificación del tiempo).

## Pasos

 - Agregando el Espacio (Skybox) 
 - Agregando Planeta Tierra
	 - Crea esfera
	 - Crea material 
 - Agregando la Luna 	
	 - Crea esfera 	
	 - Crea material
 - Crear script rotar 
 - Creación del Sol (https://drive.google.com/file/d/1CzAzfXrg7-VEdV6zX0VyuKZCo7D_MTa9/view)**
 - Anidar planetas 
 - Agregar script, rotar a cada planeta*

*Al anidar un planeta en su padre (ej. Luna en Tierra) el programa tomará como centro para aplicar la rotación el ancla del planeta padre, de esta forma con un solo script podremos crear el movimiento de rotación y translación (rotación sobre el eje del padre).
**Se utilizó como referencia ese manal para crear el Shader que genera el sol.


