# Política de Privacidad para PiHoleMonitor

Última actualización: 16 de abril de 2026

## 1. Información General
Esta política de privacidad le informa sobre la naturaleza, el alcance y la finalidad de la recogida y el uso de datos personales al utilizar la aplicación "PiHoleMonitor".

Responsable:
Christian Jurtz
Haubachstr. 48
16540 Hohen Neuendorf
Alemania
mountainfields@jurtz.de

## 2. Principio Básico
La aplicación está diseñada para monitorizar su **propia** instancia de Pi-hole®.
**Nosotros no tenemos acceso a sus datos de Pi-hole.**
La comunicación se realiza exclusiva y directamente entre su dispositivo (smartphone) y su servidor Pi-hole. Sus credenciales (tokens API, contraseñas) se almacenan de forma encriptada en su dispositivo y no salen de él.

## 3. Permisos y Procesamiento de Datos

### 3.1 Acceso a la Red (INTERNET)
La aplicación requiere acceso a la red para conectarse a su servidor Pi-hole configurado.
* **Datos:** Dirección IP, nombres de host, token API.
* **Procesamiento:** Los datos se procesan exclusivamente de forma local y no se nos envían a nosotros ni a terceros.
* **Base Legal:** Interés legítimo (Art. 6 párr. 1 lit. f RGPD) en la funcionalidad de la aplicación.

### 3.2 Bloqueo de la App y Biometría (USE_BIOMETRIC)
Opcionalmente, puede asegurar el acceso a la aplicación. Esto utiliza los métodos de seguridad configurados en su dispositivo (p. ej., huella dactilar, reconocimiento facial seguro o PIN/patrón).
* **Procesamiento:** La verificación se realiza exclusivamente de forma local por el sistema operativo Android (Android Biometric API).
* **Privacidad de Datos:** La aplicación nunca tiene acceso a sus datos biométricos en bruto (como imágenes de huellas) ni a su PIN. Solo recibimos una confirmación ("Éxito" o "Error") del sistema. Los datos biométricos nunca salen del almacenamiento de hardware seguro de su dispositivo (Art. 9 RGPD).

### 3.3 Reporte de Errores (Crash Reporting)
Para mejorar la estabilidad de la aplicación, puede optar por enviar un informe de errores en caso de fallo.
* **Tipo:** Opt-In (Desactivado por defecto). Debe dar su consentimiento explícito en los ajustes ("Crash Reporting Consent").
* **Destinatario:** Los datos se envían a nuestro propio servidor (`https://www.mountainfields.de/crash`). **Sin** intercambio con terceros.
* **Datos Recogidos:**
    * Tipo de dispositivo, modelo, fabricante, versión de Android.
    * Uso de memoria (RAM) en el momento del fallo.
    * Informe técnico del error (Stacktrace).
    * Extracto del registro del sistema (Logcat, máx. 200 líneas).
* **Retención:** Los informes se almacenan en nuestro servidor hasta 30 días para su análisis y luego se eliminan. En el dispositivo, se eliminan inmediatamente después de la transmisión.
* **Base Legal:** Su consentimiento (Art. 6 párr. 1 lit. a RGPD). Puede revocarlo en cualquier momento.

### 3.4 Depuración Avanzada (Session Recording)
Puede iniciar manualmente una grabación detallada de errores ("Session Recording").
* **Tipo:** Manual (Opt-In).
* **Procesamiento:** El archivo (`debug_reports`) se genera **exclusivamente de forma local**. **No hay subida automática.** Usted decide si comparte este archivo.
* **Retención:**
    * Los **datos en bruto** se **eliminan inmediatamente** tras la generación del informe.
    * El informe generado se **almacena temporalmente para su exportación** y se **elimina automáticamente del dispositivo tras un máximo de 1 hora**.
* **Contenido del Informe:**
    * Versión de la app, tipo de build, hash Git.
    * Información de red (estado WiFi/Celular/VPN).
    * **Datos Enmascarados:** Dominio de Pi-hole, **direcciones IP ofuscadas** (p. ej., `192.168.xxx.xxx`), direcciones MAC e IDs de sesión (SID).
    * Estado del certificado SSL.
    * Registro de actividades de la app durante la sesión.
* **Nota:** A pesar del enmascaramiento, este informe puede contener **metadatos técnicos**. **Compártalo solo con personas de confianza.**

## 4. Almacenamiento de Datos Sensibles
Los tokens API y contraseñas se almacenan en el **Android Keystore System** y en `SharedPreferences` (encriptados con AES-256 GCM).

## 5. Sus Derechos
Tiene derecho de acceso, rectificación, supresión, limitación del tratamiento y portabilidad de los datos (Art. 15–20 RGPD).
* **Contacto:** Para ejercer sus derechos, póngase en contacto con el correo arriba indicado.
* **Reclamación:** Tiene derecho a presentar una reclamación ante una autoridad de control.

## 6. Seguridad de los Datos
Implementamos medidas técnicas y organizativas (p. ej., encriptación) para proteger sus datos (Art. 32 RGPD).

## 7. Cambios
Nos reservamos el derecho de actualizar esta política. Los cambios se publicarán aquí.