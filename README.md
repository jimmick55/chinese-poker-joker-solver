# Joker Chinese Poker Solver

Enter your 13 cards and the four face-up cards. The solver checks every legal front–middle–back setup, deals the remaining cards to three opponents thousands of times, and ranks setups by expected points.

56 cards · 4 jokers wild 1 point per row Scoop doubles everything Scoop all 3 pays ×4 Royalties paid only when the row wins Joker face-up doubles stakes

Your hand

Face-up (out of play)

Typing: ranks A K Q J 10 (or T) 9–2, suits s h c d (or ♠♥♣♦), jokers as `jk`. Typing replaces whichever pile is selected above. Click a card in a pile to remove it.

## Best setup

Pick 13 cards and press Solve.

How points are counted

- Each row you win against an opponent pays 1 point plus that row's royalty. Each row you lose costs 1 point plus the opponent's royalty. Royalties are paid only when the row wins.
- Winning all three rows against one opponent doubles everything won from that opponent, royalties included. Losing all three doubles what you pay.
- Scooping all three opponents doubles again what each one pays you (×4 in total). The same applies against you: an opponent who scoops you and both other players collects ×4 from you. Every opponent must play their hand, so an opponent's natural cancels this bonus.
- A joker among the face-up cards doubles every payment that game, naturals included. If you enter fewer than four face-up cards, the missing ones are drawn at random in each simulated deal.
- Royalties. Front: trips 2, two jokers 9 (in place of the trips 2). Middle: full house 1, quads 7, straight flush 9, five of a kind 15. Back: quads 3, straight flush 4, five of a kind 7.
- Two jokers in the front make trips of the third card (two jokers with a 5 are three 5s), so the middle must be at least that strong.
- Naturals (no jokers in hand) collect 6 from each opponent. If an opponent has a natural, you pay them 6 and your hand doesn't play against theirs. Two naturals cancel.
- Straights rank A-K-Q-J-10, then A-2-3-4-5, then K-high down to 6-high. Ties go to the suit of the highest card (♠ ♥ ♣ ♦). A joker that decides a suit tiebreak counts as a spade. In a flush, jokers become the highest missing ranks.
- Opponents set their hands with a strength model that weighs each row's chance of winning and royalties, tuned on tens of thousands of simulated hands. They never foul. Real opponents may play better or worse, so treat the totals as estimates.
- "Per row" values include the scoop doubling, so front + middle + back + opponent naturals = total. Every setup is scored against the same simulated deals, so the ranking between setups is sharper than the ± range suggests.