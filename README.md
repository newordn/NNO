# NNO
My collection of snippets and courses in any languages
Just boilerplate scripts and courses, that i used to use every day. :smile: 

***
# JAVA 10,11 SYNTAX
the var keyword to infere type,
## Making a http request with Java
Synchronous way
var request = HttpRequest.newBuilder()
    .uri(URI.create("https://winterbe.com"))
    .GET()
    .build();
var client = HttpClient.newHttpClient();
HttpResponse<String> response = client.send(request, HttpResponse.BodyHandlers.ofString());
System.out.println(response.body())
Asynchronous way 
var request = HttpRequest.newBuilder()
    .uri(URI.create("https://winterbe.com"))
    .build();
var client = HttpClient.newHttpClient();
client.sendAsync(request, HttpResponse.BodyHandlers.ofString())
    .thenApply(HttpResponse::body)
    .thenAccept(System.out::println);
