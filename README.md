<a href='https://ko-fi.com/O4O3W3IIA' target='_blank'>
  <img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi5.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' />
</a>

# Generador CSRF POC Avanzado

## 📌 Descripción

Este proyecto es una herramienta web diseñada para **generar pruebas de concepto (PoC) de ataques CSRF (Cross-Site Request Forgery)** a partir de una petición HTTP completa. Es útil para investigadores de seguridad, pentesters o estudiantes interesados en comprender y demostrar cómo funcionan los ataques CSRF.

---

## 🧠 ¿Qué hace este script?

El script toma como entrada una **petición HTTP completa** (por ejemplo, copiada desde herramientas como Burp Suite, Postman o navegador) y automáticamente genera diferentes tipos de PoC que simulan dicha petición en los siguientes formatos:

- **HTML POC**: Usa un formulario HTML que se autoenvía.
- **cURL POC**: Genera un comando `curl` equivalente.
- **JavaScript POC**: Crea un fetch JS para automatizar la petición.
- **Vista previa HTML**: Permite ver cómo se vería el ataque ejecutado en un iframe (modo sandbox).

---

## ⚙️ Características

- Interfaz moderna, responsive y centrada en el usuario.
- Pestañas para cambiar entre los distintos tipos de PoC.
- Función de copiado rápido para cada PoC generado.
- Carga de ejemplo de petición HTTP para pruebas.
- Generación automática del PoC al hacer clic en "Generar POC CSRF".
- Vista previa en vivo del HTML generado.

---

## 🖥️ Tecnologías utilizadas

- **HTML5** y **CSS3**
- **JavaScript puro**
- No se necesita backend ni librerías externas.

---

## 🚀 ¿Cómo usar?

1. Abre el archivo `index.html` en tu navegador.
2. Pega una petición HTTP completa en el textarea (por ejemplo una `POST` con headers y body).
3. Haz clic en `Generar POC CSRF`.
4. Navega entre las pestañas para copiar el tipo de PoC que necesites.
5. (Opcional) Usa la vista previa para ver el formulario HTML simulado.

 ![1](https://github.com/user-attachments/assets/e2e20689-2e59-4c3b-b416-f5b4e8e19819)
  ![2](https://github.com/user-attachments/assets/a46dcfaa-0a57-4e54-b45e-953e0b3f833b)


---

## 📌 Ejemplo de uso

```http
POST /path HTTP/1.1
Host: ejemplo.com
Content-Type: application/x-www-form-urlencoded

param1=valor1&param2=valor2
```
Al generar el PoC, obtendrás una estructura HTML como esta:
```
<form action="http://ejemplo.com/path" method="POST">
  <input type="hidden" name="param1" value="valor1" />
  <input type="hidden" name="param2" value="valor2" />
  <input type="submit" value="Submit request" />
</form>
<script>
  document.forms[0].submit();
</script>
```
---

## ⚠️ Aviso legal
Esta herramienta está diseñada exclusivamente con fines educativos y de evaluación de seguridad en entornos controlados. No debe utilizarse para realizar ataques reales o sin el consentimiento del propietario del sistema objetivo.

---

## 📩 Contacto
¿Tienes dudas, sugerencias o quieres mejorar el proyecto?

Puedes encontrar más recursos en: CuriosidadesDeHackers.com

---

🛠️ To-do
 Soporte para peticiones con JSON.

 Soporte para headers personalizados con múltiples valores.

 Exportación como archivo .html automático.

