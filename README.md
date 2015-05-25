# Pract1
operaciones
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

	namespace operaciones
{
    class Program
    {

        static int Suma(int a, int b) 
        {
            int suma = a + b;
            return suma;
        }
        static int Resta(int a, int b)
        {
            int resta = a - b;
            return resta;
        }
        static int Multi(int a, int b)
        {
            int multi = a * b;
            return multi;
        }
        static int Divi(int a, int b)
        {
            int divi = a / b;
            return divi;
        }
        static int Are_cua(int lad)
        {
            int are_cua = lad * lad;
            return are_cua;
        }


        static void Main(string[] args)
        {

            int a, b, opc1;
        	Console.Write("1.-Calcular operaciones: ");
        	Console.Write("\n2.-Calcular Area: ");
        	Console.Write("\nElije una Opcion: ");
        	opc1 =int.Parse(Console.ReadLine());
        
        	if(opc1 == 1)
        	{
            	Console.Write("\nINGRESE PRIMER VALOR: ");
            	a = int.Parse(Console.ReadLine());
            	Console.Write("\nINGRESE SEGUNDO VALOR: ");
            	b = int.Parse(Console.ReadLine());
            	Console.Write("\n1.-Suma");
	        	Console.Write("\n2.-Resta");
	        	Console.Write("\n3.-Multiplicacion");
	        	Console.Write("\n4.-Division");
	        	Console.Write("\nElije una Opcion:");
	        
	        	switch (Console.Read())
		    	{ 
                  case '1': Console.Write("Suma = " + Suma(a,b));
                              break; 
		          case '2': Console.Write("Resta = " + Resta(a,b)); 
                              break; 
		    	  case '3': Console.Write("Multiplicación = " + Multi(a,b));
                              break; 
		    	  case '4': Console.Write("División = " + Divi(a,b));
                              break; 
            	} Console.ReadKey();
       		 }
	    	 else if(opc1 == 2)
	    	 {   
	    		int bas ,alt,lad,opc2;
	    		double rad;
	    	
            	Console.Write("\n1.-Area del Triangulo");
	    		Console.Write("\n2.-Area del Cicurlo");
	    		Console.Write("\n3.-Area del Cuadrado");
	    		Console.Write("\nElije una Opcion: ");
	    		opc2 = int.Parse(Console.ReadLine());
	    	
           		switch (opc2)
		    	{   
	    	
	        	  case 1: Console.Write("\nIngresa Valor de la base: " );
	        	      		bas = int.Parse(Console.ReadLine());
	        		  		Console.Write("\nIngresa Valor de la Altura: " ); 
	        		  		alt = int.Parse(Console.ReadLine());
	        		  		
	        		  		double result = (bas * alt) / 2;
	        		  		Console.Write("\nArea del Triangulo = " + result);
                      		break; 
                      		
		    	  case 2: Console.Write("\nIngresa Valor del Radio: " );
		    	            
		    	  rad = Int32.Parse(Console.ReadLine());
	        	      		double resul = rad * rad *  3.14;
	        		  		Console.Write("\nArea del Circulo = " + resul);
                      		break; 
                      		
		    	  case 3: Console.Write("Ingresa Valor de un lado" );
	        	      		lad = int.Parse(Console.ReadLine());
	        		  		Console.Write("Area del Cuadrado = " + Are_cua(lad));
                      		break;
                      		
            	  default:  Console.Write("Opcion invalida ");
            		  		break;
            		  		
           		} Console.ReadKey();
		    } 
        }
    }
}
