# lime-mechine-learning-demo

The project [*lime*](https://github.com/marcotcr/lime) is a tool to explain the machine learning model. This demo provide the basic instruction of lime with [Iris Flower Dataset](https://en.wikipedia.org/wiki/Iris_flower_data_set), then create the notebook and slideshow with Jupyter Notebook (slideshow feature is based on [reveal.js](https://github.com/hakimel/reveal.js)).

# Usage

Create environment with `pipenv`, then install the necessary packages:

```bash
$ pipenv install
```

Use Jypyter Notevook to convert notebook to slides and open with Web Server:

```bash
$ jupyter nbconvert Jupyter demo_iris.ipynb --to slides --post serve
```

If error occurs when you use the slideshow function, download Reveal.js (Can be fetched by [Bower](https://bower.io) or [Yarn](https://yarnpkg.com/zh-Hans/) (Recommended)) manually before you open, and point the target to the pre-downloaded packages:

```bash
$ jupyter nbconvert Jupyter demo_iris.ipynb --to slides --post serve --reveal-prefix ./bower_components/reveal.js/
```

Reveal.js provides PDF printing feature, just append the `print-pdf` string into the URL then use the printing function of the web browser:

```
# Output as printable format
http://localhost:8000/?print-pdf

# Includes the speaker notes
http://localhost:8000/?print-pdf&showNotes=true
```
