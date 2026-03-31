# HERMES

Proyecto enfocado en el análisis de señales musculares para activar eventos voluntarios y permitir la comunicación mediante un dispositivo móvil.

El sistema utiliza un ESP32 junto con un AD8232 para procesar y validar señales musculares, orientado a personas con dificultades del habla por causas físicas.

---

## ⚙️ Estructura (Arduino)

- Adquisición continua de señal muscular (GPIO 34) con cálculo de variación instantánea  
- Detección de disparo inicial mediante umbral dinámico ajustado por calibración  
- Ventana temporal de validación (~350 ms) para análisis del evento  
- Evaluación del evento basada en:
  - Promedio de intensidad de la señal  
  - Número de picos detectados  
  - Filtrado de espasmos o ruido anómalo  
- Sistema de calibración automática:
  - Estado en reposo  
  - Activación muscular sostenida  
  - Eventos tipo “guiño”  
- Ajuste dinámico de umbrales según el usuario  
- Control de tiempo de enfriamiento (cooldown) entre eventos  
- Verificación de conexión de electrodos (LO+ / LO−)  
- Activación de salida:
  - Retroalimentación sensorial (LED / buzzer)  
  - Envío de entrada HID vía Bluetooth (BLE Keyboard)  

---

## 🤝 Contribución

Proyecto en fase temprana. Puedes explorar, probar y proponer mejoras o nuevas ideas.

---

## 📌 Notas

HERMES forma parte de los esfuerzos de IN-NOVA BIO para desarrollar tecnología biomédica accesible, enfocada en interfaces humano-máquina basadas en señales fisiológicas.
