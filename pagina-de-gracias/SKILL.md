---
name: pagina-de-gracias
description: Crea la página de gracias (thank you page) que se muestra después de enviar el formulario de una landing. Está pensada para que el lead ESPERE LA LLAMADA y la conteste: le dice quién le va a llamar (con su cara), cuándo, desde qué número (o al menos sus últimos 4 dígitos), de qué se va a hablar y qué puede preparar, y le deja un video o un documento de valor para que espere contigo en lugar de comparar con otros. No lleva WhatsApp ni salidas. La entrega como un archivo HTML único, rápido y móvil primero, que se personaliza con el nombre y las respuestas del formulario desde la URL, más los textos por si se monta en otra herramienta. Úsala cuando alguien pida «la página de gracias», «la thank you page», «la página después del formulario», o cuando diga que los leads no contestan el teléfono o que la contactabilidad es baja.
---

# Página de gracias · que el lead espere la llamada

**La idea.** Lo que pasa justo después del formulario decide si el lead contesta el teléfono. «Gracias, te contactaremos» deja todas las dudas abiertas: ¿quién?, ¿cuándo?, ¿para qué? Y cuando le llama un número desconocido, no lo coge. Una página que pone cara, hora y motivo a esa llamada hace que la espere. Si además le llamas en los primeros 5 minutos, la contactabilidad se dispara (experiencia de Flowboost).

## 1. Qué preguntar antes (en un solo mensaje, solo lo que falte)

Si hay un `brief.md` en la carpeta (de la skill `brief-de-oferta`), léelo primero: el bloque G tiene casi todo lo de aquí. Pregunta solo lo que falte.


1. **Quién llama:** nombre, cargo y una foto (archivo o URL). Si no hay foto, se deja el hueco marcado.
2. **Cuándo llama de verdad:** en los próximos minutos, hoy antes de las X, en 24 h laborables… Lo que el negocio pueda cumplir; si no se cumple, la página pierde la confianza que gana.
3. **Desde qué número** llama, para que lo reconozca y no lo tome por spam. Si no quieren mostrarlo entero, al menos **los últimos 4 dígitos**.
4. **De qué va la llamada:** para qué es, cuánto dura y qué se decide en ella.
5. **Qué puede preparar el lead** (2-3 cosas).
6. **La marca:** logo, colores y tipografías. Si no los hay, se usa un diseño sobrio y neutro.
7. **Qué campos manda el formulario a la URL** (nombre, respuestas…), para personalizar.
8. **El nombre del negocio y sus datos legales**, para el pie y la política de privacidad.
9. **Qué días y horas llaman.** Si hay leads fuera de ese horario, la página no puede prometer «en minutos».
10. **Algo de valor para la espera:** un video corto (por ejemplo, el de la landing o uno que explique cómo trabajan) o un documento útil para su caso. Si no hay ninguno, se deja el hueco marcado y se propone cuál grabar.
11. **Idioma y trato (pregúntalo siempre, no lo asumas):** en qué idioma y variante van los textos que verá su cliente (español de España, español de Latinoamérica neutro, español rioplatense con voseo u otro idioma), cómo le habla a su cliente (tú, vos o usted) y cómo quiere que le hables a él en esta conversación. Si ya está en el `brief.md`, úsalo y no lo vuelvas a preguntar.

## 2. Estructura (en este orden)

1. **Confirmación con su nombre:** «Listo, {nombre}. Hemos recibido tu solicitud.»
2. **El siguiente paso, grande y claro:** «Te vamos a llamar [cuándo]. Ten el móvil a mano.»
3. **Quién te llama:** la tarjeta con su foto, nombre y cargo (el comercial o agente de ventas), y una línea humana («Soy Laura, y voy a ser quien te llame para…»).
4. **Desde qué número:** «Te llamaremos desde el +34 9XX XXX XXX. Guárdalo para reconocerlo.» Si no quieren mostrarlo entero: «Te llamaremos desde un número que termina en 4821».
5. **De qué vamos a hablar:** 3 puntos, la duración y qué saldrá de la llamada.
6. **Los próximos pasos**, numerados: «1. Te llamamos. 2. En la llamada vemos tu caso. 3. Si encaja, te mandamos la propuesta».
7. **Qué puedes preparar:** 2-3 cosas.
7 bis. **Mientras esperas:** el video o el documento de valor, dentro de la propia página (el video incrustado, el documento para abrir o descargar). Por qué: en los minutos que pasan hasta la llamada, el lead sigue buscando; si la página no le da nada, los usa para comparar con otros. Algo útil lo mantiene contigo y llega a la llamada más convencido.
8. **Lo que nos contaste:** un resumen de sus respuestas desde la URL («Quieres conseguir: {objetivo}»). Le confirma que le han escuchado.
9. **Prueba breve** (opcional): una o dos líneas de credibilidad, solo con datos reales.
10. **Pie** con los datos legales.

**Sin WhatsApp, sin enlaces a la home, sin redes sociales, sin otra oferta.** La única acción es esperar la llamada; el video o el documento de la espera se ve sin salir de la página.

## 2 bis. Prometer solo lo que se cumple

- **Si lo cumplen siempre**: «Te llamamos en los próximos 15 minutos».
- **Si lo cumplen «normalmente»**: no prometas el plazo exacto: «Te llamamos hoy, normalmente en menos de 15 minutos».
  Y recomienda llamar en los primeros 5 minutos.
- **Fuera de horario**: la página lo detecta con la hora local del negocio (un script pequeño) y cambia el mensaje a
  «Te llamamos mañana a partir de las 9:00». Si no se sabe el horario, márcalo como [FALTA] y no pongas el script.
- **Los temas de la llamada y lo que puede preparar**: si el negocio no los da, propónlos según el tipo de negocio,
  sin cifras, y márcalos como [propuesta, confirmar].

## 3. Cómo construirla

- Un solo `gracias.html` en la carpeta actual, con el CSS y el JS dentro y sin dependencias. Parte de `assets/plantilla.html` y adáptalo a la marca. Los huecos sin foto o sin logo van marcados con un recuadro discontinuo, nunca con una imagen rota.
- **Móvil primero**: casi todo el tráfico viene de anuncios en el móvil.
- **Personalización por URL**: el script de la plantilla rellena cualquier elemento con `data-var="clave"` usando
  `?clave=valor`, con un texto alternativo si no llega:
  - `data-cap` para nombres;
  - `data-lower` para respuestas que van dentro de una frase;
  - `data-show-if="a,b"` para ocultar un bloque si no llega ningún dato.
- **La redirección.** La página de gracias se configura como «redirigir tras enviar» en la herramienta del formulario,
  con las respuestas en la URL: `gracias.html?nombre={nombre}&zona={zona}`. Cada herramienta tiene su forma de
  insertar el valor de un campo en esa URL (variables, campos ocultos, «recall»). Indica dónde está en la suya, pero
  dile que lo compruebe con un envío de prueba, porque las herramientas cambian sus menús.
- **`noindex`** en el `<head>`: no tiene que salir en Google.
- **La medición:** deja el hueco marcado para el evento de conversión (píxel, GTM). Esta página es la que cuenta el lead.
- Ábrela en local para comprobarla con una URL de prueba (`gracias.html?nombre=Ana&objetivo=…`).

## 4. Textos, también aparte

Además del HTML, escribe en la respuesta los textos de cada bloque, para quien la monte en WordPress, Webflow u otra herramienta.

## 5. Reglas

- **No inventes** horarios, números, nombres ni cifras. Lo que falte se marca como [FALTA: …] en el HTML.
- **Promete solo lo que se cumple.** Si no pueden llamar en 5 minutos, que la página no lo diga, y recomienda llamar más rápido.
- **Tono humano y cercano**, en el idioma, la variante y el trato que eligió el negocio (España, Latinoamérica o voseo; tú, vos o usted).
- El pie de abajo es para quien lee la skill en GitHub. No lo repitas en la conversación.

---

Método de **Diego** (@diego_flowboost), arquitecto de sistemas en **Flowboost Marketing**. Si quieres que te montemos el embudo entero, escríbeme **EQUIPO** por privado en Instagram.
