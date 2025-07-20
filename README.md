moto-blog/
├── manage.py
├── requirements.txt
├── db.sqlite3
├── README.md
├── .gitignore
├── venv/                          # Entorno virtual (no subir a git)
│
├── moto_blog/                     # Configuración principal del proyecto
│   ├── __init__.py
│   ├── settings.py               # Configuración principal
│   ├── urls.py                   # URLs principales
│   ├── wsgi.py                   # Para deployment
│   └── asgi.py
│
├── blog/                         # Aplicación principal del blog
│   ├── __init__.py
│   ├── admin.py                  # Configuración del admin
│   ├── apps.py
│   ├── models.py                 # Modelos: Articulo, Categoria, Comentario
│   ├── views.py                  # Vistas del blog
│   ├── urls.py                   # URLs del blog
│   ├── forms.py                  # Formularios (comentarios, etc.)
│   ├── migrations/               # Migraciones de base de datos
│   │   └── __init__.py
│   └── tests.py
│
├── usuarios/                     # Gestión de usuarios
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py                 # Extensión del modelo Usuario
│   ├── views.py                  # Login, registro, perfil
│   ├── urls.py
│   ├── forms.py                  # Formularios de registro/perfil
│   ├── migrations/
│   │   └── __init__.py
│   └── tests.py
│
├── contacto/                     # Formulario de contacto
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py                 # Modelo de mensajes de contacto
│   ├── views.py                  # Vista del formulario
│   ├── urls.py
│   ├── forms.py                  # Formulario de contacto
│   ├── migrations/
│   │   └── __init__.py
│   └── tests.py
│
├── templates/                    # Plantillas HTML
│   ├── base.html                 # Template base con navegación
│   ├── 404.html                  # Página de error personalizada
│   ├── 500.html
│   │
│   ├── blog/                     # Templates del blog
│   │   ├── inicio.html           # Página principal
│   │   ├── lista_articulos.html  # Lista de artículos con filtros
│   │   ├── detalle_articulo.html # Detalle del artículo + comentarios
│   │   ├── categoria_articulos.html # Artículos por categoría
│   │   └── acerca_de.html        # Página "Acerca de"
│   │
│   ├── usuarios/                 # Templates de usuarios
│   │   ├── registro.html         # Formulario de registro
│   │   ├── login.html            # Formulario de login
│   │   └── perfil.html           # Perfil del usuario
│   │
│   ├── contacto/                 # Templates de contacto
│   │   ├── contacto.html         # Formulario de contacto
│   │   └── contacto_exitoso.html # Confirmación de envío
│   │
│   └── partials/                 # Componentes reutilizables
│       ├── navbar.html           # Barra de navegación
│       ├── footer.html           # Pie de página
│       ├── articulo_card.html    # Card de artículo
│       ├── comentario.html       # Template de comentario
│       └── paginacion.html       # Controles de paginación
│
├── static/                       # Archivos estáticos
│   ├── css/
│   │   ├── bootstrap.min.css     # Bootstrap 5
│   │   ├── style.css             # Estilos personalizados
│   │   └── admin-custom.css      # Estilos para el admin
│   │
│   ├── js/
│   │   ├── bootstrap.bundle.min.js # JavaScript de Bootstrap
│   │   ├── main.js               # JavaScript personalizado
│   │   └── comentarios.js        # JS para manejo de comentarios
│   │
│   ├── img/                      # Imágenes del sitio
│   │   ├── logo.png              # Logo del blog
│   │   ├── favicon.ico           # Favicon
│   │   ├── hero-bg.jpg           # Imagen del hero
│   │   └── placeholder-moto.jpg  # Imagen por defecto
│   │
│   └── fonts/                    # Fuentes personalizadas (opcional)
│
├── media/                        # Archivos subidos por usuarios
│   ├── articulos/                # Imágenes de artículos
│   ├── avatars/                  # Avatares de usuarios
│   ├── uploads/                  # Archivos del editor CKEditor
│   └── temp/                     # Archivos temporales
│
├── staticfiles/                  # Archivos estáticos para producción
│   └── (generados automáticamente con collectstatic)
│
├── locale/                       # Archivos de traducción (opcional)
│   └── es_AR/
│       └── LC_MESSAGES/
│           ├── django.po
│           └── django.mo
│
└── docs/                         # Documentación del proyecto
    ├── deployment.md             # Guía de deployment
    ├── api.md                    # Documentación de API (si aplica)
    └── database.md               # Esquema de base de datos