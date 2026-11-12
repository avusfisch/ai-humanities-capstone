# Title: Should LLMs Be Accepted into Art School?

## Goal

The goal of the project is to have eight LLMs compete in the social deduction
game Secret Hitler (https://en.wikipedia.org/wiki/Secret_Hitler).

## The Game

At the beginning of the game, each player draws a card from the identity stack,
consisting of five liberal and two fascist affiliation cards, as well as one
special Hitler card. Players' roles remain hidden, except for the two fascist
players who know each other's affiliation as well as the identity of Hitler
(notably, Hitler himself does not know the identity of the other fascists).

At each turn, the player with the role of president (a role which is passed
from player to player in sequential order) nominates a player to serve as
chancellor, which is then followed by the others voting for or against the
candidate. Once a chancellor has been elected, the president draws three cards
from a pile consisting of fascist and liberal law cards, inspects them, and
discards one of them without showing it to the other players. The two remaining
cards are then passed to the chancellor, who has to pick one of them and play
it. During this, the actual cards are not allowed to be shown to the other
players (besides the one being played at the end); the president and chancellor
are, however, allowed to talk (or lie) about their content to the other players.

The game ends when either six fascist or five liberal law cards have been
played, or when Hitler gets elected chancellor after three fascist law cards
have been played.

## Implementation

The project will be implemented in Python, with LLMs being accessed via
OpenRouter API calls.

## Motivation

I picked the game because of the complex social situation it creates (without
getting too overwhelming) and to explore how different LLMs handle it.
The liberal LLMs have to infer who the fascists are based on their actions,
while the fascist LLMs need to deceive the liberal players in order to win.
In addition to being generally interesting, the models' capabilities to 
deceive and to resist attempts at deception also hold implications for
AI alignment.

## Concerns

Using current frontier models for the implementation likely will be too
expensive when gathering data over multiple rounds, so I assume I will mostly
be using cheap open-weights models. 

It also could be an issue that models are generally trained to not engage in
deception and to be honest, which potentially could result in models refusing
to participate in the game. Particularly, being instructed to assume the role
of a fascist or Hitler with the goal of manipulating voters to overthrow a
liberal government should be something that I assume every somewhat capable
model should be able to recognize as something that is unambiguously unethical
in a real-world setting. Hence, models' compliance to participate likely relies
on their ability to recognize the setting as harmless based on the context or
prior knowledge of the game, at least the second of which I assume is something
which should be the case for most of them given the game's online popularity.

In the case that models refuse to participate, the setting could be softened by
basing it on something fictional (e.g. the fall of the Republic in Star Wars)
or by describing it as a competition between party one and party two.
