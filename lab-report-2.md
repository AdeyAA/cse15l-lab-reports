`Part 1`

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    StringBuilder chatMessages = new StringBuilder();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String queryString = url.getQuery();
            if (queryString != null) {
                String[] chatInfo = queryString.split("&");
                String message = null;
                String user = null;

                for (String info : chatInfo) {
                    String[] keyValue = info.split("=");
                    if (keyValue.length == 2) {
                        if (keyValue[0].equals("s")) {
                            message = keyValue[1];
                        } else if (keyValue[0].equals("user")) {
                            user = keyValue[1];
                        }
                    }
                }

                if (message != null && user != null) {
                    String chatMessage = String.format("%s: %s\n", user, message);
                    chatMessages.append(chatMessage);
                    return chatMessages.toString();
                } else {
                    return "Invalid input for /add-message!";
                }
            } else {
                return "Missing input for /add-message!";
            }
        } else {
           
            return chatMessages.toString();
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
}
```
