//David Calen 2022-02-23
import java.util.Scanner;
import java.io.IOException;
import java.util.ArrayList;
public class Kommentarer3 {
    public static void main(String[] args) {

        char oldc = '0';

        boolean inc = false;
        boolean inp = false;

        ArrayList<String> arraylist = new ArrayList<String>();
        String filteredtext = "";
        String text = "";
        Scanner scan = new Scanner(System.in);

        while (scan.hasNextLine()){
            String string = scan.nextLine();
            arraylist.add(string);
        }
        for (String i : arraylist){
            text += i + "\n";
        }
        for(int i = 0; i < text.length(); i++) {
            char c = text.charAt(i);
            if(c =='%'){
                if(inc==false){
                    if(inp == true){
                        inp = false;
                        c = '\0';
                    }
                    else{
                        inp = true;
                    }    
                }
            }
            else if(inp == false){
                if(c == '*'){ //Stanger kommentar
                    if(text.charAt(i+1) == '/'){
                        if(inc == true){
                            inc = false;
                            c = '\0';
                            text = text.substring(0, i) +'\0' + text.substring(i+2,text.length()-1);
                        }
                    }
                //else{
                //    oldc = c;
                //    }
                    
                }
                else if(c == '/'){
                    if(text.charAt(i+1) == '*'){ //Oppnar kommentar
                        inc = true;
                        c = '\0';
                    }
                }
            }

            
            if(inc == false && inp == false){
                if((c != '*' && oldc != '/') || (c!= '/' && oldc != '*') || c!='\0'){
                    filteredtext = filteredtext + c;
                }
        
                }
            
        }
        System.out.println(filteredtext);
        
    }
}

    


