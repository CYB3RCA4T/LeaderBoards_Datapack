> **⚠️ Unofficial Fork**
>
> This is an unofficial fork of [LeaderBoards Datapack](https://modrinth.com/datapack/leaderboards-datapack), originally created by [DJTgeekk](https://github.com/DJTgeekk). This fork includes modifications and updates by CYB3RCA4T for newer Minecraft versions.
>
> This project is independent and is not affiliated with or endorsed by the original author. See [LICENSE](LICENSE) for copyright and license details.

**Original source code:** [DJTgeekk/LeaderBoards_Datapack](https://github.com/DJTgeekk/LeaderBoards_Datapack)

# LeaderBoards Datapack 1.21.6+

A Datapack to place LeaderBoards Ranking players of your server on a given scoreboard objective.

![Fixed Leaderboard example](https://cdn.modrinth.com/data/cached_images/291cff70d6a66cfb2ff6dd5f85803a5077e65344.png)

## How to use

LeaderBoards Datapack 1.21.6+ uses the Dialog feature to provide an easy to use interface to create and edit Leaderboards

### Add a LeaderBoard

```
/function leaderboard:_dialog/add_leaderboard_dialog
```

- **time_mode** option will display the score as a time with hours, minutes, seconds and 1/20th of a second (ticks). It requires the given score to be a time in ticks. Extended, keeps ms even when value is bigger than 1 hour

- **reverse_order** option will reverse the order of the players in the LeaderBoard. Puts the lowest score first.

- **no_zero** option will remove players with either no score or a score that equals 0 from the LeaderBoard. This is especially useful in reverse mode to avoid having new players at the top of the LeaderBoard by default.

- **billboard** option set the billboard type that the LeaderBoard will use.  
It can be set to vertical, horizontal or fixed  
When using **fixed** billboard type, the direction is set from the head direction of the player executing the command.  
tips: you can use `/tp @s ~ ~ ~ x y`, with x and y set to the rotation if you want the leaderboard to be aligned to a specific angle

- **medal_color** option will add medal like colors the the top 3 ranks

- **always_show_closest_player** option highlights the line of the nearest player. If this player's rank is not present in the base list (cause of max_players option), it will add an extra line under the default one with the closest player score.

- **bright** option sets the text_displays with constant full brigthness

### Remove a LeaderBoard

This will remove the nearest LeaderBoard.

```
/function leaderboard:commands/remove_leaderboard
```
---

### Edit a LeaderBoard

This will edit the nearest leaderBoard.

```
/function leaderboard:_dialog/edit_leaderboard_dialog
```
---

### Reset
You can reset all leaderboards using:
```
/function leaderboard:commands/reset
```
**This will remove all tracking tag from players and their names from the list. Their names should be auto added after a reset. (Only works on online players)**

---

### Uninstall

```
/function leaderboard:commands/uninstall
```
**This will disable the datapack and remove all LeaderBoards**