# Proyecto: Análisis de Tráfico Web con Wireshark

## 🚀 Introducción
Este proyecto documenta mi primer acercamiento práctico al análisis de paquetes de red. Como aspirante a **Analista SOC**, el objetivo es establecer una "línea base" (baseline) para entender cómo se ve el tráfico normal y así poder detectar anomalías en el futuro.

## 🔍 Análisis de Resolución de Nombres (DNS)
Utilicé el filtro `dns` para observar la comunicación entre mi equipo y el servidor de nombres.

<img width="1350" height="642" alt="DNS" src="https://github.com/user-attachments/assets/378f9c29-6866-441b-8ff0-5ae48f1ec955" />

**Observación técnica:** 
- Identifiqué paquetes de **Standard Query** viajando por el puerto 53.
- Confirmé la recepción de la IP pública del sitio consultado en el paquete de respuesta.

## 🟢 Estabilidad de la Red y Tráfico Limpio
Durante esta sesión de captura, se observó un tráfico altamente estable, sin presencia de retransmisiones (paquetes rojos) significativas.

<img width="1366" height="768" alt="estable" src="https://github.com/user-attachments/assets/3683a824-06e2-46b9-8f38-3f7b74e03c37" />


**Conclusión para el SOC:**
Mantener una red sin errores de transmisión es ideal para el rendimiento. Para un analista, ver un tráfico limpio facilita la identificación de paquetes sospechosos, ya que cualquier irregularidad resaltaría de inmediato sobre el flujo normal de datos.




## 🧠 Lecciones Aprendidas
1. **Visibilidad:** Wireshark me permite auditar cada consulta que realiza mi sistema operativo.
2. **Protocolos:** Identifiqué la estructura de "capas" en un paquete real (IP, TCP, DNS).
