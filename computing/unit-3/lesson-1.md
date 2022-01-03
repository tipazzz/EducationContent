### @explicitHints 1

# Lesson 1: Code a Park Fence

## Step 1
Rename the **run** element of the ``||Player:on chat command||`` block to **park_fence**. 

Drag and drop the ``||Agent:agent set active slot||`` code block to the coding Workspace and add it to your  ``||Player:on chat command||`` code block.

Drag and drop the ``||Agent:agent move [forward]||`` code block to the coding Workspace and add it to your ``||Player:on chat command||`` code block, setting it to up.

#### ~ tutorialhint
``` blocks
player.onChat("park_fence", function () {
    agent.setSlot(1)
    agent.move(UP, 1)
})
```
## Step 2
Drag the ``||Loops:repeat [4] times||`` into your ``||Player:on chat command||`` set and change it to **2**. 

#### ~ tutorialhint
``` blocks
player.onChat("park_fence", function () {
    agent.setSlot(1)
    agent.move(UP, 1)
    for (let index = 0; index < 2; index++) {
    	
    }
})
```

## Step 3
Drag the ``||Agent:agent move [forward]||`` code block to the coding Workspace, add it to your ``||Player:on chat command||`` code block, inside the ``||Loops:repeat [4] times||`` loop, then set it to our first number, **25**(from **Step 5**). 

Drag the ``||Agent:agent place [forward]||`` code block to the coding Workspace, add it to your ``||Player:on chat command||`` code block, inside the ``||Loops:repeats [2] times||`` loop, under the ``||Agent.agent move[forward]||`` code block, then set it to **down**.

#### ~ tutorialhint
``` blocks
player.onChat("park_fence", function () {
    agent.setSlot(1)
    agent.move(UP, 1)
    for (let index = 0; index < 2; index++) {
        agent.move(FORWARD, 25)
        agent.place(DOWN)
    }
})
```

## Step 4
Drag the ``||Agent:agent turn [left]||`` code block to your ``||PLayer:on chat command||`` code block, inside the ``||Loops:repeat [2] times||`` and set it to the direction your Agent needs to turn. In our example, this is **left**. 

#### ~ tutorialhint
``` blocks
player.onChat("park_fence", function () {
    agent.setSlot(1)
    agent.move(UP, 1)
    for (let index = 0; index < 2; index++) {
        agent.move(FORWARD, 25)
        agent.place(DOWN)
        agent.turn(LEFT_TURN)
    }
})
```

## Step 5
Drag the ``||Agent:agent move [forward]||`` code block to your ``||Player:on chat command||`` code block, then set it to our second number, **23** (from **Step 6**). 

Drag the ``||Agent:agent place[forward]||`` code block in your ``||Player:on chat command||`` code block, then set it to **down**.

#### ~ tutorialhint
``` blocks
player.onChat("park_fence", function () {
    agent.setSlot(1)
    agent.move(UP, 1)
    for (let index = 0; index < 2; index++) {
        agent.move(FORWARD, 25)
        agent.place(DOWN)
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 23)
        agent.place(DOWN)
    }
})
```

## Step 6
Drag one more ``||Agent:agent turn [left]||`` code block to your ``||Player:on chat command||`` code block inside the **loop** and leave it set to **left**.

#### ~ tutorialhint
``` blocks
player.onChat("park_fence", function () {
    agent.setSlot(1)
    agent.move(UP, 1)
    for (let index = 0; index < 2; index++) {
        agent.move(FORWARD, 25)
        agent.place(DOWN)
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 23)
        agent.place(DOWN)
        agent.turn(LEFT_TURN)
    }
})
```

## Step 7
Test your code. Place your Agent on the starting block and run your code by pressing **T** to open the chat box and type **park_fence**. 
