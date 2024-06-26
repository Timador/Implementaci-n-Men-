package ImplementacionMenu;

import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.*;
import javafx.scene.layout.BorderPane;
import javafx.stage.Stage;

public class AplicacionMenu extends Application {

	 @Override
	    public void start(Stage primaryStage) {
	        primaryStage.setTitle("JavaFX Menu Example");

	        // Crear la barra de menú
	        MenuBar menuBar = new MenuBar();

	        // Menú Archivo
	        Menu fileMenu = new Menu("Archivo");
	        MenuItem newFile = new MenuItem("Nuevo");
	        MenuItem openFile = new MenuItem("Abrir");
	        MenuItem saveFile = new MenuItem("Guardar");
	        SeparatorMenuItem separator1 = new SeparatorMenuItem();
	        MenuItem exitApp = new MenuItem("Salir");

	        // Añadir elementos al menú Archivo
	        fileMenu.getItems().addAll(newFile, openFile, saveFile, separator1, exitApp);

	        // Menú Editar
	        Menu editMenu = new Menu("Editar");
	        MenuItem cut = new MenuItem("Cortar");
	        MenuItem copy = new MenuItem("Copiar");
	        MenuItem paste = new MenuItem("Pegar");
	        SeparatorMenuItem separator2 = new SeparatorMenuItem();
	        MenuItem delete = new MenuItem("Eliminar");

	        // Añadir elementos al menú Editar
	        editMenu.getItems().addAll(cut, copy, paste, separator2, delete);

	        // Menú Ayuda
	        Menu helpMenu = new Menu("Ayuda");
	        MenuItem about = new MenuItem("Acerca de");

	        // Añadir elementos al menú Ayuda
	        helpMenu.getItems().add(about);

	        // Añadir los menús a la barra de menú
	        menuBar.getMenus().addAll(fileMenu, editMenu, helpMenu);

	        // Crear un Label para mostrar mensajes
	        Label messageLabel = new Label("Selecciona una opción del menú");

	        // Definir acciones para los elementos del menú Archivo
	        newFile.setOnAction(e -> {
	            System.out.println("Nuevo archivo creado");
	            messageLabel.setText("Nuevo archivo creado");
	        });
	        openFile.setOnAction(e -> {
	            System.out.println("Abrir archivo");
	            messageLabel.setText("Abrir archivo");
	        });
	        saveFile.setOnAction(e -> {
	            System.out.println("Guardar archivo");
	            messageLabel.setText("Guardar archivo");
	        });
	        exitApp.setOnAction(e -> {
	            System.out.println("Saliendo de la aplicación");
	            primaryStage.close();
	        });

	        // Definir acciones para los elementos del menú Editar
	        cut.setOnAction(e -> {
	            System.out.println("Cortar");
	            messageLabel.setText("Cortar");
	        });
	        copy.setOnAction(e -> {
	            System.out.println("Copiar");
	            messageLabel.setText("Copiar");
	        });
	        paste.setOnAction(e -> {
	            System.out.println("Pegar");
	            messageLabel.setText("Pegar");
	        });
	        delete.setOnAction(e -> {
	            System.out.println("Eliminar");
	            messageLabel.setText("Eliminar");
	        });

	        // Definir acción para el elemento del menú Ayuda
	        about.setOnAction(e -> {
	            System.out.println("Acerca de esta aplicación");
	            messageLabel.setText("Acerca de esta aplicación");
	        });

	        // Crear el layout principal
	        BorderPane layout = new BorderPane();
	        layout.setTop(menuBar); // Colocar la barra de menú en la parte superior
	        layout.setCenter(messageLabel); // Colocar el Label en el centro

	        // Crear la escena y añadirla al escenario
	        Scene scene = new Scene(layout, 800, 600);
	        primaryStage.setScene(scene);
	        primaryStage.show(); // Mostrar la ventana
	    }

	    public static void main(String[] args) {
	        launch(args); // Iniciar la aplicación JavaFX
	    }
	}

IMAGEN DE LA CONSOLA (se añadió un Label que muestre el mensaje de la opción selecionada)
 ![image](https://github.com/Timador/Implementaci-n-Men-/assets/168133781/df9c844e-de9c-474c-83df-0027b0b8c4fe)
