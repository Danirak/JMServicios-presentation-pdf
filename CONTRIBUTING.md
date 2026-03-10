# 🤝 Contribuir al Proyecto

¡Gracias por tu interés en mejorar esta plantilla! Las contribuciones son bienvenidas y apreciadas.

## 📝 Cómo Contribuir

### Reportar Problemas

Si encuentras un error o tienes una sugerencia:

1. Ve a [Issues](https://github.com/Danirak/JMServicios-presentation-pdf/issues)
2. Verifica que no exista un issue similar
3. Crea un nuevo issue con:
   - **Título descriptivo**
   - **Descripción detallada** del problema
   - **Pasos para reproducir** (si es un bug)
   - **Comportamiento esperado vs actual**
   - **Capturas de pantalla** (si aplica)
   - **Versión de LaTeX** que estás usando

### Proponer Mejoras

Para nuevas características o mejoras:

1. Abre un [Discussion](https://github.com/Danirak/JMServicios-presentation-pdf/discussions)
2. Describe tu idea y por qué sería útil
3. Espera feedback de la comunidad
4. Si hay consenso, crea un issue y luego un PR

### Enviar Pull Requests

#### Proceso

1. **Fork** este repositorio
2. **Crea una rama** para tu feature:
   ```bash
   git checkout -b feature/mi-mejora
   ```
3. **Realiza tus cambios**:
   - Mantén el código limpio y organizado
   - Sigue las convenciones del proyecto
   - Comenta código complejo
4. **Prueba tus cambios**:
   - Compila el documento LaTeX
   - Verifica que no haya errores
   - Revisa el PDF generado
5. **Commit con mensajes claros**:
   ```bash
   git commit -m "feat: agrega nueva sección de testimonios"
   ```
6. **Push a tu fork**:
   ```bash
   git push origin feature/mi-mejora
   ```
7. **Crea un Pull Request** en GitHub

#### Convenciones de Commits

Usa el formato de [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` - Nueva característica
- `fix:` - Corrección de bug
- `docs:` - Cambios en documentación
- `style:` - Formato, espacios, etc
- `refactor:` - Reestructuración de código
- `test:` - Agregar pruebas
- `chore:` - Tareas de mantenimiento

**Ejemplos:**
```
feat: agrega sección de portfolio
fix: corrige espaciado en sección de servicios
docs: actualiza guía de instalación
style: mejora formato de colores
```

## 🎨 Áreas Para Contribuir

### Ideas Bienvenidas

- ✅ **Nuevas secciones** (Portfolio, Testimonios, Equipo, etc.)
- ✅ **Temas de colores** predefinidos
- ✅ **Ejemplos adicionales** de uso
- ✅ **Mejoras en documentación**
- ✅ **Traducciones** del README y guías
- ✅ **Scripts de automatización**
- ✅ **Plantillas variantes** (1 página, múltiples páginas, etc.)
- ✅ **Mejoras de diseño**

### Ejemplos de Contribuciones Valiosas

1. **Agregar nuevas secciones reutilizables**
   - Sección de timeline
   - Sección de estadísticas
   - Sección de equipo con fotos

2. **Crear temas de colores**
   - Tema corporativo azul
   - Tema tecnológico verde
   - Tema creativo morado

3. **Mejorar documentación**
   - Videos tutoriales
   - GIFs animados de proceso
   - Capturas de antes/después

4. **Scripts útiles**
   - Script para cambiar colores automáticamente
   - Validador de estructura LaTeX
   - Generador de servicios desde CSV

## 📏 Guías de Estilo

### Código LaTeX

```latex
% ✅ BIEN: Comentarios descriptivos
% SECCIÓN 1: PORTADA - Información principal de la empresa
\colorbox{azulJM}{\parbox{21cm}{
    ...
}}

% ✅ BIEN: Indentación consistente (4 espacios)
\begin{center}
    \includegraphics[width=8cm]{logo.png}
    
    \vspace{1cm}
    
    {\Large\textbf{Título}}
\end{center}

% ❌ MAL: Sin comentarios ni estructura
\colorbox{azulJM}{\parbox{21cm}{
\includegraphics[width=8cm]{logo.png}
{\Large\textbf{Título}}}}
```

### Documentación

- ✅ Usa emojis para hacer el contenido más visual
- ✅ Incluye ejemplos de código con comentarios
- ✅ Divide en secciones claras con encabezados
- ✅ Proporciona capturas de pantalla cuando sea útil
- ❌ Evita jerga técnica innecesaria
- ❌ No uses párrafos muy largos sin breaks

### Commits

```bash
# ✅ BIEN: Descriptivo y específico
feat: agrega sección de testimonios con grid de 3 columnas
fix: corrige espaciado entre servicios en vista mobile
docs: actualiza QUICK_START con ejemplos de iconos

# ❌ MAL: Vago y sin contexto
fix: arreglé algo
update: cambios
mejoras
```

## 🧪 Testing

Antes de enviar un PR, verifica:

- [ ] El documento compila sin errores
- [ ] El PDF se genera correctamente
- [ ] Los colores se ven bien en el resultado
- [ ] Las imágenes se cargan correctamente
- [ ] Los enlaces en el README funcionan
- [ ] La documentación está actualizada
- [ ] Los comentarios del código están claros

### Compilar y Probar

```bash
# Compilar
pdflatex presentacion_jmservicios.tex

# Verificar errores
# Revisa el archivo .log para warnings

# Visualizar
# Abre el PDF generado y revisa cada sección
```

## 📋 Checklist para PRs

Asegúrate de que tu PR incluya:

- [ ] Descripción clara de qué cambia y por qué
- [ ] Código compilado y probado
- [ ] Documentación actualizada (si aplica)
- [ ] Capturas de pantalla (para cambios visuales)
- [ ] Commits con mensajes descriptivos
- [ ] Branch actualizada con main

## 🎓 Recursos para Contribuir

### Aprender LaTeX

- [Overleaf Learn](https://www.overleaf.com/learn)
- [LaTeX Wikibook](https://en.wikibooks.org/wiki/LaTeX)
- [TikZ Manual](https://ctan.org/pkg/pgf)

### Diseño y Colores

- [Adobe Color](https://color.adobe.com/)
- [Coolors](https://coolors.co/)
- [HTML Color Codes](https://htmlcolorcodes.com/)

### Git y GitHub

- [GitHub Flow](https://guides.github.com/introduction/flow/)
- [Git Handbook](https://guides.github.com/introduction/git-handbook/)

## ❓ Preguntas

Si tienes dudas sobre cómo contribuir:

1. Lee esta guía completamente
2. Revisa [Issues](https://github.com/Danirak/JMServicios-presentation-pdf/issues) existentes
3. Pregunta en [Discussions](https://github.com/Danirak/JMServicios-presentation-pdf/discussions)
4. Contacta a los mantenedores

## 🌟 Reconocimientos

Todos los contribuidores serán mencionados en el README y tendrán nuestro agradecimiento.

¡Esperamos tu contribución! 🚀

---

**Gracias por hacer que esta plantilla sea mejor para todos** ❤️
