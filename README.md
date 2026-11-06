# Kerr Black Hole 3D Raytracer 

Simulador gráfico en tiempo real de un agujero negro en rotación (métrica de Kerr) desarrollado desde cero en **C++** y **OpenGL Compute Shaders**.


##  Características Técnicas

* **Integrador Numérico RK4 (Runge-Kutta de 4to orden):** Simulación de geodésicas nulas optimizada mediante coordenadas cartesianas normalizadas por la masa geométrica $M$ para evitar desbordamientos en campos gravitatorios extremos.
* **Métrica de Kerr Dinámica ($a \in [-0.99, 0.99]$):** Control en tiempo real del espín del agujero negro, modelando con precisión el arrastre del espacio-tiempo (*frame-dragging*).
* **Cálculo Exacto de la ISCO:** Determinación del radio de la órbita circular estable más interna utilizando las ecuaciones de Bardeen-Press-Teukolsky.
* **Óptica Relativista del Disco de Acreción:** 
  * Corrimiento al rojo gravitacional (*gravitational redshift*).
  * Efecto Doppler relativista (*beaming*) en el plasma en órbita.
  * Lente gravitacional de órdenes superiores con múltiples cruces del plano ecuatorial.

##  Controles Interactivos

* **Flechas Arriba / Abajo (`↑` / `↓`):** Incrementa o reduce dinámicamente el espín del agujero negro ($a$).
* **Teclas `1`, `2`, `3`:** Cambian instantáneamente entre perfiles predefinidos (Schwarzschild $a=0$, Kerr prógrado extremo y Kerr retrógrado extremo).
* **Mouse (Clic izquierdo y arrastrar):** Navegación orbital fluida alrededor de la singularidad.
* **Scroll del Mouse:** Zoom in / zoom out en el espacio-tiempo.

##  Stack Tecnológico
* **Lenguaje:** C++
* **Gráficos:** OpenGL 4.3+ (Compute Shaders, UBOs)
* **Matemáticas:** GLM
* **Ventana y Contexto:** GLFW & GLEW