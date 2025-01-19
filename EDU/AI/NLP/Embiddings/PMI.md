Tags: #
____
# PMI formula 


$PMI(w_1,w_2) = log\frac{P(w_1,w_2)}{P(w_1)P(w_2)}$

$P(w) = \frac{Freq(w)}{totalWordCount}$

#### Example
0. We have a string
    "this is a foo bar bar black sheep  foo bar bar black sheep foo bar bar black sheep shep bar bar black sentence"
1. **Convert it to tokens**
```python
[1] "this"  "is"    "a"     "foo"   "bar"   "bar"   "black" "sheep"
[9] "foo"   "bar"   "bar"   "black"
```
   2.  **Count of Words**
      this is a foo bar black sheep shep sentence 
      1 1 1 3 8 4 3 1 1
  3. **Create Co-occurence matrix**
```
|features | this| is | a  | foo | bar | black | sheep | shep |sentence |
|---------|-----|----|----|-----|-----|-------|-------|------|---------|
| this    | 0   | 1  | 0  | 0   | 0   | 0     | 0     | 0    | 0       |
| is      | 0   | 0  | 1  | 0   | 0   | 0     | 0     | 0    | 0       |
| a       | 0   | 0  | 0  | 1   | 0   | 0     | 0     | 0    | 0       |
| foo     | 0   | 0  | 0  | 0   | 3   | 0     | 0     | 0    | 0       |
| bar     | 0   | 0  | 0  | 0   | 4   | 4     | 0     | 0    | 0       |
| black   | 0   | 0  | 0  | 0   | 0   | 0     | 3     | 0    | 1       |
| sheep   | 0   | 0  | 0  | 2   | 0   | 0     | 0     | 1    | 0       |
| shep    | 0   | 0  | 0  | 0   | 1   | 0     | 0     | 0    | 0       |
| sentence| 0   | 0  | 0  | 0   | 0   | 0     | 0     | 0    | 0       |
```
4. **Compute PMI score**
$$ PMI(foo, bar) = log_2(\frac{\frac{3}{23}}{\frac{3}{23}*\frac{8}{23}}) $$
```
(('is', 'a'), 4.523561956057013)
(('this', 'is'), 4.523561956057013)
(('a', 'foo'), 2.938599455335857)
(('sheep', 'shep'), 2.938599455335857)
(('black', 'sheep'), 2.5235619560570135)
(('black', 'sentence'), 2.523561956057013)
(('sheep', 'foo'), 2.3536369546147005)
(('bar', 'black'), 1.523561956057013)
**(('foo', 'bar'), 1.523561956057013)**
(('shep', 'bar'), 1.523561956057013)
(('bar', 'bar'), 0.5235619560570131)
```
____
### Zero-Links

____
### Links