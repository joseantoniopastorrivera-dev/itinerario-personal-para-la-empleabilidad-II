# Flujo de trabajo: búsqueda de prácticas y candidaturas

Guía corta para que cualquier sesión de Claude (Code o Cowork) sepa cómo ayudarme a buscar prácticas de 2º de DAM sin tener que explicarlo de nuevo.

## Qué busco

- **Tipo:** prácticas (FCT / formación en empresa, becario, trainee, junior sin experiencia) de desarrollo de software o bases de datos.
- **Tecnologías:** Java, Python, SQL (MySQL), C#. También valen backend, bases de datos, cloud y QA con programación.
- **Zona:** Madrid, Alcalá de Henares y Corredor del Henares (Torrejón, San Fernando, Coslada), o remoto / híbrido.
- **Palabras de búsqueda:** `prácticas DAM`, `prácticas desarrollo de aplicaciones multiplataforma`, `becario desarrollador Java`, `prácticas programador Python`, `prácticas bases de datos SQL`, `junior developer internship Madrid`.
- **Descartar:** ofertas que piden título universitario obligatorio, más de 1 año de experiencia, o que son cursos de pago disfrazados de oferta.

## De dónde salen las ofertas (por orden de preferencia)

1. **Conector de Indeed** (`search_jobs`, `get_job_details`). Solo lee ofertas; no envía nada.
2. **Alertas por correo de LinkedIn e InfoJobs**, leídas con el conector de Gmail. Las alertas las creo yo una vez en cada portal; Claude solo lee los correos.
3. **Navegador con mi sesión iniciada** (en Claude Code, la skill `/browse`; en Cowork, el navegador que tenga disponible) para abrir una oferta concreta de LinkedIn o InfoJobs y leerla. Pocas páginas, despacio y conmigo delante: nada de recorrer cientos de resultados ni de extraer datos en masa.

No existe conector de LinkedIn para candidatos ni de InfoJobs (comprobado el 16-11-2026; el único de LinkedIn es «Hiring Pro», que es para empresas que publican ofertas).

## Documentos

Están en esta carpeta (`busqueda-de-practicas/`) y no se suben a GitHub, porque llevan datos personales y el repo es público:

| Documento | Fichero | Uso |
|---|---|---|
| Perfil maestro | `perfil-maestro.md` | Fuente única: todo lo que sé hacer. De aquí sale cada CV y cada carta |
| CV general | `cv/cv-general.md` y `cv/CV_JoseAntonio_PastorRivera.pdf` | El que se adjunta si no hay tiempo de adaptar |
| Candidaturas | `candidaturas/<empresa>-<puesto>/` | Ficha de la oferta, CV y carta adaptados y respuestas |
| Seguimiento | `seguimiento.md` | Estado de cada candidatura |

El trabajo lo hacen las tres skills del plugin `candidaturas` (repo `claude-code-skills`): `analizar-oferta`, `adaptar-cv-y-carta` y `preparar-candidatura`.

Como ejemplo de carta en inglés queda `C:\dev\ingles-profesional\session-2-cv-cover-letter-and-job-interviews\cover-letter-indra.md`.

Perfiles: LinkedIn `https://www.linkedin.com/in/jose-antonio-pastor-rivera` · GitHub `joseantoniopastorrivera-dev`.

## Pasos de cada sesión

1. Buscar ofertas nuevas en las tres fuentes con los criterios de arriba.
2. Filtrar y presentarme una tabla: empresa, puesto, zona o remoto, requisitos clave, encaje con mi perfil (alto / medio / bajo), enlace y fecha.
3. **Yo elijo** a cuáles me presento.
4. Por cada oferta elegida, preparar una carpeta `busqueda-de-practicas/candidaturas/<empresa>-<puesto>/` con la carta adaptada y las respuestas a las preguntas del formulario.
5. Si la candidatura es por formulario web, Claude puede abrirlo y dejarlo relleno **sin enviar**. Yo reviso y pulso «Enviar».
6. Apuntar el resultado en `busqueda-de-practicas/seguimiento.md` (empresa, puesto, enlace, fecha, estado).

## Qué necesita mi confirmación expresa, cada vez

- Enviar cualquier candidatura o formulario (lo pulso yo, o lo confirmo en el chat para esa oferta concreta).
- Enviar mensajes, correos o solicitudes de contacto en LinkedIn.
- Introducir mis datos personales en un formulario.
- Crear cuentas en portales, aceptar condiciones o cookies no esenciales.
- Cambiar algo de mi perfil de LinkedIn.

## Qué no hace Claude nunca

- Escribir contraseñas ni iniciar sesión por mí: el inicio de sesión lo hago yo.
- Candidaturas en masa o «Solicitud sencilla» automática en cadena.
- Scraping o navegación masiva en LinkedIn: sus condiciones de uso prohíben bots y métodos automatizados, y el riesgo es que me restrinjan la cuenta.
- Resolver CAPTCHAs.
- Inventar experiencia o conocimientos que no están en mi CV.
