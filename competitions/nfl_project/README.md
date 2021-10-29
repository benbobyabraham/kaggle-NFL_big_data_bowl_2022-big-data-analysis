# NFL Big Data Bowl 2022
### Help evaluate special teams performance
[Go to page ...](https://www.kaggle.com/c/nfl-big-data-bowl-2022/overview)

# Overview
## Description
Before National Football League (NFL) coaches celebrate a big W, they strategize ways to improve field position and score points. Both of these objectives receive significant contributions from special teams plays, which consist of punts, kickoffs, field goals and extra points. These play types take on important roles in a game’s final score—so much so that coaches say they're a third of the game. Yet special teams remain an understudied part of American football, with an opportunity for data science to offer better ways to understand its impact.

The 2022 Big Data Bowl creates the opportunity for you (and the world!) to learn more about special teams play than ever before. We've provided the [NFL's Next Gen Stats](https://nextgenstats.nfl.com/) (NGS) tracking data from all 2018-2020 special teams plays. This data provides location information for each special teams player, wherever they are on the field, and includes their speed, acceleration, and direction. Additionally, and for the first time in Big Data Bowl history, participants can utilize scouting data from [PFF](https://www.pff.com/), which supplements the tracking data with football specific metrics that coaches find critical to team success.

The NFL is America's most popular sports league. Founded in 1920, the organization behind American football has developed the model for the successful modern sports league. They're committed to advancing every aspect of the game, including the lesser researched special teams. In this competition, you’ll quantify what happens on special teams plays. You might create a new special teams metric, quantify team or individual strategies, rank players, or even something we haven’t considered.

With your creativity and analytical skills, the development of these new methods could lead to additional stats for special teams plays. If successful, your effort [may even be adopted by the NFL](https://www.nfl.com/news/next-gen-stats-intro-to-expected-rushing-yards) for on air distribution, and you can watch future games knowing you had a hand in improving America's most popular sports league.

## Evaluation
### Overview
Your challenge is to generate actionable, practical, and novel insights from player tracking data that corresponds to special teams play. There are several potential topics for participants to analyze.

These include, but are not limited to:

1. Create a new special teams metric. The winning algorithm from the 2020 Big Data Bowl has been adopted by the NFL/NFL Network for on air distribution, and we are hopeful that there could be a new stat for special teams plays that could come from this year’s competition
2. Quantify special teams strategy. Special teams’ coaches are among the most creative and innovative in the league. Compare/contrast how each team game plans. Which strategies yield the best results? What are other strategies that could be adopted?
3. Rank special teams players. Each team employs a variety of players (including longsnappers, kickers, punters, and other utility special teams players). How do they stack up with respect to one another?
The above list is not comprehensive, nor is it meant to be a guide for participants to cover. We are open to all special teams related ideas in this year’s competition.

Submissions that examine one idea more thoroughly are preferred versus those that examine several ideas somewhat thoroughly.

### Scoring
An entry to the competition consists of a Notebook submission that is evaluated on the following five components, where 0 is the low score and 10 is the high score. Submissions will be judged based on how well they address:

##### Innovation:

- Are the proposed findings actionable?
- Is this a way of looking at tracking data that is novel?
- Is this project creative?

##### Accuracy:

- Is the work correct?
- Are claims backed up by data?
- Are the statistical models appropriate given the data?

##### Relevance:

- Would NFL teams (or the league office) be able to use these results on a week-to-week basis?
- Does the analysis account for variables that make football data complex?

##### Clarity:

- Evaluate the writing with respect to how clear the writer(s) make findings.

##### Data visualization/tables:

- Are the charts and tables provided accessible, interesting, visually appealing, and accurate?

Judges will consist of analytics staffers that are working for either (i) NFL headquarters, (ii) the 32 NFL teams, or (iii) player tracking vendors that work with NFL teams. Scores will be averaged so that each of the components above are weighed equally.

The top scoring entries in each of the following two categories will be awarded as winners.

**Open Competition:** Any submission related to Special Teams play can submit to the Open Competition.

**College Competition:** Same as the above but only open to college students. Students may only submit to either the Open or College Competition but not both.

### Notebook requirements
Notebooks should consist of no more than 2,000 words and no more than 10 tables/figures. Submissions will not be penalized for any number of words or figures under this limit. Participants are encouraged to show statistical code if it helps readers better understand their analyses; most, if not all code, however, should be hidden in the Appendix.

All notebooks submitted must be made public on or before the submission deadline to be eligible. If submitting as a team, all team members must be listed as collaborators on all notebooks submitted.

Any notebook that does not use the player tracking data will not be scored.

## Timeline
- September 23, 2021 - Start Date.

- January 6, 2022 - Entry and Final submission deadline.

All deadlines are at 11:59 PM UTC on the corresponding day unless otherwise noted. The competition organizers reserve the right to update the contest timeline if they deem it necessary.

## Submission Instructions

You can make as many submissions as you like, but we will only consider your latest submission before the deadline of January 7th.

If you are submitting as a team, you do NOT need to merge within the Kaggle platform (it's actually disabled), but all team members must be listed as collaborators on the submitted Notebook, and all team members must accept the competition rules before the submission deadline.

A valid submission will include a Notebook Analysis. All notebooks submitted must be made public on or before the submission deadline to be eligible. If submitting as a team, all team members must be listed as collaborators on all notebooks submitted.

**Click here to go to the [Submission form](https://www.kaggle.com/nfl-big-data-bowl-2022)**

# Data Description
## Summary of data
The 2022 Big Data Bowl data contains Next Gen Stats player tracking, play, game, player, and PFF scouting data for all 2018-2020 Special Teams plays. Here, you'll find a summary of each data set in the 2022 Data Bowl, a list of key variables to join on, and a description of each variable.

##File descriptions
- Game data: The games.csv contains the teams playing in each game. The key variable is gameId.

- Play data: The plays.csv file contains play-level information from each game. The key variables are gameId and playId.

- Player data: The players.csv file contains player-level information from players that participated in any of the tracking data files. The key variable is nflId.

- Tracking data: Files tracking[season].csv contain player tracking data from season [season]. The key variables are gameId, playId, and nflId.

- PFF Scouting data: The PFFScoutingData.csv file contains play-level scouting information for each game. The key variables are gameId and playId.

## Game data
- gameId: Game identifier, unique (numeric)
- season: Season of game
- week: Week of game
- gameDate: Game Date (time, mm/dd/yyyy)
- gameTimeEastern: Start time of game (time, HH:MM:SS, EST)
- homeTeamAbbr: Home team three-letter code (text)
- visitorTeamAbbr: Visiting team three-letter code (text)

## Play data
- gameId: Game identifier, unique (numeric)
- playId: Play identifier, not unique across games (numeric)
- playDescription: Description of play (text)
- quarter: Game quarter (numeric)
- down: Down (numeric)
- yardsToGo: Distance needed for a first down (numeric)
- possessionTeam: Team punting, placekicking or kicking off the ball (text)
- specialTeamsPlayType: Formation of play: Extra Point, Field Goal, Kickoff or Punt (text)
- specialTeamsPlayResult: Special Teams outcome of play - dependent on play type: Blocked Kick Attempt, Blocked Punt, Downed, Fair Catch, Kick Attempt Good, Kick Attempt No Good, Kickoff Team Recovery, Muffed, Non-Special Teams Result, Out of Bounds, Return or Touchback (text)
- kickerId: nflId of placekicker, punter or kickoff specialist on play (numeric)
- returnerId: nflId(s) of returner(s) on play if there was a special teams return. Multiple returners on a play are separated by a ; (text)
- kickBlockerId: nflId of blocker of kick on play if there was a blocked field goal or blocked punt (numeric)
- yardlineSide: 3-letter team code corresponding to line-of-scrimmage (text)
- yardlineNumber: Yard line at line-of-scrimmage (numeric)
- gameClock: Time on clock of play (MM:SS)
- penaltyCodes: NFL categorization of the penalties that occurred on the play. A standard penalty code followed by a d means the penalty was on the defense. Multiple penalties on a play are separated by a ; (text)
- penaltyJerseyNumber: Jersey number and team code of the player committing each penalty. Multiple penalties on a play are separated by a ; (text)
penaltyYards: yards gained by possessionTeam by penalty (numeric)
- preSnapHomeScore: Home score prior to the play (numeric)
- preSnapVisitorScore: Visiting team score prior to the play (numeric)
- passResult: Scrimmage outcome of the play if specialTeamsPlayResult is "Non-Special Teams Result" (C: Complete pass, I: Incomplete pass, S: Quarterback sack, IN: Intercepted pass, R: Scramble, ' ': Designed Rush, text)
- kickLength: Kick length in air of kickoff, field goal or punt (numeric)
- kickReturnYardage: Yards gained by return team if there was a return on a kickoff or punt (numeric)
- playResult: Net yards gained by the kicking team, including penalty yardage (numeric)
- absoluteYardlineNumber: Location of ball downfield in tracking data coordinates (numeric)

## Player data
- gameId: Game identifier, unique (numeric)
- playId: Play identifier, not unique across games (numeric)
- nflId: Player identification number, unique across players (numeric)
- Height: Player height (text)
- Weight: Player weight (numeric)
- birthDate: Date of birth (YYYY-MM-DD)
- collegeName: Player college (text)
- Position: Player position (text)
- displayName: Player name (text)

## Tracking data
Files tracking[season].csv contains player tracking data from season [season].

- time: Time stamp of play (time, yyyy-mm-dd, hh:mm:ss)
- x: Player position along the long axis of the field, 0 - 120 yards. See Figure 1 below. (numeric)
- y: Player position along the short axis of the field, 0 - 53.3 yards. See Figure 1 below. (numeric)
- s: Speed in yards/second (numeric)
- a: Speed in yards/second^2 (numeric)
- dis: Distance traveled from prior time point, in yards (numeric)
- o: Player orientation (deg), 0 - 360 degrees (numeric)
- dir: Angle of player motion (deg), 0 - 360 degrees (numeric)
- event: Tagged play details, including moment of ball snap, pass release, pass catch, tackle, etc (text)
- nflId: Player identification number, unique across players (numeric)
- displayName: Player name (text)
- jerseyNumber: Jersey number of player (numeric)
- position: Player position group (text)
- team: Team (away or home) of corresponding player (text)
- frameId: Frame identifier for each play, starting at 1 (numeric)
- gameId: Game identifier, unique (numeric)
- playId: Play identifier, not unique across games (numeric)
- playDirection: Direction that the offense is moving (left or right)

## PFF Scouting data
- gameId: Game identifier, unique (numeric)
- playId: Play identifier, not unique across games (numeric)
- snapDetail: On Punts, whether the snap was on target and if not, provides detail (H: High, L: Low, <: Left, >: Right, OK: Accurate Snap, text)
- operationTime: Timing from snap to kick on punt plays in seconds: (numeric)
- hangTime: Hangtime of player's punt or kickoff attempt in seconds. Timing is taken from impact with foot to impact with the ground or a player. (numeric)
- kickType: Kickoff or Punt Type (text).
	- Possible values for kickoff plays:
		- D: Deep - your normal deep kick with decent hang time
		- F: Flat - different than a Squib in that it will have some hang time and no roll but has a lower trajectory and hang time than a Deep kick off
		- K: Free Kick - Kick after a safety
		- O: Obvious Onside - score and situation dictates the need to regain possession. Also the hands team is on for the returning team
		- P: Pooch kick - high for hangtime but not a lot of distance - usually targeting an upman
		- Q: Squib - low-line drive kick that bounces or rolls considerably, with virtually no hang time
		- S: Surprise Onside - accounting for score and situation an onsides kick that the returning team doesn’t expect. Hands teams probably aren't on the field
		- B: Deep Direct OOB - Kickoff that is aimed deep (regular kickoff) that goes OOB directly (doesn't bounce)
	- Possible values for punt plays:
		- N: Normal - standard punt style
		- R: Rugby style punt
		- A: Nose down or Aussie-style punts
- kickDirectionIntended: Intended kick direction from the kicking team's perspective - based on how coverage unit sets up and other factors (L: Left, R: Right, C: Center, text).
- kickDirectionActual: Actual kick direction from the kicking team's perspective (L: Left, R: Right, C: Center, text).
- returnDirectionIntended: The return direction the punt return or kick off return unit is set up for from the return team's perspective (L: Left, R: Right, C: Center, text).
- returnDirectionActual: Actual return direction from the return team's perspective (L: Left, R: Right, C: Center, text).
- missedTacklers: Jersey number and team code of player(s) charged with a missed tackle on the play. It will be reasonable to assume that he should have brought down the ball carrier and failed to do so. This situation does not have to entail contact, but it most frequently does. Missed tackles on a QB by a pass rusher are also included here. Multiple missed tacklers on a play are separated by a ; (text).
- assistTacklers: Jersey number and team code of player(s) assisting on the tackle. Multiple assist tacklers on a play are separated by a ; (text).
tacklers: Jersey number and team code of player making the tackle (text).
- kickoffReturnFormation: 3 digit code indicating the number of players in the Front Wall, Mid Wall and Back Wall (text).
- gunners: Jersey number and team code of player(s) lined up as gunner on punt unit. Multiple gunners on a play are separated by a ; (text).
- puntRushers: Jersey number and team code of player(s) on the punt return unit with "Punt Rush" role for actively trying to block the punt. Does not include players crossing the line of scrimmage to engage in punt coverage players in a "Hold Up" role. Multiple punt rushers on a play are separated by a ; (text).
- specialTeamsSafeties: Jersey number and team code for player(s) with "Safety" roles on kickoff coverage and field goal/extra point block units - and those not actively advancing towards the line of scrimmage on the punt return unit. Multiple special teams safeties on a play are separated by a ; (text).
- vises: Jersey number and team code for player(s) with a "Vise" role on the punt return unit. Multiple vises on a play are separated by a ; (text).
- kickContactType: Detail on how a punt was fielded, or what happened when it wasn't fielded (text).
	- Possible values:
		- BB: Bounced Backwards
		- BC: Bobbled Catch from Air
		- BF: Bounced Forwards
		- BOG: Bobbled on Ground
		- CC: Clean Catch from Air
		- CFFG: Clean Field From Ground
		- DEZ: Direct to Endzone
		- ICC: Incidental Coverage Team Contact
		- KTB: Kick Team Knocked Back
		- KTC: Kick Team Catch
		- KTF: Kick Team Knocked Forward
		- MBC: Muffed by Contact with Non-Designated Returner
		- MBDR: Muffed by Designated Returner
		- OOB: Directly Out Of Bounds


![Football field layout](https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F3258%2F820e86013d48faacf33b7a32a15e814c%2FIncreasing%20Dir%20and%20O.png?generation=1572285857588233&alt=media)
