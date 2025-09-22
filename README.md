# MiniMonster
Script for [Spike2](https://ced.co.uk/products/spkovin) to analyze patch-clamp data.

## Installation
This script is developed for [Spike2 v10](https://ced.co.uk/products/spike2history/10). It should be compatible with [Spike2 v6](https://ced.co.uk/products/spike2history/6) or higher, however compatibility with these older versions is not tested.  
Copy the scipt folder in any directory and open the **MiniMonster.s2s** file using Spike2.

## Quick Guide
- Run the script either with a data file open or open a file when prompted.
- Select the channel you want to analyze when prompted (you can only analyze one channel at a time currently).
- Place the cursors left and right of a section of you signal that does **NOT** contain any of the peaks you want to analyze to estimate signal background levels.
- adjust settings to your liking and press "OK" (the script will automatically load the last used configuration).
- Make changes during manual review if desired.
- Output is generated in the textwindow to the left and can be saved to disk.


## Changelog v1.7b
* 1.76b
  - Report SEM and SD for Amplitude, Slope, Half-width and decay for summary statistics.
* 1.75b
  - Peak review dialog can now cycle only between approved events.
* 1.74b
  - Added channel standard deviation to settings dialog and protocol.
  - Cancelling the settings dialog and terminating the script will no longer leave an empty marker channel behind.
  - Report event onset and end times.
  - Save marker channel to disk at the end.
  - Generate WaveMark channel of approved peaks.
* 1.73b
  - Query user to open a Spike2 Datafile if none is open at script start.
* 1.72b
  - Only load channel number from config file if the channel exists as Waveform channel in current data file.  
* 1.71b
  - Fixed a bug that would cause negative frequencies when the processed channels were discarded.
  - Correctly disable maunual mode settings on initial settings dialog load.
  - Fixed includes working correctly if Spikes is started from a folder different to the one containing the main script.
* 1.7b
  - Changed Settings dialog and  added saving and loading of config files.

_For changes in earlier versions address the changelog included in the MiniMonster.s2s Versions() procedure._