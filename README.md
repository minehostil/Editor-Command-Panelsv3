
📖 Como funciona el Generador
1. Ajustes del Panel.
Es la configuración básica para que el menú exista y sea accesible.
 * ID del Panel: El nombre técnico del archivo.
   * Ejemplo: Si pones temporada_invierno, el archivo se creará como temporada_invierno.yml.
 * Comando de Apertura: La palabra mágica en el chat.
   * Ejemplo: Si pones pase, el jugador escribirá /pase para ver sus premios.
 * Material de Fondo: Lo que rellena el espacio "vacío".
   * Ejemplo: Usar GRAY_STAINED_GLASS_PANE crea un marco gris que hace que los niveles (en colores brillantes) resalten mucho más.
2. Sistema de Permisos (El Candado)
Controla quién ha reclamado qué. Es lo que evita que alguien "bugee" el sistema.
 * Permiso Base: La raíz de la jerarquía.
   * Ejemplo: Si el permiso es vip.pase, el generador creará automáticamente permisos como vip.pase.1, vip.pase.2, etc.
 * Comando LuckPerms: Lo que se ejecuta en la consola al reclamar.
   * Ejemplo: lp user %player% permission set vip.pase.5 true — esto le dice al servidor: "Este usuario ya completó el nivel 5, no se lo vuelvas a dar".
3. Estados de Niveles (Feedback Visual)
Cambia la cara del nivel según el progreso del usuario.
 * Bloqueado:
   * Ejemplo: Nivel 10 (Material: RED_STAINED_GLASS_PANE). Si el jugador solo ha llegado al nivel 3, el 10 le aparecerá en rojo y, al hacer clic, escuchará un "¡No!" (sonido de aldeano).
 * Reclamar (Desbloqueado):
   * Ejemplo: Nivel 4 (Material: ORANGE_STAINED_GLASS_PANE). El jugador ya cumplió los requisitos. El icono brilla en naranja y le dice: "¡Haz clic para cobrar!".
 * Completado:
   * Ejemplo: Nivel 1 (Material: LIME_STAINED_GLASS_PANE). Como ya lo reclamó, el bloque es verde. Ya no da premios, solo muestra que esa meta ya se alcanzó.
4. Layouts y Patrones (El Diseño)
Define el camino que sigue el jugador en el menú.
 * Patrones: La ruta de los iconos.
   * Ejemplo (Serpiente): Los niveles van del slot 10 al 16, bajan al 25 y regresan al 19. Crea un efecto visual de "camino" o "mapa" muy superior a una simple cuadrícula.
 * Batch (Cantidad): Cuántos niveles quieres mostrar.
   * Ejemplo: Si pones 21, el generador creará exactamente 21 niveles siguiendo el patrón elegido.
5. Recompensas (Los Premios)
Aquí es donde configuras qué gana el jugador.
 * Filtrado por Nivel:
   * Ejemplo: Quieres que cada nivel dé 100 de Dinero, pero que solo cada 5 niveles dé 1 Llave VIP. En la recompensa de la llave, pones en niveles: 5, 10, 15, 20. El sistema ocultará la llave en los niveles 1, 2, 3, 4, etc.
 * Modo Multiplicar vs Suma:
   * Ejemplo (Mult): Si pones $1.000 y modo multiplicar, el Nivel 1 da $1.000, el Nivel 2 da $2.000, el Nivel 10 da $10.000. ¡Ideal para recompensar el esfuerzo de niveles altos!
6. Requisitos Progresivos (El Desafío)
Lo que el jugador debe hacer para desbloquear el nivel.
 * Variables Dinámicas:
   * Ejemplo: Si usas la variable de bloques minados %statistic_mine_block%. Para el Nivel 1 pides 500 bloques, pero configuras un aumento de 500 por nivel. El Nivel 2 pedirá 1.000, el Nivel 3 pedirá 1.500, y así sucesivamente.
