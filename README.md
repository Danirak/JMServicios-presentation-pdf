# 📄 Plantilla de Presentación PDF con LaTeX

Plantilla profesional para crear presentaciones corporativas en formato PDF usando LaTeX. Diseñada originalmente para JMSERVICIOS SPA.

## ✨ Características

- 🎨 **Diseño profesional y moderno** con colores personalizables
- 📐 **Layout de página única** tipo "landing page" en PDF
- 🖼️ **Secciones personalizables**: Portada, Sobre Nosotros, Servicios, Contacto
- 🎯 **Fácil de adaptar** para cualquier empresa o proyecto
- 🚀 **Múltiples opciones de compilación** (Windows, Mac, Linux, Online)
- 💼 **Iconos FontAwesome** integrados
- 🌈 **Sistema de colores corporativos** fácil de modificar

## 📋 Estructura del Proyecto

```
├── presentacion_jmservicios.tex    # Archivo principal LaTeX
├── public/
│   └── images/                     # Carpeta para imágenes
│       └── general/
│           └── logo.png            # Logo de la empresa
├── README.md                       # Este archivo
└── CUSTOMIZATION_GUIDE.md          # Guía de personalización
```

## 🚀 Instalación y Uso Rápido

### Opción 1: Usar Overleaf (Recomendado - Sin instalación)

1. Ve a [Overleaf](https://www.overleaf.com/)
2. Crea una cuenta gratuita
3. Crea un nuevo proyecto ("New Project" → "Upload Project")
4. Sube este proyecto completo (como ZIP)
5. Abre `presentacion_jmservicios.tex`
6. Personaliza los colores, textos e imágenes
7. Compila con el botón verde "Recompile"

### Opción 2: Instalar LaTeX en Windows

1. **Descargar e instalar MiKTeX**:
   - Ve a: https://miktex.org/download
   - Durante la instalación, selecciona "Install packages on-the-fly: Yes"

2. **Compilar el documento**:
   ```powershell
   cd ruta/al/proyecto
   pdflatex presentacion_jmservicios.tex
   pdflatex presentacion_jmservicios.tex
   ```
   (Se ejecuta dos veces para generar correctamente las referencias)

### Opción 3: VS Code con LaTeX Workshop

1. Instala [VS Code](https://code.visualstudio.com/)
2. Instala la extensión "[LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)"
3. Instala MiKTeX (ver Opción 2)
4. Abre el archivo `.tex` y presiona `Ctrl+Alt+B` para compilar
5. El PDF se generará automáticamente

### Opción 4: macOS con MacTeX

1. Instala [MacTeX](https://www.tug.org/mactex/)
2. Compila con: `pdflatex presentacion_jmservicios.tex`

### Opción 5: Linux

```bash
# Ubuntu/Debian
sudo apt-get install texlive-full

# Fedora
sudo dnf install texlive-scheme-full

# Compilar
pdflatex presentacion_jmservicios.tex
```

## 🎨 Personalización Rápida

### Cambiar Colores Corporativos

Abre `presentacion_jmservicios.tex` y busca estas líneas al inicio:

```latex
\definecolor{azulJM}{HTML}{284564}      % Color principal
\definecolor{naranjaJM}{HTML}{F49D10}   % Color de acento
\definecolor{blancoJM}{HTML}{FFFFFF}    % Fondo
```

Reemplaza los códigos hexadecimales con tus colores corporativos.

### Cambiar Logo

1. Reemplaza el archivo `public/images/general/logo.png` con tu logo
2. Formato recomendado: PNG con fondo transparente
3. Tamaño recomendado: 800x800 px mínimo

### Personalizar Contenido

Para una guía detallada de personalización, consulta [CUSTOMIZATION_GUIDE.md](CUSTOMIZATION_GUIDE.md)

## 📦 Dependencias de LaTeX

Esta plantilla utiliza los siguientes paquetes:

- `geometry` - Configuración de página
- `inputenc`, `babel` - Soporte de español y UTF-8
- `graphicx` - Imágenes
- `tikz` - Gráficos y diseño
- `fontawesome5` - Iconos

Estos se instalan automáticamente con MiKTeX o distribuciones completas de LaTeX.

## 🎯 Secciones Incluidas

La plantilla incluye las siguientes secciones:

1. **Portada** - Logo, nombre de empresa, slogan, estadísticas clave
2. **Sobre Nosotros** - Historia, misión, visión, cifras destacadas
3. **Servicios** - Grid de servicios con iconos y descripciones
4. **Contacto** - Información de contacto, email, teléfono, web

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Si tienes sugerencias o mejoras:

1. Haz un fork del proyecto
2. Crea una rama para tu feature (`git checkout -b feature/nueva-caracteristica`)
3. Commit tus cambios (`git commit -m 'Agrega nueva característica'`)
4. Push a la rama (`git push origin feature/nueva-caracteristica`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está disponible como plantilla de código abierto. Siéntete libre de usarlo y adaptarlo para tus propios proyectos.

## 💬 Soporte

Si tienes preguntas o necesitas ayuda:

- 📖 Consulta la [Guía de Personalización](CUSTOMIZATION_GUIDE.md)
- 🐛 Reporta problemas en [GitHub Issues](https://github.com/Danirak/JMServicios-presentation-pdf/issues)
- 📧 Contacta al mantenedor del proyecto

## ⭐ Ejemplo de Resultado

Este proyecto fue originalmente creado para JMSERVICIOS SPA. El archivo original (`presentacion_jmservicios.tex`) puede servir como ejemplo de referencia para tu propia implementación.

---

**¡Empieza a crear tu presentación profesional hoy!** 🚀
