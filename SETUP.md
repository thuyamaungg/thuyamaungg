# Profile README setup

## 1. Create the repository

The name must match your username exactly:

```
https://github.com/thuyamaungg/thuyamaungg
```

Public. Tick "Add a README file" — GitHub then tells you it's a special repository, which confirms the name is right.

## 2. Add these files

```
README.md
assets/                       9 animated SVGs
.github/workflows/snake.yml
.github/workflows/profile-3d.yml
.github/workflows/metrics.yml
```

The workflows use `github.repository_owner`, so they need no editing.

## 3. Run the workflows once, by hand

Three sections of the README point at files that don't exist yet: the metrics card, the contribution snake and the 3D graph. Until the workflows run, those three show as broken images.

Go to the **Actions** tab. If you see "Workflows aren't being run on this forked repository" or a disabled notice, click to enable them. Then for each of the three:

1. Select it in the left sidebar
2. Click **Run workflow** on the right
3. Wait one to three minutes

After that they run daily at midnight UTC on their own.

## 4. Check the result

Open your **profile page**, not the repository page.

- Nine local SVGs animating — sweep lines, marching dashes, orbit rings, growing bars
- The typing banner cycling four lines
- All badges loading; a broken one shows as a small grey box
- Metrics, snake and 3D graph present after the workflows finish

## 5. Known wrinkles

**Snake shows a broken image.** It publishes to a branch called `output`, which the workflow creates on its first successful run. If `snake.yml` failed, check the Actions log — the usual cause is Actions lacking write permission, under Settings → Actions → General → Workflow permissions.

**Metrics card fails.** `lowlighter/metrics` works with the default token but does more with a personal access token. If it errors, create a classic PAT with `public_repo` scope, save it as a repository secret named `METRICS_TOKEN`, and re-run.

**An SVG shows broken.** Path case. GitHub is case-sensitive; `Assets/Hero.svg` won't match `assets/hero.svg`.

**Animation looks frozen.** GitHub caches images through a proxy. Hard-refresh, then wait a few minutes.

## 6. Keeping numbers honest

145 tests, 20/21 eval, 169 tests, 92% coverage appear in three places: the README table, `hero.svg` and `terminal-intro.svg`. When they change, update all three — the SVGs have them baked into the artwork.

## 7. About the three generated graphics

The metrics card, snake and 3D graph read your public commit history. Yours starts recently, so for the first while they'll look sparse next to the three shipped systems above them.

They fill in as you commit. If they look thin enough to distract, comment those three image tags out and put them back in a few months — everything else on the page stands without them.
