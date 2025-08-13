Small website of where to find us around the internet, and a little about what we have done.

# Contributing

To edit this website:

1. Open your repository in your preferred text editor.
2. Locate the `data.toml` file and update it with your information.

<details>
<summary>Click to <b>Learn</b> all the available settings here</summary>

## Fields

- `name`: Your name (e.g., "Vahid Al")
- `description`: A brief bio about yourself (e.g., "Software Developer and passionate about creating things")
- `keywords`: Keywords for the keywords meta tag (e.g., "python, javascript, go")
- `image`: The file address of your avatar. Place your avatar inside the `dist/img/` folder (e.g., "me.jpeg" - Note that the `/dist/img/` address is not included)
- `theme`: Choose your website theme: "dark" or "light" (e.g., "dark")
- `primary_color`: Specify your website's primary color using a hexadecimal color code (e.g., "#00897b")
- `text_align`: Specify the text alignment for your website: "right", "left" or "center" (e.g., "center")
- `gtag_id`: Your Google Analytics tracking ID (e.g., "G-33WB8LVHR6")
- `base_url`: The base URL for your website, mentioned in **1. Create a Repository** step (e.g., <https://thevahidal.github.io/jake>)

#### Sections

You can add multiple sections based on your requirements.
For example, you may want a section for your projects, another for your social media links, and another for your merchandise products.

Each section is defined using `[[sections]]` and has the following components:

- `title`: The title of the section (e.g., "Projects")
- `description`: A brief description of the section (e.g., "Here are some of my projects")
- `direction`: The direction of the section: "row" or "column" (e.g., "row")
- `item_style`: The style of the items in the section: "outline" or "filled" (e.g., "outline")
- `items`: The items associated with the section.

#### Items

Each item is defined using `[[sections.items]]` and has the following components:

- `title`: The title of the item (e.g., "Soul")
- `description`: A brief description of the item (e.g., "An SQLite REST and Real-time server")
- `url`: The URL associated with the item (e.g., "<https://github.com/thevahidal/soul>")

</details>


### Local Development

If you'd like to test or customize this project locally without triggering GitHub Actions, follow the steps below to set up and run the pipeline on your machine.

#### Prerequisites

Ensure the following are installed:

- [Python 3.11+](https://www.python.org/)
- [Poetry](https://python-poetry.org/) (You can install Poetry via [pipx](https://pypa.github.io/pipx/): `pipx install poetry`)

#### Steps for Local Development

1. **Clone the repository**:

```bash
git clone https://github.com/entrypointdailies/connect.git
cd jake
```

2. Install dependencies using `Poetry`:

```bash
poetry install --no-root
```

3. Run the generator script: This will generate the HTML files and output them to the `dist/` directory.

```bash
poetry run python script.py
```

4. Preview your changes: Open the generated HTML files in your browser or use a local server to serve the dist folder:

```bash
python -m http.server --directory dist 8000
```

Then, open [http://localhost:8000](http://localhost:8000) in your browser.

#### Optional: Build Automation Script

To simplify these steps, you can use the provided `local_run.sh` script. This script will automate the process.

Make the script executable:

```bash
chmod +x local_run.sh
```

Run it with:

```bash
./local_run.sh
```

## License

This project is licensed under the [MIT License](LICENSE).
