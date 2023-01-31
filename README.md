# sarakoa-github.io

import com.aspose.pdf.*;

import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;

public class directorio {
    public static void main(String[] args) {

        String titulo = "Aplicacion Viafirma";

        System.out.println(titulo);

        String rootDir = "/Users/usuario/Desktop/directorio";
        try {
            Files.walk(Paths.get(rootDir))
                    .filter(Files::isRegularFile)
                    .forEach(System.out::println);
        } catch (IOException e) {
            e.printStackTrace();
        }

        Document document = new Document("C:/Users/usuario/Desktop/directorio/manuel.pdf");
        Page page = document.getPages().add();
        TextFragment text = new TextFragment("Pagina agregada");
        text.setFootNote(new Note("agrego página en blanco"));
        page.getParagraphs().add(text);
        document.save("C:/Users/usuario/Desktop/directorio/manuel.pdf");

        Document document1 = new Document("C:/Users/usuario/Desktop/directorio/sara.pdf");
        Page page1 = document1.getPages().add();
        TextFragment text1 = new TextFragment("Pagina agregada");
        text.setFootNote(new Note("agrego página en blanco"));
        page.getParagraphs().add(text);
        document1.save("C:/Users/usuario/Desktop/directorio/sara.pdf");

        Document document2 = new Document("C:/Users/usuario/Desktop/directorio/padron.pdf");
        Page page2 = document2.getPages().add();
        TextFragment text2 = new TextFragment("Pagina agregada");
        text.setFootNote(new Note("agrego página en blanco"));
        page.getParagraphs().add(text);
        document2.save("C:/Users/usuario/Desktop/directorio/padron.pdf");

        Document document3 = new Document("C:/Users/usuario/Desktop/directorio/familia.pdf");
        Page page3 = document3.getPages().add();
        TextFragment text3 = new TextFragment("Pagina agregada");
        text.setFootNote(new Note("agrego página en blanco"));
        page.getParagraphs().add(text);
        document3.save("C:/Users/usuario/Desktop/directorio/familia.pdf");




        }

    }




