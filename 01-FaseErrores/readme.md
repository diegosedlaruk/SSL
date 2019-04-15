* punto 2: 
	-	a. comando ejecutado: gcc -E hello2.c -o hello2.i
	-	b. resultado obtenido: se creó un archivo nuevo hello2.i con el proprocesamiento de hello2.c

	Análisis del contenido: este archivo nuevo hello2.i reemplazó las definiciones dadas con los #define por el código correspondiente (en este caso #include stdio.h) 
	y reemplazó los comentarios por un espacio.

* punto 4:
	-	Según información recopilada printf es utilizada para mostrar una cadena de caracteres con cierto formato. Al formato se le pueden agregar placeholders 
		que serán sobreescribidos con argumentos posteriormente. 

* punto 5:
	-	a. comando ejecutado: gcc -E hello3.c -o hello3.i
	-	b. resultado obtenido: se creó un nuevo archivo hello3.i con el preprocesamiento de hello3.c
	
	Diferencias entre hello2.i y hello3.i: Las diferencias entre ambos es que hello3.i tiene menos código que hello2.i y el preprocesamiento fué más rápido.
	
* punto 6:
	- 	a. comando ejecutado: gcc -S hello3.i -o hello3.s
	-	b. error obtenido: expected declaration or statemente at end of input.

* punto 7:
	-	a. comando ejecutado: gcc -E hello4.c -o hello4.i      gcc -S hello4.i -o hello4.s
	-	b. resultado obtenido: se generó un archivo hello4.s
	
* punto 8:
	-	se puede visualizar el lenguaje ensamblador del código escrito. También se puede visualizar como todavía no reemplazó el código de las funciones
		incluidas con el #include, ejemplo línea 22: "call _prontf".
	
* punto 9:
	-	a. comando ejecutado: gcc -O hello4.s -o hello4.o
	-	b. error obtenido: undefined reference to 'prontf', ld returned 1 exit status.
	
* punto 10:
	-	Este punto no supe como hacerlo.
	
* punto 11:
	-	a. comandos ejecutados: gcc -E hello5.c -o hello5.i      gcc -S hello5.i -o hello5.s	gcc -O hello5.s -o hello5.o      gcc hello5.o 
	-	b. error obtenido: pude generar hasta el archivo hello5.o, pero al querer generar el ejecutable desde este archivo objeto rompe. El error 
			obtenido es el siguiente: Could not find abbrev number 84. también indica 'undefined reference to _Jv_RegisterClasses'

* punto 12:
	Este paso no pude realizarlo debido a que no pude generar el ejecutable en el paso 11.
	
* punto 13:
	Este paso no pude hacerlo ya que arrastro el error del paso 11.
	
* punto 14:
	-	a. comando ejecutado: gcc hello7.c -o hello7.exe
	-	b. resultado obtenido: se generó el ejecutable hello7.exe aunque también me generó unas advertencias en la consola que indican que hay una declaración
		   implícita de la función printf. Indica que se debe incluir stdio.h o proveer de una declaración de printf.

* punto 15:
		Funciona debido a que por defecto, el comando que genera un ejecutable directamente desde un .c busca en las librerías estandar las definiciones
		de las funciones declaradas. 
