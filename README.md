# Fire Food — Aplicación Android para Gestión de Comidas Rápidas

**Fire Food** es una **aplicación móvil Android** desarrollada en **Java**, orientada a la **visualización y gestión de productos, servicios y sucursales** de un negocio de comida rápida.

La aplicación implementa una **arquitectura por capas**, utiliza **SQLite** para persistencia local y presenta una interfaz gráfica intuitiva basada en **Activities, Fragments y Adapters**.  
El proyecto fue desarrollado con **fines académicos**, como parte de un reto o proyecto universitario.

---

## Características principales

- Pantalla de **Splash Screen**
- Menú principal con navegación por secciones
- Gestión de:
  - Productos
  - Servicios
  - Sucursales
- Persistencia de datos local con **SQLite**
- Uso de **Adapters personalizados** para listas y grillas
- Separación por capas:
  - Presentación
  - Modelo
  - Datos
  - Casos de uso
- Interfaz gráfica con **XML**
- Aplicación compilable como **APK**

---

## Arquitectura del sistema

Splash Screen  
↓  
MainActivity  
↓  
Menú Principal  
↓  
Fragments (Servicios / Sucursales)  
↓  
Adapters personalizados  
↓  
Modelos de datos  
↓  
SQLite (DBHelper)  

---

## Tecnologías utilizadas

- **Java**
- **Android Studio**
- **Android SDK**
- **SQLite**
- **Gradle**
- **XML (UI)**
- **RecyclerView / GridView**
- **Adapters personalizados**

---

## Estructura del proyecto

```

Fire-food-main
│
├── app/
│ ├── src/
│ │ ├── main/
│ │ │ ├── java/com/example/reto_3/
│ │ │ │ ├── adaptadores/
│ │ │ │ │ ├── ProductoAdapter.java
│ │ │ │ │ ├── ServicioAdapter.java
│ │ │ │ │ └── SucursalAdapter.java
│ │ │ │ │
│ │ │ │ ├── casos_uso/
│ │ │ │ │ └── CasoUsoProducto.java
│ │ │ │ │
│ │ │ │ ├── datos/
│ │ │ │ │ └── DBHelper.java
│ │ │ │ │
│ │ │ │ ├── modelo/
│ │ │ │ │ ├── Productos.java
│ │ │ │ │ ├── Servicios.java
│ │ │ │ │ └── Sucursales.java
│ │ │ │ │
│ │ │ │ └── presentacion/
│ │ │ │ ├── MainActivity.java
│ │ │ │ ├── SplashScreen.java
│ │ │ │ ├── Main_menu.java
│ │ │ │ ├── FormActivity.java
│ │ │ │ ├── Form_menu.java
│ │ │ │ ├── Servicios.java
│ │ │ │ └── Sucursales.java
│ │ │ │
│ │ │ ├── res/
│ │ │ │ ├── layout/
│ │ │ │ ├── drawable/
│ │ │ │ ├── menu/
│ │ │ │ └── values/
│ │ │ │
│ │ │ └── AndroidManifest.xml
│ │ │
│ │ └── test/
│ │
├── gradle/
├── build.gradle
├── settings.gradle
├── gradlew
├── app-debug.apk
└── README.md

```


---

## Descripción de los componentes

### Capa de Presentación (`presentacion`)

Contiene las **Activities y Fragments** encargados de la interacción con el usuario.

- `SplashScreen.java`: Pantalla inicial de carga
- `MainActivity.java`: Actividad principal
- `Main_menu.java`: Menú de navegación
- `Servicios.java`: Fragment para mostrar servicios
- `Sucursales.java`: Fragment para mostrar sucursales
- `FormActivity.java`: Formularios de ingreso de información

---

### Capa de Modelo (`modelo`)

Define las **entidades del sistema**.

- `Productos.java`
- `Servicios.java`
- `Sucursales.java`

Cada clase encapsula atributos y métodos relacionados con su entidad.

---

### Capa de Datos (`datos`)

- `DBHelper.java`  
  Clase encargada de:
  - Crear la base de datos SQLite
  - Definir tablas
  - Insertar y consultar datos
  - Administrar la persistencia local

---

### Capa de Casos de Uso (`casos_uso`)

- `CasoUsoProducto.java`  
  Implementa la lógica de negocio asociada a los productos, actuando como intermediario entre la UI y la base de datos.

---

### Adaptadores (`adaptadores`)

Adapters personalizados para mostrar datos en listas o grillas:

- `ProductoAdapter.java`
- `ServicioAdapter.java`
- `SucursalAdapter.java`

---

## Ejecución del proyecto

```bash
# 1. Abrir Android Studio
# 2. Seleccionar "Open an existing project"
# 3. Abrir la carpeta Fire-food-main
# 4. Esperar sincronización de Gradle
# 5. Ejecutar en emulador o dispositivo físico


o instalar el apk:

app-debug.apk

para Android 12
