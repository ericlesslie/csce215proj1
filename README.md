# CSCE 215 Project 1

Hey! This is the github repo I made to store the files for the project we're doing that's due Thursday.

## The Problem

![alt text](https://www.electronics-tutorials.ws/wp-content/uploads/2013/10/segment4.gif?fit=277%2C236 "Logo Title Text 1")

## TO DO

1. Finish Truth Table - Done
2. Overall Structure - WIP
3. Better Communication - WIP - Texts? Email? No other commits?
4. K-Maps - Done

### Truth Table

Finished:

| num | w | x | y | z | | a | b | c | d | e | f | g |
|:-:|:-:|:-:|:-:|:-:| |:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| 0 | 0 | 0 | 0 | 0 | | 1 | 1 | 1 | 1 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 | 1 | | 0 | 1 | 1 | 0 | 0 | 0 | 0 |
| 2 | 0 | 0 | 1 | 0 | | 1 | 1 | 0 | 1 | 1 | 0 | 1 |
| 3 | 0 | 0 | 1 | 1 | | 1 | 1 | 1 | 1 | 0 | 0 | 1 |
| 4 | 0 | 1 | 0 | 0 | | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
| 5 | 0 | 1 | 0 | 1 | | 1 | 0 | 1 | 1 | 0 | 1 | 1 |
| 6 | 0 | 1 | 1 | 0 | | 1 | 0 | 1 | 1 | 1 | 1 | 1 |
| 7 | 0 | 1 | 1 | 1 | | 1 | 1 | 1 | 0 | 0 | 0 | 0 |
| 8 | 1 | 0 | 0 | 0 | | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| 9 | 1 | 0 | 0 | 1 | | 1 | 1 | 1 | 1 | 0 | 1 | 1 |

### Minterm Expressions

Finished, and they are:

Edit: Added SoP version for "clarity"

| pin | minterm expression simplified | sop minterm expressions |
| :-: | :--------------------------------------: | :------------: |
| a |  m0 + m2 + m3 + m5 + m6 + m7 + m8 + m9 | w'x'y'z' + w'x'yz' + w'x'yz + w'xy'z + w'xyz' + w'xyz + wx'y'z' + wx'y'z |
| b | m0 + m1 + m2 + m3 + m4 + m7 + m8 + m9 | w'x'y'z' + w'x'y'z + w'x'yz' + w'x'yz + w'xy'z' + w'xyz + wx'y'z' + wx'y'z |
| c | m0 + m1 + m3 + m4 + m5 + m6 + m7 + m8 + m9 | w'x'y'z' + w'x'y'z + w'x'yz + w'xy'z' + w'xy'z + w'xyz' + w'xyz + wx'y'z' + wx'y'z |
| d | m0 + m2 + m3 + m5 + m6 + m8 + m9 | w'x'y'z' + w'x'yz' + w'x'yz  + w'xy'z + w'xyz' + wx'y'z' + wx'y'z |
| e | m0 + m2 + m6 + m8 | w'x'y'z' + w'x'yz' + w'xyz' + wx'y'z' |
| f | m0 + m4 + m5 + m6 + m8 + m9 | w'x'y'z' + w'xy'z' + w'xy'z + w'xyz' + wx'y'z' + wx'y'z |
| g | m2 + m3 + m4 + m5 + m6 + m8 + m9 | w'x'yz' + w'x'yz + w'xy'z' + w'xy'z + w'xyz' + wx'y'z' + wx'y'z |


### K-Maps from Minterms

Finished

Decided to do k-maps considering the long minterms are headache inducing

#### General M 4-Var K-Map

|wx\yz| 00 | 01 | 11 | 10 |
|:--:|:--:|:--:|:--:|:--:|
| 00 | m0 | m1 | m3 | m2 |
| 01 | m4 | m5 | m7 | m6 |
| 11 | m12 | m13 | m15 | m14 |
| 10 | m8 | m9 | m11| m10 |

Since we aren't using m10-m15 consider those Don't Cares for the standard problem

#### Map for A

|wx\yz| 00 | 01 | 11 | 10 |
|:--:|:--:|:--:|:--:|:--:|
| 00 | 1  |    | 1  | 1  |
| 01 |    | 1  | 1  | 1  |
| 11 | X  | X  | X  | X  |
| 10 | 1  | 1  | X  | X  |

Simplified: y + w ++ w'xz + w'x'y'z' 

#### Map for B

|wx\yz| 00 | 01 | 11 | 10 |
|:--:|:--:|:--:|:--:|:--:|
| 00 | 1  | 1  | 1  | 1  |
| 01 | 1  |    | 1  |    |
| 11 | X  | X  | X  | X  |
| 10 | 1  | 1  | X  | X  |

Simplified: w + w'x' + y'z' + yz

#### Map for C

|wx\yz| 00 | 01 | 11 | 10 |
|:--:|:--:|:--:|:--:|:--:|
| 00 | 1  | 1  | 1  |    |
| 01 | 1  | 1  | 1  | 1  |
| 11 | X  | X  | X  | X  |
| 10 | 1  | 1  | X  | X  |

Simplified: w + y' + yz + w'x

#### Map for D

|wx\yz| 00 | 01 | 11 | 10 |
|:--:|:--:|:--:|:--:|:--:|
| 00 | 1  |    | 1  | 1  |
| 01 |    | 1  |    | 1  |
| 11 | X  | X  | X  | X  |
| 10 | 1  | 1  | X  | X  |

Simplified: w + yz' + w'x'y + y'z + w'x'y'z'

#### Map for E

|wx\yz| 00 | 01 | 11 | 10 |
|:--:|:--:|:--:|:--:|:--:|
| 00 | 1  |    |    | 1  |
| 01 |    |    |    | 1  |
| 11 | X  | X  | X  | X  |
| 10 | 1  |    | X  | X  |

Simplified: yz' + wy'z' + w'x'y'z'

#### Map for F

|wx\yz| 00 | 01 | 11 | 10 |
|:--:|:--:|:--:|:--:|:--:|
| 00 | 1  |    |    |    |
| 01 | 1  | 1  |    | 1  |
| 11 | X  | X  | X  | X  |
| 10 | 1  | 1  | X  | X  |

Simplified: w + y'z' + w'xy' + xyz'

#### Map for G

|wx\yz| 00 | 01 | 11 | 10 |
|:--:|:--:|:--:|:--:|:--:|
| 00 |    |    | 1  | 1  |
| 01 | 1  | 1  |    | 1  |
| 11 | X  | X  | X  | X  |
| 10 | 1  | 1  | X  | X  |

Simplified: w + yz' + w'x'y + w'xy'

## Simplified SOP Expressions for Outputs

| pin | sop simplified |
| :-: | :------------: |
| a | y + w + w'xz + w'x'y'z'|
| b | w + y' + yz + w'x |
| c | w + y' + yz + w'x |
| d | w + yz' + w'x'y + y'z + w'x'y'z' |
| e | yz' + wy'z' + w'x'y'z' |
| f | w + y'z' + w'xy' + xyz' |
| g | w + yz' + w'x'y + w'xy' |
