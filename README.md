#  Sistema de compra de ingresso cinema e teatro ( TESTE 1 )
package cine;

public class BilheteriaCine {
    String fileira;
    int cadeira;
    double ingresso;
    double lanche;
    double combo1;
    double combo2;
    String resev;
    int cad;
    TitleFilm titlefilm;
    TitlePeça titlepeça;
    
    void calcCombo(){
       combo1 = (ingresso + lanche);
    }
       void calcCombo2();
       combo2 = (ingresso + lanche)*(2)-(10.0);
    }
}
package cine;
public class BilheteriaTeatro extends BilheteriaCine{
}
package cine;
public class TitleFilm {
    String nome;
}
package cine;
public class TitlePeça extends TitleFilm {
}



package cine;

import java.util.Scanner;

public class Teste {
    public static void main(String[] args) {
        Scanner into = new Scanner( System.in);
    
        BilheteriaCine b1 = new BilheteriaCine();
        BilheteriaTeatro t1 = new BilheteriaTeatro(); // t01 intancia da classe teatro
        
        TitleFilm t01 = new TitleFilm(); // t1 intancia da classe Title
        TitleFilm t02 = new TitleFilm();
        TitlePeça p1 = new TitlePeça();
        TitlePeça p2 = new TitlePeça();
        
//  ESCOLHA ENTRE FILME OU PEÇA.
    
        System.out.println("\n Para Filme Digite - 1 \n para Peça Teatral Digite - 2 ");
        int i=into.nextInt();
        if(i == 1){ //////////////////// 1 para escolher filme 
//intancia FILME     
            b1.ingresso = 28.0;
            b1.lanche = 20.0;
            b1.calcCombo();
            b1.calcCombo2();
            
//intancia TITULO FILME
             
            t01.nome  = "Era do Gelo";
            t02.nome = "Titanic";
            
           
            System.out.println("Escolha o Filme \n 1 - Era do gelo \n 2 - Titanic");
            int f = into.nextInt();
                if (f == 1){
                    b1.titlefilm = t01;
                }
                else {
                    b1.titlefilm = t02;
                }
// SAIDA DE DADOS FILME

            System.out.println(" imgresso: " +b1.ingresso);
            System.out.println(" lanche: " +b1.lanche);
            System.out.println(" Filme : " +b1.titlefilm.nome);
            System.out.println("\n Para 1 Pessoas digite - 1 \n para 2 pessoas com desc de R$ 10,00 digite - 2"); 
            
            int d = into.nextInt(); 
            if (d == 1){
            System.out.println(" VALOR COMBO PARA 1  " +b1.combo1);  // ingresso + lanche
            }else{
                System.out.println(" VALOR COMBO PARA 2  " +b1.combo2);  //2 ingressos + 2 lanche 
            System.out.println("Escolha a Fileira de A - J ");
            b1.fileira = into.next();
            System.out.println("Escolha a Cadeira de 1 - 50");
            b1.cadeira = into.nextInt();
            System.out.println("ASSENTO RESERVADO: " +b1.fileira +b1.cadeira);
            }
            System.out.println("Escolha a Fileira de A - J ");
            b1.fileira = into.next();
            System.out.println("Escolha a Cadeira de 1 - 50");
            b1.cadeira = into.nextInt();
            System.out.println("ASSENTO RESERVADO: " +b1.fileira +b1.cadeira);
        }       
        
            else if (i == 2){ ///////////////////////// 2 para escolher Teatro;
//intancia TEATRO
            t1.ingresso = 30.0;
            t1.lanche = 20.0;
            t1.calcCombo();
            t1.calcCombo2();
           
            
//intancia NOME PEÇA
            
            p1.nome = " vida a Dois";
            p2.nome = " Casa Assombrada";

            System.out.println(" Escolha o Peça \n 1 - Vida a dois \n 2 - Casa Assombrada");
            int t = into.nextInt();
                if (t == 1)
                    t1.titlepeça = p1;
                else 
                    t1.titlepeça = p2;
            System.out.println(" Peça :  " +t1.titlepeça.nome );
            System.out.println(" Ingresso: " +t1.ingresso);
            System.out.println(" Lanche: " +t1.lanche);

// SAIDA DE DADOS TEATRO
            System.out.println("\n Para 1 Pessoas digite 1 \n para 2 pessoas com desc de R$ 10,00 digite 2"); 
            int c = into.nextByte();
                if( c == 1)
                System.out.println(" VALOR COMBO PARA 1  " +t1.combo1); // ingresso + lanche
                else{
                    System.out.println(" VALOR COMBO PARA 2  " +t1.combo2); //2 ingressos + 2 lanche
                    System.out.println("Escolha a Fileira de A - J ");  
                    t1.fileira = into.next();
                    System.out.println("Escolha a Cadeira de 1 - 50");
                    t1.cadeira = into.nextInt();
                    System.out.println("ASSENTO RESERVADO: " +t1.fileira +t1.cadeira);
                } 
            System.out.println("Escolha a Fileira de A - J ");  
            t1.fileira = into.next();
            System.out.println("Escolha a Cadeira de 1 - 50");
            t1.cadeira = into.nextInt();
            System.out.println("ASSENTO RESERVADO: " +t1.fileira +t1.cadeira);
        }
    }
}
