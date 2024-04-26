En este apartado creare markdowns para completar el apartado 0 del curso de FullStack Open de la universidad de Helsinki, Finlandia.

# Diagrama de Secuencias
 ### ** Browser && Server**

```mermaid
graph TD;
    A[User] -->|Send Note| B(Server);
    B -->| POST Request| C(new_note);
    C -->|redirection| D(notes);
    D -->|Request GET| E(main.css);
    D -->|Request GET| F(main.js);
    D -->|Request GET| G(data.json);

```
