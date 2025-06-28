# 📬 Formulario de Contacto - HTML + Docker + Nginx

Este proyecto es un formulario de contacto básico construido con **HTML, CSS y JavaScript**, y desplegado usando **Docker** con **Nginx** como servidor web. Es ideal para practicar despliegues de aplicaciones estáticas dentro de contenedores Docker.

---

## 🧾 Descripción

El formulario permite al usuario ingresar su **nombre**, **correo electrónico** y **mensaje**. Al enviarlo, se muestra una alerta de confirmación simulando el envío exitoso.

Este sitio estático es servido desde un contenedor Docker usando la imagen ligera `nginx:alpine`.

---

## 🛠️ Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript
- Docker
- Nginx (`nginx:alpine`)

---

## 📁 Estructura del Proyecto

```
📦 Formulario-contacto/
├── Dockerfile
├── index.html
├── style.css
└── script.js
```

---

## 🐳 Cómo ejecutar con Docker

> Asegúrate de tener Docker instalado en tu máquina.

### 1. Clona este repositorio

```bash
git clone https://github.com/BCProyect/ProyectoSO
cd tu-repo
```

### 2. Construye la imagen Docker

```bash
docker build -t formulario-contacto .
```

### 3. Ejecuta el contenedor

```bash
docker run -d -p 8080:80 --name contacto-app formulario-contacto
```

🔗 Abre tu navegador y ve a:  
[http://localhost:8080](http://localhost:8080)

---

## 🧱 Contenido del `Dockerfile`

```dockerfile
FROM nginx:alpine

RUN rm -rf /usr/share/nginx/html/*

COPY . /usr/share/nginx/html

EXPOSE 80
```

Este archivo:
- Usa una imagen ligera de Nginx.
- Elimina el contenido HTML por defecto.
- Copia todos tus archivos (`.html`, `.css`, `.js`) a la carpeta raíz de Nginx.
- Expone el puerto 80 para que la app sea accesible.

---

## 📄 Licencia

MIT © Equipo1SO

---

## 💬 Créditos

Creado por Tu Equipo1SO como práctica de despliegue estático con Docker.

