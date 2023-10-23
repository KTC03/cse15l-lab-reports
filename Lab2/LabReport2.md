# Lab 2 : Servers and SSH Keys

### Code for StringServer.java

```
import java.io.IOException;
import java.net.URI;
import java.net.URLDecoder;
import java.nio.charset.StandardCharsets;

class StringHandler implements URLHandler {
    private StringBuilder messageBuffer = new StringBuilder();
    private int messageCounter = 0;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String query = url.getQuery();
            if (query != null) {
                String[] params = query.split("=");
                if (params.length == 2 && params[0].equals("s")) {
                    try {
                        String decodedMessage = URLDecoder.decode(params[1], StandardCharsets.UTF_8.toString());
                        messageCounter++;
                        messageBuffer.append(messageCounter).append(". ").append(decodedMessage).append("\n");
                        return messageBuffer.toString();
                    } catch (IOException e) {
                        e.printStackTrace();
                    }
                }
            }
        }
        return "Invalid request! Use /add-message?s=<message>";
    }
}

public class StringServer {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new StringHandler());
    }
}
```
### Using /add-message 
1. First message: "Hello!"

!Image[message1.png]


