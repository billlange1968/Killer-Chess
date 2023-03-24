<h1>Killer Chess</h1>
<strong>By Greg Knauss</strong></br>
<em>From Antic Magazine, February 1988</em>
</br>

![killer_chess_title](https://user-images.githubusercontent.com/3913623/227552824-a8fccbee-816b-454c-a7f7-5ae609c50e09.png)

<h2>Two-player ACTION! shootout</h2>
<p>Killer Chess brings a new frenzy of aggression to the classic game, as you mop up the chessboard without waiting for your opponent to make moves. This type-in program is written in <a href="http://www.atarimania.com/utility-atari-400-800-xl-xe-action_s10963.html">ACTION!</a> and requires the ACTION! language cartridge from Optimized Systems Software, as well as an 8-bit Atari computer with at least 32K memory and a disk drive.</p>

<p>Unless you're a real fanatic or a tournament contender, I'll bet that you don't play much chess anymore. Let's face it, most "regular folks" find chess boring!</p>

<p>But now imagine a revitalized, fast-ACTION! chess-where the players don't take turns.</p>

<p>That's right. . . no turns. Killer Chess players make legal chess moves as fast as they can, deciding on instant strategies that they would have spent dull minutes pondering in a traditional game. Stodgy old chess becomes a fast-gun shootout.</p>

<p>Welcome to Killer Chess, written in ACTION! the fast, powerful programming language from Optimized Systems Software. You and your human opponent will use an Atari 8-bit computer and a pair of joysticks to battle it out in a radical new version of a traditional game.</p>

<h2>GETTING STARTED</h2>
<p>TYPING IT IN: Insert the ACTION! cartridge into your 8-bit Atari and type in Listing 1, KILLER.ACT Type carefully; because there isn't a TYPO II for ACTION! After you have a copy of the complete program safely saved, go to the monitor by pressing [CONTROL] [SHIFT] [M] and compile the program by typing [C] [RETURN]. When the cursor starts blinking again, type [R] [RETURN] and the title page should appear.</p>

<p>MONTHLY DISK USERS: You can play Killer Chess without owning the ACTION! cartridge. Just insert your Antic Monthly Disk into your disk drive, remove all cartridges from your Atari (XL/XE owners should press the [OPTION] key) and turn on your Atari. When the DOS menu appears, just type [L][RETURN], then type KILLER.EXE [RETURN].</p>

<p>When the title screen is seen, press [START] to begin a game. When the game begins, both players will be able to simultaneously move their respective cursors around the board. With joystick 0, player 1 controls the white cursor and white pieces. With joystick 1, player 2 controls the gray cursor and gray pieces.</p>

![killer_chess_game](https://user-images.githubusercontent.com/3913623/227552934-563492d5-2548-49da-a6db-f3fd6bebabba.png)

<h2>PLAYING KILLER CHESS</h2>
<p>Simply place the cursor over any piece you want to move and press the joystick button. Now move the cursor over a square that would be a legal move for that piece and press the button again. If the move is illegal, the computer will tell you so -with a rather unpleasant sound- and let you try again. Otherwise the piece will be placed at the new square. If you accidentally pick up a piece and don't want to move it, just replace the cursor over the piece you selected and press the button again. The piece will be dropped.</p>

<p>To capture an enemy, simply make a legal move on top of it. The offending piece will be removed from play. You can capture a piece your opponent is "holding". The piece isn't actually moved until it is set down again.</p>

<p>To win, just land one of your characters on top of the opponent's King. To return to the title screen press [START] or wait about 10 seconds.</p>

<p>Killer Chess does not have castling or en passant moves, which are allowed under advanced chess rules but would be too confusing here.</p>

<h2>ABOUT THE PROGRAM</h2>
<p>The biggest programming problem in Killer Chess was detecting illegal chess moves. My solution is quite simple and can be applied to any chess program. The method is even fast enough to be used with BASIC.</p>

<p>Here's what I did: When a piece is selected, its old position is recorded. Each new position chosen by a player is also recorded. The old position is then subtracted from the new position and stored in a "delta" value, one delta for X and one for Y Delta means how much something changes. So if the new X position is 5 more than the previous one, the Delta X would be five. If the new Y position is 1 less than the old, Delta Y would be -1.</p>

<p>I then used IF statements to determine if the piece was allowed to move to that spot. For instance, a pawn is only allowed to move forward, so I checked to make sure that Delta X is equal to nothing but 1. If the old position was equal to its starting position, I allowed it to move an extra space-because Pawns can move two spaces on their first move.</p>

<p>If the Pawn's new position is on top of an opponent's piece, I allowed for a Delta Y movement of either 1 or -1. Combined with the Delta X, that would result in diagonal movement. Simple, really. It just took a bit of planning to work out the values for the special conditions of each chess piece.</p>

<h2>Listing 1: KILLER.ACT</h2>
<em>killer.act listing in repository has ATASCII characters (control characters, inverse characters, etc.) replaced with ATASCII character codes so they are displayable.</em></br>

![kchess act](https://user-images.githubusercontent.com/3913623/227076395-c7b36769-d04c-4360-8196-6e3fd0f88642.png)

<h2>References</h2>

<a href="https://archive.org/details/1988-02-anticmagazine/Antic_Vol_6-10_1988-02_Scanning_Images/page/n10/mode/1up?view=theater">Killer Chess Article in Antic Magazine</a></br>
<a href="https://archive.org/details/1988-02-anticmagazine/Antic_Vol_6-10_1988-02_Scanning_Images/page/n74/mode/1up?view=theater">Killer Chess Listing  In Antic Magazine</a></br>
<a href="https://atariwiki.org/wiki/Wiki.jsp?page=Killer%20Chess">Killer Chess at AtariWiki</a></br>
<a href="https://www.akk.org/~flo/ATASCII.pdf">ATASCII Chart PDF File</a></br>

