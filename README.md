# My Ingress banners

A page of the Ingress mission banners I have done: my mission medals from Ingress, matched with
[Bannergress](https://bannergress.com), with a map of where each banner starts.

This repository (`ingress-banners` unless you chose another name) is made and filled by the
[KMyBanners app](https://github.com/elkuku/KMyBanners) — there is nothing to edit by hand.

## How it works

1. In the app, sign in with GitHub: it creates this repository from
   [KMyBanners-template](https://github.com/elkuku/KMyBanners-template) and turns on GitHub Pages.
2. Sign in to Bannergress in the app: it saves your done list here (`done.json`).
3. In Ingress, open your agent profile, tap the arrow next to the mission medals and take screenshots
   while you scroll down (about half a screen each, wait until the pictures have loaded). Share them
   to the app: it puts them in `inbox/`. Later, for new medals, screenshots from the top down to medals
   that were there before are enough.
4. The workflow stitches the screenshots (`capture/medals.jpg`), matches every medal row with your done
   list by picture and publishes the page. Medals it can't match for sure are marked **To check**:
   pick the banner in the app (saved in `corrections.json`).

The page is at `https://<your GitHub name>.github.io/<repository name>/`. You can rename the repository in
the app's settings: the page then moves to the new address (GitHub doesn't forward the old one). The app
finds the repository by its topic `kmybanners`, and so does the
[directory of agents' pages](https://elkuku.github.io/KMyBanners-directory/), which lists the public pages once a day.

**Privacy:** the page is public and shows on a map where you did banners, and it is listed in the directory.
Delete the repository to remove the page; it then also leaves the directory with its next daily update.

## Files

| File | |
|---|---|
| `config.json` | Your agent name |
| `inbox/` | New screenshots from the app (the workflow moves them to `captures/`) |
| `captures/` | The screenshots of every build, kept |
| `capture/medals.jpg` | Your stitched mission medals: new screenshots are joined onto them |
| `done.json` | Your Bannergress done list |
| `corrections.json` | Medals you matched by hand in the app |
| `notes.json` | Optional notes per banner (Bannergress id → text) |

The build itself is in [elkuku/KMyBanners-tool](https://github.com/elkuku/KMyBanners-tool).
