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

<div id="xiangqi-notation"></div>

<script>
  var board = new XiangqiViewer.Board('#xiangqi-notation', 50, 2);
  board.defaultSetup();
  // board.place
  // var positionData = [
  //   {code: 'e', red: false, file: 2, rank: 0},
  //   {code: 'r', red: true, file: 0, rank: 8},
  // ];
  var moves = [
    {instruction: 'c2=5', red: true, analysis: 'a common opening'},
    {instruction: 'c8=5', red: false},
    {instruction: 'h2+3', red: true},
    {instruction: 'e3+5', red: false},
    {instruction: 'a6+5', red: true}
  ];

  board.setMoveList(moves);
</script>
