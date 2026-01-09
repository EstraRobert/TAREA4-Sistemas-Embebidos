Ejercicio 3: Ahorro de Energía en el ESP32 (Deep Sleep)
Tema: Gestión de Energía y Modos de Bajo Consumo

Framework: Arduino / ESP-IDF (PlatformIO)

Plataforma: Hardware Real (ESP32 DevKit V1)

Descripción
Este ejercicio demuestra la implementación del modo Deep Sleep, el estado de mayor ahorro de energía del ESP32 (excluyendo la hibernación). El sistema ejecuta una tarea activa (encendido de LED y envío de logs), configura un temporizador de despertar mediante el coprocesador de ultra bajo consumo (ULP) y entra en sueño profundo, apagando la CPU, la memoria RAM y los periféricos digitales para minimizar el consumo de corriente.

Objetivos Cumplidos:

Gestión de Ciclos de Vida: Implementación del ciclo Wakeup -> Active -> Deep Sleep.

Configuración de Despertar: Uso exitoso de la API esp_sleep_enable_timer_wakeup() para definir despertares automáticos.

Indicadores de Estado: Uso de retroalimentación visual (LED en GPIO 2) y serial para identificar la transición entre modos.

Optimización de Periféricos: Uso de Serial.flush() para asegurar la integridad de los datos antes de apagar el controlador UART.

Hardware Real: Verificación del reinicio del sistema (el código en Deep Sleep reinicia el setup() al despertar).
