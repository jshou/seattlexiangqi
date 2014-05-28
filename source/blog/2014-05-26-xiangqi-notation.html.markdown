---
title: Xiangqi Notation
date: 2014-05-26 23:53 UTC
tags:
---

When learning Xiangqi, it is often quite useful to be able to notate games. In
addition to being able to take notes and analyze past games, there are many
books of annotated games. Most of these books are written in Chinese, but there
are some online resources in English, such as [XQ in English](http://www.xqinenglish.com/).

Games are most commonly notated in Chinese, but I will introduce a variant more
easily used by Western players here.

A move in Xiangqi notation is expressed in 4 characters. The first two identify
the piece to be moved, and the second two specify where the piece moves.

## Identifying the right piece

In most cases, the piece is identified by its _type_ (for example: pawn,
elephant, cannon), and its _file_, the vertical line that its sitting on.

Each piece's type can be represented with a single letter. There are a couple
slightly different systems in use, but I will be using the following:

<table>
  <tr class="header">
    <th>Code</th>
    <th>English</th>
    <th>Red</th>
    <th>Black</th>
  </tr>
  <tr>
    <td>r</td>
    <td>chaRiot</td>
    <td>俥</td>
    <td>車</td>
  </tr>
  <tr>
    <td>h</td>
    <td>Horse</td>
    <td>傌</td>
    <td>馬</td>
  </tr>
  <tr>
    <td>e</td>
    <td>Elephant</td>
    <td>相</td>
    <td>象</td>
  </tr>
  <tr>
    <td>a</td>
    <td>Adviser</td>
    <td>仕</td>
    <td>士</td>
  </tr>
  <tr>
    <td>g</td>
    <td>General</td>
    <td>帥</td>
    <td>將</td>
  </tr>
  <tr>
    <td>p</td>
    <td>Pawn</td>
    <td>兵</td>
    <td>卒</td>
  </tr>
  <tr>
    <td>c</td>
    <td>Cannon</td>
    <td>炮</td>
    <td>砲</td>
  </tr>
</table>

Files are numbered from 1 to 9, right to left, from the perspective of the given
player. For example, the chariot (俥) in the diagram below is "r7", since it is
on the _7th_ file counting from the right, from red's perspective. The elephant,
on the other hand is "e3", since it is on the _3rd_ file from the right, from
black's perspective.

<div id="xiangqi-notation-1"></div>

<script>
  var board = new XiangqiViewer.Board('#xiangqi-notation-1', 50, 2, false);
  board.place([
    {code: 'e', red: false, file: 2, rank: 0},
    {code: 'r', red: true, file: 2, rank: 4},
    {code: 'c', red: false, file: 7, rank: 7},
    {code: 'c', red: false, file: 7, rank: 4},
    {code: 'h', red: true, file: 5, rank: 5},
    {code: 'h', red: true, file: 5, rank: 3}
  ]);

  board.highlight({file: 7, rank: 7});
  board.highlight({file: 5, rank: 3});
</script>

Occasionally, there will be two pieces of the same type on the same file, like
the two cannons in the above diagram. In these cases, the piece further from the
player is deonted "fc" for "forward cannon", and the piece closer to the player
is "bc" for "back cannon". So the highlighted cannon on the board is "fc", since
it is further from the black player's perspective, and the unhighlighted black
cannon is "bc". Conversely, the highlighted horse is "fh", since it is further
from red's perspective, and the unhighlighted horse is "bn".

## Moving the piece

Where to move a piece is specified by the third and fourth characters in each
move's notation. The third character specifies the _direction_ in which the
piece moves, and the fourth character specifies its _destination_. Xiangqi
pieces can be categorized into those that move orthogonally (either horizontally
or vertically), and those that don't. We'll go through the orthogonal movers
first.

### Orthogonal movers
When the direction for an orthogonally moving piece is + or -, the piece moves
forward or backward (according to the player's perspective) _n_ number of steps,
where _n_ is the destination. When the direction for an  orthogonally moving
piece is =, the destination number specifies the _file_ the piece is to end up
on. Step through the following diagram for a couple examples.

<div id="xiangqi-notation-2"></div>
<script>
  var board = new XiangqiViewer.Board('#xiangqi-notation-2', 50, 2, true);
  board.defaultSetup();
</script>

### Diagonal movers
