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
elephant, cannon), and its _file_, the vertical line that its sitting on. Files
are numbered from 1 to 9, right to left, from the perspective of the given
player.

This means that on the diagram below, the chariot (

<div id="xiangqi-notation-1"></div>

<script>
  var board = new XiangqiViewer.Board('#xiangqi-notation-1', 50, 2, false);
  board.place([
    {code: 'e', red: false, file: 2, rank: 0},
    {code: 'r', red: true, file: 2, rank: 4}
  ]);
</script>

## Moving the piece
