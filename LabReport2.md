# **Lab Report 2**
## Part 1
Here is the code for my Chat Server:

`import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    
    String s = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return s;
        /*} else if (url.getPath().equals("/increment")) {
            num += 1;
            return String.format("Number incremented!");*/
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("&");
                String[] sParameters = parameters[0].split("=");
                String[] userParameters = parameters[1].split("=");
                if (userParameters[0].equals("user")) {
                    s = s + userParameters[1] + ": ";
                }
                if(sParameters[0].equals("s")){
                    s = s + sParameters[1] + "\n";
                }
                return s;
            }
            return "404 Not Found!";
        }
    }
}

class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}`
And here are some of examples of outputs using `/add-message`:

