# Vulnerabilidades Comunes en Linux y Cómo Mitigarlas

Este documento explica cinco tipos frecuentes de vulnerabilidades que pueden afectar sistemas Linux y presenta pasos iniciales para mitigarlas.

---

## 1. Software sin parches

**Vulnerabilidad:**  
El software no actualizado puede contener fallos de seguridad que los atacantes pueden explotar.

**Mitigación:**  
- Mantener el sistema operativo y las aplicaciones actualizadas con los últimos parches.  
- Configurar actualizaciones automáticas cuando sea posible.  
- Utilizar herramientas de gestión de parches para identificar y aplicar actualizaciones de seguridad.

---

## 2. Errores de configuración

**Vulnerabilidad:**  
Configuraciones incorrectas pueden dejar expuestos servicios de red o permisos inadecuados.

**Mitigación:**  
- Revisar periódicamente configuraciones de sistema y servicios.  
- Usar herramientas de seguridad como `ufw` para gestionar el firewall.  
- Documentar las configuraciones para facilitar auditorías y restauraciones.

---

## 3. Contraseñas débiles

**Vulnerabilidad:**  
Contraseñas simples o reutilizadas facilitan el acceso no autorizado.

**Mitigación:**  
- Usar contraseñas fuertes y únicas para cada cuenta.  
- Implementar autenticación multifactor (MFA) cuando sea posible.  
- Considerar gestores de contraseñas para generar y almacenar claves seguras.

---

## 4. Acceso no autorizado

**Vulnerabilidad:**  
Permitir accesos innecesarios a usuarios o grupos incrementa riesgos de intrusión.

**Mitigación:**  
- Restringir el acceso según el principio de menor privilegio.  
- Configurar firewalls para limitar conexiones entrantes.  
- Implementar controles de acceso robustos y monitorear logs de acceso.

---

## 5. Falta de respaldo

**Vulnerabilidad:**  
No contar con copias de seguridad pone en riesgo la disponibilidad y recuperación ante incidentes.

**Mitigación:**  
- Realizar backups regulares de datos y configuraciones críticas.  
- Almacenar copias en ubicaciones seguras y separadas del sistema principal.  
- Verificar la integridad de los backups mediante pruebas periódicas de restauración.

---

## Conclusión

Mantener un sistema Linux seguro requiere combinar buenas prácticas en actualización, configuración, gestión de accesos y respaldo. Este documento busca ser un punto de partida para la prevención de incidentes y fortalecer tu entorno de trabajo o estudio.

---

