# **Lab Report 2** <br />
Margaret Jones <br />
Monday 4PM - 6PM <br />

## **PART 1** 

## **StringServer Code** <br />
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String stringData = ""; //string to keep track of added messages
    Integer num = 1; //int to keep track of list numbering

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) { //case when no message is added
            return String.format("%s", stringData);
        } else if (url.getPath().contains("/add-message")) { 
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                String message = parameters[1]; //add users message to stringData
                stringData += String.format("%d. %s\n", num, message); 
                num += 1; 
                return stringData;
                }
            } return "404 Not Found!";
    }
}
class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
## **add-messages ex. 1**
![Image](addmessages(ex1).png)


# **Part2**
![Image](no_pass_serv.png)

# **Part3**
