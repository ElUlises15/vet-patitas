# Entrega — Vet Patitas del Sur

Completado: sitio estático de cuatro páginas, sin framework ni build.
- index.html: portada, cuidados, perros/gatos, sala y CTA.
- servicios.html: propuesta de cuidados, consultas y prevención.
- equipo.html: enfoque de atención; nombres y matrículas pendientes.
- contacto.html: WhatsApp demo, barrio, preparación y preguntas desplegables.
- styles.css y script.js compartidos. Menú móvil accesible, cierre con Escape, foco visible, enlace para saltar al contenido y huellas animadas al ingresar por scroll. Movimiento reducido desactiva animación.
- Cinco imágenes originales generadas con herramienta integrada image_gen: assets/hero-consulta.png, perro.png, gato.png, sala.png, equipo.png. Versiones WebP optimizadas usadas en las páginas (~1 MB entre las cinco). Prompts completos: assets/IMAGE-PROMPTS.md.
- Meta noindex/nofollow en cada página. _headers configura X-Robots-Tag en hosts compatibles; debe verificarse al alojar. robots.txt permite leer el noindex.
- WhatsApp: https://wa.me/541155550707 con mensaje preparado. No se envió ningún mensaje.

## Verificación
Servidor local: python3 -m http.server 8077.
Playwright/Chrome: cuatro páginas a 1280 y 390px. Resultado final en qa/results.json y ocho capturas en qa/.
Todas: sin desborde horizontal, sin imágenes rotas, sin errores de JavaScript, un h1 y noindex presente. Se recorrió toda la página para cargar imágenes lazy antes de capturar.
Menú móvil: abre, expone aria-expanded=true y cierra con Escape. Reduced-motion: animation-name=none en huellas.
Enlaces y archivos locales revisados con HTMLParser: todos los destinos existen. Capturas revisadas visualmente de portada desktop/mobile, equipo desktop y contacto mobile. Se corrigió recorte de fotos y carga diferida durante captura.
No se afirma auditoría completa de accesibilidad ni se probó un hosting de producción. Fuentes de Google requieren conexión; hay fallback serif/sans-serif.

## Contenido y estado
Demo claramente identificada. Imágenes ilustrativas con IA. Dirección exacta, horarios, disponibilidad de servicios, profesionales y matrículas pendientes; no se inventaron reseñas ni credenciales. El teléfono suministrado es de demostración. No hay formulario ni reservas simuladas.
Diseño y referencias documentados en spec.md. Guías aplicadas: anti-generico, frontend-design, kit veterinaria y web-review.
Sin git, sin publicación externa.
