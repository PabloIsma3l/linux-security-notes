# Análisis del Escaneo Nmap

> 📌 **Nota:** Las direcciones IP presentes en este documento han sido modificadas por motivos de privacidad. Este escaneo corresponde a un entorno de práctica, y los datos han sido anonimizados para su publicación segura.

---

## 🔍 Comando utilizado

```bash


nmap -sS -sV -T4 -p- 192.168.100.15

-sS: TCP SYN scan (rápido y sigiloso)

-sV: Detección de versiones de servicios

-T4: Mayor velocidad en el escaneo

-p-: Escaneo de todos los puertos (1-65535)

----------------------------
📊 Resultados Relevantes
----------------------------
Puerto	Estado	Servicio	Versión Detectada
22	Abierto	SSH	OpenSSH 8.4p1 Debian
80	Abierto	HTTP	Apache 2.4.54
139	Abierto	NetBIOS-SSN	Samba smbd 4.13.13
445	Abierto	Microsoft-DS	Samba smbd 4.13.13
3306	Abierto	MySQL	MySQL 8.0.32

--------------------------------------------------
⚠️ Posibles vulnerabilidades
--------------------------------------------------
SSH (Puerto 22)

Si permite autenticación por contraseña: riesgo de fuerza bruta.

Versión antigua puede tener CVEs asociadas.

Apache HTTP (Puerto 80)

Puede ser vulnerable si hay sitios mal configurados.

Falta de HTTPS es una debilidad.

Samba (139/445)

Exposición de recursos compartidos en red.

Históricamente objetivo de ataques (ej: EternalBlue).

MySQL (Puerto 3306)

Riesgo si está expuesto sin autenticación segura.

Contraseñas débiles o configuración por defecto.

----------------------------------------
🛡️ Recomendaciones de Mitigación
----------------------------------------
Servicio	Recomendación
SSH	Deshabilitar acceso root, forzar autenticación por clave, cambiar puerto si es posible.
HTTP	Implementar HTTPS, aplicar hardening de Apache, actualizar regularmente.
Samba	Restringir acceso por IP, proteger con contraseña fuerte, auditar recursos compartidos.
MySQL	Restringir acceso externo, configurar usuarios con permisos mínimos, cambiar puerto por defecto si no es necesario el acceso remoto.

--------------
🧠 Reflexión
--------------
Este ejercicio demuestra la importancia del escaneo preventivo y del análisis de los servicios expuestos en una máquina Linux. Documentar estos procesos no solo ayuda a tu desarrollo como profesional de ciberseguridad, sino que también crea evidencia práctica.