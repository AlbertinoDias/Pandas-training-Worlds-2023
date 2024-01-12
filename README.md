# Pandas training Worlds 2023
Project made to learn/test Pandas. Used to analize/track what happened on the League of legends worlds 2023 tournament. All the info was added by hand.
<header>

<h1>CSV Contents</h1>

<h2>champions.csv</h2>

This is the main .csv, here every information related to the teams/champions/players is stored:

<ul>															
  <li>champion: String, stores the name of the champion picked</li>
  <li>picked: Bool, if true, the champion was picked, if false, the champion was banned</li>
  <li>side: String, B if blue side R if red side</li>
  <li>order: Int, indicates in which position of the draft (1-5) the champion was picked/banned</li>
  <li>team: String, the initials of the team that picked the champion</li>
  <li>enemy: String, the initials of the oposite team from the one that picked the champion</li>
  <li>game: Int, stores the game number (first game for those teams at that date, 3rd game etc)</li>
  <li>position: String, role that the champion was used in (TOP, JUNGLE, MID, ADC, SUPPORT)</li>
  <li>player: String, Name of the player that picked the champion</li>
  <li>fb: Bool, if true, that was who got the first blood kill, otherwise false (only 1 true per game) </li>
  <li>kills: Int, number of kills that game</li>
  <li>deaths: Int, number of deaths that game</li>
  <li>assists: Int, number of assists that game</li>
  <li>date: Date, the date in which the game took place (YYYY-MM-DD) </li>
  <li>won: Bool, true if the team won, false if they lost</li>
  <li>time: Time, the time it took for the game to end</li>
  <li>penta: Bool, true if that player/champion got a penta that game, false other wise</li>
  <li>stage: String, the stage at which the game was played (PLAY-INS, SWISS, QUARTER, SEMI, FINALS) </li>
</ul>

<h2>teams_region.csv</h2>
Created to train merging dataframes

<ul>															
  <li>region: String, the initials of the Region the team belongs to</li>
  <li>team: String, the initials of the team that picked the champion</li>
</ul>

<h2>games.csv</h2>
The same as champions.csv but with "region" added, a String that stores from what reagion the "team" is, was added at the end of everything as an afterthought to train merging dataframes

<h2>drakes.csv</h2>

This is the secondary .csv, here every information related to the dragons killed is stored:

<ul>															
  <li>type: String, name of the dragon (ocean, infernal, cloud, mountain, hextech, chemtech)</li>
  <li>team: String, initials of the team that killed the dragon</li>
  <li>enemy: String, initials of the team that is playing against the team that killed the dragon</li>
  <li>game: Int, stores the game number (first game for those teams at that date, 3rd game etc)</li>
  <li>order: Int, indicates in which position of the order of dragon kills that game it was</li>
  <li>time: Time, the time of the game the dragon was killed</li>
  <li>date: Date, the date in which the game took place (YYYY-MM-DD) </li>
  <li>won: Bool, Bool, true if the team that killed the drake won, false if they lost</li>
  <li>stage: String, the stage at which the game was played (PLAY-INS, SWISS, QUARTER, SEMI, FINALS)</li>
</ul>


<h1>How to run</h1>

Before running the code, it is important to note that since this was for a learning experience some code was not erased despite nor working currentely,
at the end of the project, adaptation were made so the code would work for a specified time and thus some previous code was not mantained anymore.

<h2>Cells to run (in order)</h2>

This means that every cell bellow the "title" is to be run:
<ol>															
  <li>Imports and stuff</li>
  <li>Open all csv</li>
  <li>Functions to control the csv</li>
   <ol>
     <li>including: Champions csv</li>
     <li>including: dragon csv</li>
    </ol>
  <li>Controllers</li>
    <ol>
     <li>including: champions time modifier</li>
     <li>including: drakes time modifier</li>
    </ol>
</ol>


<h2>Chose the dates</h2>
After running those cells, the first cell bellow the "Controllers" has 3 variables that can be changed to get specific time frames, every time possible is a variable that was assigned above those 3:
<ul>															
  <li>between_time: Chose 2 times to get data only between those 2 times</li>
  <li>less_than: Chose a date to get everything up to that date</li>
  <li>exact_date: Chose a specific date to get</li>
</ul>

For the full event ignore this step and see next

<h2>Run the analysis</h2>
To check the data scroll down until you reach the title "Specific time"

Here you will see that in every cell, before the function there are 4 linees that start with a "@"
3 of them need to be commented ("#") at all times and the uncommented one is what will dictate what time frame the function will output:
(X represents either "champions" or "drakes" depending on the cell)
<ul>															
  <li>modify_X_date_everything : Get the data from all the games</li>
  <li>modify_X_date_before: Get the data from the specified date in the variable: "less_than" of the previous step</li>
  <li>modify_X_date_between : Get the data from the specified date in the variable: "between_time" of the previous step</li>
  <li>modify_X_exact_date : Get the data from the specified date in the variable: "exact_date" of the previous step</li>
</ul>



