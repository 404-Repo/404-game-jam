# 404 game jam, 001

Site: https://game.404.xyz Method: https://github.com/404-Repo/404-game-recipe

This repo is where entries land. One pull request per entry, adding one file to `entries/`. The rules below are the rules; the site restates them, and where they differ this file wins.

## Dates (all UTC)

| when | what |
|---|---|
| 11 Sep 2026, 12:00 | opens. Recipe, harness and Atlas credits available. Building earlier is fine; the first commit of your entry repo must be on or after 11 Sep 00:00 UTC. |
| 18 Sep | office hours. Questions answered, one entry taken apart live. |
| 25 Sep, 23:59 | closes. Pull request open, jam gate passed, play link working. |
| 27 Sep | shortlist published here and on X. Community vote opens. |
| 28 Sep, 12:00 | community vote closes. |
| 28 Sep | winner announced on stage at Exploit Summit, Montreal. Nobody has to be there. |
| by 28 Oct | prizes paid. |

## Prizes

Prizes are denominated in TAO and paid in TAO to one Bittensor wallet per team, within 30 days of the announcement. Dollar figures are for orientation only, at about 260 USD per TAO on 7 Sep 2026.

| place | TAO | about | also |
|---|---|---|---|
| first | 5 | 1,300 USD | announced on stage, a build breakdown published with 404 |
| second | 3 | 780 USD | showcase slot and a post on the 404 channel |
| third | 1.5 | 390 USD | showcase slot and a post on the 404 channel |
| community | 0.5 | 130 USD | voted by entrants, on the shortlist |

Everyone keeps their game. Ten entrants receive a free Atlas licence, chosen by the judges from the shortlist and the honourable mentions. The best entries are showcased by 404 on X.

## The one hard rule, and how it is checked

**Every 3D object in your game is Three.js code written through the 404 recipe.** No downloaded meshes, no asset store, no hand modelling, and no mesh smuggled in as data: an asset module must build its geometry from Three.js constructors and operations, not from a literal vertex array or a base64 blob. `harness/ship.mjs` in the recipe warns on modules with more than 64 numeric literals in one array and on base64 in asset modules; a judge reads anything it flags.

Textures, skies, sprites, sound and music may be files: generated on Atlas with your jam credits, or your own, declared in your entry.

## Everything else

- **Team.** One to four people. One entry per person.
- **Source.** Your entry repo is public. Its history is real: the first commit is on or after 11 Sep 00:00 UTC, and the work is in the commits, not in one upload at the end.
- **Original.** No trademarked characters, names or logos. The 404 reference games (Drive, Rust 17, Costa Verde, the warehouse example, Lantern Run) may be read and learned from. Copying their assets or code into an entry disqualifies it.
- **Tools.** Any agent, any models, any generator for images and sound. Name them in your entry. Atlas is optional; the credits exist so nobody pays for images. Sign up for them at https://app.atlas.design/campaign/404-game-jam.
- **Yours.** You keep ownership of your game. By entering you grant 404 a perpetual, worldwide, royalty free, non-exclusive licence to display, stream, clip and write about your game and its play link for the jam and its promotion. You confirm you hold the rights to everything in your entry, including third party content. The build breakdown for the winner is written with the winner; nothing from your repo is published without asking first. Outputs generated on Atlas jam credits are yours to use, under the Atlas terms.
- **Eligibility.** 18 or the age of majority where you live. Not open where prohibited by law, or to anyone on a sanctions list. People who work on 404, the 404 subnet, or Atlas can enter and cannot win. Winners are responsible for their own taxes. The organisers may ask a winner to confirm their identity before paying.

## The gate

Your entry must pass the jam gate against your live URL on a phone viewport under a 4G profile, with a real touch:

```
git clone https://github.com/404-Repo/404-game-recipe && cd 404-game-recipe && npm install
node harness/jam.mjs https://you.github.io/yourgame/game/ --commit=<sha>
```

It checks: ready within the time limit, total size under 10 MB, starts from a real tap, moves under a real finger, stays under 900 draw calls and 1.5M triangles, no 404s, no console errors. It prints a verdict block. Paste that block, unedited, into your pull request. We rerun it against the same URL and commit before merging.

## How to submit

1. Fork this repo. Add `entries/<your-slug>.json`, copying `entries/_template.json`.
2. Open a pull request. The template asks for the verdict block and your three sentences.
3. Your entry appears on the site when the pull request is merged, which happens when our rerun of the gate agrees with yours. Nothing is curated in or out before judging.

## Judging

Two stages, published so nobody has to guess.

**Stage one, blind pairs.** Every entry appears in about six pairs against other entries: two frames in motion side by side, names off, order shuffled, judged on one question only: does it look like a made thing. Three judges. The top twelve are the shortlist.

**Stage two, hands on.** Each shortlisted game is played by every judge for thirty minutes on a phone and a laptop, then scored on four questions with the weights below.

| weight | question |
|---|---|
| 40 | Is it good to play |
| 30 | Does it look like a made thing |
| 20 | What did you find that nobody else tried |
| 10 | How it was made, with the receipts: your repo, your gate runs, what you threw away |

The 20 for "what did you find that nobody else tried" is about the game itself: a mechanic, a rule, a look or a control scheme that no other entry has, judged against the other entries on the shortlist, not against the recipe or the harness. How you got there is scored in the 10 row. Say your find in the `what_i_found` field of your entry file.

Judges are announced before entries close. Anyone with a conflict (they built a reference game, they work on the thing an entry was built with) declares it and does not score that entry.

**Community vote.** Entrants vote for one shortlisted entry other than their own by reacting with a thumbs up to its pull request between 27 Sep and 28 Sep 12:00 UTC. One GitHub account, one vote, entrants only. Reactions from accounts that did not enter are not counted.

## When things go wrong

- **Late.** Pull requests opened after 25 Sep 23:59 UTC are not judged. No exceptions, so leave margin.
- **Broken at close.** If your play link is down or fails our gate rerun, you get one 24 hour window to fix the deploy without changing the game (same commit, or a commit that only changes paths and hosting). Once.
- **Ties.** Judge majority in stage two. If still tied, the community vote decides.
- **Disqualification.** Decided by the jam team, with a written reason posted on the pull request. You have 24 hours to respond before it is final.
- **Fewer than twelve entries pass.** Everything that passes is the shortlist.
- **Questions.** The 404 Discord is fastest: https://discord.gg/5qvNHuWxTH. Otherwise open an issue here, ask on X at @404gen_, or come to office hours on 18 Sep.
- **Entering elsewhere.** Your game is yours. Enter it in other jams and hackathons too; Tripo's Tripothon takes submissions from 15 September to 5 October.
