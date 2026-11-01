# Reference scan and design hypotheses

Research date: 2026-10-28. Scope: publicly accessible Roblox experience descriptions and official Creator documentation. This is a lightweight competitor scan, **not** a playtest or a review-data study.

## Reference experiences

- [Climb Scary Worm Tower 3](https://www.roblox.com/games/136070094363960/Climb-Scary-Worm-Tower-3) — its public description asks whether players can reach the top without being eaten, hints at other monsters and future ways to defend against “slappers,” and says it is inspired by other scary games. Roblox’s server page reported no running experiences when checked, so I could not inspect direct gameplay.
- [Climb Scary Worm Tower](https://www.roblox.com/games/79392214809379/Climb-Scary-Worm-Tower) — its public description similarly centers on reaching the top without being eaten and mentions possible new monsters/NPCs.
- [Climb Scary Worm Tower (Brazilian Territory)](https://www.roblox.com/games/103481122176780/Climb-Scary-Worm-Tower) — the public description promises a surprise at the end and advertises a group-exclusive Lava Slap; listing tags mention tower/obby, coins, and tools.
- [Tower of Hell](https://www.roblox.com/games/1962086868/Tower-of-Hell) — a useful broad tower-obby comparison. Signal Spire deliberately takes a different difficulty stance by including checkpoints rather than requiring a full restart after every failure.

## What is verified, and what is not

The pages establish a recognizable genre promise: climb an obstacle tower under pressure, with scary-monster framing. They do **not** establish specific player pain points. Search results and third-party clips were too anecdotal to support claims that a particular reference has broken checkpoints, bad controls, unfair difficulty, or poor performance. Treat these as hypotheses for our own tests, not accusations about competitors.

## Signal Spire differentiation hypotheses

1. **Clarity before fear:** the hazard gives an eight-second warning and has a visible red wave. Test whether players understand what to do before danger arrives.
2. **Recovery without erasing progress:** clear teal team checkpoints save progress for the current server. Test whether failure feels fair without removing tension.
3. **Co-op that helps instead of blocking:** a player unlocking a checkpoint helps the current server. No two-player lock, paid rescue, or mandatory friend gate.
4. **Mobile readability:** high-contrast ledges, broad landings, short HUD copy, and Roblox's standard touch controls. Real-device tests are still required.
5. **Fair rewards:** optional shards are collectibles, not paywalls or paid randomized rewards.

## What to measure during playtests

- The stage/step where new players fail or stop climbing.
- Whether players notice and understand each Echo warning.
- Whether checkpoints prevent an unwanted full restart and whether they feel too forgiving or punishing.
- Completion rate and time to first checkpoint, separately for solo and party play.
- Device/input type, frame performance, and qualitative player comments.

Do not tune for session length at any cost. Optimize for understandable, enjoyable sessions and let players stop without losing earned progress.

## Roblox Studio / launch workflow references

- [Publish experiences and places](https://create.roblox.com/docs/production/publishing/publish-games-and-places)
- [Retention analytics](https://create.roblox.com/docs/production/analytics/retention)
- [Monetization overview](https://create.roblox.com/docs/production/monetization)
- [Passes](https://create.roblox.com/docs/production/monetization/passes)
- [Developer products](https://create.roblox.com/docs/production/monetization/developer-products)
- [Creator Rewards](https://create.roblox.com/docs/creator-rewards)
- [Developer Exchange (DevEx)](https://create.roblox.com/docs/production/monetization/developer-exchange)

Roblox documents several possible ways to monetize, including passes and developer products. They require intentional in-experience setup, eligibility can change, and earning income is not guaranteed. The prototype intentionally contains no purchases.

## REA and RRE-Site

- [morluto/rea](https://github.com/morluto/rea) is an agent/MCP reverse-engineering workflow for inspecting software; it is not a Roblox Studio builder or normal Luau project generator.
- [ROBLOX-Reverse-Engineering/RRE-Site](https://github.com/ROBLOX-Reverse-Engineering/RRE-Site) is work-in-progress reverse-engineering documentation, not a Roblox game starter project.

Neither is needed to build this original experience. Use Studio and Luau for this project. Do not reverse-engineer or copy another creator's private content.
