<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script type="text/javascript">
        var a = "Yo soy";
        let b = "Tu padre";
        document.write("Constante a contiene  "+ a );
        document.write("</br>");
        document.write("Variable b contiene  "+ b);
        document.write("</br>");
        document.write(a + "  "+ b);

    </script>
    <p>El signo "+" sirve para concatenar cades de texto</p>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h2>Objets JavaScript </h2>

    <p>Hay dos formas diferentes de acceder a ua propidedad de objeto.</p>

    <p>Puede usar person.propiedad o person["propiedad"]</p>

    <p id="demo"></p>

    <script>
        //Crear objeto
        const person= {
            fristName: "Alexis",
            lastName: "Rios",
            id : 1234
        };
        // Mostrar informacion del objeto

        document.getElementById("demo").innerHTML = person.fristName + "  " + person.lastName;
    </script>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <button onclick="document.getElementById('demo').innerHTML=Date()">La hora es? </button>

    <p id="demo"></p>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>JavaScript Funciones</h1>

    <p>Llame a una funcion que realiza un calculo y devuelve el resultado</p>

    <p id="demo"></p>

    <script>
        function myFuntion(p1,p2){
            return p1*p2;
        }
        let result = myFuntion(4,3);
        document.getElementById("demo").innerHTML = result;
    </script>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Funciones en Pantalla</title>
</head>
<body>
    <h2>Funciones en Pantalla</h2>

    <p>Resultado de la primera función:</p>
    <p id="resultado1"></p>

    <p>Resultado de la segunda función:</p>
    <p id="resultado2"></p>

    <script>
        const funcion1 = function(a, b) {
            let chuck = 42;
            return a + b + chuck;
        };

        const funcion2 = (a, b) => {
            let chuck = 42;
            return a + b + chuck;
        };

        const resultado1 = funcion1(5, 7);
        const resultado2 = funcion2(10, 20);

        document.getElementById("resultado1").textContent = `Resultado 1: ${resultado1}`;
        document.getElementById("resultado2").textContent = `Resultado 2: ${resultado2}`;
    </script>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>setTimeout Anidado</title>
</head>
<body>
    <h2>setTimeout Anidado con Función Callback</h2>

    <p id="output"></p>

    <script>
        const outputElement = document.getElementById('output');

        setTimeout(function() {
            outputElement.textContent = 'Primera función';
            setTimeout(function() {
                outputElement.textContent += '\nSegunda función';
            }, 1000); // Después de 1 segundo
        }, 2000); // Después de 2 segundos
    </script>
</body>
</html>



<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <h2>Formulario Punto #4 </h2>

    <form id="producto-form">
        <label for="codigo">Código:</label>
        <input type="text" id="codigo"><br><br>

        <label for="descripcion">Descripción:</label>
        <input type="text" id="descripcion""><br><br>

        <label for=" precio">Precio:</label>
        <input type="number" id="precio"><br><br>

        <label for="cantidad">Cantidad:</label>
        <input type="number" id="cantidad"><br><br>

        <label for="lote">Lote:</label>
        <input type="text" id="lote"><br><br>

        <label for="stockMin">Stock Mínimo:</label>
        <input type="number" id="stockMin"><br><br>

        <label for="stockMax">Stock Máximo:</label>
        <input type="number" id="stockMax"><br><br>
    </form>

    <script>
        const producto = {
            codigo: "1234",
            descripcion: "CocaCola 1.5",
            precio: "4.500",
            cantidad: "20",
            lote: "13/09/2022",
            stockMin: "30",
            stockMax: "100"
        };

        for (const prop in producto) {
            if (producto.hasOwnProperty(prop)) {
                document.getElementById(prop).value = producto[prop];
            }
        }
    </script>
</body>

</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplos de Eventos</title>
</head>
<body>
    <!-- Ejemplo 1: Click (clic) -->
    <button id="myButton">Haz clic</button>
    <br>

    <!-- Ejemplo 2: Mouseover (pasar el mouse por encima) -->
    <div id="myDiv">Pasa el mouse aquí</div>
    <br>

    <!-- Ejemplo 3: Keydown (tecla presionada) -->
    <input type="text" id="myInput" placeholder="Presiona una tecla">
    <br>

    <!-- Ejemplo 4: Submit (enviar) -->
    <form id="myForm">
        <input type="text" name="username" placeholder="Usuario">
        <input type="password" name="password" placeholder="Contraseña">
        <button type="submit">Iniciar sesión</button>
    </form>
    <br>

    <!-- Ejemplo 5: Load (carga) -->
    <img id="myImage" src="https://desarrolloweb.com/media/272/eventos-en-javascript.jpg" alt="Imagen">

    <script>
        // Ejemplo 1: Click (clic)
        document.getElementById("myButton").addEventListener("click", function() {
            alert("¡Hiciste clic en el botón!");
        });

        // Ejemplo 2: Mouseover (pasar el mouse por encima)
        document.getElementById("myDiv").addEventListener("mouseover", function() {
            this.style.backgroundColor = "lightblue";
        });

        // Ejemplo 3: Keydown (tecla presionada)
        document.getElementById("myInput").addEventListener("keydown", function(event) {
            console.log("Tecla presionada:", event.key);
        });

        // Ejemplo 4: Submit (enviar)
        document.getElementById("myForm").addEventListener("submit", function(event) {
            event.preventDefault(); // Evita el envío del formulario por defecto
            alert("Formulario enviado");
        });

        // Ejemplo 5: Load (carga)
        document.getElementById("myImage").addEventListener("load", function() {
            console.log("La imagen se ha cargado");
        });
    </script>
</body>
</html>



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Descuentos</title>
</head>
<body>
    <h2>Calculadora de Descuentos</h2>

    <p>Ingrese el precio, la cantidad y el porcentaje de descuento:</p>

    <label for="precio">Precio:</label>
    <input type="number" id="precio" value="100"><br><br>

    <label for="cantidad">Cantidad:</label>
    <input type="number" id="cantidad" value="5"><br><br>

    <label for="descuento">Porcentaje de Descuento:</label>
    <input type="number" id="descuento" value="10"><br><br>

    <button id="calcularBtn">Calcular</button>

    <p id="resultado"></p>

    <script>
        function calcularDescuento(precio, cantidad, porcentajeDescuento) {
            const descuento = (precio * porcentajeDescuento) / 100;
            const totalPagar = (precio - descuento) * cantidad;
            return totalPagar;
        }

        const calcularBtn = document.getElementById("calcularBtn");
        calcularBtn.addEventListener("click", function() {
            const precio = parseFloat(document.getElementById("precio").value);
            const cantidad = parseFloat(document.getElementById("cantidad").value);
            const porcentajeDescuento = parseFloat(document.getElementById("descuento").value);

            const totalAPagar = calcularDescuento(precio, cantidad, porcentajeDescuento);
            document.getElementById("resultado").textContent = `Total a pagar: ${totalAPagar}`;
        });
    </script>
</body>
</html>



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Promesa con Condicional</title>
</head>
<body>
    <h2>Promesa con Condicional</h2>

    <p id="output">Esperando el resultado...</p>

    <script>
        const randomNumber = Math.random();
        
        const promise = new Promise((resolve, reject) => {
            if (randomNumber > 0.5) {
                resolve("¡Número mayor que 0.5!");
            } else {
                reject("¡Número menor que 0.5!");
            }
        });
        
        promise.then(result => {
            document.getElementById("output").textContent = result;
        }).catch(error => {
            document.getElementById("output").textContent = error;
        });
    </script>
</body>
</html>


<!-- Su documentación aquí -->






