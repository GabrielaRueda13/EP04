
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>

struct cancion{
  char titulo[30];  
  char interprete[30];
  char album[30];
  char genero[10];
  float duracion;
  float precio;
  int valoracion; 
  int numCancion; 
  int cantRepr; 
  int anio; 
    struct cancion *siguiente;
    struct cancion *anterior; 
};

void encabezado(){
            printf("\t\t _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _\n"); 
            printf("\t\t/- - - - - - - - - - - - - - - - - - - - - \\ \n");
            printf("\t\t| |  \t\t21:59 p.m.          26%%  | |\n");
           // printf("\t\t| | 1: 123456789112345678921234567891    | |\n");
}

void inferior(){
    printf("\t\t| |______________________________________| |\n");
    printf("\t\t| |  \t\t\t\t\t | |\n\n"); 
}
void reproductor_menu(){
    printf("\t\t _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ \n"); 
    printf("\t\t/- - - - - - - - - - - - - - - - - - - - - \\ \n");
    printf("\t\t| |  \t\t21:59 p.m.          26%%  | |\n");
    printf("\t\t| |_________________________________\t | |\n");
    printf("\t\t| | 1 Agregar canci%cn a la playlist |  \t | |\n", 162);
    printf("\t\t| | 2 Ver playlist\t\t    |    | |\n"); 
    printf("\t\t| | 3 Eliminar canci%cn\t\t    |    | |\n", 162); 
    printf("\t\t| | 4 Reproducir\t\t    |    | |\n"); 
    printf("\t\t| | 5 Reordenar \t\t    |    | |\n"); 
    printf("\t\t| | 6 Buscar canci%cn \t\t    |    | |\n", 162); 
    printf("\t\t| | 7 Salir\t\t\t    |    | |\n"); 
  //  printf("\t\t| |  \t\t\t\t\t | |\n");
   // printf("\t\t| |  \t\t\t\t\t | |\n");
    printf("\t\t| |______________________________________| |\n");
    printf("\t\t| |  \t\t\t\t\t | |\n"); 
    printf("\t\t| |  \t\t   **** \t\t | |\n"); 
    printf("\t\t| |  \t   *   \t   MENU\t     * \t         | |\n"); 
    printf("\t\t| |  \t *   \t\t          * \t | |\n"); 
    printf("\t\t| |\t*<<   \t\t         >>* \t | |\n"); 
    printf("\t\t| |  \t *   \t    ||           * \t | |\n"); 
    printf("\t\t| |  \t   *\t   ****      * \t\t | |\n"); 
    printf("\t\t\\ \\- - - - - - - - - - - - - - - - - - - / / \n"); 
    printf("\t\t \\_ _ _ _ _ _ _ _ _ _ _ _  _ _ _ _ _ _ _ _/ \n");
    
    printf("\n\t::Elija una opci%cn: ", 162);
}

int ver_Playlist(struct cancion *inP ){
   int error=0;
    int i=1; 
	if(inP!=NULL){
            encabezado(); 
            printf("\t\t| | :: PlayList :: \t\t\t | |\n");  
		while(inP!=NULL){
			//printf("\t\t| | 1: 123456789112345678921234567891    | |\n");
			printf("\t\t| |: %d  %s  \n", i, inP->titulo); 
			printf("\t\t| |:: Album: %s \n", inP->album); 
			printf("\t\t| |:: Artista: %s \n", inP->interprete); 
			
			inP=inP->siguiente; 
            i++; 
		}
        inferior(); 
		
	} else {
		error=1;
	}
	
	
	
	
	
	return error; 
    
}
int info_Playlist(struct cancion *inP){
    
}
int main(int argc, char **argv)
{
	int op=0, error=0;
    struct cancion *in=NULL, *fi=NULL, tmpCancion, *valores; 
    while (op!=7){
        reproductor_menu(); 
        scanf("%d%*c", &op); 
        
        switch(op){
            
            case 1:
            
            break;
            
            case 2:
                error=ver_Playlist(in);
                if(error)
                    encabezado();
                    printf("\t\t| | :: PlayList :: \t\t\t | |\n"); 
                    printf("\t\t| | :: No hay canciones en la playlist   | |\n"); 
                    inferior(); 
            
            break;
            
            case 3:
            
            break;
            
            case 4:
            
            break;
            
            case 5:
            
            break;
            
            case 6:
            
            break;
            
            case 7:
            default:
                    printf("\t\t******\n\n"); 
        }
        
    }
    
}
