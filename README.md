# Portal del paciente — Plataforma de Citas Médicas

Interfaz web (React) del proyecto. Es el contenedor **Portal web** del diagrama C4 nivel 2.

La arquitectura, la documentación de diseño y el arranque del sistema completo están en el repositorio hermano
[SistemaSitasMedicasBackend](https://github.com/Andres-Maya/SistemaSitasMedicasBackend). Allí, `docker compose up --build`
compila este portal dentro del API Gateway y queda disponible en http://localhost:8080.

Los dos repositorios deben clonarse uno al lado del otro:

```
carpeta/
├── SistemaSitasMedicasBackend/
└── SistemaSitasMedicasFrontend/   ← este repositorio
```

## Desarrollo local (opcional)

Con el sistema levantado desde el repositorio del backend:

```bash
cd frontend
npm install
npm start
```

El portal llama a la API en `http://localhost:8080/api/clinica` (configurable con `REACT_APP_API_URL`).
El frontend no sabe cuántos servicios hay detrás: el gateway enruta cada ruta al servicio dueño de su contexto.
