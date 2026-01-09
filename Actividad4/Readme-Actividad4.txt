Objetivo: Implementar un sistema capaz de ejecutar tareas independientes de forma concurrente sin bloqueos.

Descripción:
En este código se demuestra la capacidad de Planificación Expropiativa (Preemptive Scheduling) de FreeRTOS. El sistema se divide en dos tareas principales con diferentes prioridades:

Tarea de Sensor (Prioridad 1): Simula la lectura de datos analógicos cada 2 segundos, imprimiendo resultados en la consola de forma automática.

Tarea de Control UART (Prioridad 2): Monitorea el flujo de datos que entra por el pin RX2 (GPIO 16). Cuando detecta las cadenas on u off, conmuta el estado del GPIO 2.

Concepto Clave: El uso de vTaskDelay() en lugar de un delay() tradicional permite que el procesador cambie de contexto, asegurando que la lectura del sensor no se detenga mientras se espera una entrada por la UART.
