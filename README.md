
# Friendship Manager DApp

## Overview

FriendshipManager is a decentralized application (dApp) built using React, Solidity, and web3 technologies. The application allows users to manage friendships on the Ethereum blockchain. Users can add, remove, and view their friends, as well as see friends of friends and their friendship history. The project also integrates decentralized friend recommendations using Circles, and it leverages subgraphs to track and query smart contract data.

## Features

1. **Add Friend:** Users can add new friends by inputting the wallet address of the friend.
2. **Remove Friend:** Users can remove a friend from their list.
3. **Friends List:** Displays a list of all the user's friends.
4. **Friends of Friends:** Shows friends of the user's friends.
5. **Friendship History:** Provides a history of friendship interactions.
6. **Decentralized Friend Recommendations:** Recommends friends based on mutual connections.
7. **Graph Integration:** Uses subgraphs to track and query smart contracts for efficient data retrieval and relationship mapping.

## Installation

### Prerequisites

- **Node.js** and **npm** installed.
- **MetaMask** browser extension for Ethereum wallet management.

### Clone the Repository

\`\`\`bash
git clone https://github.com/yourusername/friendship-manager-dapp.git
cd friendship-manager-dapp
\`\`\`

### Install Dependencies

\`\`\`bash
npm install
\`\`\`

## Usage

1. **Start the Application**

   \`\`\`bash
   npm start
   \`\`\`

2. **Interact with the DApp**

   - On startup, the DApp will prompt the user to input their Ethereum wallet address.
   - Users can manage their friendships using the provided features.

## Project Structure

- **/src**
  - **/components**
    - **AddFriend.js**: Component for adding a new friend.
    - **RemoveFriend.js**: Component for removing a friend.
    - **FriendsList.js**: Component for listing friends.
    - **FriendsOfFriends.js**: Component for showing friends of friends.
    - **FriendshipHistory.js**: Component for viewing friendship history.
    - **FriendRecommendations.js**: Component for decentralized friend recommendations.
  - **App.js**: Main application component.

- **/graphs**
  - **subgraph.yaml**: Configuration for tracking the FriendshipManager smart contract.
  - **schema.graphql**: GraphQL schema for querying data.
  
##Circles Integration

The project integrates Circles for decentralized friend recommendations. Circles uses trust relationships to recommend new friends to users based on their existing connections.
## Graph Integration

The project integrates graph technology to enable efficient querying of the FriendshipManager smart contract. The subgraph tracks contract events, allowing users to easily retrieve and visualize data, such as friendship connections and history.

### Querying the Subgraph

You can query the subgraph using GraphQL. Below is an example of how to fetch all friends of a user:

\`\`\`graphql
{
  user(id: "0xUserAddress") {
    friends {
      id
      name
    }
  }
}
\`\`\`

## Deployment

### Build the Application

\`\`\`bash
npm run build
\`\`\`

### Deploying the Subgraph

1. Ensure you have the Graph CLI installed:

   \`\`\`bash
   npm install -g @graphprotocol/graph-cli
   \`\`\`

2. Deploy the subgraph:

   \`\`\`bash
   graph deploy --product hosted-service <your-subgraph-name>
   \`\`\`

## Contribution

Contributions are welcome! Please fork the repository and submit a pull request for any features or improvements.

## License

This project is licensed under the MIT License.
