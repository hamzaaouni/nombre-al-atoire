# nombre-al-atoire
// jeu de nombre aléatoire  

import java.util.Scanner;

import java.util.Random;

public class Jeu {

public static void main(String[] args) {

      Scanner sc = new Scanner(System.in);

      Random rm = new Random();

int nAleatoire, nEntree,comp=0,tent;

nAleatoire = rm.nextInt(100)+1;//from 1 to 100

      System.out.println("Combien des tentatives tu veux (saisir un nombre) ");

tent = sc.nextInt();

      System.out.println("On va commencer avec le nombre? (entre 0 et 100) "); 

do{

nEntree = sc.nextInt();

comp++;

if(nEntree == nAleatoire) {

      System.out.println("Bravo nombre trouvé en "+comp+" tentatives");

      break;   

}

if(nEntree > nAleatoire )

    System.out.println("le nombre est plus petit");

else

    System.out.println("le nombre est plus grand ");

if(comp>tent-1)

{   System.out.println("vous avez perdu");      		

    break;}

}while(nEntree != nAleatoire);

}  

}
