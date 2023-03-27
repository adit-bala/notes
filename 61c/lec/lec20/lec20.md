# RISC V Datapath 2

![review](img/review.png)

## Implementing Loads

![lw](img/lw.png)

## Saving Memory Read to RegFile

![image_2023-03-03-10-14-09](img/image_2023-03-03-10-14-09.png)

![image_2023-03-03-10-14-34](img/image_2023-03-03-10-14-34.png)
- light up with clock cycle, load in `load` instruction
- load bits into the right registers/places

![load_diff_widths](img/load_diff_widths.png)

## Implementing stores
![sw](img/sw.png)

- writeback goes to sleep, since we are writing to registers and not to memory
- how do we tell system to go to sleep

![updated_blocks](img/updated_blocks.png)

## B-Format

![b-format](img/b-format.png)

![branches_compute](img/branches_compute.png)

![bcb](img/bcb.png)
