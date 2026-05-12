# 10  tools

## Overview

[TASK]: Write a base conversion tool that accepts arguments from argv and outputs something along
                                                                            those lines:
```
1:
    dec:  41
    hex:  0x29
    bin:  0b101001
    oct:  0o51
    asc:  ')'
2:
    dec:  76
    hex:  0x4C
    bin:  0b1001100
    oct:  0o114
    asc:  'L'
3:
    dec:  45
    hex:  0x2D
    bin:  0b101101
    oct:  0o55
    asc:  '-'
4:
    dec:  48
    hex:  0x30
    bin:  0b110000
    oct:  0o60
    asc:  '0'
5:
    dec:  28
    hex:  0x1C
    bin:  0b11100
    oct:  0o34
6:
    dec:  1001
    hex:  0x3E9
    bin:  0b1111101001
    oct:  0o1751
```
`asc` stands for ascii
The ascii text should only appear if the integer is actually printable as a character
The binary shall accept `n` arguments and handle them all

Basic error handling and recovery:
```
1:
[error]: invalid byte/bytes "501" in "0b1010501"
2:
    dec:  76
    hex:  0x4C
    bin:  0b1001100
    oct:  0o114
    asc:  'L'
3:
[error]: invalid byte/bytes "h5" in "4h5"
4:
    dec:  48
    hex:  0x30
    bin:  0b110000
    oct:  0o60
    asc:  '0'
5:
[error]: invalid byte/bytes "b4" in "0o3b4"
```

One last thing - if only one argument is provided it should not print the `index:` part
Such as: 
```
    dec:  100
    hex:  0x64
    bin:  0b1100100
    oct:  0o144
    asc:  'd'
```

Hint: strtoull(3)

