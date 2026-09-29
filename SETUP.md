# Profile README setup

## 1. Create the repository

The repository name must match your GitHub username **exactly**, or the profile page won't pick it up.

If your username is `thuyamaungg`, create:

```
https://github.com/thuyamaungg/thuyamaungg
```

Make it public. Tick "Add a README file" — GitHub will then tell you it's a special repository, which confirms the name is right.

## 2. Add these files at the root

```
README.md
assets/hero.svg
assets/timeline.svg
assets/system-orbit.svg
assets/capability.svg
assets/footer-wave.svg
```

## 3. Check before you trust it

Open your profile page, not the repository page. The README renders above your pinned repositories.

Look for:

- All five SVGs animating — sweep lines, marching dashes, floating cards, growing bars
- The typing banner cycling through four lines
- Every badge loading (a broken one shows as a small grey box)
- The three repository links resolving

## 4. If the SVGs don't animate

GitHub serves images through a caching proxy. A freshly pushed SVG sometimes caches before it's ready. Hard-refresh the page, and if it's still static, wait a few minutes and try again.

If an SVG shows as a broken image, the path is wrong — GitHub is case-sensitive, so `Assets/Hero.svg` won't match `assets/hero.svg`.

## 5. Keep it current

The numbers in `README.md` and inside `hero.svg` and the proof-of-work table are hard-coded: 145 tests, 20/21 eval, 169 tests, 92% coverage. When those change, update both the README and the SVG — the SVG has them baked into the artwork.

## What this package deliberately leaves out

No contribution streak counter, no stats cards, no language-percentage charts, no contribution snake.

Those services read your public commit history. Yours starts recently, because you spent twenty years running a business rather than committing to GitHub. The cards would report that as a weak signal and undercut the three shipped systems the rest of the page is built on.

If you want them later, they're one line each — but add them after your commit history has a year behind it.
