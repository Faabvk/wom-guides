<div align = "center">

![Wise Old Man logo](https://github.com/wise-old-man/wise-old-man/assets/3278148/c4c8a2ce-7f61-4b6e-ba97-5d9d5bf6b1d1)

🔗 [www.wiseoldman.net](https://wiseoldman.net/)

[Website](https://wiseoldman.net/) |
[Discord](https://discord.gg/Ky5vNt2) |
[Patreon](https://www.patreon.com/wiseoldman)
 
</div>

## How Wise Old Man works

This is arguably the most important part to understand when you use Wise Old Man. Understanding how it works will answer a lot of questions you might already have, or might have in the future.

- [How Wise Old Man works](#how-wise-old-man-works)
  - [Snapshots](#snapshots)
  - [What this means for players](#what-this-means-for-players)
  - [Updating](#updating)
  - [TL;DR / FAQ](#tldr--faq)


### Snapshots

Jagex provides developers with only a very limited API to read the HiScores in a computer-friendly way, that does not track anything itself. That means all that Wise Old Man sees, is the player's rank on the HiScores for each Metric (skill/boss/activity), the level or kill count for each Metric, and in case of a skill, the experience. This information is updated every time the players logs out of RuneScape. That means if your XP is 100, but you've gotten to 200 while playing, this will not be shown on the HiScores until you log out.

Wise Old Man tracks this through Snapshots. Every time a player is updated on Wise Old Man, it takes a Snapshot of the player's stats from the HiScores API, at that moment in time.

Wise Old Man saves this snapshot in a database, and the next time a player is updated it saves another Snapshot. These Snapshots are used to generate a timeline for a player, and this is how a player's XP/KC gains are determined.

### What this means for players

The process of updating players, and making snapshots does (in a lot of cases) not happen automatically, especially when you've never used Wise Old Man before.

When you first use Wise Old Man, and update yourself to take your very first Snapshot, things can look quite dull. Most likely it'll look like

- you've never gained any XP
- you have no boss KC, even though you know you do
- Some (or all) skills will be level 1, even though you know they're not

The first option should be self-explanatory, with the information above. Wise Old Man has never taken a Snapshot of your stats before, so it has no historical data to say you've gained XP over a certain timeframe. The first Snapshot it takes is your starting point.

The latter two options are because your skills/boss KC have progressed to little for you to rank on the RuneScape HiScores. RuneScape only lists the Top 2 Million players for each Metric. For some unpopular skills like Runecrafting, this means you don't need that high of a level to be listed, but for popular skills, like Attack or Strength, means you need a lot of it to be listed, but if you are not listed, Wise Old Man can not see your level.

### Updating

So in order for your gains to be accurately shown on Wise Old Man, you need to make sure your stats are updated on Wise Old Man. You can do this manually, but that can be easily forgotten or become very tedious. That's why there are two very handy ways to automatically update on WOM.

The built-in RuneLite Plugin "XP Updater" was especially made for this, just enable it and make sure to tick the box for Wise Old Man. This will automatically update you on Wise Old Man every time you log out of RuneScape. But Wise Old Man also has it's [own RuneLite Plugin](https://runelite.net/plugin-hub/show/wom-utils)! Not only does this does this do the same to make sure your gains get accurately tracked over time, it has a bunch of other helpful ways to get the most out of Wise Old Man.

### TL;DR / FAQ

Short questions give short answers :)

If these answers dont clear things up, please read the rest of the guide.

***I just used Wise Old Man for the first time, why does it say I gained nothing?***

This is the first time Wise Old Man collects data for your account, it has no historical data to compare to, so this is your starting point.

***A bunch of my stats are level 1 on Wise Old Man, even though I've definitely leveled them up***

The stats (or Metrics) of your account are too low to be listed on the RuneScape HiScores, so Wise Old Man can't see your actual level.

