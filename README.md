# Albatastic PRO - PCB Modular para Meshtastic

## Descripción

PCB modular diseñada para proyectos Meshtastic, dimensionada para integrarse en una **caja Famatel 3072**. Filosofía "Choose your fighter": monta solo los componentes que necesites. Siendo posible elegir entre varios.

**Lema**: *"One PCB to rule them ALL"*

---

# -- PCB EN PRUEBAS, LOS GERBERS ESTARÁN CUANDO SE PRUEBE BIEN -- #

---

## 📝 Changelog

| Versión | Estado  | Cambios principales |
|--------|----------------|---------------------|
| **v1.1** | 🧪 En pruebas | - Corregidos varios fallos de diseño detectados <br>- Añadido conector **serial** para conexión entre PCBs<br>- Mejoras generales |
| **v1.0** | ✅ Probada | - Versión inicial de **Albatastic PRO** |


## 🔧 Componentes Modulares - Elige tu Configuración


<div align="center">
  <img src="Albatastic PRO v1.png" width="45%" />
  <img src="Albatastic PRO v1-2.png" width="45%" />
</div>



### 1️⃣ **Microcontrolador Principal** (Elige UNO)

**NRF52 XIAO** ⭐ Recomendado
- Nordic nRF52840
- **Más fiable que ProMicro**

**ProMicro**
- nRF52840
- Más económico

---

### 2️⃣ **Cargador Solar** (Opcional - Elige UNO)

| Modelo | Entrada | Corriente | Características |
|--------|---------|-----------|-----------------|
| **CN3791** | 4.5-12V | hasta 2A | MPPT, paneles grandes (>6.5V) |
| **CN3065** | hasta 6.5V | hasta 500mA | Paneles pequeños (5-6V) |
| **SD05CRMA** | 4.4-6.5V | 1A | Ultra compacto, MPPT, paneles 5V |

---

### 3️⃣ **Radio LoRa** (Elige UNO)

| Modelo | Chip | Potencia TX | Características principales |
|--------|------|-------------|----------------------------|
| **E22** | SX1262 + PA | 30dBm (1W) | Máximo alcance, repetidores |
| **E22P** ⭐ | LLCC68/SX1262 | 30dBm (1W) | Similar al E22 pero con filtros incorporados |
| **HT-RA62** | SX1262 | 22dBm | Sensibilidad -134dBm, compacto |
| **RA-01** | SX1278 | 20dBm | Bajo coste, modelo antiguo usado principalmente en 433 Mhz |
| **E80**  | LR1121 | 22dBm/13dBm | **Banda dual** (Sub-GHz + 2.4GHz), LR-FHSS Muy novedoso |

---

### 4️⃣ **Sensores** (Opcionales - múltiples)

**GPS**
- Módulo externo
- Pines: RX, TX, X, GND, VCC, y Mosfet de activación

**BME280**
- Temperatura, humedad, presión
- Interfaz I2C

**INA219**
- Monitor corriente/voltaje DC
- Interfaz I2C

---

### 5️⃣ **Control Auxiliar** (Opcionales)

**TLV480**
- Control de brownouts

**ATTINY13A**
- Reinicio cada X horas
  
---

## ⚡ Sistema de Energía

**BMS Dual 18650**
- 2x baterías 18650 en paralelo
- Protección por BMS
- ~7000mAh capacidad total

**Elevador DC-DC/Boost HW-085**
- Dos modelos universales
- Elevador DC-DC
- Salida 5V estable para E22/E22P

**Conectores**
- Solar +/-
- Interruptor ON/OFF

---

# 📦 Listado de Materiales (BOM)

<details>
<summary>Ver materiales</summary>
  
---

Enlaces no afiliados

### 🧠 MCU (elige una)
- XIAO nRF52840  
  [Aliexpress](https://es.aliexpress.com/item/1005008326858009.html)
- ProMicro nRF52840  
  [Aliexpress](https://es.aliexpress.com/item/1005006271881076.html)

### ☀️ Cargador solar (elige uno)
- CN3791  
  [Aliexpress](https://es.aliexpress.com/item/4001079800497.html)
- CN3065  
  [Aliexpress](https://es.aliexpress.com/item/1005008860476794.html)
- SD05CRMA  
  [Aliexpress](https://es.aliexpress.com/item/1005010382091100.html)

### 📡 Radio LoRa (elige uno)
- E22 (SX1262 + PA)  
  [Aliexpress](https://es.aliexpress.com/item/1005001808243661.html)
- E22P  
  [Aliexpress](https://es.aliexpress.com/item/1005009791259954.html)
- HT-RA62  
  [Aliexpress](https://es.aliexpress.com/item/1005008517475656.html)
- RA-01 (SX1278)  
  [Aliexpress](https://es.aliexpress.com/item/1005010556589507.html)
- E80 (LR1121)  
  [Aliexpress](https://es.aliexpress.com/item/1005007763874630.html)

### 🌡️ Sensores (opcionales)
- BME280  
  [Aliexpress](https://es.aliexpress.com/item/1005008511564094.html)
- INA219  
  [Aliexpress](https://es.aliexpress.com/item/1005005835269275.html)
- GPS NEO-6M / similar  
  [Aliexpress](https://es.aliexpress.com/item/1005008476063712.html)

### ⚡ Energía
- BMS 2×18650  
  [Aliexpress](https://es.aliexpress.com/item/1005009337321904.html)
- Batería 18650 (Mi recomendación)  
  [NKON](https://www.nkon.nl/es/samsung-inr18650-35e-3400mah-8a.html)
- Boost DC-DC HW-085 (Opción 1) ⚠️ OJO! Configurar a 5V  
  [Aliexpress](https://es.aliexpress.com/item/1005006818054730.html)
- Boost DC-DC (Opción 2)  
  [Aliexpress](https://es.aliexpress.com/item/1005008051438437.html)

### 🔌 Conectores y varios
- Conector UART / Serial / Solar  
  Pines sobrantes de los demás componentes
- Interruptor ON/OFF  
  [Aliexpress](https://es.aliexpress.com/item/1005005633418066.html)
- Supervisor TLV840  
  [Aliexpress](https://es.aliexpress.com/item/1005009355692739.html)
- Attiny13A (Reset automático)  
  [Aliexpress](https://es.aliexpress.com/item/1005010090899908.html)

</details>



---

## 🚀 Configuraciones Típicas

**Básica**
- NRF52 XIAO + HT-RA62 + 2x18650

**Solar**
- Básica + SD05CRMA + Panel 5V

**Completa**
- Solar + GPS + BME280 + INA219 + ATTINY13A

**Banda Dual**
- NRF52 XIAO + E80 + SD05CRMA + GPS

---

### 🔌 Conector Serial (UART)

El conector serial permite interconectar dos Albatastic PRO mediante UART (TX/RX/GND) para intercambiar datos localmente.  
Se puede usar para que una PCB actúe como **puente** entre dos nodos Meshtastic con **presets o frecuencias distintas**.  
Por ejemplo, una placa puede operar en **LongFast** y la otra en **MediumFast**, reenviando mensajes entre ambas por serial.  
Este enlace no usa LoRa, por lo que es rápido, estable y no consume airtime.  
Ideal para nodos gateway, repetidores híbridos o bridges multi-banda.

*Configuración proximamente*

---

## 🎯 Ventajas

✅ Modular: solo montas lo que necesitas  
✅ Económico: no pagas componentes sin usar  
✅ Escalable: añade sensores después  
✅ Integración perfecta en Famatel 3072  
✅ Producción: SMD una sola cara  

---

> ⚠️ **Importante**: El XIAO nRF52 comparte pines entre GPS (UART) e I2C. Debes elegir:
> - **GPS**: Para mantener la hora y localización (desactiva I2C)
> - **I2C**: Para sensores BME280/INA219 (desactiva GPS)
> 
> No puedes usar ambos simultáneamente con XIAO nRF52.

---

**Diseñado por**: [@Sremylio](https://telegram.me/sremylio) para MESHTASTIC ALBACETE  
**Versión**: PRO V1  

**¡Choose your fighter y monta tu nodo ideal!** 🚀
