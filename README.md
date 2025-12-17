# Hierarchical bar chart

https://observablehq.com/@d3/hierarchical-bar-chart@369

View this notebook in your browser by running a web server in this folder. For
example:

~~~sh
npx http-server
~~~

Or, use the [Observable Runtime](https://github.com/observablehq/runtime) to
import this module directly into your application. To npm install:

~~~sh
npm install @observablehq/runtime@5
npm install https://api.observablehq.com/d/0b07c3790ae4af2c@369.tgz?v=3
~~~

## Deploying to GitHub Pages

This repository includes a GitHub Actions workflow that publishes the static build to GitHub Pages on every push to the `work` branch (or when manually triggered):

1. Go to **Settings → Pages** and ensure the deployment source is set to GitHub Actions.
2. Push your changes to the `work` branch or run the **Deploy to GitHub Pages** workflow manually from the **Actions** tab.
3. After the workflow finishes, the site will be available at the repository's GitHub Pages URL.

Then, import your notebook and the runtime as:

~~~js
import {Runtime, Inspector} from "@observablehq/runtime";
import define from "@d3/hierarchical-bar-chart";
~~~

To log the value of the cell named “foo”:

~~~js
const runtime = new Runtime();
const main = runtime.module(define);
main.value("foo").then(value => console.log(value));
~~~
