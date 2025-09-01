# AI Builders: LatinX Edition

This is a static podcast website for **AI Builders: LatinX Edition**, built with HTML and Bootstrap 5, and structured for easy deployment on Cloudflare Pages.

## Features
- Modern, responsive design using Bootstrap 5
- SDLC-compliant project structure
- Podcast homepage with hero section and branding
- Individual episode pages with show notes and audio player
- Brand logo integrated in the hero section
- Ready for static hosting (Cloudflare Pages, Netlify, etc.)

## Project Structure

```
public/
	assets/
		brand/
			ai-builders-latinx-ediition-logo.png   # Podcast logo
		dist/
			css/
			js/
	blog/
		podcast-index.html   # Homepage
		episode1.html        # Episode 1
		episode2.html        # Episode 2
```

## Usage

1. Clone the repository:
	 ```sh
	 git clone https://github.com/vhr1975/ai-builders-latinx-edition.git
	 ```
2. Serve the `public/` directory with a static server for local development, e.g.:
	 ```sh
	 cd ai-builders-latinx-edition/public
	 python3 -m http.server
	 ```
3. Deploy the `public/` directory to your static hosting provider (e.g., Cloudflare Pages).

## Customization
- Update the logo in `public/assets/brand/` as needed.
- Add new episodes by copying and editing the episode HTML files.

## License
MIT