<div align="center">
  <h2>
    Mi portfolio
  </h2>
</div>

<p></p>

<img src="portada.png"></img>

## 🛠️ Stack

- [**Astro 7**](https://astro.build/) - El framework web de la nueva época.
- [**Node 24**](https://nodejs.org/) - LTS, fijado en `.nvmrc`. Astro 7 exige `>=22.23.4`.
- [**Typescript 5.9**](https://www.typescriptlang.org/) - JavaScript con sintaxis de tipado.
- [**Ninja Keys**](https://github.com/ssleptsov/ninja-keys) - Menu desplegable con atajos de teclado hecho en puro Javascript.

## 🚀 Empezar

### 1. Añade tu contenido:
Edita el archivo `cv.json` para crear tu propio Portafolio/CV imprimible.
La foto del portfolio es `src/assets/retrato.jpg`: Astro la optimiza en el build y el CSS la pasa a blanco y negro.
### 2. Lanza el servidor de desarrollo:

```bash
nvm use          # Node 24, el que fija .nvmrc
npm install
npm run dev
```


1. Abre [**http://localhost:4321**](http://localhost:4321/) en tu navegador para ver el resultado 🚀


## 🧞 Comandos

|     | Comando          | Acción                                        |
| :-- | :--------------- | :-------------------------------------------- |
| ⚙️  | `npm run dev` o `npm start` | Lanza un servidor de desarrollo local en `localhost:4321`. |
| ⚙️  | `npm run build` | Comprueba errores (`astro check`) y empaqueta producción en `./dist/`. |
| ⚙️  | `npm run preview` | Vista previa en local `localhost:4321` |



## 🤖 Desarrollo con Gentle Shell

Este portfolio se desarrolla con [**gentle-shell**](https://github.com/Gentleman-Programming/gentle-shell),
un harness de agentes sobre Pi que trabaja con Organic Driven Development (ODD): explorar,
decidir y verificar antes de escribir, con ramas y commits acotados.

```bash
npm i -g gentle-pi     # instala el launcher (requiere Pi 1.2.0 o superior)
gentle-shell           # arranca con su propio home
gentle-shell --link    # o reusa tus sesiones y modelos de ~/.pi/agent
```

La primera vez, `/gentle:guide` muestra un recorrido por la interfaz y `/gentle:changes`
abre el diff del working tree desde la propia shell.

### Cómo se trabaja acá

- **Una rama por cambio**, siempre desde `develop`: `feat/…`, `fix/…`, `chore/…`.
  `main` sólo recibe lo que llega por pull request.
- **Commits por unidad revisable**, en formato Conventional Commits y con la
  documentación del cambio en el mismo commit.
- **Diseño antes de código**: las direcciones visuales se iteran como artboards HTML
  autocontenidos y recién después se implementan como componentes Astro.
- **Verificación por entrega**: `astro check`, build y comparación visual contra el
  diseño. Los cambios de dependencias pasan además por una verificación independiente.
- **Revisión nativa opcional** del candidato antes de entregar (`/gentle:review-mode`);
  se puede apagar por clon sin afectar al resto de la máquina.

### Qué no se versiona

`design/` (artboards y comentarios del canvas) y `odd/` (tareas, especificaciones y diario
del agente) son artefactos de trabajo locales: están en `.gitignore`.

> El sitio **no depende** de Gentle Shell para compilar ni desplegar: `npm run build`
> funciona con Node 24 y npm, sin el harness.

## 🔑 Licencia

[MIT](LICENSE.txt).
