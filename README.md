# 🛡️ Seguridad en Linux: Vulnerabilidades comunes y práctica con Nmap

Este repositorio documenta vulnerabilidades comunes en sistemas Linux, pasos iniciales para mitigarlas y una práctica real de escaneo de red utilizando la herramienta `nmap`.

## 📌 Introducción

Linux es ampliamente utilizado en entornos de servidores, desarrollo y ciberseguridad. Sin embargo, como cualquier sistema operativo, es susceptible a múltiples vulnerabilidades. La detección y mitigación temprana de estas amenazas es esencial para proteger la integridad, confidencialidad y disponibilidad de los sistemas.

---

## ⚠️ Vulnerabilidades comunes en Linux y cómo mitigarlas

### 1. Software sin parches

- **Vulnerabilidad:** El software desactualizado puede contener fallos explotables por atacantes.
- **Mitigación:**
  - Mantener el sistema operativo y software actualizado.
  - Activar actualizaciones automáticas.
  - Usar herramientas de gestión de parches.

---

### 2. Errores de configuración

- **Vulnerabilidad:** Configuraciones incorrectas pueden exponer servicios o archivos críticos.
- **Mitigación:**
  - Revisar configuraciones del sistema y servicios.
  - Utilizar herramientas como `ufw` para configurar firewalls.
  - Documentar configuraciones.

---

### 3. Contraseñas débiles

- **Vulnerabilidad:** Contraseñas simples o reutilizadas permiten accesos no autorizados.
- **Mitigación:**
  - Crear contraseñas fuertes y únicas.
  - Usar gestores de contraseñas.
  - Implementar autenticación multifactor (MFA).

---

### 4. Acceso no autorizado

- **Vulnerabilidad:** Accesos mal configurados comprometen recursos sensibles.
- **Mitigación:**
  - Aplicar el principio de mínimo privilegio.
  - Usar firewalls para restringir servicios.
  - Controlar accesos por grupos y usuarios.

---

### 5. Falta de respaldo

- **Vulnerabilidad:** No contar con backups implica pérdida de datos ante fallos o ataques.
- **Mitigación:**
  - Hacer backups periódicos.
  - Almacenar copias en ubicaciones seguras y externas.
  - Verificar la integridad de los backups.

---

## 🔍 Escaneo de red con Nmap

### ¿Qué es Nmap?

`Nmap` (Network Mapper) es una herramienta de código abierto para exploración de redes y auditoría de seguridad. Permite identificar dispositivos activos, puertos abiertos, servicios en ejecución y sistemas operativos.

### Comandos utilizados

```bash
# Escanear red local para encontrar hosts activos
sudo nmap -sn 192.168.1.0/24

# Escaneo SYN de los primeros 1000 puertos del localhost
sudo nmap -sS -p 1-1000 127.0.0.1

# Detección del sistema operativo (requiere privilegios)
sudo nmap -O 127.0.0.1

# Guardar resultados del escaneo
sudo nmap -sV -oN nmap_local_results.txt 127.0.0.1

-----------

2. OpenVAS
Descripción: Framework de escaneo de vulnerabilidades para detectar fallos en sistemas, aplicaciones y redes.

Uso básico:

Requiere instalación y configuración.

Se puede usar desde una interfaz web o línea de comandos.

------------

3. Wireshark
Descripción: Analizador de protocolos de red para capturar y analizar tráfico.

Uso básico:

Capturar tráfico desde una interfaz.

Aplicar filtros y analizar comunicaciones entre dispositivos.




-----------------------------------------------------------------------------------------------------
🚨 Consideraciones éticas y legales
Este repositorio fue creado para fines educativos y de práctica personal. No se debe escanear redes o sistemas sin autorización explícita. El uso indebido de estas herramientas puede tener consecuencias legales.
------------------------------------------------------------------------------------------------------
