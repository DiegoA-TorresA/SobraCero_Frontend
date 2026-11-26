# 🌱 SobraCero — Frontend Oficial

> **Marketplace de rescate de alimentos**: ventas con descuento de excedentes comerciales y canal de donaciones directas para organizaciones sociales vulnerables.

Este repositorio contiene la **Aplicación Web SPA (Frontend)** de **SobraCero**, construida con **Angular 22**, TypeScript y SCSS, con despliegue activo en GitHub Pages y flujo de trabajo colaborativo **Gitflow**.

* 🌐 **Demo en vivo (GitHub Pages):** [https://diegoa-torresa.github.io/SobraCero_Frontend/](https://diegoa-torresa.github.io/SobraCero_Frontend/)
* ⚙️ **Repositorio del Backend (API REST Spring Boot):** [DiegoA-TorresA/SobraCero_Backend](https://github.com/DiegoA-TorresA/SobraCero_Backend)

---

## 📁 Estructura del Proyecto

```text
SobraCero_Frontend/
├── public/                    # Recursos estáticos y reglas de redirección SPA
├── src/
│   ├── app/
│   │   ├── core/              # Servicios API, interceptores JWT, guards y sesión
│   │   ├── layout/            # Shell principal, navegación y panel de perfil
│   │   ├── shared/            # Componentes reutilizables, pipes, toasts y directivas
│   │   └── features/          # Módulos por dominio (landing, auth, consumidor, comercio, organizacion, admin, impacto)
│   ├── environments/          # Configuración local (localhost:8080) y producción (Render)
│   └── styles.scss            # Design tokens, tema oscuro automático y micro-interacciones
├── angular.json               # Configuración del workspace Angular
├── package.json               # Dependencias y scripts de ejecución
└── .github/                   # CODEOWNERS y plantilla de Pull Request
```

---

## 👥 Equipo y Asignación de Módulos (Gitflow)

| Estudiante | Rol / Módulo Asignado | Carpeta en el Repositorio | Rama de Trabajo |
|---|---|---|---|
| **Diego Torres (Lead)** | Arquitectura Base, Core, Layout, Auth y Notificaciones | `src/app/core/`, `layout/`, `auth/`, `notificaciones/` | `main` y `develop` |
| **Angello Castillo** | Landing pública, Impacto público y Página 404 | `src/app/features/landing/` | `feature/parte-2-landing` |
| **Luz Gonzales** | Consumidor (Ofertas cercanas, Mapa, Pago y Reservas) | `src/app/features/consumidor/` | `feature/parte-3-consumidor` |
| **Alvaro Grados** | Comercio (Publicar oferta, Canjear código, Donaciones) | `src/app/features/comercio/` | `feature/parte-4-comercio` |
| **William Villacorta** | Organización Social (Donaciones, Recojos, Ley 30498) | `src/app/features/organizacion/` | `feature/parte-5-organizacion` |
| **Mathias Oré** | Administración, Impacto, Reporte CSV, Predicción y Animaciones | `src/app/features/admin/`, `impacto/`, `layout/perfil/` | `feature/parte-6-admin-impacto`, `feature/animaciones-perfil` |

---

## 💻 Ejecución en Local

### Requisitos
* **Node.js 22 LTS** o superior (`npm`).
* Backend ejecutándose en local ([`SobraCero_Backend`](https://github.com/DiegoA-TorresA/SobraCero_Backend) en `http://localhost:8080`) **o** usar directamente el backend desplegado en la nube.

### 1. Clonar e instalar dependencias
```bash
git clone https://github.com/DiegoA-TorresA/SobraCero_Frontend.git
cd SobraCero_Frontend
npm install
```

### 2. Iniciar la aplicación
* **Opción A — Conectado al backend local (`http://localhost:8080`):**
  ```bash
  npm start
  ```
* **Opción B — Conectado al backend desplegado en la nube (Render):**
  ```bash
  npm run start:cloud
  ```

La aplicación se abrirá en `http://localhost:4200`.

### 3. Compilar para producción
```bash
npm run build
```

---

## 🔑 Credenciales Demo para Pruebas

* **Consumidor:** `consumidor@demo.pe` | Clave: `Demo1234`
* **Comercio:** `comercio1@demo.pe` | Clave: `Demo1234`
* **Organización Social:** `ong1@demo.pe` | Clave: `Demo1234`
* **Administrador:** `admin@sobracero.pe` | Clave: `Admin1234`

---

## 📝 Estándar de Commits (Conventional Commits)

Todos los commits siguen **Conventional Commits**: `<tipo>(<alcance>): <descripción en minúsculas>` (`feat`, `fix`, `chore`, `docs`, `style`, `refactor`).
