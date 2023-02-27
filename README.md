# Repo 4
## Prime Numbers
For finding prime numbers until an nth number, I defined  4 variables:
1. The input n, which is a  whole number.
2. A list divisores_x where I store a temporary value.
3. A whole number x for storing a variable of a loop.
4. A second whole number divisor for another loop.

The algorithm starts a first loop that goes from 1=x to n, and then makes another loop from divisor = 2 to the integer equal or right below the square root of x. It checks if the module of x/divisor equals 0, if this is the case it appends it to the list. After checking the other modules, it exits the loop and checks if the list is empty. An empty list means that the number is prime because there were no divisors diferent from 1 and the number itself.
If the condition is met, the number is printed and the loop starts again.

##### Below is the pseudocode for finding prime numbers.
    
    [variables]
    n : entero
    divisores_x : lista[]
    
    inicio
    	Para (x=1 hasta n) hacer
    		Para (divisor=2 hasta entero(sqrt(x))) hacer
    			Si modulo(x,divisor) == 0 entonces
    				agregar divisor a divisores_x
    		Fin para
    		Si longitud de divisores_x == 0
    			escribir("x") 
    	Fin para
    Fin
And this is its flowchart.	
<img width="303" alt="Screenshot_20230226_192316" src="https://user-images.githubusercontent.com/124604730/221446772-111511c4-8bfd-410e-b7c6-48b6d28e3f7c.png">



## Square Root
The process for finding the sqaure root with three decimals of an integer is far more extensive than the one for finding prime numbers. Therefore, I'm not going to explain it so deeply. 
The Square Root algorithm basically subtracts, devides and adds new pairs of numbers for repeating the process over and over until the remainder equals 0, or the decimal places equal 3. So, what makes the process of finding the sqaure root quite extensive, is the number of decisions the algorithm must make in a loop. Moreover, it must take into account, what it previously has done.
For example: If in the last loop I have added a pair of 00 to the remainder, and when I substract the next posible answer to the remainder it still equals a negative number, then I can´t add again another pair of 00, I must write 0 as the answer. 

An observation to this pseudocode, it reuses a considerable block of code, in this case a function could be called. 

##### Below is the pseudocode for finding the sqaure root of an integer.
    
    [variables]
    n = entero_1
    x = entero_2
    c = 0 (contador)
    p = cifra de 1 o mas dígitos
    cifras_res = enetro_3
    parejas = lista[p1, p2...]
    res = resultado entero/decimal
    
    Para (x=1 hasta n con paso -2) hacer	
    	agregar a parejas
    Fin para
    
    p = parejas(1)
    Para (x=1 hasta x<=p/2) hacer			
    	agregar x*x a cifras_res
    Fin para
    
    res = maximo valor en cifras_res
    
    Si (p-res == 0 y longitud de parejas == 0) hacer
    	escribir resultado
    
    Para (x=2 hasta longitud(parejas)) hacer
    	Si ((p-(res*2 + 1)) == a número negativo) hacer
    		Si (en el loop anterior se añadió 00 o se añdió pareja) hacer
    			Para (x=0 hasta 9) hacer
    				Si ((res*2 con unidad x) * x)  <= a p hacer
    					p = p - (res*2 con unidad x) * x
    					añadir x a res 
    					Si (c == 3 o p == 0) hacer
    						escribir resultado con coma en el tercer lugar de der a izq.
    					Sino x = x + 1
    			Fin para
    Fin para
    		 
    		Sino 
    			añadir 00 a la der de p 
    			c = c + 1
    			x = x + 1
    			
    				
    	Sino
    		Si (en el loop anterior se añadió 00 o se añdió pareja) hacer
    			Para (x=0 hasta 9) hacer
    				Si ((res*2 con unidad x) * x)  <= a p hacer
    					p = p - (res*2 con unidad x) * x
    					añadir x a res 
    					Si (c == 3 o p == 0) hacer
    						escribir resultado con coma en el tercer lugar de der a izq.
    					Sino x = x + 1
    	
    			Fin para
    Fin	     
	
  This is the flowchart
  

<img width="343" alt="Screenshot_20230226_192937" src="https://user-images.githubusercontent.com/124604730/221447136-0507ff96-e3d2-47ab-9b9b-782b1154c842.png">
<img width="339" alt="Screenshot_20230226_193605" src="https://user-images.githubusercontent.com/124604730/221447555-cb937bb3-6ae2-4cbc-85fd-dd605098502c.png">

<img width="296" alt="Screenshot_20230226_193403" src="https://user-images.githubusercontent.com/124604730/221447380-1a0e80db-fe74-44d8-ad74-8c4e51256d7c.png">


P.D. I'am sorry not to upload the pseudocode nor flowcharts in english, I realised late it was a good idea to write this repo in english. 
