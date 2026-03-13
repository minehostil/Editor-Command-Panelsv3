📘 Guía Rápida: Uso del Generador
1. Ajustes del Panel
 * ID del Panel: El nombre que tendrá el archivo (ej: recompensas_v1).
 * Permiso de Apertura: El permiso necesario para abrir el menú (ej: menu.usar).
 * Título Visual: El nombre que verán los jugadores arriba del inventario.
 * Comando de Apertura: El comando que escribirán en el chat (ej: /premios).
 * Mensajes (Éxito/Fallo): Lo que sale en el chat al reclamar o al no cumplir requisitos.
 * Material de Fondo: El bloque que rellena los huecos vacíos.
2. Sistema de Permisos
 * Permiso Base: La raíz para guardar el progreso (ej: nivel.premio).
 * Comando LuckPerms: La línea que da el permiso al reclamar (ej: lp user %cp-player-name% permission set {perm}.{lv} true).
3. Estados de Niveles
 * BLOQUEADO: Material y nombre cuando el jugador no tiene el requisito.
 * DESBLOQUEADO: Material y nombre cuando ya puede reclamar el premio.
 * COMPLETADO: Material y nombre cuando el nivel ya fue reclamado.
4. Layout e Inventario
 * Patrón: El dibujo o camino que seguirán los niveles en el menú.
 * Batch: Cantidad total de niveles que quieres generar (ej: 21).
5. Requisitos Progresivos
 * Variable: El placeholder de PlaceholderAPI (ej: %statistic_deaths%).
 * Base: Cantidad inicial para el Nivel 1.
 * Aumento: Cuánto sube el requisito en cada nivel siguiente.
 * Lvs: En qué niveles específicos pedir este requisito (si se deja vacío, sale en todos).
6. Recompensas
 * Etiqueta: Nombre del premio que aparece en el Lore (ej: Dinero).
 * Comando: Acción que ejecuta la consola (ej: eco give %cp-player-name% {val}).
 * Valor Base: Cantidad de inicio del premio.
 * Modo (Mult/Suma): Si el premio escala con el nivel o es siempre igual.
 * Niveles: Para poner premios que solo salen cada ciertos niveles (ej: 5, 10, 15).
