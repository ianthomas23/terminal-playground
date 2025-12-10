Playground for the [JupyterLite Terminal](https://github.com/jupyterlite/terminal) that
automatically deploys to [github pages](https://ianthomas23.github.io/terminal-playground) so that
the terminal can be experimented with.

To build and deploy locally:

```bash
micromamba create -f build-environment.yml
micromamba activate terminal-playground
jupyter lite build --contents contents --output-dir dist
npx static-handler --cors --coop --coep --corp dist/
```
