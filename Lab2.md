#Search Engine and DeBugging using JUnit.

##Search Engine
     
     import java.io.IOException;
     import java.net.URI;
     import java.util.ArrayList;


     class Handler implements URLHandler {
     // The one bit of state on the server: a number that will be manipulated by
     // various requests.
     ArrayList<String> words = new ArrayList<String>();
     
     public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Welcome to my Search Engine \n To add to the engine do '/add?=' then what you would want to add \n To Search type '/search?=' then what you want to search");
        }
        else if(url.getPath().contains("/add"))
        {
            String[] parameters = url.getQuery().split("=");
            words.add(parameters[1]);
            return String.format("Documented!");
        }
        else if(url.getPath().contains("/search"))
        {
            String s= "";
            String[] parameters = url.getQuery().split("=");
            for(int x = 0;x < words.size(); x++)
            {
                if(words.get(x).contains(parameters[1]))
                {
                    s += words.get(x) + "\n";
                }
            }
            if(s.equals(""))
            {
                return String.format("We have found nothing");
            }
            else
            {
            return String.format("We found these: %s", s);
            }
        } 
        else
        return "404 Not Found!";
      }
     }
    


class SearchEngine {
        public static void main(String[] args) throws IOException {
            if(args.length == 0){
                System.out.println("Missing port number! Try any number between 1024 to 49151");
                return;
            }
    
            int port = Integer.parseInt(args[0]);
    
            Server.start(port, new Handler());
        }
    }


Above is the code to the search Engine I created last week