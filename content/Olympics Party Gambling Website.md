**Goal**
Build a website for olympics party for people to gamble on games.

# Requirements
- Users can are given a fixed sum of money
- Users can place bets on the currently active game for either a win or a loss.
- Odds are calculated with an algorithm
- At the end of each game, the admin user manually informs the system that the game is over.
- After the game has been marked as over, players are awarded their money and shown the next game.
- Users should be able to view a live leaderboard for both money and points
- Users are assigned to a country. Each country has a series of offsets which are used when gambling.
Optional
- Users are prompted at predefined times to buy items
- Items can then be used to interact with different players

# HLD
- User interface
	- Communicates with backend using websockets for real-time updates.
- Database stores results of games & current user balances
	- Allows for the app to restart and scores to be persisted.
- Monolithic backend app
	- No need for scalability

## Backend App HLD
- Login endpoint - no auth
- Betting interface endpoint - authed
- Leaderboard view - no auth

- Credentials manually inserted
- Countries stored in an Enum
- Users stored in an Enum

- Insert games with a SQL script

## FE HLD
- Looks not important
- Ease of dev important
- Must have nice websocket integration
# Spring WebSockets


# Items to do
- **DONE** Set up basic spring & react app & test websockets
	- OG1 - Create Spring App
	- OG2 - Create React App
	- OG3 - Test websockets
- create basic single user app to place a bet on a game.
- Support multiple users betting on same game
- Create basic admin console with ability to end game
- Update FE to respond to ended game
- Create overview page

# Investigations
## How to call an endpoint in react?

## React refresher
### State
`useState()` creates a state variable
A hook, meaning it can only be called at the top level of a component

**Why state over a var?** 
- Local vars dont persist over renders of the page
- Changing local vars doesnt trigger a re-render

The state var contains the state persisted over renders and the setState function sets the state and triggers a rerender.

**How to use setState**


## Typescript refresher
