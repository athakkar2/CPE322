# Lab 1 Documentation

## Installing GHDL and GTKWave

Since I am running MSYS2 with MinGW on my machine, I installed GHDL using the MSYS2 native package, which can be found [here](https://packages.msys2.org/package/mingw-w64-x86_64-ghdl).

There was an error downloading GTKWave using its corresponding MSYS2 package, so I downloaded the binaries [here](https://sourceforge.net/projects/gtkwave/files/) and added the bin folder to my path so MSYS2 would recognize it.

## Half Adder

![GTKWave Ouput for Half Adder](halfadder.png)

First I used some GHDL commands before using GTKWave to give a graphical representation of the Half Adder:

```bash
ghdl -a ha.vhdl
ghdl -a ha_tb.vhdl
ghdl -e ha_tb
ghdl -r ha_tb --vcd=ha.vcd
```

 Then I used the following command to open GTKWave and display the Half Adder file graphically:

 ```bash
 gtkwave ha.vcd
 ```

## Full Adder

![GTKWave Output for Full Adder](fulladder.png)

First I used some GHDL commands before using GTKWave to give a graphical representation of the Full Adder:

```bash
ghdl -a adder.vhdl
ghdl -a adder_tb.vhdl
ghdl -e adder_tb
ghdl -r adder_tb --vcd=adder.vcd
```

 Then I used the following command to open GTKWave and display the Full Adder file graphically:

 ```bash
 gtkwave adder.vcd
 ```

## D Flip-Flop

![GTKWave Output for D Flip-Flop](dflipflop.png)

First I used some GHDL commands before using GTKWave to give a graphical representation of the Full Adder:

```bash
ghdl -a dff.vhdl
ghdl -a dff_tb.vhdl
ghdl -e dff_tb
ghdl -r dff_tb --vcd=dff.vcd
```

 Then I used the following command to open GTKWave and display the D Flip-Flop file graphically:

 ```bash
 gtkwave dff.vcd
 ```
