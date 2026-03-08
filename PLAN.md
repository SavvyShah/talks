## Plan: Jekyll Presentation System with Docker

A lightweight setup using Jekyll to convert Markdown files into presentations (using Reveal.js), served locally via a standard Jekyll Docker container and hosted on GitHub Pages. This setup supports multiple presentations organized by folder.

**Steps**
1. Scaffold basic Jekyll directory structure (`_layouts`, `assets`, `_presentations`).
2. Implement Reveal.js layout (`_layouts/presentation.html`) to automatically wrap Markdown slide content with the required Reveal.js boilerplate scripts and styles.
3. Configure `_config.yml` for GitHub Pages compatibility and map the `_presentations` collection to use the Reveal.js layout by default.
4. Create a `docker-compose.yml` that uses the official `jekyll/jekyll` image, mounts the local repo, and exposes the required ports for live-reloading during development.
5. Create an index page (`index.html`) to serve as a directory listing all available presentations.
6. Provide a template Markdown file (`template/index.md`) for easily scaffolding new talks.
7. Document commands in `README.md` for starting the Docker container and adding new presentations.
8. **Jekyll Markdown Bypass**: To use `.md` files without Jekyll converting them to HTML, use `include_relative` in the layout to read the raw file and strip YAML frontmatter. This allows Reveal.js to receive the literal Markdown content it requires.

**Relevant files**
- `_config.yml` — Site configuration and collections setup.
- `_layouts/presentation.html` — Base layout injecting Reveal.js dependencies.
- `_includes/head.html` and `_includes/footer.html` — Layout includes.
- `docker-compose.yml` — Docker development configuration.
- `index.html` — Main landing page displaying all talks.

**Verification**
1. Run `docker-compose up` and verify the Jekyll server starts successfully and mounts files.
2. Navigate to `http://localhost:4000` to see the index page.
3. Click on a sample presentation link and verify Reveal.js renders the markdown slides correctly.
4. Edit the sample markdown presentation and verify live-reloading works in the container.

**Decisions**
- **Framework**: Use Reveal.js embedded in a Jekyll layout as it parses standard Markdown separator tags out-of-the-box and requires no extra custom compilation plugins (which often clash with GitHub pages default safe mode).
- **Structure**: Presentations will be defined as a Jekyll collection (e.g., `_presentations/2026-topic-name.md`) so they can be easily listed on a home page.
- **Docker**: Rely on `docker-compose.yml` and the standard `jekyll/jekyll` image to keep the host machine clean and isolate dependencies.
