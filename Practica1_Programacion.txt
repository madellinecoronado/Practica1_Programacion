/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package practica1;


import java.util.ArrayList;
import java.util.Scanner;
import java.io.FileWriter;
import java.io.IOException;
import java.io.*;
import java.util.Iterator;

public class Practica1 {
    
    
    
    public static class Computadora{
        public String correoElectronico;
        public String nombreDispositivo;
        public String numeroTelefonico;
        public String visible;
        
       public Computadora(String correoElectronico, String nombreDispositivo, String visible){
            this.correoElectronico = correoElectronico;
            this.nombreDispositivo = nombreDispositivo;
            this.visible = visible;
        }

        public Computadora() {
            //throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
        }
        
        public String getCorreoElectronico(){
            return correoElectronico;
        }
        
        public void setCorreoElectronico(String correoElectronico){
            this.correoElectronico = correoElectronico;
        }
        
        public String getNombreDispositivo(){
            return nombreDispositivo;
        }
        
        public void setNombreDispositivo(String nombreDispositivo){
            this.nombreDispositivo = nombreDispositivo;
        }
        
        public String getNumeroTelefonico(){
            return numeroTelefonico;
        }
        
        public void setNnumeroTelefonico(String numeroTelefonico){
            this.numeroTelefonico = numeroTelefonico;
        }
        
        public String getVisible(){
            return visible;
        }
        
        public void setVisible(String visible){
            this.visible = visible;
        }
    }
    
    
    
    public static class Tablet{
        public String correoElectronicoTablet;
        public String nombreDispositivoTablet;
        public String visibleTablet;
        
        public Tablet(String correoElectronicoTablet, String nombreDispositivoTablet, String visibleTablet){
            this.correoElectronicoTablet = correoElectronicoTablet;
            this.nombreDispositivoTablet = nombreDispositivoTablet;
            this.visibleTablet = visibleTablet;
        }

        private Tablet() {
           // throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
        }
        
        public String getCorreoElectronicoTablet(){
            return correoElectronicoTablet;
        }
        
        public void setCorreoElectronicoTablet(String correoElectronicoTablet){
            this.correoElectronicoTablet = correoElectronicoTablet;
        }
        
        public String getNombreDispositivoTablet(){
            return nombreDispositivoTablet;
        }
        
        public void setNombreDispositivoTablet(String nombreDispositivoTablet){
            this.nombreDispositivoTablet = nombreDispositivoTablet;
        }
        
        public String getVisibleTablet(){
            return visibleTablet;
        }
        
        public void setVisibleTablet(String visibleTablet){
            this.visibleTablet = visibleTablet;
        }
    }
    
        public static class Smartwatch{
        public String correoElectronicoSmartwatch;
        public String nombreDispositivoSmartwatch;
        public String visibleSmartwatch;
        
        public Smartwatch(String correoElectronicoSmartwatch, String nombreDispositivoSmartwatch, String visibleSmartwatch){
            this.correoElectronicoSmartwatch = correoElectronicoSmartwatch;
            this.nombreDispositivoSmartwatch = nombreDispositivoSmartwatch;
            this.visibleSmartwatch = visibleSmartwatch;
        }

        private Smartwatch() {
            //throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
        }
        
        public String getCorreoElectronicoSmartwatch(){
            return correoElectronicoSmartwatch;
        }
        
        public void setCorreoElectronicoSmartwatch(String correoElectronicoSmartwatch){
            this.correoElectronicoSmartwatch = correoElectronicoSmartwatch;
        }
        
        public String getNombreDispositivoSmartwatch(){
            return nombreDispositivoSmartwatch;
        }
        
        public void setNombreDispositivoSmartwatch(String nombreDispositivoSmartwatch){
            this.nombreDispositivoSmartwatch = nombreDispositivoSmartwatch;
        }
        
        public String getVisibleSmartwatch(){
            return visibleSmartwatch;
        }
        
        public void setVisibleSmartwatch(String visibleSmartwatch){
            this.visibleSmartwatch = visibleSmartwatch;
        }
    }
        
        public static class Smartphone{
        public String correoElectronicoSmartphone;
        public String nombreDispositivoSmartphone;
        public String numeroTelefonicoSmartphone;
        public String visibleSmartphone;
        
        public Smartphone(String correoElectronicoSmartphone, String nombreDispositivoSmartphone, String numeroTelefonicoSmartphone, String visibleSmartphone){
            this.correoElectronicoSmartphone = correoElectronicoSmartphone;
            this.nombreDispositivoSmartphone = nombreDispositivoSmartphone;
            this.numeroTelefonicoSmartphone = numeroTelefonicoSmartphone;
            this.visibleSmartphone = visibleSmartphone;
        }

        private Smartphone() {
            //throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
        }
        
        public String getCorreoElectronicoSmartphone(){
            return correoElectronicoSmartphone;
        }
        
        public void setCorreoElectronicoSmartphone(String correoElectronicoSmartphone){
            this.correoElectronicoSmartphone = correoElectronicoSmartphone;
        }
        
        public String getNumeroTelefonicoSmartphone(){
            return numeroTelefonicoSmartphone;
        }
        
        public void setNumeroTelefonicoSmartphone(String numeroTelefonicoSmartphone){
            this.numeroTelefonicoSmartphone = numeroTelefonicoSmartphone;
        }
        
        public String getNombreDispositivoSmartphone(){
            return nombreDispositivoSmartphone;
        }
        
        public void setNombreDispositivoSmartphone(String nombreDispositivoSmartphone){
            this.nombreDispositivoSmartphone = nombreDispositivoSmartphone;
        }
        
        public String getVisibleSmartphone(){
            return visibleSmartphone;
        }
        
        public void setVisibleSmartphone(String visibleSmartphone){
            this.visibleSmartphone = visibleSmartphone;
        }
    }
        
        public static class archivos {
            
            public String leerTxt(String direccion) throws FileNotFoundException, IOException{
                
                String texto = "";
                
                try{
                    
                    BufferedReader bf = new BufferedReader(new FileReader (direccion));
                    String temp = "";
                    String bfRead;
                    while ((bfRead = bf.readLine()) != null){
                        
                        temp = temp + bfRead;
                         
                    }
                          texto = temp;

                }catch(Exception e){ 
                System.err.println("No se encontro archivo");
            
            }
                return texto;
            }
           
        }
    
        
    
    /**
     * @param args the command line arguments
         * @throws java.io.IOException
     */
    
    /*public static void imprimir(ArrayList<String> computadoras) {
        for (String elemento : computadoras)
            System.out.print(elemento + "-");
        System.out.println();
    }*/
    public static void main(String[] args) throws IOException {
        // TODO code application logic here
        FileWriter ficheroComputadora = new FileWriter ("C:/Users/Pablo/Desktop/ficheroComputadora.txt");
        FileWriter ficheroTablet = new FileWriter ("C:/Users/Pablo/Desktop/ficheroTablet.txt");
        FileWriter ficheroSmartwatch = new FileWriter ("C:/Users/Pablo/Desktop/ficheroSmartwatch.txt");
        FileWriter ficheroSmartphone= new FileWriter ("C:/Users/Pablo/Desktop/ficheroSmartphone.txt");
        
        
        ArrayList<Computadora> computadoras = new ArrayList<Computadora>() ;
        Computadora computadora = new Computadora();
        
        
        ArrayList<Tablet> tablets = new ArrayList<Tablet>() ;
        Tablet tablet = new Tablet();
        
        ArrayList<Smartwatch> smartwatchs = new ArrayList<Smartwatch>() ;
        Smartwatch smartwatch = new Smartwatch();
        
                ArrayList<Smartphone> smartphones = new ArrayList<Smartphone>() ;
        Smartphone smartphone = new Smartphone();
        //disp = new ArrayList<Dispositivos>();

        
        Scanner crear = new Scanner(System.in);
        int opcion;

do{
        System.out.println("-------------------------- Ecosistema de Dispotivos --------------------------");
        System.out.println("1. Crear dispositivo");
        System.out.println("2. Administrar dispositivo");
        System.out.println("3. Acciones con dispositivos");
        System.out.println("4. Acciones externas de dispositivos");
        System.out.println("5. Cargas masivas");
        System.out.println("6. Logs");
        System.out.println("7. Salir");
        System.out.println("");
        System.out.println("Seleccione tipo de dispositivo a crear:");
        System.out.println("------------------------------------------------------------------------------");
        
        opcion = crear.nextInt();
        
    switch(opcion){
        case 1:
            Scanner creacion = new Scanner(System.in);
            int opcionCreacion = 0 ;
        
            System.out.println("----------------------------- Crear Dispositivo -----------------------------");
            System.out.println("1. Computadora portátil");
            System.out.println("2. Tablet");
            System.out.println("3. SmartWatch");
            System.out.println("4. Smartphone");
            System.out.println("5. Auriculares inalámbricos");
            System.out.println("");
            System.out.println("Seleccione tipo de dispositivo a crear:");
            System.out.println("------------------------------------------------------------------------------");
        
            opcionCreacion = creacion.nextInt();
            
            switch(opcionCreacion){
                case 1:
                 
                Scanner creacionComputadora = new Scanner(System.in);
                            
                System.out.println("------------------ Creación de nueva Computadora portatil ---------------------");
                System.out.println("Correo electrónico:");
                String correoElectronico = creacionComputadora.next();
                System.out.println("Nombre del dispositivo:");
                String nombreDispositivo = creacionComputadora.next();
                System.out.println("Visible para conexión:");
                System.out.println("SI        NO");
                String visible = creacionComputadora.next();
                System.out.println("");
                System.out.println("Presione enter para confirmar los datos...");
                System.out.println("------------------------------------------------------------------------------");
                
                computadora.setCorreoElectronico(correoElectronico);
                computadora.setNombreDispositivo(nombreDispositivo);
                computadora.setVisible(visible);

                computadoras.add(computadora);
                
                //Computadora computadora = new Computadora(correoElectronico, nombreDispositivo, visible);
          
                
                System.out.println("----------------------- Nueva Computadora portatil --------------------------");
                System.out.println("");
               /* for (Computadora modelComputadora : listaComputadora) {
                  System.out.println("Correo electrónico: " + modelComputadora.getCorreoElectronico());
                  System.out.println("Nombre del dispositivo: " + modelComputadora.getNombreDispositivo());
                  System.out.println("Visible para conexion: " + modelComputadora.getVisible());
                  /*ficheroComputadora.write("Correo electrónico: " + modelComputadora.getCorreoElectronico() + "\n");
                  ficheroComputadora.write("Nombre del dispositivo: " + modelComputadora.getNombreDispositivo() + "\n");
                  ficheroComputadora.write("Visible para conexion: " + modelComputadora.getVisible() + "\n");
                }
               ficheroComputadora.close();*/
                //System.out.println(computadora.getNombreDispositivo());
                
                System.out.println("");
                System.out.println("Nota: El dispositivo será encendido por defecto.");
                   

                break;
                
                
                
                case 2:
                    
                Scanner creacionTablet = new Scanner(System.in);
                
                System.out.println("------------------------ Creación de nueva Tablet -------------------------");
                System.out.println("Correo electrónico:");
                String correoElectronicoTablet = creacionTablet.next();
                System.out.println("Nombre del dispositivo:");
                String nombreDispositivoTablet = creacionTablet.next();
                System.out.println("Visible para conexión:");
                System.out.println("SI        NO");
                String visibleTablet = creacionTablet.next();
                System.out.println("");
                System.out.println("Presione enter para confirmar los datos...");
                System.out.println("--------------------------------------------------------------------------");
                
                /*Tablet tablet = new Tablet(correoElectronicoTablet, nombreDispositivoTablet, visibleTablet);
                ArrayList<Tablet> listaTablet = new ArrayList<Tablet>();*/
               //listaTablet.add(tablet);
                
                tablet.setCorreoElectronicoTablet(correoElectronicoTablet);
                tablet.setNombreDispositivoTablet(nombreDispositivoTablet);
                tablet.setVisibleTablet(visibleTablet);

                tablets.add(tablet);
                
                System.out.println("------------------------------ Nueva Tablet ------------------------------");
                System.out.println("");
                /*for (Tablet modelTablet : listaTablet) {
                  System.out.println("Correo electrónico: " + modelTablet.getCorreoElectronicoTablet());
                  System.out.println("Nombre del dispositivo: " + modelTablet.getNombreDispositivoTablet());
                  System.out.println("Visible para conexion: " + modelTablet.getVisibleTablet());
                  ficheroTablet.write("Correo electrónico: " + modelTablet.getCorreoElectronicoTablet() + "\n");
                  ficheroTablet.write("Nombre del dispositivo: " + modelTablet.getNombreDispositivoTablet() + "\n");
                  ficheroTablet.write("Visible para conexion: " + modelTablet.getVisibleTablet() + "\n");
                }
                ficheroTablet.close();*/
                System.out.println("");
                System.out.println("Nota: El dispositivo será encendido por defecto.");
                
                break;
                
                case 3:
                    
                Scanner creacionSmartwatch = new Scanner(System.in);
                    
                System.out.println("------------------ Creación de nuevo SmartWatch ---------------------");
                System.out.println("Correo electrónico:");
                String correoElectronicoSmartwatch = creacionSmartwatch.next();
                System.out.println("Nombre del dispositivo:");
                String nombreDispositivoSmartwatch = creacionSmartwatch.next();
                System.out.println("Visible para conexión:");
                System.out.println("SI        NO");
                String visibleSmartwatch = creacionSmartwatch.next();
                System.out.println("");
                System.out.println("Presione enter para confirmar los datos...");
                System.out.println("-----------------------------------------------------------------");
                
              //  Smartwatch smartwatch = new Smartwatch(correoElectronicoSmartwatch, nombreDispositivoSmartwatch, visibleSmartwatch);
                //ArrayList<Smartwatch> listaSmartwatch = new ArrayList<Smartwatch>();
                //listaSmartwatch.add(smartwatch);
                
                smartwatch.setCorreoElectronicoSmartwatch(correoElectronicoSmartwatch);
                smartwatch.setNombreDispositivoSmartwatch(nombreDispositivoSmartwatch);
                smartwatch.setVisibleSmartwatch(visibleSmartwatch);

                smartwatchs.add(smartwatch);
                
                System.out.println("------------------------------ Nuevo Smartwatch ------------------------------");
                System.out.println("");
                /*for (Smartwatch modelSmartwatch : listaSmartwatch) {
                  System.out.println("Correo electrónico: " + modelSmartwatch.getCorreoElectronicoSmartwatch());
                  System.out.println("Nombre del dispositivo: " + modelSmartwatch.getNombreDispositivoSmartwatch());
                  System.out.println("Visible para conexion: " + modelSmartwatch.getVisibleSmartwatch());
                  ficheroSmartwatch.write("Correo electrónico: " + modelSmartwatch.getCorreoElectronicoSmartwatch() + "\n");
                  ficheroSmartwatch.write("Nombre del dispositivo: " + modelSmartwatch.getNombreDispositivoSmartwatch() + "\n");
                  ficheroSmartwatch.write("Visible para conexion: " + modelSmartwatch.getVisibleSmartwatch() + "\n");
                }
                ficheroSmartwatch.close();*/
                System.out.println("");
                System.out.println("Nota: El dispositivo será encendido por defecto.");
                
                break;
                    
                case 4:
                    
                Scanner creacionSmartphone = new Scanner(System.in);
                    
                System.out.println("------------------ Creación de nuevo Smartphone ---------------------");
                System.out.println("Correo electrónico:");
                String correoElectronicoSmartphone = creacionSmartphone.next();
                System.out.println("Nombre del dispositivo:");
                String nombreDispositivoSmartphone = creacionSmartphone.next();
                System.out.println("Numero Telefonico:");
                String numeroTelefonicoSmartphone = creacionSmartphone.next();
                System.out.println("Visible para conexión:");
                System.out.println("SI        NO");
                String visibleSmartphone = creacionSmartphone.next();
                System.out.println("");
                System.out.println("Presione enter para confirmar los datos...");
                System.out.println("-----------------------------------------------------------------");
                
                /*Smartphone smartphone = new Smartphone(correoElectronicoSmartphone, nombreDispositivoSmartphone, numeroTelefonicoSmartphone, visibleSmartphone);
                ArrayList<Smartphone> listaSmartphone = new ArrayList<Smartphone>();
                listaSmartphone.add(smartphone);*/
                
                smartphone.setCorreoElectronicoSmartphone(correoElectronicoSmartphone);
                smartphone.setNombreDispositivoSmartphone(nombreDispositivoSmartphone);
                smartphone.setNombreDispositivoSmartphone(numeroTelefonicoSmartphone);
                smartphone.setVisibleSmartphone(visibleSmartphone);

                smartphones.add(smartphone);
                
                System.out.println("------------------------- Nuevo Smartphone ----------------------------");
                System.out.println("");
              /* for (Smartphone modelSmartphone : listaSmartphone) {
                  System.out.println("Correo electrónico: " + modelSmartphone.getCorreoElectronicoSmartphone());
                  System.out.println("Nombre del dispositivo: " + modelSmartphone.getNombreDispositivoSmartphone());
                  System.out.println("Numero Telefonico: " + modelSmartphone.getNumeroTelefonicoSmartphone());
                  System.out.println("Visible para conexion: " + modelSmartphone.getVisibleSmartphone());
                  ficheroSmartphone.write("Correo electrónico: " + modelSmartphone.getCorreoElectronicoSmartphone() + "\n");
                  ficheroSmartphone.write("Nombre del dispositivo: " + modelSmartphone.getNombreDispositivoSmartphone() + "\n");
                  ficheroSmartphone.write("Numero Telefonico: " + modelSmartphone.getNumeroTelefonicoSmartphone() + "\n");      
                  ficheroSmartphone.write("Visible para conexion: " + modelSmartphone.getVisibleSmartphone() + "\n");
                }
                ficheroSmartphone.close();*/
                System.out.println("");
                System.out.println("Nota: El dispositivo será encendido por defecto.");
                break;
                
                case 5:
                    
                System.out.println("------------------ Creación de nuevo Auriculares ---------------------");
                System.out.println("Listado de dispositivos:");
                //for (Computadora model : listaComputadora) {
                  //System.out.println(model.getNombreDispositivo());
                //}
                
               // archivos a = new archivos();
                /*System.out.println(a.leerTxt("C:/Users/Pablo/Desktop/ficheroComputadora.txt"));
                System.out.println(a.leerTxt("C:/Users/Pablo/Desktop/ficheroTablet.txt"));
                System.out.println(a.leerTxt("C:/Users/Pablo/Desktop/ficheroSmartwatch.txt"));
                System.out.println(a.leerTxt("C:/Users/Pablo/Desktop/ficheroSmartphone.txt"));*/
                
                
                /*ReporteDispositivos reporte = new ReporteDispositivos();
                reporte.generarReporte(computadoras);*/
                
                /*System.out.println(computadoras.size());
                
                Iterator it=computadoras.iterator();
                while(it.hasNext()){
                    Object objeto = it.next();
                    Dispositivos dispositivo=(Dispositivos)objeto;
                    System.out.println(dispositivo.getNombreDispositivo());
                }*/
                
                
            /*for(int i = 0; i < disp.size(); i++) {
                System.out.println(disp.get(i).getNombreDispositivo());
            }*/
                
                System.out.println(computadora.getNombreDispositivo() + "\n" + tablet.getNombreDispositivoTablet()
                + "\n" + smartwatch.getNombreDispositivoSmartwatch() + "\n" + smartphone.getNombreDispositivoSmartphone());
            
                //imprimir(computadoras);
                
                System.out.println("Seleccione un dispositivo para enlazar los auriculares:");
                System.out.println("");
                System.out.println("-----------------------------------------------------------------");
                
            }break;
            
        case 2:
            
            Scanner administrar = new Scanner(System.in);
            int opcionAdministrar = 0 ;
            
        
            System.out.println("------------------ Administrar Dispositivos ---------------------");
            System.out.println("1. Computadora portátil");
            System.out.println("2. Tablet");
            System.out.println("3. SmartWatch");
            System.out.println("4. Smartphone");
            System.out.println("5. Auriculares inalámbricos");
            System.out.println("");
            System.out.println("Seleccione tipo de dispositivo a administrar:");
            System.out.println("-----------------------------------------------------------------");
        
            opcionAdministrar = administrar.nextInt();
            
            switch(opcionAdministrar){
                case 1: 
                System.out.println("------------------ Computadoras creadas ---------------------");
                System.out.println("Listado de dispositivos:");
                System.out.println("");
                
                System.out.println(computadora.getNombreDispositivo());
                System.out.println("");
                System.out.println("Seleccione un dispositivo para administrar:");
                System.out.println("-----------------------------------------------------------------");
                
                System.out.println("-------------- Administración de computadora---------------------");
                System.out.println("");
                System.out.println("Nombre del dispositivo seleccionado: " + computadora.getNombreDispositivo());
                System.out.println("");
                System.out.println("1. Editar correo electrónico");
                System.out.println("2. Editar nombre del dispositivo");
                System.out.println("3. Apagar visibilidad del dispositivo");
                System.out.println("4. Apagar dispositivo");
                System.out.println("");
                System.out.println("Seleccione la propiedad a editar:");
                System.out.println("");
                System.out.println("-----------------------------------------------------------------");
                break;
                
                case 2: 
                System.out.println("------------------ Tablets creadas ---------------------");
                System.out.println("Listado de dispositivos:");
                System.out.println("");
                System.out.println(tablet.getNombreDispositivoTablet());
                System.out.println("");
                System.out.println("Seleccione un dispositivo para administrar:");
                System.out.println("-----------------------------------------------------------------");
                
                 
                System.out.println("-------------- Administración de tablet---------------------");
                System.out.println("");
                System.out.println("Nombre del dispositivo seleccionado: " + tablet.getNombreDispositivoTablet());
                System.out.println("");
                System.out.println("1. Editar correo electrónico");
                System.out.println("2. Editar nombre del dispositivo");
                System.out.println("3. Apagar visibilidad del dispositivo");
                System.out.println("4. Apagar dispositivo");
                System.out.println("");
                System.out.println("Seleccione la propiedad a editar:");
                System.out.println("");
                System.out.println("-----------------------------------------------------------------");
                break;
                
                case 3: 
                System.out.println("------------------ Smartwatch creados ---------------------");
                System.out.println("Listado de dispositivos:");
                System.out.println("");
                System.out.println(smartwatch.getNombreDispositivoSmartwatch());
                System.out.println("");
                System.out.println("Seleccione un dispositivo para administrar:");
                System.out.println("-----------------------------------------------------------------");
                
                 
                System.out.println("-------------- Administración de smartwatch---------------------");
                System.out.println("");
                System.out.println("Nombre del dispositivo seleccionado: " + smartwatch.getNombreDispositivoSmartwatch());
                System.out.println("");
                System.out.println("1. Editar correo electrónico");
                System.out.println("2. Editar nombre del dispositivo");
                System.out.println("3. Apagar visibilidad del dispositivo");
                System.out.println("4. Apagar dispositivo");
                System.out.println("");
                System.out.println("Seleccione la propiedad a editar:");
                System.out.println("");
                System.out.println("-----------------------------------------------------------------");
                break;
                
                case 4: 
                System.out.println("------------------ Smartphones creados ---------------------");
                System.out.println("Listado de dispositivos:");
                System.out.println("");
                System.out.println(smartphone.getNombreDispositivoSmartphone());
                System.out.println("");
                System.out.println("Seleccione un dispositivo para administrar:");
                System.out.println("-----------------------------------------------------------------");
                
                 
                System.out.println("-------------- Administración de smartphone---------------------");
                System.out.println("");
                System.out.println("Nombre del dispositivo seleccionado: " + smartphone.getNombreDispositivoSmartphone());
                System.out.println("");
                System.out.println("1. Editar correo electrónico");
                System.out.println("2. Editar nombre del dispositivo");
                System.out.println("3. Apagar visibilidad del dispositivo");
                System.out.println("4. Apagar dispositivo");
                System.out.println("");
                System.out.println("Seleccione la propiedad a editar:");
                System.out.println("");
                System.out.println("-----------------------------------------------------------------");
                break;
                
                case 5: 
                System.out.println("------------------ Auriculares creados ---------------------");
                System.out.println("Listado de dispositivos:");
                System.out.println("");
                System.out.println("");
                System.out.println("Seleccione un dispositivo para administrar:");
                System.out.println("-----------------------------------------------------------------");
            }break;
            
        case 3:
            Scanner acciones = new Scanner(System.in);
            int opcionAcciones = 0 ;
            
        
            System.out.println("------------------ Acciones con Dispositivos ---------------------");
            System.out.println("Selecciones el tipo de dispositivo:");
            System.out.println("");  
            System.out.println("1. Computadora portátil");
            System.out.println("2. Tablet");
            System.out.println("3. SmartWatch");
            System.out.println("4. Smartphone");
            System.out.println("5. Auriculares inalámbricos");
            System.out.println("");
            System.out.println("Seleccione un tipo de dispositivo:");
            System.out.println("");
            System.out.println("-----------------------------------------------------------------");
        
            opcionAcciones = acciones.nextInt();
            
            switch(opcionAcciones){
                case 1:
                System.out.println("------------------ Acciones con Dispositivos ---------------------");
                System.out.println("");  
                System.out.println("Tipo de dispositivo: Computadora portátil");
                System.out.println("Nombre del Dispositivo:");
                System.out.println(""); 
                System.out.println("Seleccione el tipo de acción a realizar:");
                System.out.println(""); 
                System.out.println("1. Tomar fotografía");
                System.out.println("2. Copiar texto");
                System.out.println("3. Pegar texto");
                System.out.println("4. Compartir documentos");
                System.out.println("5. Reproducir música");
                System.out.println("");
                System.out.println("Seleccione acción a realizar:");
                System.out.println("");
                System.out.println("-----------------------------------------------------------------");
                break;
                
                case 2:
                System.out.println("------------------ Acciones con Dispositivos ---------------------");
                System.out.println("");  
                System.out.println("Tipo de dispositivo: Tablet");
                System.out.println("Nombre del Dispositivo:");
                System.out.println(""); 
                System.out.println("Seleccione el tipo de acción a realizar:");
                System.out.println(""); 
                System.out.println("1. Tomar fotografía");
                System.out.println("2. Copiar texto");
                System.out.println("3. Pegar texto");
                System.out.println("4. Compartir documentos");
                System.out.println("5. Reproducir música");
                System.out.println("");
                System.out.println("Seleccione acción a realizar:");
                System.out.println("");
                System.out.println("-----------------------------------------------------------------");
                break;
                
                case 3:
                System.out.println("------------------ Acciones con Dispositivos ---------------------");
                System.out.println("");  
                System.out.println("Tipo de dispositivo: Smartwatch");
                System.out.println("Nombre del Dispositivo:");
                System.out.println(""); 
                System.out.println("Seleccione el tipo de acción a realizar:");
                System.out.println(""); 
                System.out.println("1. Tomar fotografía");
                System.out.println("2. Copiar texto");
                System.out.println("3. Reproducir música");
                System.out.println("");
                System.out.println("Seleccione acción a realizar:");
                System.out.println("");
                System.out.println("-----------------------------------------------------------------");
                break;
                
                case 4:
                System.out.println("------------------ Acciones con Dispositivos ---------------------");
                System.out.println("");  
                System.out.println("Tipo de dispositivo: Smartphone");
                System.out.println("Nombre del Dispositivo:");
                System.out.println(""); 
                System.out.println("Seleccione el tipo de acción a realizar:");
                System.out.println(""); 
                System.out.println("1. Tomar fotografía");
                System.out.println("2. Copiar texto");
                System.out.println("3. Pegar texto");
                System.out.println("4. Compartir documentos");
                System.out.println("5. Reproducir música");
                System.out.println("");
                System.out.println("Seleccione acción a realizar:");
                System.out.println("");
                System.out.println("-----------------------------------------------------------------");
                break;
            }
        }
    }while(opcion < 7);}
    }
