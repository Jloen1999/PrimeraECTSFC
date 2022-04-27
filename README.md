# PRIMER ECTS DE FUNDAMENTOS DE COMPUTADORES 💻

[![BashLinux](https://img.shields.io/badge/gnu%20bash-%234EAA25.svg?&style=for-the-badge&logo=gnu%20bash&logoColor=white)](#ComparativaBash)
[![PowerShell](https://img.shields.io/badge/powershell-%235391FE.svg?&style=for-the-badge&logo=powershell&logoColor=white)](#PowerShell)
[![GitHub](https://img.shields.io/badge/github-%23181717.svg?&style=for-the-badge&logo=github&logoColor=white)](#Github)
[![git](https://img.shields.io/badge/git-%23F05032.svg?&style=for-the-badge&logo=git&logoColor=white)](#Github)

![Nombre](https://img.shields.io/badge/Nombre:-Jose%20Luis%20Obiang%20Ela%20Nanguan-orange) <br>
![Profesor](https://img.shields.io/badge/Profesor:-Francisco%20Fernandez%20de%20Vega-orange) <br>
![Fecha](https://img.shields.io/badge/Fecha-27%2F04%2F2022-orange)

<h2>PowerShell VS Bash Linux y la importancia de Github y Git</h2>

<ol>
<li><a href="#PowerShell"><strong>PowerShell</strong></a></li>
<li><a href="#ComparativaBash"><strong>Comandos PowerShell vs Bash Linux</strong></a></li>
<li><a href="#Github"><strong>Git en Github</strong></a></li>
</ol>

```mermaid
flowchart LR
A[PowerShell]-->|Comparativa| B(Bash Scripting)
B --> C{Git}
C -->D[Github]
```

<h3 style="color:magenta"><u>PowerShell</u></h3>

1. <a href="#Introducción">___Introducción___</a>
2. <a href="#Comandos">___La línea de comandos___</a>
3. <a href="#Significado">___¿Qué es PowerShell?___</a>
4. <a href="#Consola">___Abrir la consola de PowerShell___</a>
5. <a href="#Ayuda">___La ayuda en PowerShell___</a>
6. <a href="#Archivos">___Gestión de archivos y carpetas___</a>
7. <a href="#Tuberias">___Tuberías y redireccionamiento___</a>
8. <a href="#Scripts">___Iniciación a los scripts___</a>
9. <a href="#F1">___Fundamentos de scripts-I: Variables___</a>
10. <a href="F2">___Fundamentos de scripts-II: Estructuras de control y funciones___</a>


```mermaid
flowchart LR
A[Introduccion]-->B(linea de comandos)
B --> C{Que es PowerShell?}
C -->D[la consola de PowerShell]
D -->E[La ayuda en PowerShell]
E -->F[Gestion de archivos y carpetas]
F -->G[Tuberias y redireccionamiento]
G -->H[Iniciacion a los scripts]
H -->I[Fundamentos de scripts-I: Variables]
I -->J[Fundamentos de scripts-II: Estructuras de control y funciones]
```


<p style="color:green" id="Introducción"><strong style="font-size: 18px">Introducción</strong>

> La interfaz de usuario es el medio que utilizamos para comunicarnos con el ordenador.

> Interfaz gráfica: GUI(Proporciona un entorno visual)

> Interfaz de línea de comandos:CLI(Command Line Interface, nos permite dar instrucciones por medio de una línea de texto)

**¿Cuál de las dos debemos utilizar?**

> La respuesta es fácil, depende de lo que queramos hacer, si quieres navegar, trabajar con un procesador de texto, hoja de cálculo, retocar fotografía, etc, tu respuesta es la interfaz gráfica.
> Y si lo que quieres es automatizar tareas, crear usuarios de forma masiva, comprobar conectividad con servidores pues la respuesta es PowerShell(La linea de comandos)

</p>   
<p style="color:green" id="Comandos"><strong style="font-size: 18px">La línea de comandos</strong>

Vamos a ver ahora cómo ha evolucionado la línea de comandos de Windows

___CMD o símbolo del sistema:___

Todavía convive con nosotros pero cada vez se utiliza menos, tal vez para hacer un ping o ipconfig
```cmd
ping 8.8.8.8 (Para comprobar si nuestra PC tiene conexión a Internet)
```
![img.png](img.png)

```cmd
ipconfig (Para ver los adaptadores de red de la PC)
```
![img_1.png](img_1.png)

___PowerShell___

En cambio la PowerShell se pensó como una herramienta de reemplazo del CMD y con el tiempo se ha convertido en una herramienta poderosa de gestión tanto para usuarios domésticos como administradores

</p>
<p style="color:green" id="Significado"><strong style="font-size: 18px">¿Qué es PowerShell?</strong>



</p>

<p id="PowerShell">La PowerShell es una nueva línea de comandos, es decir, es una herramienta multiplataforma utilizada principalmente por los administradores de Sistemas Windows para automatizar tareas y tener un mayor control del sistema.
Esta herramienta está formada por una shell de comandos, un lenguaje de scripting y un marco de administración de configuración.
Trabaja con objetos, acepta y devuelve objetos en vez de texto como ocurre con el CMD 

***¿Dónde podemos encontrar PowerShell?*** En Windows 10 la encontramos, Windows Server, Microsoft Azure, SQL Server, Sercivios de Office 365, se encuentra prácticamente en todos los productos de Microsoft

<table>
    <thead>
        <tr>
           <th colspan="2">Versiones</th>   
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>Versión</th>
            <th>año</th>
        </tr>
        <tr>
            <th>V1</th>
            <th>2006</th>
        </tr>
        <tr>
            <th>V2</th>
            <th>2009</th>
        </tr>
        <tr>
            <th>V3</th>
            <th>2012</th>
        </tr>
        <tr>
            <th>V4</th>
            <th>2013</th>
        </tr>
        <tr>
            <th>V5</th>
            <th>2016</th>
        </tr>
        <tr>
            <th>V5.1</th>
            <th>2017</th>
        </tr>
        <tr>
            <th>V Core 6.0</th>
            <th>2018</th>
        </tr>
    </tbody>
</table>

No tenemos que confundir:
* Windows PowerShell ISE, es un entorno en el que podemos ejecutar comandos, escribir, probar y depurar script.
* Windows PowerShell es la consola de comandos.

***¿Qué requisitos se necesitan para aprender dicha herramienta?***
Como se trata de un curso a nivel de iniciación en PowerShell, cualquier persona con conocimientos de informática a nivel de usuario podría hacerlo sin mayor problema, ahora bien hay una parte en la que se habla de variables y estructuras condicionales y entonces aquí si se requiere conocimientos mínimos de programación

***¿Qué máquina necesitamos para trabajar en PowerShell?***
Es suficiente con tener un Windows 10 instalado o bien un Windows Server
¿Qué contenidos vamos a ver?

**Vamos a ver:**

<p style="color:green" id="Consola"><strong>Abrir la consola de PowerShell</strong></p>
Hay varias maneras de abrir la consola de comandos en Windows:

* Dando click derecho sobre el símbolo de Windows y pinchamos donde aparece PowerShell
* Pulsando Windows+R y escribimos `PowerShell`

Podemos ver la versión que tiene nuestro PowerShell con el comando `get-host`
![img_2.png](img_2.png)


> Este curso está planteado en lo más práctico posible. Las Prácticas que vamos a realizar son las siguientes:
>
>> ___En el primer momento empezaremos a trabajar con la PowerShell y la PowerShell ISE(que es el entorn)___
>>
>
>> ___Vamos a buscar Información___
>>
>
>> ___Vamos a utilizar los comandos básicos relacionados con la gestión de archivos y carpetas___
>>
>
>> ___Vamos a enlazar la salida de un comando con la entrada de otro y redireccionar la salida___
>>
>
>> ___Y Vamos a realizar pequeños scripts y hablando de Scrips, vamos a hacer un script en el que combinaremos esctructuras condicionales, repetitivas y redireccionamiento.___
>>

***¿Qué vamos a conseguir al finalizar este curso?***

Pues vamos a:

<table>
<tr>
<th><strong>A manejar tanto la PowerShell como la PowerShell ISE con soltura.</strong></th>
<th><strong>Buscar información en la ayuda de PowerShell.</strong></th>
<th><strong>Conocer los comandos básicos.</strong></th>
<th><strong>Ser capaces de realizar scripts para automatizar determinadas tareas.</strong></th>
</tr>
</table>

<h3 style="color:magenta">PowerShell vs Bash Linux</h3>
<p id="ComparativaBash">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid dolores incidunt placeat tempore. Aliquid aspernatur commodi dicta earum facilis minima nam, neque obcaecati provident quisquam unde vero! Atque aut distinctio ducimus exercitationem fuga illo odio praesentium quaerat quasi tempore. Ab, beatae blanditiis, consectetur consequatur dignissimos eaque error eum fugiat harum nulla quam quisquam quod, sunt vitae?</p>
<h3 style="color:magenta">Git en Github</h3>

```mermaid
flowchart LR;
B["fa:fa-twitter PC"]
    B-->C[fa:fa-ban PowerShell]
    B-->D(fa:fa-spinner Bash Script);
    B-->E(fa:fa-camera-retro Otro lenguaje)
    C-->F(fa:fa-camera-retro Fichero)
    D-->F(fa:fa-camera-retro Fichero)
    E-->F(fa:fa-camera-retro Fichero)
    F-->G(fa:fa-spinner Git)
    G-->H(fa:fa-spinner Github)
```

<p id="Github">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eaque esse harum modi omnis veritatis. Accusantium, architecto, aspernatur assumenda blanditiis commodi cum cumque cupiditate dignissimos dolore enim facere fugit harum incidunt maiores maxime minima modi natus nostrum nulla numquam, quasi ratione repellat sint totam velit voluptas voluptate voluptates! Ab asperiores at cupiditate dicta dolore dolorem dolores dolorum ea, eaque earum, error est hic, illum ipsa magni maxime minus nesciunt nostrum odit officia quae quam quas quidem quis quo reprehenderit tempora tempore. Animi corporis ea eligendi hic mollitia, nulla!</p>
