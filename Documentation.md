# NFT Mine Game Documentation

## Overview

The NFT Mine Game is a web-based card-matching game that combines entertainment with educational elements focused on blockchain technology. Players flip cards to find matching pairs while learning about blockchain concepts through simulated transactions using **Move** on the Aptos blockchain.

## Technologies Used

### Front-end Development
- **HTML**: Provides the structure of the game interface.
- **CSS**: Styles the game elements for visual appeal.
- **JavaScript**: Implements game mechanics and user interactions.

### Blockchain Integration
- **Move**: Integrates blockchain functionality. Upon game completion, **Move** simulates transaction details such as transaction ID, success status, and Aptos amount earned, displayed to the player.

### Deployment Platform
- **Netlify**: Hosts and deploys the game online, ensuring accessibility and ease of deployment.

## Features

1. **Card Matching**: Players click to flip cards and find matching pairs.
2. **Shuffling**: Cards are shuffled at the start of each game for randomness.
3. **Win Popup**: Upon completing the game, a popup congratulates the player and displays blockchain transaction details using **Move**.

## Code Example: Integration of Move in `game.js`

```javascript
// Example of Move integration in game.js

// Function to display transaction details using Move after winning
function displayMoveDetails() {
    const moveDetails = document.createElement('div');
    moveDetails.classList.add('popup');
    const message = document.createElement('p');
    message.textContent = 'Congratulations! You won an NFT on the Aptos blockchain.';
    moveDetails.appendChild(message);

    // Simulated Move transaction details
    const transactionDetails = document.createElement('p');
    transactionDetails.textContent = `Transaction ID: ${Math.random().toString(36).substr(2, 9)} | Status: Success | Amount: 10 APT`;
    moveDetails.appendChild(transactionDetails);

    document.body.appendChild(moveDetails);

    // Remove transaction details after a delay
    setTimeout(() => {
        moveDetails.remove();
    }, 4000);
}
```


## Conclusion

The NFT Mine Game provides an engaging gaming experience while introducing players to blockchain technology through **Move** and the Aptos blockchain. By integrating educational elements with gameplay, the game aims to foster understanding and interest in decentralized technologies among its players.
