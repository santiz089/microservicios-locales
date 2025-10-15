# 🌐 Microservicios Locales

Proyecto desarrollado como práctica de servicios web en Node.js.  
Permite registrar, consultar y visualizar servicios locales en un mapa interactivo utilizando **SQLite**, **Express**, y la **API de geolocalización de OpenStreetMap (Nominatim)**.

---

## 🚀 Funcionalidad principal

- Registrar nuevos **servicios locales** (con dirección y descripción).  
- Obtener automáticamente las **coordenadas geográficas** de cada dirección.  
- Visualizar los servicios en un **mapa interactivo (Leaflet)**.  
- Enviar **solicitudes de usuarios** hacia los servicios registrados.  
- Mantener todos los datos en una base **SQLite** persistente.

---

## 🧩 Tecnologías utilizadas

- **Node.js** y **Express.js** → para el servidor y las rutas REST.
- **SQLite3** → como base de datos local.
- **Leaflet.js** → para mostrar los servicios en un mapa.
- **OpenStreetMap (API Nominatim)** → para convertir direcciones en coordenadas (geocodificación).
- **HTML, CSS, JavaScript (frontend)** → para la interfaz de usuario.

---

## ⚙️ Instalación y ejecución

1. Clona o descarga este repositorio.
2. Abre una terminal en la carpeta del proyecto.
3. Instala las dependencias:
   ```bash
   npm install
   ```
4. Inicia el servidor:
   ```bash
   node index.js
   ```
5. Abre en tu navegador:
   ```
   http://localhost:3000
   ```

---

## 📡 Endpoints principales (API REST)

| Método | Ruta | Descripción |
|--------|------|--------------|
| **GET** | `/servicios` | Devuelve todos los servicios registrados. |
| **POST** | `/servicios` | Crea un nuevo servicio (usa geocodificación). |
| **GET** | `/solicitudes` | Lista todas las solicitudes. |
| **POST** | `/solicitudes` | Crea una nueva solicitud de usuario. |

---

## 💾 Estructura de la base de datos

**Tabla `servicios`**
| Campo | Tipo | Descripción |
|--------|------|-------------|
| id | INTEGER | Identificador único |
| nombre | TEXT | Nombre del servicio |
| direccion | TEXT | Dirección completa |
| descripcion | TEXT | Descripción del servicio |
| lat | REAL | Latitud geográfica |
| lon | REAL | Longitud geográfica |

**Tabla `solicitudes`**
| Campo | Tipo | Descripción |
|--------|------|-------------|
| id | INTEGER | Identificador único |
| usuario | TEXT | Nombre del solicitante |
| servicio | TEXT | Nombre del servicio solicitado |

---

## ⚠️ Errores comunes

- **Error de permisos PowerShell:**  
  Ejecutar antes de usar npm:  
  ```bash
  Set-ExecutionPolicy RemoteSigned
  ```
- **Error en instalación:**  
  Asegúrate de tener instalado **Node.js v18+** y **npm** correctamente.

---

## 📄 Licencia

Este proyecto está licenciado bajo la **Licencia MIT**.  
Eres libre de usar, modificar y distribuir el código siempre que mantengas el aviso de derechos de autor.

---

## 👨‍💻 Autor

**Luis Santiz**  
Proyecto académico — *Servicios Web*  
Instituto Tecnológico de Iztapalapa  
2025
