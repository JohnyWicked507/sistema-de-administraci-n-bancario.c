#include<stdio.h>
#include<math.h>
#include<stdlib.h>
#define cuenta 472395814

//FUNCION DEPOSITO
float depo(float capital,float d){    
float saldo;   
capital+=(capital*0.0125)+d;   
return(capital);

}

//FUNCION TRANSFERElNCIA
float transfer(float capital,float trans){ 
float saldo;   
capital=capital-trans; 
return(capital);

}

//PROGRAMA PRINCIPAL
int main(){
int menu[99],i;
float monto[99];
floatcapital,deposito,transferencia,opc,cont,saldo,retiro,contret,conttran,acum,contdep;
int contrase; 
cont=0; 
contdep=0; 
contret=0; 
conttran=0;
 acum=0; i=0;
char nombre[50];


printf("\t**BIENVENIDO AL BANCO ABC** \n");
printf("Por favor ingrese su nombre \n");    
gets(nombre);       
printf("Ingrese su numero de cuenta\n");       
scanf("%d",&contrase);    
system("CLS");if(contrase != cuenta){


do{        
system("CLS");        
printf("Numero de cuenta invalido\n");        
printf("Ingrese su numero de cuenta\n");        
scanf("%d",&contrase);        
system("CLS");        
}while(contrase!=cuenta);}if(contrase==cuenta){        
printf("\t SEA BIENVENIDO A SU CUENTA\n");        
printf("Ingrese su capital\n");        
scanf("%f",&capital);


if(capital>=100){
do{        
printf("\nESCOJA LA OPCION QUE DESEA REALIZAR\n");        
printf("1.Deposito \n2.Retiro \n3.Transferencia \n4.Salir \n OPCION:");        
scanf("%f",&opc);        
system("CLS");
if(opc>4 || opc<1){        
printf("Opcion no valida\n");        
printf("Por favor ingrese una opcion valida\n");

}


saldo=transfer(capital,transferencia);        
capital=capital-transferencia;      
 // cont++;       
 conttran++;        
menu[i]=3;        
monto[i]=transferencia;}    
if(saldo<100){           
 i--;        
printf("Usted no puede retirar esta cantidad ya que su capital quedara por debajo de los 100 dolares\n");        
capital=capital+retiro;       
 saldo=saldo+transferencia;        
//cont++;        conttran--;  


  }      


  printf("Su saldo actual es de:%f",saldo);}cont=contdep+contret+conttran;
if(opc==4){        
printf("\t BANCO ABC-ESTADO DE CUENTA\n");        
printf("Cliente: %s",nombre);        
printf("\nN de Cuenta: %d",contrase);        
printf("\nN\t Tipo de transaccion \t Monto\n");       
 for(i=1;i<=cont;i++)

{            

printf("%i",i);           
 if(menu[i]==1){                
printf("\t DEPOSITO");               
 printf("\t\t %.2f\n",monto[i]);}           
 else if(menu[i]==2){                
printf("\t RETIRO\t\t\t %.2f\n",monto[i]);}            
else if(menu[i]==3){                
printf("\t TRANSFERENCIA\t\t %2.f\n ",monto[i]);

}      
 
       printf("\nSu saldo es:%f",capital);
}

}while(opc==1|| opc==2 || opc==3 || opc>4 || opc<1);}else{        
printf("Usted no puede tener un capital menor a 100");

}
}
}
