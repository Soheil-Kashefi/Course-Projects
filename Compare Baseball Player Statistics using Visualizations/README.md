⚾ Comparing Baseball Player Statistics Using Visualizations

An analytical and visual comparison of two of Major League Baseball’s most powerful sluggers — Aaron Judge and Giancarlo Stanton — using Statcast data.

🚀 Project Overview

This project explores how data and visualization can illuminate the similarities and differences between Aaron Judge and Giancarlo Stanton — two of baseball’s biggest and hardest-hitting players.

Standing 6'7" (2.01 m) and weighing 282 pounds (128 kg), Judge is among the physically largest players in MLB history. Together with Stanton, he helped define an era of power hitting. In 2017, Stanton led the league with 59 home runs, followed by Judge with 52, far ahead of the next-best total of 45.

But despite their shared dominance at the plate, their underlying performance patterns differ. Using Statcast data, this project dives deep into how and why.

⚙️ About Statcast

Statcast is a state-of-the-art tracking system that uses a combination of high-speed cameras and radar to measure the precise location and motion of baseballs and players in real time.

Since being introduced to all 30 MLB ballparks in 2015, Statcast has revolutionized the game — powering an analytics “arms race” where teams hire data scientists and analysts to gain every possible competitive edge.

📊 Dataset Information

This analysis uses Statcast data for both Aaron Judge and Giancarlo Stanton covering the 2015–2017 seasons.
Each row represents a single pitch thrown to the player.

Datasets

judge.csv — Statcast data for Aaron Judge

stanton.csv — Statcast data for Giancarlo Stanton

Key Variables

Pitch-level attributes: pitch type, speed, spin rate, location

Batted ball metrics: exit velocity, launch angle, hit distance

Outcome metrics: event (e.g., single, double, home run), xBA, xSLG

🛠️ Technical Implementation
Technology	Purpose
Python	Core programming language
pandas	Data wrangling and manipulation
matplotlib	Data visualization and plotting
seaborn	Statistical and comparative charts
Jupyter Notebook	Interactive development environment
🎨 Custom Visualization Functions

Two helper functions are included to visualize Statcast strike zones and map pitch locations accurately:

assign_x_coord() → Converts Statcast zone numbers to x-coordinates

assign_y_coord() → Converts Statcast zone numbers to y-coordinates

These are used to plot heatmaps and scatter plots of pitch outcomes and contact locations.

🔍 Step-by-Step Analysis Workflow
1. Filter Data for 2017

Filtered each player’s dataset to only include records from the 2017 season using .loc[].

Accessed the events column and used .value_counts() to identify event distributions.

Saved results to judge_events_2017 and stanton_events_2017.

2. Filter for Home Runs

Isolated all rows where events == "home_run" to create dedicated DataFrames for both players’ home runs.

3. Create KDE Plots

Used sns.kdeplot() to visualize the launch angle (x-axis) vs launch speed (y-axis) for both players side by side:

Set up plots with plt.subplots(ncols=2, sharex=True, sharey=True)

Compared clustering patterns to determine whose home runs shared tighter performance zones.

4. Concatenate Home Run Data

Combined both players’ home run DataFrames using pd.concat() for cross-player visual comparisons.

5. Create Boxplots

Plotted release_speed by player_name using sns.boxplot() to compare median pitch speeds faced by each player.

6. Focus on Strike Zone (Zones ≤ 9)

Filtered out pitches outside the main strike zone using .loc[], keeping only zones <= 9.
Saved these subsets as judge_strike_hr and stanton_strike_hr.

7. Assign Cartesian Coordinates

Added new columns zone_x and zone_y using the custom coordinate functions (assign_x_coord, assign_y_coord) with .apply(axis=1) for both players.

8. Create 2D Histograms

Generated 2D histograms using plt.hist2d() to visualize strike zone home run density.
Included a plt.colorbar() to interpret frequency intensity across the grid.

📁 Project Structure

Compare-Baseball-Player-Statistics-using-Visualizations
├── README.md                                    # Project documentation
├── Compare_Baseball_Player_Statistics_using_Visualizations.ipynb  # Main analysis notebook
├── judge.csv                                    # Aaron Judge Statcast data
├── stanton.csv                                  # Giancarlo Stanton Statcast data
└── zone.png                                     # Strike zone visualization
