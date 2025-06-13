## 🗂️ Estructura del Proyecto

La siguiente es la estructura base del proyecto

```bash
RickAndMortyChallenge/
├── 📁 App/     
│   ├── 📁 Extensions           # Extensiones útiles (por ejemplo, Optional, Moya)
│   ├── 📁 Utilities            # Constantes y helpers generales
│   └── 📁 SupportingFiles      # Recursos como Assets y AppIcon
│
├── 📁 Dependencies/            # Configuración de dependencias externas (ej. Moya)
│
├── 📁 Domain/                  # Lógica del dominio de la app
│   ├── 📁 Models               # Modelos base de datos/API
│   ├── 📁 Repositories         # Definición de interfaces de acceso a datos
│   └── 📁 UseCase              # Casos de uso con lógica de negocio
│
├── 📁 Networking/              # Capa de red
│   ├── 📁 APIs                 # Definiciones de endpoints
│   ├── 📁 DTOs                 # Objetos de transferencia de datos
│   └── 📁 RepositoriesImpl     # Implementaciones reales de los repositorios
│
├── 📁 Presentations/           # Todo lo relacionado con la UI
│   ├── 📁 Navigation           # Coordinadores o rutas de navegación
│   └── 📁 Screens
│       ├── 📁 View             # Vistas SwiftUI
│       ├── 📁 ViewModels       # Lógica de presentación
│       └── 📁 CommonComponents # Componentes UI reutilizables
```
## 🎯 Propósito de la aplicación

Esta aplicación fue creada como un desafío técnico que pone a prueba el manejo de:

- 📡 Consumo de APIs REST usando `URLSession`.
- 🧠 Manejo de modelos de datos complejos (codificación/decodificación JSON).
- 🎨 Construcción de interfaces modernas usando `SwiftUI`.
- 🚦 Gestión de estados de red, carga y errores.
- 📦 Arquitectura MVVM y separación de responsabilidades.

---

## 🛠️ Tecnologías empleadas

| Tecnología  | Uso principal                                      |
|-------------|----------------------------------------------------|
| Swift       | Lenguaje de programación nativo para iOS           |
| SwiftUI     | Construcción de la interfaz moderna y reactiva     |
| Combine     | Manejo reactivo del flujo de datos (opcional)      |
| URLSession  | Consumo de servicios REST                          |
| MVVM        | Patrón de arquitectura para organización del código |

---

## ✅ Requisitos mínimos

- iOS 15 o superior  
- Xcode 14 o superior  
- Conexión a internet para cargar los datos

---

Con esta aplicación, los fans de Rick and Morty pueden tener una experiencia inmersiva y rápida directamente desde su dispositivo móvil.

