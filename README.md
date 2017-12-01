# UrnaEletronicaAnhembi

package urnaeletronic;


public class UrnaEletronic {

   
    public static void main(String[] args) {
   Urna urna = new Urna();
    urna.getMenuDeOpções();
 
    }
    
}


package urnaeletronic;

import java.util.Scanner;


public class Candidato {
  private int AdicionarVoto;
    private int RetornarVoto;
   int votos;
   private int votoscan2;
  private  int votosResult;

    Candidato() {
  }

    public int getVotosResult() {
    Urna urna = new Urna();
        this.x = this.votos - this.votoscan2;
        System.out.println("total de votos e "+this.x);   
     return votosResult;
        
    }

    public void setVotosResult(int votosResult) {
        this.votosResult = votosResult;
    }

    public Candidato(int votos, int votoscan2, int votoscan3, int votoscan4, int x) {
       this.votoscan2 = votoscan2;
        this.x = x;
        this.votos = votos;
    }
    private int x;
Scanner e = new Scanner(System.in);


    
    public Candidato(int AdicionarVoto, int RetornarVoto) {
        this.AdicionarVoto = AdicionarVoto;
        this.RetornarVoto = RetornarVoto;
    }

    public int getAdicionarVoto() {
        
        System.out.println("adicionar quantos votos ? ");
        this.votos =e.nextInt();
        return AdicionarVoto;
    }

    public void setAdicionarVoto(int AdicionarVoto) {
        this.AdicionarVoto = AdicionarVoto;
    }

    public int getRetornarVoto() {
      
     
        System.out.println("retirar quantos votos ? ");
      this.votoscan2 = e.nextInt();   
        return RetornarVoto;
    }

    public void setRetornarVoto(int RetornarVoto) {
        this.RetornarVoto = RetornarVoto;
    }
  
}



package urnaeletronic;
import java.util.Scanner;
public class Urna {
    int MenuDeOpções;
    private int CadastroDeCandidato;
    private int IniciarEleição;
   private int ResultadoDeEleição;
   Scanner e = new Scanner (System.in);
   int candidato1 ;
int candidato2 ;
int candidato3 ;
int candidato4;
String nomeCandidato1;
String nomeCandidato2;
String nomeCandidato3;
String nomeCandidato4;
String partidoCandidato1;
String partidoCandidato2;
String partidoCandidato3;
String partidoCandidato4;
private int voto1;
 private int voto2;
 private int voto3;
private int voto4;
private int voto5;

    public Urna(int MenuDeOpções, int CadastroDeCandidato, int IniciarEleição, int ResultadoDeEleição, int candidato1, int candidato2, int candidato3, int candidato4, String nomeCandidato1, String nomeCandidato2, String nomeCandidato3, String nomeCandidato4, String partidoCandidato1, String partidoCandidato2, String partidoCandidato3, String partidoCandidato4, int numerodecandidatos) {
        this.MenuDeOpções = MenuDeOpções;
        this.CadastroDeCandidato = CadastroDeCandidato;
        this.IniciarEleição = IniciarEleição;
        this.ResultadoDeEleição = ResultadoDeEleição;
        this.candidato1 = candidato1;
        this.candidato2 = candidato2;
        this.candidato3 = candidato3;
        this.candidato4 = candidato4;
        this.nomeCandidato1 = nomeCandidato1;
        this.nomeCandidato2 = nomeCandidato2;
        this.nomeCandidato3 = nomeCandidato3;
        this.nomeCandidato4 = nomeCandidato4;
        this.partidoCandidato1 = partidoCandidato1;
        this.partidoCandidato2 = partidoCandidato2;
        this.partidoCandidato3 = partidoCandidato3;
        this.partidoCandidato4 = partidoCandidato4;
        this.numerodecandidatos = numerodecandidatos;
        this.voto1 = voto1;
        this.voto2 = voto2;
        this.voto3 = voto3;
        this.voto4 = voto4;
    }

 
private int numerodecandidatos;

 
   
    
    public Urna(int MenuDeOpções, int CadastroDeCandidato, int IniciarEleição, int ResultadoDeEleição) {
        this.MenuDeOpções = MenuDeOpções;
        this.CadastroDeCandidato = CadastroDeCandidato;
        this.IniciarEleição = IniciarEleição;
        this.ResultadoDeEleição = ResultadoDeEleição;
    }

    Urna() {
}

    public int getMenuDeOpções() {
        System.out.println("###################################-Bem vindo a Urna eletronica-#############################");
        System.out.println("Escolha uma das opções");
        System.out.println("1-CadastroCandidato");
        System.out.println("2-iniciarEleições");
        System.out.println("3-sair");
        int escolha = e.nextInt();
       
        if(escolha == 1){
            System.out.println("CadastroCandidato");
            getCadastroDeCandidato();
            
        }else{
            
        }if(escolha == 2){
            System.out.println("IniciarEleição");
            getIniciarEleição();
        }else{
            
        }if(escolha == 3){
            System.out.println("Sair");
            System.exit(0);
        }
        
        
        
        
        return MenuDeOpções;
    }

    public void setMenuDeOpções(int MenuDeOpções) {
        this.MenuDeOpções = MenuDeOpções;
    }

    public int  getCadastroDeCandidato() {
        System.out.println("Deseja cadastrar quantos candidatos ? ");
        this.numerodecandidatos = e.nextInt();
        if (this.numerodecandidatos > 4){
            System.out.println("Nao permitido");  
             getMenuDeOpções();  
        
        }else if(this.numerodecandidatos == 1) { 
            System.out.println("Nome "+" informe abaixo");
            this.nomeCandidato1 = e.next();
           
            System.out.println("partido "+ "informe abaixo ");
            this.partidoCandidato1 = e.next();
             
            System.out.println("numero do candidato"+" informe abaixo");
            this.candidato1= e.nextInt();
            
            getResultadoDeEleição();
        
        }else if(this.numerodecandidatos == 2){
            System.out.println("Nome "+" informe abaixo");
            this.nomeCandidato1 = e.next();
            System.out.println("partido "+ "informe abaixo ");
            this.partidoCandidato1 = e.next();
            System.out.println("numero do candidato"+" informe abaixo");
            this.candidato1= e.nextInt();
            
            System.out.println("Nome do segundo candidato "+" informe abaixo");
            this.nomeCandidato2 =e.next();
            System.out.println("partido do segundo candidato "+ "informe abaixo ");
            this.partidoCandidato2 = e.next();
            System.out.println("numero do segundo candidato "+" informe abaixo");
            this.candidato2= e.nextInt();
            getIniciarEleição();
           
        
            
        }else if(this.numerodecandidatos == 3){
            System.out.println("Nome "+" informe abaixo");
            this.nomeCandidato1 = e.next();
            System.out.println("partido "+ "informe abaixo ");
            this.partidoCandidato1 =e.next();
            System.out.println("numero do candidato"+" informe abaixo");
            this.candidato1= e.nextInt();
            
            System.out.println("Nome do segundo candidato "+" informe abaixo");
            this.nomeCandidato2 = e.next();
            System.out.println("partido do segundo candidato "+ "informe abaixo ");
            this.partidoCandidato2 =e.next();
            System.out.println("numero do segundo candidato "+" informe abaixo");
            this.candidato2= e.nextInt();
            
            System.out.println("Nome do terceiro candidato "+" informe abaixo");
            this.nomeCandidato3 = e.next();
            System.out.println("partido do terceiro candidato "+ "informe abaixo ");
            this.partidoCandidato3 = e.next();
            System.out.println("numero do terceiro candidato "+" informe abaixo");
            this.candidato3= e.nextInt();
            
            getIniciarEleição();
             
        }else if(this.numerodecandidatos == 4){
            System.out.println("Nome "+" informe abaixo");
            this.nomeCandidato1 = e.next();
            System.out.println("partido "+ "informe abaixo ");
            this.partidoCandidato1 =e.next();
            System.out.println("numero do candidato"+" informe abaixo");
            this.candidato1= e.nextInt();
            
            System.out.println("Nome do segundo candidato "+" informe abaixo");
            this.nomeCandidato2 = e.next();
            System.out.println("partido do segundo candidato "+ "informe abaixo ");
            this.partidoCandidato2 =e.next();
            System.out.println("numero do segundo candidato "+" informe abaixo");
            this.candidato2= e.nextInt();
            
            System.out.println("Nome do terceiro candidato "+" informe abaixo");
            this.nomeCandidato3 = e.next();
            System.out.println("partido do terceiro candidato "+ "informe abaixo ");
            this.partidoCandidato3 = e.next();
            System.out.println("numero do terceiro candidato "+" informe abaixo");
            this.candidato3= e.nextInt();
            
            System.out.println("Nome do quarto candidato "+" informe abaixo");
            this.nomeCandidato4 = e.next();
            System.out.println("partido do quarto candidato "+ "informe abaixo ");
            this.partidoCandidato4 = e.next();
            System.out.println("numero do quarto candidato "+" informe abaixo");
            this.candidato4= e.nextInt();
            getIniciarEleição();
        }
        return 0;
       
       
   
    }
       
    public void setCadastroDeCandidato(int CadastroDeCandidato) {
     
           this.CadastroDeCandidato = CadastroDeCandidato;
    }

    public int getIniciarEleição() {
       Candidato candidato = new Candidato();
     if(this.numerodecandidatos == 2){
         System.out.println("candidatato "+ this.nomeCandidato1);
         System.out.println("Adicionar voto "+"\n");
       
        candidato.getAdicionarVoto();
       this.voto1 = candidato.votos;
         System.out.println("candidato "+ this.nomeCandidato2);
         System.out.println("adicionar voto"+"\n");
         candidato.getAdicionarVoto();
         this.voto2 = candidato.votos;
  getResultadoDeEleição();
     }if(this.numerodecandidatos == 3 ){
         System.out.println("candidatato "+ this.nomeCandidato1);
         System.out.println("Adicionar voto "+"\n");
       
        candidato.getAdicionarVoto();
       this.voto1 = candidato.votos;
        System.out.println("candidatato "+ this.nomeCandidato2);
         System.out.println("Adicionar voto "+"\n");
       
        candidato.getAdicionarVoto();
       this.voto2 = candidato.votos;
        System.out.println("candidatato "+ this.nomeCandidato3);
         System.out.println("Adicionar voto "+"\n");
       
        candidato.getAdicionarVoto();
       this.voto3 = candidato.votos;
        getResultadoDeEleição();
     }else if(this.numerodecandidatos==4){
          System.out.println("candidatato "+ this.nomeCandidato1);
         System.out.println("Adicionar voto "+"\n");
       
        candidato.getAdicionarVoto();
       this.voto1 = candidato.votos;
        System.out.println("candidatato "+ this.nomeCandidato2);
         System.out.println("Adicionar voto "+"\n");
       
        candidato.getAdicionarVoto();
       this.voto2 = candidato.votos;
        System.out.println("candidatato "+ this.nomeCandidato3);
         System.out.println("Adicionar voto "+"\n");
       
        candidato.getAdicionarVoto();
       this.voto3 = candidato.votos;
        System.out.println("candidatato "+ this.nomeCandidato4);
         System.out.println("Adicionar voto "+"\n");
       
        candidato.getAdicionarVoto();
       this.voto4 = candidato.votos;
          getResultadoDeEleição();
     } else if(this.numerodecandidatos == 0 ){
         System.out.println("nao ha candidatos cadastrados"+"\n");
         getMenuDeOpções();
         
     }  
     
        return IniciarEleição;
    
    }
     
    public void setIniciarEleição(int IniciarEleição) {
        this.IniciarEleição = IniciarEleição;
    }

    public int getResultadoDeEleição() {
        
        
        if(this.numerodecandidatos == 2){
            if(this.voto1 > this.voto2){
                System.out.println("Candidato " + this.nomeCandidato1 + " partido " + this.partidoCandidato1 + " numero " + this.candidato1); 
                System.out.println("Foi Eleito");
            }else if(this.voto1 < this.voto2){
                System.out.println("Candidato " + this.nomeCandidato2 + " partido " + this.partidoCandidato2 + " numero " + this.candidato2);
                System.out.println("Foi Eleito");
               
            }else if(this.voto1 == this.voto2){
                System.out.println("Empate");
                System.out.println("Recotagem");
                getIniciarEleição();
            }
        }else if(this.numerodecandidatos == 3){
           if (this.voto1 > this.voto2) {
            if(this.voto1 > this.voto3){   
            System.out.println("Candidato " + this.nomeCandidato1 + " partido " + this.partidoCandidato1 + " numero " + this.candidato1); 
                System.out.println("Foi Eleito");  
        }
        }
           else if (this.voto2> this.voto1){
        if(this.voto2 > this.voto3){
            System.out.println("Candidato "+ this.nomeCandidato2 + " partido " + this.partidoCandidato2 + " numero "+this.candidato2); 
                System.out.println("Foi Eleito");  
        } }
           else if (this.voto3 >this.voto1){
               if(this.voto3 > this.voto2){
                System.out.println("Candidato " + this.nomeCandidato3 + " partido "+ this.partidoCandidato3 + " numero " + this.candidato3); 
                System.out.println("Foi Eleito");     
               }
           }else if (this.voto3 ==this.voto1){
               if(this.voto3 == this.voto2){
                    System.out.println("Empate");
                System.out.println("Recotagem");
                getIniciarEleição();
               }
           }
        
        }else if(this.numerodecandidatos == 4){
            if(this.voto1 > this.voto2){
                if(this.voto1 >this.voto3){
                    if(this.voto1>this.voto4){
                     System.out.println("Candidato " + this.nomeCandidato1 + " partido " + this.partidoCandidato1 + " numero " + this.candidato1); 
                System.out.println("Foi Eleito");     
                    }
                }
            }
             if(this.voto2 > this.voto1){
                if(this.voto2 >this.voto3){
                    if(this.voto2>this.voto4){
                     System.out.println("Candidato " + this.nomeCandidato2 + " partido "+ this.partidoCandidato2 + "numero " + this.candidato2); 
                System.out.println("Foi Eleito");     
                    }
                }
            }
              if(this.voto3 > this.voto2){
                if(this.voto3 >this.voto1){
                    if(this.voto3>this.voto4){
                     System.out.println(" Candidato " + this.nomeCandidato3 + " partido " + this.partidoCandidato3 + " numero " + this.candidato3); 
                System.out.println("Foi Eleito");     
                    }
                }
            } if(this.voto4 > this.voto2){
                if(this.voto4 >this.voto3){
                    if(this.voto4>this.voto4){
                     System.out.println("Candidato " + this.nomeCandidato4 + "partido " + this.partidoCandidato4 + "numero " + this.candidato4); 
                System.out.println("Foi Eleito");     
                    }
                }
            }
             if(this.voto2 == this.voto1){
                if(this.voto2 ==this.voto3){
                    if(this.voto2==this.voto4){
                     System.out.println("Empate");
                System.out.println("Recotagem");
                getIniciarEleição();     
                    }
                }
            }
        }else if(this.numerodecandidatos == 1){
         System.out.println("Candidato " + this.nomeCandidato1+ " partido "+ this.partidoCandidato1 +" numero " + this.candidato1); 
                System.out.println("Foi Eleito");    
        }
          
        return ResultadoDeEleição;
    }

    public void setResultadoDeEleição(int ResultadoDeEleição) {
        this.ResultadoDeEleição = ResultadoDeEleição;
    }

}
