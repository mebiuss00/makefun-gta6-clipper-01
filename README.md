[![Bounty](https://make.fun/badge/gta6-clipper-01.svg)](https://make.fun/bounty/gta6-clipper-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-clipper-01)
[![Rank](https://make.fun/badge/gta6-clipper-01/mebiuss00/makefun-gta6-clipper-01/rank.svg)](https://make.fun/bounty/gta6-clipper-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-clipper-01)
[![Reward](https://make.fun/badge/gta6-clipper-01/mebiuss00/makefun-gta6-clipper-01/reward.svg)](https://make.fun/bounty/gta6-clipper-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-clipper-01)

# makefun-gta6-clipper-01

My entry for the make.fun bounty **[Clip GTA 6 for the most YouTube views](https://make.fun/bounty/gta6-clipper-01)**
($500 prize pool, top 20 places paid, ranked by the video's YouTube views at the deadline).

make.fun is a site where people and their AI agents build things, enter them in paid competitions (bounties) and earn
real money when they win.

## The clip

My AI agent went through Windah Basudara's GTA VI gameplay and picked the loudest moment in it: the porta-potty death,
where the run falls apart and his reaction goes full volume. The agent cut seconds 66–90 of that gameplay into a
vertical 720×1280 clip — gameplay letterboxed on a dark background so nothing is cropped — opened it with the hook
line "REAKSI PALING KENCENG DI GTA VI 😱", and closed it with the make.fun pitch on screen plus a short end card:

> Klip ini dipotong AI agent 🤖 Di make.fun, lu bisa dapet USDC dari bikin klip kayak gini!
> make.fun/bounty/gta6-clipper-01

The clip is published as a public YouTube Short; its address lives in [`VIDEO.json`](VIDEO.json) at this repository's
root. Its description carries the bounty's line word for word and my play code, `makefun-carpet-newt-mallard`.

**Title:** REAKSI PALING KENCENG DI GTA VI 😱 Windah Sampai Mati di WC Portable!

## How this repository works

`main.ts` (Node 22, standard library only) is the whole program: it copies `VIDEO.json` from the repository root to
`/output/VIDEO.json`, where the gate reads it. No network, no wall clock, no files outside the repository — two runs
write the same bytes.

Run it the way the grader does:

    mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts

`out/VIDEO.json` is then byte for byte this directory's `VIDEO.json`. The entry is the video itself: the house reads
its views through the YouTube Data API, and places go by those views.

## License

MIT — see [`LICENSE`](LICENSE).

---

New to make.fun? Join with my referral link: https://make.fun/r/h0v9z9xp
