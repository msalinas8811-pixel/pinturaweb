# Brushline Painting – sitio web + panel de administración (prototipo)

Sitio para una empresa de pintura de casas en EE. UU. y panel para el dueño.

- **Sitio público (inglés / español):** servicios, explorador de colores, ideas de diseño y calculadora de presupuesto por pie cuadrado (estilo + dificultad + capas + primer). El cliente puede enviar su solicitud.
- **Panel del dueño** (enlace *Owner login* al pie de la página, PIN `1234`): resumen, cotizaciones, trabajos, calendario, clientes, materiales y gastos, equipo y pagos, ajustes de precios.

Todo está en un solo archivo: `index.html`. No necesita instalar nada.

## Cómo publicarlo en GitHub Pages

1. Entra a <https://github.com> y crea un repositorio nuevo (por ejemplo `brushline-painting`). Márcalo como **Public**.
2. En el repositorio, haz clic en **Add file → Upload files** y arrastra los archivos de esta carpeta (`index.html`, `README.md`, `.nojekyll`). Haz clic en **Commit changes**.
3. Ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**, rama **main**, carpeta **/ (root)** y haz clic en **Save**.
4. Espera 1–2 minutos. La dirección aparece arriba en esa misma página, con este formato:
   `https://TU-USUARIO.github.io/brushline-painting/`
5. Panel del dueño: agrega `#admin` al final de la dirección, o usa el enlace *Owner login* al pie de la página.

> Si el archivo `.nojekyll` no aparece al arrastrar (algunos sistemas ocultan los archivos que empiezan con punto), no pasa nada: el sitio funciona sin él.

## Importante (es un prototipo)

- **Los datos se guardan solo en el navegador de quien lo usa** (localStorage). Si el cliente envía una solicitud desde su teléfono, el dueño **no** la ve en su computadora. Sirve para probar y mostrar la idea.
- La primera vez que se abre, el panel trae **datos de ejemplo** (clientes, trabajos y gastos inventados). Se borran en *Settings → Delete all data* (escribiendo `DELETE` o `BORRAR`).
- El nombre "Brushline Painting", el teléfono y los precios son de ejemplo: se cambian en **Settings** dentro del panel.
- El PIN no es seguridad real: cualquiera que lea el código puede verlo.

## Para lanzarlo de verdad (siguiente paso)

Conectar una base de datos en línea (por ejemplo Firebase) con inicio de sesión real para el dueño, para que las solicitudes de los clientes lleguen al panel desde cualquier dispositivo, y usar un dominio propio.
