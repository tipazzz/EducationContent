### @explicitHints 1

# Lesson 1: Code a Road Network

## Step 1
Переименуйте текст **run** в блоке ``||Player:on chat command||`` на  **дорога**. Выберите блок ``||Blocks:fill with||`` и вставьте его внутрь вашего блока ``||Player:on chat command||``.

### ~ tutorialhint
``` blocks
player.onChat("road_1", function () {
    blocks.fill(
    GRASS,

    pos(0, 0, 0),
    pos(0, 0, 0),
    FillOperation.Replace
    )
})
```

## Step 2
Используйте всплывающее меню, чтобы заменить **Траву** to **Серый бетон**.
### ~ tutorialhint

``` blocks
player.onChat("road_1", function () {
    blocks.fill(
    GRAY_CONCRETE,
    pos(0, 0, 0),
    pos(0, 0, 0),
    FillOperation.Replace
    )
})
```

## Step 3
Now open ``||Positions:POSITIONS||`` toolbox drawer and drag the world ``||Positions:[0] [0] [0]||`` code block onto your coding Workspace.
Drag the world ``||Positions:[0] [0] [0]||`` block and replace the ``||Positions:relative||`` positions block inside the ``||Blocks:fill||`` block.

### ~ tutorialhint
``` blocks
player.onChat("road_1", function () {
    blocks.fill(
    GRAY_CONCRETE,
    world(0, 0, 0),
    pos(0, 0, 0),
    FillOperation.Replace
    )
})
```

## Step 4
Drag another ``||Positions:world [0] [0] [0]||`` positions code block from the ``||Positions:POSITIONS||`` drawer and replace the second ``||Positions:relative||`` positions block inside the ``||Blocks:fill with||`` block.

### ~ tutorialhint
``` blocks
player.onChat("road_1", function () {
    blocks.fill(
    GRAY_CONCRETE,
    world(0, 0, 0),
    world(0, 0, 0),
    FillOperation.Replace
    )
})
```

## Step 5
We are almost ready to test our code, however there is one more important thing we have to do to make this code work properly. Change the center, or **Y** coordinate, to one number lower. In this example, this will be **68**. Now test your code. If you have coded correctly, you should see a road appear in place of the Grass.

### ~ tutorialhint
``` blocks
player.onChat("road_1", function () {
    blocks.fill(
    GRAY_CONCRETE,
    world(-21, 68, -565),
    world(61, 68, -569),
    FillOperation.Replace
    )
})

```

## Step 6
Repeat the steps for the second road.

### ~ tutorialhint
``` blocks
player.onChat("road_2", function () {
    blocks.fill(
    GRAY_CONCRETE,
    world(-21, 68, -532),
    world(61, 68, -536),
    FillOperation.Replace
    )
})
```

## Step 7
(Extension) With two roads done, build more using the code you have just created. When you are finished, go to the Unit 2 Lesson 1 NPC and ask for some carpet to make road markings with using your agent to place them.
