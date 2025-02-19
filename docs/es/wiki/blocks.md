# Important Blocks
##### **This page is a work in progress. It is incomplete and will have many changes in the future.**

This page will provide a brief overview of the useful blocks in the Mod. Note that this page is not a complete list of all the blocks in the Mod, but rather a list of the most useful ones; for example, normal blocks like `Namek Grass Block`, `Rocky Stone`, etc, are not included in this page.

### **1. Dragon Ball Blocks**
These blocks are used to summon Shenron or Porunga, they can be found in the Overworld and Namek, respectively.  
There are 7 Dragon Balls per world, and they are scattered around the world.  
The first time you enter the world, the Dragon Balls will be generated this way:
- 1-3 Star Dragon Balls: Between XZ: -3000 and 3000 from the spawn point
- 4 Star Dragon Ball: In Goku's House and Elder Guru's House
- 5-7 Star Dragon Balls: Between XZ: -3000 and 3000 from the spawn point

In order to summon Shenron or Porunga, you need to gather all 7 Dragon Balls and place them in a 3x3 square on the ground. Doesn't matter the order or position of the Dragon Balls, as long as they are in a 3x3 square. Here are some valid examples of how to place the Dragon Balls:
```
1 2 3  | 7 2 4  | 1 2 3 | 4   5
4 5 6  | 3 5 1  | 4 5 6 | 1 3 7
  7    | 6      |     7 | 2   6
```
The numbers represent the Dragon Balls, and the spaces represent the ground.  
As said before, doesn't matter the order or position of the Dragon Balls, as long as they are in a 3x3 square!

Once you placed the Dragon Balls, ++rbutton++ (right-click) any Dragon Ball to summon Shenron or Porunga. The Dragon Balls will be consumed in the process, and you will be able to make a wish to the Dragon. Once your wish is made, the Dragon will disappear and the Dragon Balls will be scattered around the world again!  
This time, the Dragon Balls will be generated this way:
- 1-7 Star Dragon Balls: Between XZ: -3000 and 3000 from the exact position where the Dragon disappeared.

If you're playing on a server, the Dragon Balls will left a message in the console with the exact position where they generated.

### **2. Time Chamber Portal Block**
This block is used to enter the Time Chamber, it can be found in the Kami's Lookout.  
It doesn't have crafting recipe and you can not obtain it in any way (except for Creative Mode or `/give` command).

To enter the Hyperbolic Time Chamber, you just have to ++rbutton++ (right-click) the Portal Block. Then, if you want to leave the Time Chamber, you just have to ++rbutton++ (right-click) the Portal Block again, and you will be teleported back to the Kami's Lookout.

**Note for Server Owners:** The Time Chamber Portal Block is linked to the Kami's Lookout coordinates, so if you want to make the Time Chamber Portal Block teleport back to a different location, you will have to modify the `src/main/java/com/yuseix/dragonminez/init/blocks/custom/TimeChamberPortalBlock.java` file by decompling the Mod and recompiling it.

### **3. Dr. Kikono's Armor Station**
This block is used to craft Mod's armors, it can be crafted with an exclusive Namek Material called `Kikono`.
It is very simple, you put the materials, the pattern and the iron amor piece in the Armor Station, and you have to wait a few seconds for the armor to be crafted.  
Similar to a furnace!

To view more information about the Mod's armors, check the [Armors](armors.md) page.