En este apartado creare markdowns para completar el apartado 0 del curso de FullStack Open de la universidad de Helsinki, Finlandia.

# Diagrama de Secuencias
 ### ** Browser && Server**
```mermaid
graph TD;
Browser-->Server;
```
> [!NOTE]
> When we load the page the browser send a request to the server, when the server read the request, send the information so we can see the webpage.

```mermaid
graph TD;
Browser(Using POST method)-->Server(https://studies.cs.helsinki.fi/exampleapp/new_note; 'Server verifies with a 302 status response that the information has been recieved');
```
> [!NOTE]
> We write in the form the text we want to send, then we click in the button SAVE. This triggers the new_note 302 Post Request, and it send to the server.


```mermaid
graph TD;
Browser(Send form creating 5 request to the server, first one send the form 'HTTP POST')-->Server(Responds with 'HTTP 302');
Server(Server send 'HTTP 302' it's an URL requesting the browser to refresh)-->Browser(Browser refresh and send a 'HTTP GET');
Browser(Browser sends 'HTTP GET' to server after refresh, triggering 3 requests)-->Server(Server recieve the request and send the data)
Server(send to browser notes, main.css and data.json)-->Browser(Refresh and create 3 request);
```
> [!NOTE]
> First the server recieve the data, from req.body then it creates a new note object and creates an array called 'notes'; inside the note object we find the data and date. Browser refresh and create 3 requests.  From the server we recieve [notes, main.css, data.json].
