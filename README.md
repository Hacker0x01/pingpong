# The Offical HackerOne Round The Table PingPong Laws

## Vocabulary
| Terminology   | Translates to |
| ------------- |:-------------: |
| (right) in the just   | Someone hit a ball into the net. |
| just                  | Someone hit a ball via the net onto the opponent's side. Mostly used when serving. |
| laughing              | Haha |
| laughing plural       | Haha Haha |
| good seeing           | Nice catch |
| life taker            | Someone's life has been taken. Used when life was taken by a serve. |
| life saver            | Someone's life has been [saved by another](#saving-another-players-life). |
| reset                 | Someone's second-to-last life has been taken, resetting the life score to one. |
| gandalfing            | Players applying a "you shall not pass" action to another player, while the latter is trying to hit the ball. |
| clawless victory      | Someone tries to grab the ball, but fails |
| sporty                | Someone tries to pass the ball to the person that's supposed to serve, but fails (also see: clawless victory) |

## The laws

### Walking directions
- The normal walking direction is counterclockwise.
- It's allowed to deviate from the normal walking direction, as long as the player doesn't [gandalf](#vocabulary) another position or changes its place in the line.

### Lives
- Every player gets one life at the start of every round.
- When a player wins a finale the player will win a life.
- Lives can be accumulated, there is no maximum.
- Players losing a life are required to shout the number of remaining lives. A player lost its second-to-last life is required to shout ["reset"](#vocabulary).
- Players without any lives left lost the round.
- Quitting the round voluntarily will automatically destroy all accumulated lives – it's either win or lose.

### Direct Response
- Direct Response is a move where you would directly hit the opponent's ball back without the ball having touched your side of the table.
- It's illegal to do a Direct Response when the opponent just served.
- Players can do a Direct Response as you as you don't cross the net/[just](#vocabulary)

### Apology letter
Sportsmanship and being collegial are important values of the game. Therefore remorse should be shown, saying "Sorry" without laughing, in two situations where a player loses a life:
- Ball goes into a weird angle due to hitting the side or corners of the table
- Ball slightly hits the net drastically changing trajectory

If no proper remorse is shown the player taking the life loses a life **instead**.

### Tinus Time & Jan Time
- Jan Time and Tinus Time only occurs during a final battle between the last two remaining players.
- Jan Time is when one of the two finalists makes the first point. It is not allowed to join the table yet, but it's recommended to prepare for it.
- Tinus Time is when it's a 1:1 score between the two finalist. It's allowed for the other players to join the table, creating pressure for the finalists to fail. Shouting is recommended.

*Fun fact: Tinus Time is named after the famous player blocker [@martijnrusschen](https://github.com/martijnrusschen)*, who always prematurely joined the table before the finalists were finished.

### Tap Tap

After the finals, the player that lost must tap the bat twice on the table **before** serving, signaling to others that another round can commence. Failing to do so means the player in question loses a life.
If the player in question doesn't have any lives left, this rule applies to the player who won the round.

### Dirty Tinus
- When a player serves immediately after the mistake of a previous player
- This is only allowed when the table is in a valid state; there's no
  ball on the table
- If a player purposefully tries a Dirty Tinus when the table is invalid,
  that player loses a life

### Obstacles
- It's allowed to [gandalf](#vocabulary) another player. This often happens during [Tinus Time](#tinus-half-time) or when a player is deliberately trying to sabotage the other. 
- The blocked player has to shout "gandalf" and make an effort to still try to hit back the ball, preferrably hitting the blocker with the ping pong bat.

### Table Touch
It's allowed to touch the table to support your body weight to smash the opponent by bending over the player's side of the table.

### Classics
Classics are common patterns that return in Round The Table matches, noticably by the same players, which is the reason why the classics are named after them.

| Classics       | Translates to |
| -------------  |:-------------: |
| Classic Philip | The ball served by a player never hits the opponent's side by going over the table. Named after [@philipkocanda](https://github.com/philipkocanda) |
| Classic Dirk   | The ball hits the net ([right in the just](#vocabulary)), mostly during serve. Named after [@DZittersteyn](https://github.com/DZittersteyn) |
| Classic Jeurissen | Grabbing the ball during live play, because you don’t understand the rules. It’s based on old Roman scriptures, not to be confused with [@alexanderjeurissen ](https://github.com/alexanderjeurissen) |


### Ghost Membering
- Ghost Membering is for a player to sneak back to the table in the line of players while the player was hit out of the game.
- It's allowed to Ghost Member, but when another player notices and confronts the player, the latter has to return to the side line.
- It's allowed to try to Ghost Member multiple times during a single round.

### Voting
- A voting system is applied when players are in disagreement, and it's not clear what really happened.
- Voting at the ping pong table is similar to [Roman Voting](http://ancienthistory.about.com/od/romerepublic/qt/052611-How-the-Romans-Voted-in-the-Roman-Republic.htm), except the players use the colours of their ping pong bats. Black means benefit of doubt, red results elimination from the round. The colour with the most votes rule.
- When only a single player votes and holds up the ping pong bat to vote, that player is immediately eliminated from the round. When that player was already eliminated, the player has to skip the next round.

### Being not Jens enough
"Jens" is a synonym for "good". Named after one of the wise elders of the ping pong table, [@jenskanis](https://github.com/jenskanis).

### Saving another player's life
- A player can save another player's life by hitting the ball back for the other player, when he's unable to hit it back
- The player saving the other will loose its life if the player makes a mistake. This way there is always a risk involved helping others.

### Promoting Diversity
Diversity at HackerOne is a hot topic. We aim to be as diverse as possible. Not only when working on a world-class product, but also during teambuilding. Therefore any diverse playing member (e.g. women, foreigners, visitors from other locations) will start any round with one extra beginners life. That applies only if starting first round or when player has one normal life. So basically it's:

```ruby
rounds.each do |round|
  lives ||= [Live.new(type: :normal)]
  lives << Live.new(type: :beginner) if lives.count == 1
end
```

## Introducing new laws
Please make a pull request and the elderly of the table will decide if it's merge-worthy.
