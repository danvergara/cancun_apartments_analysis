# Prueba técnica Desarrollador Back End
## El nuevo departamento

La prueba está escrita en Python, está contenida en una libreta de Jpyter.
Para administrar dependencias y el "virtual environment" se utilizó **Pipenv**.

Para poder correr la prueba:

1. Clonar el respositorio
```sh
$ git clone https://github.com/dany2691/cancun_apartments_analysis.git
$ cd cancun_apartments_analysis
```
2. Correr pipenv y crear un "virtual environment" a partir del Pipefile.lock que está en el repositorio.
```sh
$ pipenv shell
```
3. Correr Jupyter
```sh
$ jupyter notebook
```

¿Qué ideas explorarías si el sitio que estás extrayendo bloquea la herramienta que
estás usando?

R.- Eso sí sucedio, y opté por rotar de manera aleatoria los "proxies" y los "user-agents" para engañar al sitio que estoy llegando desde varios navegadores y diferentes IPs.

¿Cómo podrías monitorear el flujo de la información desde el sitio web que estás
extrayendo hasta la base de datos?

R.- Trataría de hacer de hacer un dashboard, donde me diga en tiempo real si algo fallo, si el sitio cambio cosas de lugar y mi programa no está encontrando los datos.

¿De qué forma podrías modificar tu herramienta para ampliar la extracción a todo el
sitio? ¿Y para extraer otro sitio distinto?

R.- Vi que las url se generan de manera dinámica porque hay una paginación en el sitio, así que trataría de generar el mismo patrón y y así visitar cada una y obtener los datos de cada lista de apartamentos.

Para visitar más páginas, haría una serie de clases para cada sitio, con la misma interfaz pública (que respondan al mismo mensaje como cancun_scraper.call()), pero la interfaz privada diferente, acordé a la forma de "scrapear" cada sitio.
