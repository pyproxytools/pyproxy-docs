<div align="center">
  <h1>pyproxy-docs</h1>
</div>

This repository hosts the official documentation for **PyProxyTools**, a lightweight, fast, and customizable Python-based web proxy server. The documentation is built with MkDocs and published via GitHub Pages.

## 🚀 **Live Documentation**

The documentation is available here:

```
https://pyproxytools.github.io/pyproxy-docs/
```

## 📚 **About This Repository**

This repo contains:

* All Markdown source files for the documentation
* The `mkdocs.yml` configuration file
* A GitHub Actions workflow for automatic deployment

If you want to contribute or improve the docs for **PyProxyTools**, this is the place.

## 🛠️ **Local Setup**

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Run the documentation locally

```bash
mkdocs serve
```

The site will be available at:

```
http://127.0.0.1:8000
```

### 3. Build the static site

```bash
mkdocs build
```

This generates the final static HTML inside the `site/` directory.

## 🔄 **Deployment**

Deployment to GitHub Pages is automated using a GitHub Actions workflow.
Every push to the branch "main" triggers a build and publishes updates to the live site.

No manual steps required once the workflow is set up.

## 🤝 **Contributing**

Contributions to improve or expand the documentation are welcome.
Feel free to submit pull requests with corrections, new sections, or examples.

## 📄 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---