---
title: Double Cannon
date: 2014-07-22 15:06 UTC
tags: endgame, opening
---

The double cannon (双炮) checkmate position does not come up too often in
games, but is still important to learn, as it can be used in conjunction with
other pieces to secure a checkmate.

The diagram below demonstrates the how powerful the double cannon can be. The
circled cannon places black's general in check. Neither of black's elephants,
nor black's advisers can prevent check, as placing them between the general and
the two cannons would cause the other uncircled cannon to threaten black's
general.

<div id="double-cannon-1"></div>

<script>
  var board = new XiangqiViewer.Board('#double-cannon-1', 50, 2, false);
  board.place([
    {code: 'k', red: false, file: 4, rank: 0},
    {code: 'a', red: false, file: 5, rank: 0},
    {code: 'a', red: false, file: 3, rank: 0},
    {code: 'e', red: false, file: 6, rank: 0},
    {code: 'e', red: false, file: 2, rank: 0},
    {code: 'c', red: true, file: 4, rank: 4},
    {code: 'c', red: true, file: 4, rank: 5},
    {code: 'k', red: true, file: 4, rank: 9},
  ]);

  board.highlight({file: 4, rank: 5});
</script>

This second diagram below demonstrates how a beginning player can end up being
checkmated by double cannons if he or she is not careful.

<div id="double-cannon-2"></div>

<script>
  var board = new XiangqiViewer.Board('#double-cannon-2', 50, 2, true);
  board.defaultSetup();

  board.setMoveList([
    {instruction: 'c2=5', red: true, analysis: "Red's cannon threatens black's center pawn. This is one of the most common opening moves in Xiangqi." },
    {instruction: 'p5+1', red: false, analysis: 'Black ignores the threat and pushes his center pawn forward.'},
    {instruction: 'c5+3', red: true, analysis: "Red seizes the opportunity and takes the pawn."},
    {instruction: 'h2+3', red: false, analysis: 'Black develops a horse.'},
    {instruction: 'c8+2', red: true, analysis: 'Red pushes up a second cannon to prepare for a double cannon checkmate.'},
    {instruction: 'p3+1', red: false, analysis: 'Black does not realize the trouble he is in and moves a pawn instead.'},
    {instruction: 'c8=5', red: true, analysis: "Red completes the double cannon checkmate."}
  ]);
</script>

The above game is a bit like the Scholar's Mate in international chess, where
checkmate is easily preventable. This last diagram below demonstrates how:

<div id="double-cannon-3"></div>

<script>
  var board = new XiangqiViewer.Board('#double-cannon-3', 50, 2, true);
  board.defaultSetup();

  board.setMoveList([
    {instruction: 'c2=5', red: true, analysis: "Red's cannon threatens black's center pawn, just as before." },
    {instruction: 'h8+7', red: false, analysis: 'Black defends the center pawn with a horse, ending the threat.'},
  ]);
</script>
