# Lab 3 Documentation

## Python Syntax

I reviewed the Python documentation in Professor Lu's GitHub to refresh myself with Python's syntax, and wanted to share a concept I had to learn for CS 556 which might be helpful to include in the documentation. This concept is called masking, which allows indexing based off of a conditional statement. For example, to iterate through a matrix and change all the 0's to 1's, in C++ you must do:

```C++
for(int i = 0; i < rows; i++){
  for(int j = 0; j < columns; j++){
    if(foo[i][j] == 0){
      foo[i][j] == 1;
    }
  }
}
```

It is much easier to do in Python, where all you have to do is:

```Python
foo[foo == 0] = 1
```

Masking turns 6 lines of code into one!

## Python Examples

I typed in the following commands into my terminal for this lab's demo. This was done using Python 3.10.

```bash
cd ~/iot
cd *3
python julian.py
python date_example.py
python datetime_example.py
python time_example.py
python sun.py 'New York'
python moon.py
python coordinates.py 'SC Williams Library'
python address.py '40.74480675, -74.02532862031404'
python cpu.py
python battery.py
python documentstats.py document.txt
```

To view a full logdump of my terminal while running these commands, please see the [lab3.txt](lab3.txt) file. This was dumped using the script command in my terminal.
