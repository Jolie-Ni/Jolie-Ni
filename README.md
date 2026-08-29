<<<<<<< HEAD
## Hi there 👋

<!--
**Jolie-Ni/Jolie-Ni** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
=======
# jolieni.com — deploy notes

Five files. No build step, no dependencies, no framework.

    index.html            the whole site, self-contained
    favicon.svg           Chrome, Firefox, Edge
    favicon.ico           Safari and older browsers (16, 32, 48 px inside)
    apple-touch-icon.png  iOS home screen, 180×180
    README.md             this file

The only thing loaded from outside is the Jost typeface, from Google Fonts.

---

## Option A — live in five minutes, no accounts

1. Go to https://app.netlify.com/drop
2. Drag this whole folder onto the page.
3. It is live on a `*.netlify.app` URL immediately.
4. Site settings → Domain management → Add custom domain, then follow the
   DNS instructions at your registrar.

Good for seeing it on real hardware tonight. Updating later means dragging
the folder again, which is why Option B is the better permanent home.

## Option B — the permanent setup

1. Create a GitHub repo and push these files to the root of `main`.
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git.
3. Pick the repo. Leave the build command **empty** and set the output
   directory to `/`. There is nothing to build.
4. Custom domains → Set up a domain → enter your domain.
   If your DNS is already on Cloudflare this is one click. If not,
   Cloudflare gives you the records to add at your registrar.

HTTPS is provisioned automatically on both. After this, publishing a change
is `git push`.

---

## Before you point a domain at it

- Replace every `href="#"` with a real URL. There are eight of them:
  four in Writing, four in Elsewhere.
- Check the Route years. They were estimated, not confirmed.
- Rewrite the Beijing and Vancouver lines in your own words.
- Update the footer dateline whenever you touch the page.

## Editing

Open `index.html` in any text editor. The CSS is in one `<style>` block near
the top; the colour tokens are the first thing in it. Change `--paper`,
`--celadon` or `--jade` and the whole page moves together.

Content sections are marked with HTML comments. To add a section, copy an
existing one, give it a new `id`, and add a matching `<li>` to the `.culm`
nav so the bamboo picks it up.
>>>>>>> 771048a (Initial site)
