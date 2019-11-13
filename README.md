package carlos;

import java.util.Scanner;

public class Carlos {

    public static void main(String[] args) {
        
        Scanner entrada = new Scanner(System.in);
        int vect_1, opcion, memoria;
        
        
        
        System.out.println("Bienvenido al programa Quifran, \n este programa te permite crear un vector \n"
                + "del tamaño que quieras y ordenarlo de mayor a menor o viseversa \n\n\n");
        
        System.out.println(" ingrese el tamaño del vector: ");
        vect_1 = entrada.nextInt();
        
      
        int []vector = new int[ vect_1 ];
        
        //SE LLENA EL VECTOR SEGUN USUARIO        
        for (int i = 0; i < vector.length; i++) {            
            System.out.print("Ingrese posicion #" + i + " " );
            vector[ i ] = entrada.nextInt();       
       }
        
        
        //SE PIDE SI SE QUIERE ASC/DESC
        System.out.println("Ingrese 1: para ordenar vector de forma Ascendente,  "
                + "2 para ordenar vector de forma descendente");
        
        opcion = entrada.nextInt();
        
        //OPCION ASCENDENETE
        if( opcion == 1 ){   
            
           for (int i = 0; i < vector.length; i++) {
              for (int j = 0; j < vector.length; j++) {
                        if ( vector[ i ] < vector[ j ] ){
                            memoria = vector[i];
                            vector[i] = vector[j];
                            vector[ j ] = memoria;
                        }
                 }
            }      
          }
        
        else
            //OPCION DESCENDENTE
            if( opcion == 2 ){
                for (int i = 0; i < vect_1; i++) {
                     for (int j = 0; j < vect_1; j++) {
                        if ( vector[ i ] > vector[ j ] ){
                            memoria = vector[i];
                            vector[i] = vector[j];
                            vector[ j ] = memoria;
                        }
                 }
            }
            }
            else{
                System.err.println("Dato invalido, reinicie a Quifran y y lea bien las opciones");
            }
        
        //Boorar elementos repetidos
        
      //  for (int i = 0; i < vector.length ; i++) {
            for (int j = 0; j < vector.length -1; j++) {
                    if (vector[j] == vector[j+1]) {
                        vector[j] = -1;
                    }
                              
          //  } 
        }
        
        
        //SE VISUALIZA ELEMENTOS ASC/DESC PERO BORRRANDO LOS REPETIDOS
        
        System.out.println("\n\nVECTOR ORDENADO SEGUN USUARIO \n");
        for (int i = 0; i < vect_1; i++) {
           // System.out.println("posicion #" + i + "  " + vector[ i ] );
           if(vector[ i ] != -1 ){
                System.out.println( vector[ i ] );
           } 
          

        }
         
       
    }
    
}
