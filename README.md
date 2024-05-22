# Klotski
Based on the DE1-SoC FPGA board, coded the classic game Klotski controlled by PS2 keyboard.

This project is developed by Yahe Zhang yahe.zhang@mail.utoronto.ca and Antony Weihong Zhuang antony.zhuang@mail.utoronto.ca.

How to operate:

To initiate gameplay or advance to the next level, simply press the enter key upon starting or
completing a level. To navigate within the game, utilize the PS2 keyboard to select the desired
block by entering its corresponding number. Once selected, employ the four-way arrow keys to
move the block in any of the four directions (up, down, left, and right), ensuring adherence to the
established Rules[1]. The primary objective is to move block 0 to the designated location
highlighted by a red boundary. Should the need arise, pressing the space key will reset the
game, allowing for a fresh start.

Rules[1]:

Like other sliding-block puzzles, several different-sized block pieces are placed inside a box,
which is normally 4×5 in size. Among the blocks, there is a special one (usually the largest) that
must be moved to a special area designated by the game board. The player is not allowed to
remove blocks, and may only slide blocks horizontally and vertically. Common goals are to solve
the puzzle with a minimum number of moves or in a minimum amount of time.

Attribution:

Yahe Zhang:

Game Logic - All the game framework and sets of rules to determine how the game operates.

VGA Display - Integrate double buffering forsmoother rendering; Convert images into arrays and render them on the display; Utilize a character buffer for printing characters on the screen.

Antony Zhuang:

Audio - The functionality is achieved through a polling mechanism; Upon reaching specific milestones, which are detecting a legal movement or clearing a level, the corresponding audio samples are dynamically filled into the designated audio address.

PS2 Keyboard - The system operates through a polling mechanism. When a user inputs a valid command by pressing the keys on PS2 Keyboard, the function converts this signal into another signal from the Game Logic to advance the game.
