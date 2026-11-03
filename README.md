# EV Market Strategy Suite 2026

An interactive, animated website for an EV (Electric Vehicle) market analysis project, built with **Tableau**, **Flask**, **HTML**, **CSS** and **JavaScript**.

The site presents three Tableau dashboards and one data story inside a premium glass-style interface.

## Features

- **Animated intro:** a futuristic vehicle flies in, charges from 0 to 100%, then takes off and reveals the site
- **Three analyst personas**, each with its own live Tableau dashboard:
  - Emily: Market Strategy
  - David: Business Intelligence
  - Sarah: Sustainable Mobility
- **Guided data story** embedded from Tableau Public
- **Glassmorphism design** on a midnight-blue background with champagne gold and emerald accents
- **Charging network animation** in the middle of the page
- **Finale animation** at the end of the page (vehicle arrives, battery 100%)
- Scroll-linked battery indicator in the navbar
- Photo gallery with slots for your own images
- Responsive layout and reduced-motion support

## Tech Stack

| Area | Tools |
|------|-------|
| Data visualisation | Tableau Public |
| Backend | Python, Flask |
| Frontend | HTML5, CSS3, vanilla JavaScript |
| Fonts | Sora, Manrope (Google Fonts) |

## Project Structure

```
my-flask-website/
├── app.py
├── templates/
│   └── index.html
├── static/            # optional: your photos
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd my-flask-website
```

### 2. Create a virtual environment and install Flask

```bash
python -m venv .venv
.venv\Scripts\activate        # Windows
# source .venv/bin/activate   # macOS / Linux
pip install flask
```

### 3. Run the app

```bash
python app.py
```

Open `http://127.0.0.1:5000` in your browser.

## Tableau Dashboards

The dashboards and story are embedded from Tableau Public. All links are stored in the `LINKS` object near the bottom of `templates/index.html`.

| View | Name |
|------|------|
| Dashboard 1 | 01 Emily - Market Strategy |
| Dashboard 2 | 02 David - Business Intelligence |
| Dashboard 3 | 03 Sarah - Sustainable Mobility |
| Story | Story 1 |

Workbook: `EV_Market_Strategy_Suite_2026_3_4GB_FinalDeveshgod` on Tableau Public.

## Adding Your Own Photos

Put your images in the `static/` folder and update the `PHOTOS` object in `templates/index.html`:

```js
const PHOTOS = {
  hero: "/static/ev1.jpg",
  a: "/static/ev2.jpg",
  b: "/static/ev3.jpg",
  c: "/static/ev4.jpg"
};
```

Any slot left empty keeps its built-in illustrated scene.

## Customisation

- **Colours:** edit the CSS variables at the top of the `<style>` block (`--c1`, `--c2`, `--c3`, `--bg`)
- **Intro speed:** change the timings inside the `run()` function in the script
- **Persona text:** edit the `DASH` array in the script

## Troubleshooting

- **Dashboard stays on the loading spinner:** the Tableau workbook must be public with embedding allowed. Large workbooks can take 10 to 30 seconds to load.
- **Jinja template error in Flask:** do not write `{#`, `{{` or `{%` in the CSS or JavaScript of the template. Add a space (for example `{ #home`) or wrap the code in `{% raw %}` and `{% endraw %}`.
- **Blank page:** check that the file is saved as `templates/index.html` and that you copied the full file.

## Author

**Devesh**
Data Analytics Project, 2026

## Acknowledgements

- Tableau Public for hosting the dashboards
- Google Fonts for Sora and Manrope
