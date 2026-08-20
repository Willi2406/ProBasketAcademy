🏀 ProBasket Academy

Aplicación móvil Android desarrollada para gestionar integralmente una academia de baloncesto, centralizando y automatizando las operaciones diarias. Separa de forma lógica el rendimiento deportivo de la administración financiera, manteniendo ambas áreas conectadas en una sola herramienta.

El proyecto está desarrollado utilizando Kotlin y Jetpack Compose, aplicando una arquitectura organizada por capas (Clean Architecture + MVVM) para separar la interfaz, la lógica de negocio y el acceso a datos.

🧐 Integrantes
 * William Alexander Rodríguez Valentín
 * Blayverth Reyes

🎞️ Video Promocional
(https://youtube.com/shorts/DkfQpc6ssvQ?si=AUiAAhgOkyDdDtLT)

📱 Funcionalidades
👤 Administrador / Entrenador
 * Inicio de sesión seguro mediante cuenta de Google (Credential Manager).
 * Dashboard principal con indicadores clave (jugadores activos, asistencia promedio, ingresos totales).
 * Alertas automáticas de cobros pendientes o urgentes.
 * Gestión del directorio de jugadores (creación, edición, búsqueda y asignación).
 * Registro de datos deportivos, medidas físicas y carga de documentos (Acta de nacimiento).
 * Gestión y creación de categorías o equipos (ej. U-18, U-20).
 * Asignación masiva de jugadores a categorías.
 * Calendario interactivo para la programación de eventos (partidos, entrenamientos, reuniones).
 * Control de asistencia automatizado por equipo y fecha, con historial auditable.
 * Módulo financiero completo (Estado de cuenta por jugador).
 * Gestión de suscripciones (mensuales o semanales).
 * Registro de pagos totales, abonos parciales y liquidación de deudas.
 * Perfil global de usuario.

🛠️ Tecnologías
 * Kotlin
 * Jetpack Compose
 * Material 3
 * Navigation Compose / Navigation 3
 * Room Database (SQLite)
 * Dagger Hilt
 * Kotlin Coroutines & Flows
 * Firebase Authentication
 * Google Sign-In / Credential Manager
 * Coil (Carga asíncrona de imágenes)

🏗️ Arquitectura
El proyecto mantiene separadas las diferentes responsabilidades de la aplicación, garantizando rendimiento, escalabilidad y facilidad de mantenimiento.
app/
└── src/main/java/com/probasketacademy/
    ├── data/
    │   ├── database/
    │   ├── local/ (DAOs y Entidades)
    │   ├── mapper/
    │   └── repository/
    │
    ├── domain/
    │   ├── model/
    │   ├── repository/
    │   └── usecase/
    │
    ├── di/ (Inyección de dependencias)
    │
    └── presentacion/
        ├── auth/
        ├── home/
        ├── jugadores/
        ├── categorias/
        ├── eventos/
        ├── asistencias/
        ├── pagos/
        ├── perfil/
        └── navegacion/

Esta organización permite mantener la lógica de negocio separada de la interfaz y facilita las pruebas y futuras ampliaciones del proyecto.

🧭 Flujo principal de la aplicación
       Auth (Login con Google)
                 ↓
          Panel de Control
                 ↓
  ┌──────────────┼──────────────┐
  ↓              ↓              ↓
Jugadores    Categorías     Calendario
  ↓              ↓              ↓
Ficha/Docs   Asignación     Eventos
                 ↓
          ┌──────┴──────┐
          ↓             ↓
     Asistencia      Finanzas
          ↓             ↓
    Pase de lista    Abonos/Pagos


✅ Control de Asistencia
La aplicación posee un módulo para automatizar el pase de lista diario. Permite al administrador seleccionar una fecha y una categoría específica para cargar el roster del equipo. Incluye un modo interactivo para el día actual y un modo de solo lectura para auditar el historial de días pasados.

💳 Finanzas y Pagos
La aplicación incorpora la interfaz y la lógica contable necesaria para mantener las finanzas al día, separando los datos económicos de la ficha deportiva. Permite configurar planes de pago (semanal/mensual), registrar cobros exactos, aceptar abonos parciales (calculando la deuda restante automáticamente) y saldar deudas antiguas con un solo botón.

📅 Calendario y Eventos
Un planificador visual integrado que permite visualizar la carga de trabajo mensual. El administrador puede registrar la duración, ubicación, tipo de evento (partido, entrenamiento) y hora exacta, mostrando indicadores visuales en los días con actividad programada.

📋 Gestión de Jugadores
Funciona como un CRM deportivo. Cada jugador tiene un perfil detallado que almacena su biometría, categoría asignada, contacto de emergencia del tutor legal y evidencias documentales, permitiendo cargar y recortar fotografías directamente desde el dispositivo.

🚀 Instalación
Requisitos
 * Android Studio.
 * JDK compatible con el proyecto.
 * Dispositivo Android o emulador.
 * Configuración del archivo google-services.json y claves SHA-1 para Firebase Authentication.
Clonar el repositorio
git clone https://github.com/tu-usuario/ProBasketAcademy.git

Luego:
cd ProBasketAcademy

Abre el proyecto utilizando Android Studio, espera la sincronización de Gradle, compila y ejecuta la aplicación utilizando un dispositivo físico o un emulador.

🎯 Objetivo
Desarrollar una aplicación móvil moderna que centralice todas las operaciones de una academia de baloncesto. Proporcionar a los entrenadores y administradores herramientas eficientes para gestionar rosters, evaluar la asistencia, organizar eventos y llevar un control financiero estricto y transparente desde una sola plataforma.

📌 Estado del proyecto
El proyecto cuenta con los principales flujos administrativos completamente funcionales:
 * Autenticación con Google.
 * Dashboard en tiempo real.
 * Directorio y ficha de jugadores.
 * Carga de documentos e imágenes.
 * Gestión de categorías y asignación de equipos.
 * Agenda de eventos y calendario interactivo.
 * Registro de asistencias y cálculo de promedios.
 * Sistema contable de cobros, abonos y deudas.
 * Perfil de usuario.

🎓 Proyecto académico
Proyecto Android desarrollado para la carrera de Ingeniería en Sistemas en la Universidad Católica Nordestana (UCNE), utilizando principios de Clean Architecture, separación de responsabilidades, manejo de estado mediante ViewModels, persistencia local con Room y una interfaz completamente declarativa construida con Jetpack Compose.

ProBasket Academy 🏀
