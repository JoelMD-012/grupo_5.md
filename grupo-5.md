
# Proyecto Socioformativo: Réplica de la Página Web de BOA

- **Nombre**: [Luis adolfo leon mendiola](https://www.facebook.com/share/19kpKHDiD5/?mibextid=wwXIfr)
- **Nombre**: [Joel fransisco miranda domingues](https://www.facebook.com/share/15FzGkXBQ2/)
- **Nombre**: [Luis fernando cesari chuve](https://www.facebook.com/luisfernando.cesarichuve)
- **Nombre**: [Obeth flores choque](https://www.facebook.com/)

- **Universidad**: Universidad Privada Domingo Savio
- **Carrera**: Ingeniería de Sistemas



## 📌 Introducción
Este proyecto tiene como objetivo replicar la funcionalidad básica de la página web de **Boliviana de Aviación (BOA)**, específicamente en lo que respecta al proceso de **solicitud de vuelos** y la **generación de un comprobante de reserva**. Utilizando tecnologías modernas, como **Blazor** para la interfaz web y **Supabase** como base de datos en tiempo real, este sistema permite a los usuarios seleccionar un vuelo, ingresar los datos del pasajero, confirmar la reserva y generar un comprobante descargable o imprimible.

## 🎯 Objetivo

### Objetivo General
Capacitar a los estudiantes en la implementación de un sistema de solicitud y recepción de vuelos, replicando las funcionalidades principales de la página web de BOA. El proyecto tiene como fin desarrollar competencias en el diseño de interfaces dinámicas, manejo de datos y generación de recibos.

### Objetivos Específicos
- Implementar un sistema de **solicitud de vuelos** con opciones de vuelo de ida o ida y vuelta.
- Permitir a los usuarios ingresar los **datos del pasajero** y confirmar la reserva.
- Integrar **Supabase** para gestionar las bases de datos en tiempo real, almacenando los vuelos, pasajeros y reservas.
- Crear una **interfaz de usuario** intuitiva y moderna utilizando **Blazor**.
- Generar un **comprobante de reserva** descargable o imprimible.

## 📚 Marco Teórico

### Blazor
**Blazor** es un framework web desarrollado por Microsoft que permite crear aplicaciones web interactivas utilizando **C#** en lugar de JavaScript. Existen dos versiones principales de Blazor:
- **Blazor WebAssembly**: Ejecuta el código C# en el navegador utilizando WebAssembly.
- **Blazor Server**: Ejecuta el código C# en el servidor, con la interfaz de usuario actualizándose en tiempo real a través de SignalR.

En este proyecto se utiliza **Blazor WebAssembly** para la construcción de una interfaz rica e interactiva que puede ejecutarse directamente en el navegador sin necesidad de un servidor intermedio.

### Supabase
**Supabase** es una plataforma de código abierto que proporciona una alternativa a Firebase, permitiendo crear aplicaciones con bases de datos en tiempo real, autenticación y almacenamiento de archivos. Utiliza **PostgreSQL** como base de datos subyacente y ofrece una API RESTful para interactuar con los datos, así como una integración en tiempo real mediante websockets.

En este proyecto, **Supabase** se utiliza para gestionar la base de datos que almacena los vuelos, pasajeros y reservas, permitiendo una integración en tiempo real y asegurando que la información se mantenga actualizada.

## Metodología

### Fase 1: Diseño de la Interfaz
Se diseñaron formularios interactivos utilizando **Blazor** para permitir la selección de vuelos y la captura de datos del pasajero. Estos formularios incluyen validaciones de entrada para asegurar que los datos sean correctos antes de la confirmación de la reserva.

### Fase 2: Desarrollo de la Base de Datos
Se configuró la base de datos en **Supabase**, creando las tablas necesarias para almacenar la información de los vuelos, los pasajeros y las reservas. Se configuraron relaciones entre las tablas y se habilitó la sincronización en tiempo real para reflejar cambios en la base de datos.

### Fase 3: Implementación de la Lógica de Reserva
Se implementaron las operaciones CRUD (Crear, Leer, Actualizar, Eliminar) en Blazor para interactuar con la base de datos en Supabase. La lógica de reserva asegura que, una vez confirmados los datos, la reserva se guarde y se genere un comprobante para el usuario.

### Fase 4: Generación de Comprobante
Se integró una funcionalidad para generar un **comprobante de reserva** en formato descargable o imprimible utilizando **jsPDF**, que permite crear un archivo PDF con los detalles de la reserva y los datos del pasajero.

### Fase 5: Pruebas y Optimización
Se realizaron pruebas exhaustivas en cada módulo del sistema para asegurar que funcionara correctamente. También se optimizaron las consultas a la base de datos para mejorar el rendimiento y la experiencia del usuario.

## Modelado

### Diagramas de Tablas

**Tabla Vuelos**
| Campo       | Tipo      | Descripción                          |
|-------------|-----------|--------------------------------------|
| id          | int       | Identificador único del vuelo        |
| origen      | text      | Ciudad de origen del vuelo           |
| destino     | text      | Ciudad de destino del vuelo          |
| fecha       | date      | Fecha del vuelo                      |
| hora        | time      | Hora del vuelo                       |
| precio      | decimal   | Precio del vuelo                     |

**Tabla Pasajeros**
| Campo       | Tipo      | Descripción                          |
|-------------|-----------|--------------------------------------|
| id          | int       | Identificador único del pasajero     |
| nombre      | text      | Nombre del pasajero                  |
| apellido    | text      | Apellido del pasajero                |
| documento   | text      | Documento de identidad del pasajero  |
| email       | text      | Correo electrónico del pasajero      |

**Tabla Reservas**
| Campo       | Tipo      | Descripción                          |
|-------------|-----------|--------------------------------------|
| id          | int       | Identificador único de la reserva    |
| id_pasajero | int       | Referencia al pasajero               |
| id_vuelo    | int       | Referencia al vuelo                  |
| monto_total | decimal   | Monto total de la reserva            |
| fecha_reserva | date    | Fecha en que se realizó la reserva   |

**Tabla Aviones**
| Campo       | Tipo      | Descripción                          |
|-------------|-----------|--------------------------------------|
| id          | int       | Identificador único de avion         |
| modelo      | text      | Modelo del avion                     |
| fabricante  | text      | Referencia del fabricante            |
| capacidad   | int       | Capacidad del avion                  |
| registro    | text      | Registro con el que esta en actividad|

**Tabla Empleados**
| Campo       | Tipo      | Descripción                          |
|-------------|-----------|--------------------------------------|
| id          | int       | Identificador único del Empleado     |
| nombre      | text      | Nombre del Empleado                  |
| apellido    | text      | Apellido del Empleado                |
| carga       | text      | Documento de identidad del Empleado  |
| fecha_ingreso| date     | Fecha de ingreso del pasajero        |
| Salario      | numerico | Salario del pasajero                 |



## 📊 Conclusiones

Este proyecto ha permitido obtener una visión completa sobre la integración de tecnologías modernas como **Blazor** y **Supabase** para el desarrollo de aplicaciones web. A través de este sistema, se ha logrado replicar de manera efectiva el proceso de solicitud y confirmación de vuelos, generando un comprobante descargable para los usuarios. Además, se ha optimizado la interacción con la base de datos mediante Supabase, garantizando una gestión eficiente de los datos en tiempo real.

## 📚 Bibliografía
- [Blazor Documentation](https://docs.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-5.0)
- [Supabase Documentation](https://supabase.io/docs)


- Código Fuente: [GitHub](https://github.com/JoelMD-012/grupo_5.md.git)
- Dataset: Disponible en el repositorio de GitHub.

## 📁 Anexos

### Capturas de Pantalla
- **Pantalla de Selección de Vuelo:**
  ![Selección de Vuelo](https://drive.google.com/file/d/1FlovtNUVm7kjKhrW4wPMlbsDf27cemHa/view?usp=sharing)

### Código Relevante

**Componente de Selección de Busqueda:**
```csharp
<div class="flight-search">
    <div class="tab">
        <div tabindex="0" class="@(selectedTab == 0 ? "selected" : "unselected") izquierda"
        @onclick="() => SelectTab(0)">
            <div class="iconTab0">
                <svg stroke="currentColor" fill="@(selectedTab == 0 ? "#FFCA38" : "#002F6E")" stroke-width="0" viewBox="0 0 24 24" class="h-6 w-6" height="2em" width="2em" xmlns="http://www.w3.org/2000/svg">
                    <path d="M14 8.94737L22 14V16L14 13.4737V18.8333L17 20.5V22L12.5 21L8 22V20.5L11 18.8333V13.4737L3 16V14L11 8.94737V3.5C11 2.67157 11.6716 2 12.5 2C13.3284 2 14 2.67157 14 3.5V8.94737Z">

                    </path>
                </svg>
            </div>
            <div class="iconTab0">
                <h3>Reserva</h3>
            </div>


        </div>
        <div tabindex="1" class="@(selectedTab == 1 ? "selected" : "unselected") derecha"
        @onclick="() => SelectTab(1)">
            <div class="iconTab1">
                <svg stroke="currentColor" fill="@(selectedTab == 1 ? "#FFCA38" : "#002F6E")" stroke-width="0" viewBox="0 0 24 24" class="h-6 w-6" height="2em" width="2em" xmlns="http://www.w3.org/2000/svg">
                    <path d="M21.0049 2.99979C21.5572 2.99979 22.0049 3.4475 22.0049 3.99979V9.49979C20.6242 9.49979 19.5049 10.6191 19.5049 11.9998C19.5049 13.3805 20.6242 14.4998 22.0049 14.4998V19.9998C22.0049 20.5521 21.5572 20.9998 21.0049 20.9998H3.00488C2.4526 20.9998 2.00488 20.5521 2.00488 19.9998V14.4998C3.38559 14.4998 4.50488 13.3805 4.50488 11.9998C4.50488 10.6191 3.38559 9.49979 2.00488 9.49979V3.99979C2.00488 3.4475 2.4526 2.99979 3.00488 2.99979H21.0049ZM20.0049 4.99979H4.00488V7.96779L4.16077 8.04886C5.49935 8.78084 6.42516 10.1733 6.49998 11.788L6.50488 11.9998C6.50488 13.704 5.55755 15.1869 4.16077 15.9507L4.00488 16.0308V18.9998H20.0049V16.0308L19.849 15.9507C18.5104 15.2187 17.5846 13.8263 17.5098 12.2116L17.5049 11.9998C17.5049 10.2956 18.4522 8.81266 19.849 8.04886L20.0049 7.96779V4.99979ZM16.0049 8.99979V14.9998H8.00488V8.99979H16.0049Z">
                    </path>
                </svg>
            </div>
            <div class="iconTab1">
                <h3>Iniciar Check-In</h3>
            </div>

        </div>
    </div>
    <div class="options">

        @if (selectedTab == 0)
        {
            <div class="round-trip">
                <button class="travel-button" style="background-color: @(button1Selected ? "rgb(255, 202, 56)" : "#F0F0F0");
                color: @(button1Selected ? "rgb(101 71 0)" : "#1F2937");"
                @onclick="() => changeButtonStyle(1)">
                    Ida y vuelta
                </button>
                <button class="travel-button" style="background-color: @(button2Selected ? "rgb(255, 202, 56)" : "#F0F0F0");
                color: @(button2Selected ? "rgb(101 71 0)" : "#1F2937");"
                @onclick="() => changeButtonStyle(2)">
                    Solo Ida
                </button>
            </div>
            <div class="other-options">

                <div class="option">
                    <div class="origen @(origenSelected ? "origenSelected" : "")">
                        <div class="input">
                            <input type="text" @bind="inputText1" @onblur="() => origen_blur()" placeholder="Origen" @onfocus="() => origen_focus()" />

                        </div>
                    </div>
                    <div>
                        <button class="interchange" @onclick="SwapTexts">
                            <svg stroke="rgb(255, 202, 56)" fill="rgb(255, 202, 56)" stroke-width="0" viewBox="0 0 512 512" class="w-6" height="2em" width="2em" xmlns="http://www.w3.org/2000/svg">
                                <path fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="46" d="m304 48 112 112-112 112m94.87-112H96m112 304L96 352l112-112m-94 112h302">

                                </path>
                            </svg>
                        </button>
                    </div>
                    <div class="destino @(destinoSelected ? "destinoSelected" : "")">
                        <div class="input">
                            <input placeholder="Destino" @bind="inputText2" @onfocus="() => destino_focus()" @onblur="() => destino_blur()" />
                        </div>
                    </div>
                </div>
                <div class="option">
                    <div class="salida">
                        <p>Salida</p>
                    </div>
                    @if (button1Selected == true)
                    {
                        <hr class="border-yellow" />
                        <div class="regreso">
                            <p>Regreso</p>
                        </div>
                    }

                </div>
                <div class="option">
                    <div class="pasajeros">
                        <p class="small-text">
                            Pasajeros
                        </p>
                        <p class="adulto">
                            1 Adulto
                        </p>
                    </div>

                </div>



            </div>
        }
        else
        {
            <div class="checkin">
                <button class="blue-button">Iniciar Check-In<img class="check" src="images/check.png" /></button>
            </div>
        }

    </div>
