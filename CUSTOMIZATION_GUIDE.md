# 📘 Guía de Personalización - Plantilla de Presentación PDF

Esta guía te ayudará a adaptar la plantilla para tu propia empresa o proyecto.

## 🎨 1. Configurar Colores Corporativos

### Ubicación
Abre `presentacion_jmservicios.tex` y busca estas líneas (aproximadamente líneas 14-19):

```latex
% Colores corporativos
\definecolor{azulJM}{HTML}{284564}
\definecolor{naranjaJM}{HTML}{F49D10}
\definecolor{blancoJM}{HTML}{FFFFFF}
\definecolor{grisClaro}{HTML}{F8F9FA}
\definecolor{grisOscuro}{HTML}{2C3E50}
\definecolor{grisSeccion}{HTML}{e8ebef}
```

### Cómo Cambiarlos

1. **Identifica tus colores corporativos** en formato hexadecimal (ejemplo: #FF5733)
2. **Reemplaza los valores HTML**:
   - `azulJM` → Tu color principal (usado en títulos y elementos destacados)
   - `naranjaJM` → Tu color de acento (usado en detalles y énfasis)
   - Los demás puedes dejarlos o ajustarlos según necesites

### Ejemplo de Cambio

```latex
% Antes (JM Servicios)
\definecolor{azulJM}{HTML}{284564}
\definecolor{naranjaJM}{HTML}{F49D10}

% Después (Tu Empresa)
\definecolor{azulJM}{HTML}{1E3A8A}      % Azul oscuro
\definecolor{naranjaJM}{HTML}{F59E0B}   % Ámbar
```

## 🖼️ 2. Cambiar el Logo

### Ubicación del Logo
El logo está en: `public/images/general/logo.png`

### Pasos para Cambiar

1. **Prepara tu logo**:
   - Formato: PNG con fondo transparente (recomendado)
   - Tamaño recomendado: 800x800 px o mayor
   - Aspecto: Cuadrado o apaisado funciona mejor

2. **Reemplaza el archivo**:
   - Elimina o renombra `logo.png`
   - Copia tu logo con el nombre `logo.png` en la misma carpeta

3. **Si tu logo tiene otro nombre**:
   - Busca en el archivo `.tex` la línea:
     ```latex
     \includegraphics[width=8cm]{public/images/general/logo.png}
     ```
   - Cambia `logo.png` por el nombre de tu archivo

### Ajustar Tamaño del Logo

Encuentra las líneas donde se usa `\includegraphics` y modifica el `width`:

```latex
% Logo más grande
\includegraphics[width=10cm]{public/images/general/logo.png}

% Logo más pequeño
\includegraphics[width=6cm]{public/images/general/logo.png}
```

## 📝 3. Personalizar la Portada

### Elementos a Cambiar

Busca la sección `SECCIÓN 1: PORTADA` (aproximadamente línea 23):

```latex
{\fontsize{48}{52}\selectfont\color{azulJM}\textbf{JM SERVICIOS}}
```
→ Cambia `JM SERVICIOS` por el nombre de tu empresa

```latex
{\fontsize{22}{26}\selectfont\color{naranjaJM}\textit{Construyendo Futuro, Moviendo Progreso}}
```
→ Cambia el slogan por el de tu empresa

```latex
{\LARGE\color{azulJM}Más de \textbf{30 años} de experiencia}
{\LARGE\color{azulJM}Más de \textbf{200 proyectos} exitosos}
```
→ Actualiza las estadísticas con las de tu empresa

### Ejemplo de Cambio

```latex
% Antes
{\fontsize{48}{52}\selectfont\color{azulJM}\textbf{JM SERVICIOS}}
{\fontsize{22}{26}\selectfont\color{naranjaJM}\textit{Construyendo Futuro, Moviendo Progreso}}

% Después
{\fontsize{48}{52}\selectfont\color{azulJM}\textbf{TU EMPRESA}}
{\fontsize{22}{26}\selectfont\color{naranjaJM}\textit{Tu slogan aquí}}
```

## ℹ️ 4. Personalizar "Sobre Nosotros"

### Ubicación
Busca `SECCIÓN 2: SOBRE NOSOTROS` (aproximadamente línea 69)

### Elementos a Modificar

1. **Descripción de la empresa**:
```latex
{\large JMSERVICIOS SPA es una empresa líder en el norte de Chile...}
```

2. **Estadísticas**:
```latex
\node at (4,2.2) {\fontsize{48}{52}\selectfont\color{naranjaJM}\textbf{200+}};
\node at (4,0.8) {\Large\color{grisOscuro}Proyectos Finalizados};

\node at (14,2.2) {\fontsize{48}{52}\selectfont\color{azulJM}\textbf{30+}};
\node at (14,0.8) {\Large\color{grisOscuro}Años de Experiencia};
```

3. **Misión**:
```latex
{\large Superar las expectativas de nuestros clientes con soluciones duraderas...}
```

### Consejos
- Mantén los textos concisos
- Las estadísticas deben ser números impactantes
- La misión debe ser clara y directa

## 🛠️ 5. Personalizar Servicios

### Ubicación
Busca `SECCIÓN 3: NUESTROS SERVICIOS` (aproximadamente línea 123)

### Estructura de un Servicio

Cada servicio es un bloque de este tipo:

```latex
\begin{minipage}[t]{5.5cm}
    \colorbox{blancoJM}{\parbox[t][4.5cm][t]{5.3cm}{
        \vspace{0.5cm}
        \centering
        {\color{naranjaJM}\faTractor\quad}{\Large\color{azulJM}\textbf{Movimiento de Tierras}}
        
        \vspace{0.3cm}
        
        {\small Excavaciones, nivelaciones y compactaciones...}
        \vspace{0.5cm}
    }}
\end{minipage}
```

### Modificar un Servicio

1. **Cambiar el icono**: `\faTractor` → [Lista de iconos FontAwesome](https://fontawesome.com/v5/search?m=free)
2. **Cambiar el título**: `Movimiento de Tierras` → Tu servicio
3. **Cambiar la descripción**: Texto breve explicando el servicio

### Agregar/Quitar Servicios

- Para **quitar** un servicio: elimina el bloque completo `\begin{minipage}...\end{minipage}`
- Para **agregar** un servicio: copia y pega un bloque existente, luego modifícalo
- La plantilla está diseñada para 3 servicios por fila

### Iconos FontAwesome Útiles

```latex
\faBuilding    % Edificio
\faIndustry    % Industria
\faTools       % Herramientas
\faCog         % Engranaje
\faChartLine   % Crecimiento
\faUsers       % Equipo
\faLightbulb   % Ideas
\faTruck       % Transporte
\faWrench      % Llave
\faHardHat     % Casco
```

## 📞 6. Personalizar Contacto

### Ubicación
Busca `SECCIÓN 4: CONTACTO` (aproximadamente línea 250)

### Elementos a Cambiar

```latex
{\color{azulJM}\faEnvelope} \Large contacto@jmservicios.cl
{\color{azulJM}\faPhone} \Large +56 9 1234 5678
{\color{azulJM}\faGlobe} \Large www.jmservicios.cl
{\color{azulJM}\faMapMarkerAlt} \Large Antofagasta, Chile
```

Reemplaza cada línea con tus datos de contacto.

## 🎯 7. Ajustes Avanzados

### Cambiar Tamaño de Página

Busca al inicio del documento:

```latex
\usepackage[paperwidth=21cm,paperheight=150cm,margin=0cm]{geometry}
```

- `paperheight=150cm` → Ajusta la altura total de la presentación
- Aumenta si agregas más contenido
- Disminuye si quitas secciones

### Cambiar Fuentes

Para cambiar el tamaño de los títulos principales:

```latex
{\fontsize{38}{42}\selectfont\color{azulJM}\textbf{Título}}
```

- Primer número (38): tamaño de fuente
- Segundo número (42): espacio entre líneas

### Espaciado

- `\vspace{1cm}` → Espacio vertical de 1cm
- Aumenta o disminuye el número para ajustar espacios

## ✅ Checklist de Personalización

Usa esta lista para asegurarte de personalizar todo:

- [ ] Colores corporativos definidos
- [ ] Logo reemplazado
- [ ] Nombre de empresa actualizado
- [ ] Slogan personalizado
- [ ] Estadísticas de portada modificadas
- [ ] Descripción "Sobre Nosotros" escrita
- [ ] Estadísticas de "Sobre Nosotros" actualizadas
- [ ] Misión personalizada
- [ ] Servicios modificados (títulos, iconos, descripciones)
- [ ] Información de contacto actualizada
- [ ] Compilación exitosa sin errores
- [ ] Revisión del PDF generado

## 🚀 Compilar y Probar

Después de cada cambio importante:

1. **Guarda el archivo** `.tex`
2. **Compila**:
   ```bash
   pdflatex presentacion_jmservicios.tex
   ```
3. **Revisa el PDF** generado
4. **Ajusta** según necesites

## 💡 Consejos Finales

- ✅ **Haz cambios incrementales** - Modifica una sección, compila, revisa
- ✅ **Guarda copias** - Mantén una copia del original por si algo sale mal
- ✅ **Revisa los colores** - Asegúrate de que haya buen contraste
- ✅ **Textos concisos** - Menos es más en presentaciones
- ✅ **Prueba diferentes tamaños** - Ajusta hasta que se vea profesional

## 🆘 Resolución de Problemas

### Error: "File not found"
- Verifica que la ruta a las imágenes sea correcta
- Asegúrate de que el archivo de imagen exista

### El PDF se ve cortado
- Aumenta `paperheight` en la configuración de geometría

### Los colores no se ven
- Verifica que los códigos hex sean válidos (6 dígitos)
- No uses el símbolo `#` en el código LaTeX

### Iconos no aparecen
- Asegúrate de que el paquete `fontawesome5` esté instalado
- Verifica que el nombre del icono sea correcto

---

¿Necesitas más ayuda? Abre un issue en GitHub: https://github.com/Danirak/JMServicios-presentation-pdf/issues