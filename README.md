# CERES-16
a shitty fantasy console written in rust using a proprietary MIPS based asm instruction set. a lot of inspiration from PICO-8. ceres is structured of these crates: 

- ceres-sys: the core system structure of ceres-16

### Graphics

ceres uses a 256x144 screen with a separate video buffer from the standard memory. colors are 16-bit structured like `0b0000_rrrr_gggg_bbbb` where the first four bits are ignored. the video buffer is structured row major where each u16 is an individual pixel

### Register layout and info

all registers are unsigned 16 bit

| Register number | Register name | Register usage       |
| --------------- | ------------- | -------------------- |
| 0               | z0            | always contains zero |
| 1               | gp            | global pointer       |
| 2               | gp            | stack pointer        |
| 3               | ra            | return address       |
| 4-6             | a0-a2         | argument registers   |
| 7               | v0            | return register      |
| 8               | v1            | return register 2    |
| 9-15            | t0-t6         | temporary registers  |

### Memory map and info

god oh fuck what am i even doing