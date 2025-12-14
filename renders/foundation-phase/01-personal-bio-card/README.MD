<div align="center" style="margin: 18px 0 10px 0;">
	<div id="bio-hero" style="width:160px;height:160px;border-radius:20px;overflow:hidden;margin:0 auto 14px auto;box-shadow:0 10px 30px rgba(0,0,0,0.35);background:linear-gradient(135deg,#0f172a,#0b1220);display:flex;align-items:center;justify-content:center;">
		<!-- Replace the comment below with an <img src="..."> tag to show your preferred image -->
		<!-- Example: <img src="../../assets/me.jpg" alt="BROCCOLI" style="width:100%;height:100%;object-fit:cover"> -->
	</div>
	<h1 style="margin:0;font-size:1.6rem;color:#61afef;letter-spacing:0.6px;font-weight:800;">PERSONAL BIO CARD</h1>
	<p style="margin:6px 0 0 0;color:#c8d1d9;max-width:700px;">A tiny, responsive bio/profile card built with vanilla HTML, CSS and a pinch of JavaScript — designed for quick reuse inside the Render Protocol.</p>
</div>

<div style="display:flex;gap:18px;flex-wrap:wrap;justify-content:center;margin:18px 0 6px 0;">
	<a href="index.html" style="text-decoration:none;">🔎 Live demo (open <code>index.html</code>)</a>
	<span style="color:#5c6370;">•</span>
	<a href="../../README.md" style="text-decoration:none;">📚 Back to Render Protocol</a>
</div>

## Demo

Preview locally by opening `index.html` in this folder, or run a quick server:

```powershell
# from repository root
cd renders/foundation-phase/01-personal-bio-card; python -m http.server 8000
# then open http://localhost:8000 in your browser
```

## Files

- `index.html` — markup for the bio card
- `css/style.css` — styles and responsive rules
- `js/script.js` — simple interactivity (toggle contact / copy email)
- `assets/` — images and icons

## Usage

1. Copy the entire `01-personal-bio-card` folder into any project.
2. Edit `index.html` to update your name, role and links.
3. Replace the image inside the `#bio-hero` div with your avatar (see the example comment at the top).

## Quick Copy: Minimal Markup

Paste this snippet into any page to get the card:

```html
<!-- bio-card.html (minimal) -->
<div class="bio-card">
  <img class="avatar" src="assets/avatar.jpg" alt="Avatar" />
  <h3 class="name">BROCCOLI</h3>
  <p class="role">Creative Web Developer</p>
  <div class="actions">
    <a href="#" class="btn contact">Contact</a>
  </div>
</div>
```

## CSS (essentials)

```css
.bio-card {
  width: 320px;
  max-width: 94%;
  background: linear-gradient(180deg, #0f172a 0%, #071025 100%);
  color: #e6eef8;
  padding: 18px;
  border-radius: 12px;
  box-shadow: 0 8px 30px rgba(2, 6, 23, 0.6);
}
.avatar {
  width: 96px;
  height: 96px;
  border-radius: 12px;
  object-fit: cover;
  margin-bottom: 12px;
}
.name {
  margin: 0;
  font-weight: 800;
  color: #61afef;
}
.role {
  margin: 6px 0 12px 0;
  color: #9fb0c8;
}
.btn {
  display: inline-block;
  background: #98c379;
  color: #071025;
  padding: 8px 12px;
  border-radius: 8px;
  text-decoration: none;
}
```

## Interactivity (optional)

Add tiny JS to enable copy-to-clipboard or contact toggles:

```js
document.querySelector(".contact")?.addEventListener("click", (e) => {
  e.preventDefault();
  navigator.clipboard?.writeText("thedipssoumoofficial@gmail.com");
  alert("Email copied to clipboard!");
});
```

## Customization Tips

- To change theme colors, edit CSS variables at the top of `css/style.css`.
- Swap fonts by linking Google Fonts in `index.html`.
- For advanced animations, add `@keyframes` in `css/style.css` and toggle classes in `js/script.js`.

## Accessibility & Performance

- Use `alt` attributes for images.
- Keep images optimized (webp preferred) in `assets/`.

---

Made with curiosity by BROCCOLI — enjoy adapting the card for your own renders.
