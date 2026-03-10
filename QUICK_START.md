# 🚀 Guía de Inicio Rápido

Esta guía te llevará desde cero hasta tu primera presentación personalizada en minutos.

## ⚡ Inicio Rápido (5 minutos)

### Paso 1: Clonar el Repositorio

```bash
git clone https://github.com/Danirak/JMServicios-presentation-pdf.git
cd JMServicios-presentation-pdf
```

### Paso 2: Preparar tu Logo

1. Guarda tu logo como `public/images/general/logo.png`
2. Formato recomendado: PNG con fondo transparente
3. Tamaño: mínimo 800x800 px

### Paso 3: Configurar Colores (2 minutos)

Abre `presentacion_jmservicios.tex` y busca (líneas 14-19):

```latex
\definecolor{azulJM}{HTML}{284564}      % Tu color principal
\definecolor{naranjaJM}{HTML}{F49D10}   % Tu color de acento
```

Reemplaza con tus colores corporativos:

```latex
\definecolor{azulJM}{HTML}{TU_COLOR}     % Ejemplo: 1E3A8A
\definecolor{naranjaJM}{HTML}{TU_COLOR}  % Ejemplo: F59E0B
```

### Paso 4: Personalizar Portada (3 minutos)

Busca las líneas 42-54 y actualiza:

```latex
% Línea ~42: Nombre de tu empresa
{\fontsize{48}{52}\selectfont\color{azulJM}\textbf{TU EMPRESA}}

% Línea ~45: Tu slogan
{\fontsize{22}{26}\selectfont\color{naranjaJM}\textit{Tu Slogan Aquí}}

% Líneas ~51-52: Tus estadísticas
{\LARGE\color{azulJM}Más de \textbf{XX años} de experiencia}
{\LARGE\color{azulJM}Más de \textbf{XX proyectos} exitosos}
```

### Paso 5: Compilar

#### Opción A: Overleaf (Sin instalar nada)
1. Ve a [Overleaf.com](https://www.overleaf.com)
2. Sube el proyecto
3. Clic en "Recompile"
4. ✅ ¡Listo!

#### Opción B: Local (Windows)
```powershell
# Instala MiKTeX primero: https://miktex.org/download
pdflatex presentacion_jmservicios.tex
pdflatex presentacion_jmservicios.tex  # Dos veces para referencias
```

#### Opción C: Local (Mac/Linux)
```bash
# Mac: brew install --cask mactex
# Linux: sudo apt-get install texlive-full
pdflatex presentacion_jmservicios.tex
```

## 🎨 Personalización Avanzada (15 minutos)

### Actualizar "Sobre Nosotros"

Busca la línea ~77:

```latex
{\large JMSERVICIOS SPA es una empresa líder...}
```

Reemplaza con la descripción de tu empresa (2-3 líneas máximo).

### Modificar Servicios

Cada servicio tiene esta estructura (línea ~147 en adelante):

```latex
\begin{minipage}[t]{5.5cm}
    \colorbox{blancoJM}{\parbox[t][4.5cm][t]{5.3cm}{
        \vspace{0.5cm}
        \centering
        {\color{naranjaJM}\faIcono\quad}{\Large\color{azulJM}\textbf{Título Servicio}}
        
        \vspace{0.3cm}
        
        {\small Descripción breve del servicio...}
        \vspace{0.5cm}
    }}
\end{minipage}
```

**Para cambiar un servicio:**
1. Cambia `\faIcono` por tu icono ([ver lista](https://fontawesome.com/v5/search?m=free))
2. Cambia `Título Servicio`
3. Actualiza la descripción

**Iconos útiles:**
- `\faBuilding` - Edificio
- `\faTools` - Herramientas
- `\faChartLine` - Crecimiento
- `\faUsers` - Equipo
- `\faTruck` - Transporte
- `\faLightbulb` - Ideas
- `\faCog` - Tecnología
- `\faLeaf` - Sostenibilidad

### Actualizar Contacto

Busca la sección 4 (línea ~280):

```latex
{\color{azulJM}\faEnvelope} \Large tu@email.com
{\color{azulJM}\faPhone} \Large +56 9 XXXX XXXX
{\color{azulJM}\faGlobe} \Large www.tuweb.com
{\color{azulJM}\faMapMarkerAlt} \Large Tu Ciudad, País
```

## 💡 Tips Pro

### Ajustar Espaciado

```latex
\vspace{2cm}  % Aumentar espacio vertical
\vspace{0.5cm}  % Reducir espacio vertical
```

### Cambiar Tamaño de Fuente

```latex
{\fontsize{48}{52}\selectfont ...}  % Grande
{\fontsize{24}{28}\selectfont ...}  # Mediano
{\fontsize{18}{22}\selectfont ...}  % Pequeño
```

### Agregar Más Secciones

Copia una sección completa desde el comentario `% ====` hasta el siguiente, y modifícala.

### Reducir/Aumentar Altura Total

Línea 3:

```latex
\usepackage[paperwidth=21cm,paperheight=150cm,margin=0cm]{geometry}
```

Ajusta `paperheight` según tu contenido.

## ✅ Checklist de Personalización

Usa esto para no olvidar nada:

- [ ] Clonar repositorio
- [ ] Reemplazar logo
- [ ] Cambiar colores (azulJM, naranjaJM)
- [ ] Actualizar nombre de empresa
- [ ] Cambiar slogan
- [ ] Modificar estadísticas de portada
- [ ] Escribir descripción "Sobre Nosotros"
- [ ] Actualizar cifras de experiencia/proyectos
- [ ] Personalizar misión
- [ ] Adaptar servicios (al menos 3)
- [ ] Actualizar email de contacto
- [ ] Actualizar teléfono
- [ ] Actualizar sitio web
- [ ] Actualizar ubicación
- [ ] Compilar y revisar PDF
- [ ] Hacer ajustes finales

## 🆘 Problemas Comunes

### "Package not found"
**Solución:** En MiKTeX, acepta instalar paquetes automáticamente.

### "File not found: logo.png"
**Solución:** Verifica que el logo esté en `public/images/general/logo.png`

### El PDF se ve cortado
**Solución:** Aumenta `paperheight` en la línea 3.

### Los iconos no aparecen
**Solución:** Asegúrate de que `fontawesome5` esté instalado. En Overleaf funciona automáticamente.

### Error: "Undefined control sequence"
**Solución:** Probablemente un icono mal escrito. Verifica en [FontAwesome v5](https://fontawesome.com/v5/search).

## 📚 Recursos Adicionales

- [Guía de Personalización Completa](CUSTOMIZATION_GUIDE.md)
- [Iconos FontAwesome](https://fontawesome.com/v5/search?m=free)
- [Colores Hexadecimales](https://htmlcolorcodes.com/)
- [Overleaf Tutorial](https://www.overleaf.com/learn)

## 🤝 ¿Necesitas Ayuda?

- 📖 Lee la [Guía de Personalización](CUSTOMIZATION_GUIDE.md)
- 🐛 [Reporta un problema](https://github.com/Danirak/JMServicios-presentation-pdf/issues)
- 💬 Pregunta en [Discussions](https://github.com/Danirak/JMServicios-presentation-pdf/discussions)

---

**¡En 5 minutos tendrás tu presentación lista!** 🎉
