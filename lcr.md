---
title: C++
---
[< Back to index](index.md)

## C++ - LCR Dice Game

This project is a simulated dice game called left center right. It was coded in C++ using Microsoft Visual Studios. This project includes an informal review and a walkthrough of the code after enhancement.

### Sample Code Before Enhancement
```C++
int main()
{
int numPlayers = 0;
srand((unsigned)time(NULL)); //seed the random number generator

//continues until a valid number of players is received (3 or more)
while (numPlayers < 3)
{
cout << "This game requires 3 or more players." << endl;
numPlayers = setNumPlayers();
}

players.resize(numPlayers(); //populate structure for storing player class objects with number of players

//get player names
for (unsigned int i = 0; i < players.size(); i++)
{
players.at(i).obtainName();
}

directions(): //display game rules to player

startGame(); //begin game

return 0;
}
```

### LCR Dice Game Informal Review  
<a href="http://www.youtube.com/watch?feature=player_embedded&v=ypwquhHScjg
" target="_blank"><img src="http://img.youtube.com/vi/ypwquhHScjg/0.jpg" 
alt="LCR Dice Game Narrative" width="240" height="180" border="10" /></a>

### Sample Code After Enhancement
```C++
int main()
{

	srand((unsigned)time(NULL)); //seed the random number generator

	displayDirections();

	setUpPlayers();

	startGame();

	return 0;
}
```
### LCR Dice Game Enhancement Walkthrough
<a href="http://www.youtube.com/watch?feature=player_embedded&v=lojidoW1azU
" target="_blank"><img src="http://img.youtube.com/vi/lojidoW1azU/0.jpg" 
alt="LCR Dice Game Narrative" width="240" height="180" border="10" /></a>
  
[< Back to index](index.md)
