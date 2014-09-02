---
title: Horse-Cannon Checkmate
date: 2014-06-18 04:52 UTC
tags: endgame, checkmate
---

One of the most common checkmates in xiangqi is the horse-cannon checkmate
(马后炮). In this checkmate, the cannon uses a horse as a mount (炮架) to place
the opponent's general in check. The horse also controls the opposing general's
only exits, resulting in a checkmate. The diagram below is an example (albeit
contrived) of this checkmate. The highlighted circles mark the general's only
exits from the cannon's check, which are controlled by red's horse.

<div id="horse-cannon-checkmate-1"></div>

<script>
  var board = new XiangqiViewer.Board('#horse-cannon-checkmate-1', 50, 2, false);
  board.place([
    {code: 'k', red: true, file: 4, rank: 9},
    {code: 'e', red: true, file: 4, rank: 7},
    {code: 'e', red: true, file: 2, rank: 9},
    {code: 'k', red: false, file: 4, rank: 1},
    {code: 'c', red: true, file: 1, rank: 1},
    {code: 'h', red: true, file: 2, rank: 1},
  ]);

  board.highlight({file: 4, rank: 0});
  board.highlight({file: 4, rank: 2});
</script>

This second diagram is another example of the horse-cannon checkmate. Step
through the moves to see the checkmate in action.

<div id="horse-cannon-checkmate-2"></div>

<script>
  var board = new XiangqiViewer.Board('#horse-cannon-checkmate-2', 50, 2, true);
  board.place([
    {code: 'k', red: true, file: 4, rank: 9},
    {code: 'e', red: true, file: 4, rank: 7},
    {code: 'e', red: true, file: 2, rank: 9},
    {code: 'k', red: false, file: 4, rank: 0},
    {code: 'a', red: false, file: 3, rank: 0},
    {code: 'a', red: false, file: 5, rank: 0},
    {code: 'c', red: true, file: 1, rank: 5},
    {code: 'h', red: true, file: 3, rank: 3},
  ]);

  board.setMoveList([
    {instruction: 'h6+7', red: true, analysis: "Red's horse places black in check."},
    {instruction: 'k5+1', red: false, analysis: 'Black has only one legal move.'},
    {instruction: 'c8+4', red: true, analysis: 'Red completes the horse-cannon checkmate.'},
  ]);
</script>
