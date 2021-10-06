# blockchain-developer-bootcamp-final-project

UNICORN HASH
www.unicornhash.io

DESCRIPTION
The front end website allows users to create art pieces from data they input. There’s a structure for them to enter a pattern of data and create a visual piece. To start with, for the final project, the data to be entered will be a 5x10 grid of squares. Users can choose red, blue, or yellow for each of the squares, making a pattern for the 50-square grid. 

Once they are satisfied with the pattern they created, they can COMMIT. This will create a hash of the visual on the screen (which may also include other data fields) and compare that hash to a database of stored hashes from prior users. 

If that pattern does exist, the user will have created a new pattern, and will get an opportunity to store additional data, such as their username and the date of creation, and add that pattern to the database. 

If the user’s pattern does exist in the database of hashes, then data about the stored pattern will appear: who created it and when, plus other custom data fields that may be stored.

If the pattern is newly created, the user will have the opportunity to MINT IT to a wallet address. This might entail lazy minting, like a POAP, where the user can mint it on-chain at a later time, but display the art in a wallet account. 

I’d like each pattern to have a rareness tag. In the first version, this would just be modelled on how many times that pattern has been guessed, but in a future version, it could be based on other custom data fields, such as the likelihood of attaining certain character qualities or combinations.

A future version of this could have a variety of data inputs - color choices, randomness, blockchain data, oracles, or other custom data entry - and it could output different visuals - we start with the grid of 50 squares but later it could be characters where appearance and values are determined by data entry (like CryptoZombies), or art pieces in the style of a participating artist.

ELEMENTS

WEB FRONT END

Website and front end visual data entry systems (50 squares where R,B,Y can be chosen for each one creating a pattern, and a COMMIT button. 
Website output of results of COMMIT button - yes path - display data that already exists.
Website output of results of COMMIT button - no path - “you created a new pattern! Enter more data.”
MINT button
START OVER button
Connect your web3 wallet button - or this might be required at the start to use the dapp
Wishlist: a layer of abstraction that allows text data to be turned into a visual (like CryptoZombies) for future use, and addition of randomness function (where a good source of randomness is used to choose a square but ultimately may be factored into the visual produced in a more complex way, TBA.) If I don’t complete these I at least want to think about their integration in this version.

HASHING & HASH STORAGE

Hash the visual produced by the user 
Compare the hash to a database of hashes. How is this decentralized? IPFS?
Output results of hash comparison
Prompt to add additional data (on the no path, where the pattern is new.) Store that. Is this a new hash, and if so does this unnecessarily complexify the hash database?
Increment the number of times the hash/pattern has been queried each time (for Rarity Eval)

USER ACCOUNT 

Wallet connect to recognize user and display their patterns when they return
Connection to minting function

MINTING

POAP-type lazy minting function (user can choose to mint or not)
Layer 2: Polygon
Metadata (dapp, artist info, etc)
Is it possible to take a fee on minting to chain? This would help support artists. Alternatively, possible to embed a royalty % so artist can benefit from secondary sales?

RARITY EVALUATION

Evaluate rarity based on prior searches for that pattern.
Think through evaluation of rarity based on custom data fields for future use.
High rarity value may encourage minting on-chain.

This may have to be simplified to complete a version for the final project, so I'll be focusing on the skeleton and a minimum viable dapp.
