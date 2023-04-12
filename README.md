### Hi there 👋

![Andreagriffiths11's GitHub stats](https://github-readme-stats.vercel.app/api?username=faustinoloeza&count_private=true&show_icons=true&theme=radical)

```mermaid
sequenceDiagram
    participant Cron
    participant System
    participant URL_PALACE
    participant Base_de_Datos

    Cron ->> System: Ejecuta el programa a las 9 AM
    System ->> URL_PALACE: Solicita la lista de identificadores
    URL_PALACE -->> System: Devuelve la lista de identificadores

    loop for each identificador
        System ->> Base_de_Datos: Verifica si el identificador existe
        Base_de_Datos -->> System: Devuelve el resultado de la verificación
        alt El identificador existe en la Base de Datos
            System ->> System: No hace nada
        else El identificador no existe en la Base de Datos
            System ->> URL_PALACE_DETALLE: Obtiene información del detalle del identificador
            URL_PALACE_DETALLE -->> System: Devuelve la información de detalle
            System ->> Base_de_Datos: Ingresa el identificador
            Base_de_Datos -->> System: Confirma la operación
        end
    end
    System -->> Cron: Finaliza la ejecución del programa



```
<!--
**faustinoloeza/faustinoloeza** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
