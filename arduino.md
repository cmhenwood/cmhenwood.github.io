## Spaceship Interface - Arduino

### Schematic

<img src = "images/spaceShipInterfaceSchematic.png">

### Demo

<a href="http://www.youtube.com/watch?feature=player_embedded&v=XCVt5tGuaa8
" target="_blank"><img src="http://img.youtube.com/vi/XCVt5tGuaa8/0.jpg" 
alt="Aruino - Spaceship Interface Demo" width="240" height="180" border="10" /></a>

### Code

```markdown


/*
One green LED (D1) symbolizing "system ready" remains lit until switch (SW1)
is depressed at which point two red LEDs (D2&D3) alternate turning on and off
every 250ms symbolizing "engage hyperdrive" while the switch remains depressed.
*/

int switchState = 0; //initialized to off

void setup() {

  pinMode(3,OUTPUT); //D1
  pinMode(4,OUTPUT); //D2
  pinMode(5,OUTPUT); //D3
  pinMode(2,INPUT); //SW1
}

void loop() {

  switchState = digitalRead(2); //get SW1 state
  //HIGH is on and LOW is off
  if ( switchState == LOW ) {
    digitalWrite(3, HIGH);
    digitalWrite(4, LOW);
    digitalWrite(5, LOW);

    } else {
    digitalWrite(3, LOW);
    digitalWrite(4, LOW);
    digitalWrite(5, HIGH);
    
    delay(250);
    digitalWrite(4, HIGH);
    digitalWrite(5, LOW);
    delay(250);
    }
}
```
### Spaceship Interface Narrative

<a href="http://www.youtube.com/watch?feature=player_embedded&v=_uJQshS_Upg
" target="_blank"><img src="http://img.youtube.com/vi/_uJQshS_Upg/0.jpg" 
alt="Aruino - Spaceship Interface Narrative" width="240" height="180" border="10" /></a>
