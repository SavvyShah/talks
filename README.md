# Talks Repository

This repository is a collection of presentation slides used in my YouTube videos. It serves as a central place to organize, store, and share all the slides from my talks and presentations.

## Development

This project uses Jekyll and Reveal.js with Docker for local development.

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Running locally

To start the local development server:

```bash
docker-compose up
```

Wait for the container to start, then navigate to [http://localhost:4000](http://localhost:4000).

### Adding a new presentation

1. Create a new `.md` file in [_presentations](_presentations).
2. Add the required frontmatter:

```markdown
---
title: My New Talk
theme: black
---
```

3. Write your slides in Markdown. Use `---` for horizontal slide transitions and `--` for vertical ones.

## Purpose
- Archive all presentation slides from YouTube videos
- Make slides easily accessible for viewers and collaborators
- Provide a reference for topics covered in each talk

## Structure
Slides are organized by topic, date, or video title. Each folder or file corresponds to a specific presentation.

## Usage
Feel free to browse, download, or reference the slides for your own learning or presentations. If you have suggestions or requests for future topics, please reach out via YouTube comments or open an issue.

## License
Unless otherwise noted, all slides are shared for educational purposes. Please credit the channel if you use or share them.

---
**Channel:** [YouTube](https://www.youtube.com/)

