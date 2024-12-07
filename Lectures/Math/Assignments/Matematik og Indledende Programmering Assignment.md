---
creation date: 2024-12-07 13:41
modification date: Saturday 7th December 2024 13:41:27
tags:
  - Assignments
year: 2024
semester: 3
links: "[[Matematik og Indledende Programmering 2 maj 2024]]"
---

---
# [[Matematik og Indledende Programmering Assignment]]


# Opgave 1 (15 point)

## a) Beregn værdien af udtrykket herunder:

$$\begin{bmatrix}7&1&-2\\4&4&-2\\-8&7&7\end{bmatrix}\cdot\begin{bmatrix}2\\2\\-1\end{bmatrix}$$ 

$$7\cdot2+1\cdot2-2\cdot(-1)=18$$
$$4\cdot2+4\cdot2-2\cdot(-1)=18$$
$$-8\cdot2+7\cdot2+7\cdot(-1)=-9$$

$$\begin{bmatrix}7&1&-2\\4&4&-2\\-8&7&7\end{bmatrix}\cdot\begin{bmatrix}2\\2\\-1\end{bmatrix}=\begin{bmatrix}18\\18\\-9\end{bmatrix}$$


##  b) Bestem determinanten af følgende matrice

$$A=\begin{bmatrix}6&2&1\\4&-2&2\\0&4&-4\end{bmatrix}$$


For at beregne determinanten af en 3×33 \times 33×3-matrix, bruger man **udvikling efter første række**. Formlen for determinanten ser sådan ud:
Hvis $A$ er en $3\times3$ matrix:

$$\begin{bmatrix}a&b&c\\d&e&f\\g&h&i\end{bmatrix}$$

så beregnes determinanten $\det(A)$ som:

$$det(A)=a(ei−fh)−b(di−fg)+c(dh−eg)$$

### Trinvis metode

1. **Udvikling efter første række**: Tag elementerne fra første række $(a,b,c)$, og beregn hver determinanteffekt ved at fjerne den række og søjle, hvor elementet sidder, og tage determinanten af den tilbageværende $2\times2$ matrix.
    
2. **Bestem $2\times2$ determinanter**: For hver 2×22 \times 22×2-matrix, brug formlen:

$$det(\begin{bmatrix}x&y\\z&w\end{bmatrix})=x\cdot w - y \cdot z$$




Udvikling efter første række:

$$A=\begin{bmatrix}6&2&1\\4&-2&2\\0&4&-4\end{bmatrix}$$


$$det(A)=a(ei−fh)−b(di−fg)+c(dh−eg)$$



$$det(A)=6\begin{bmatrix}-2&2\\4&-4\end{bmatrix}-2\begin{bmatrix}4&2\\0&-4\end{bmatrix}+1\begin{bmatrix}4&-2\\0&4\end{bmatrix}$$


### Beregning af $2\times2$ determinanter

- $\begin{bmatrix}-2&2\\4&-4\end{bmatrix}=$ $-2\cdot(-4)-2\cdot4\leftrightarrow 8-8=0$
- $\begin{bmatrix}4&2\\0&-4\end{bmatrix}=$ $4\cdot(-4)-2\cdot0\leftrightarrow -16-0=-16$
- $\begin{bmatrix}4&-2\\0&4\end{bmatrix}=$$4\cdot4-2\cdot0\leftrightarrow 16-0=16$


$$det(A)=6\cdot0-2\cdot(-16)+1\cdot16\leftrightarrow32+16=48$$


$$det(A)=48$$





## c) Anvend Gauss elimination til at løse ligningssystemet:


$$6x+2y+z=22$$

$$4x-2y+2z=14$$
$$0x+4y-4z=-4$$

$$\left[\begin{array}{rrr|r}6&2&1&22\\4&-2&2&14\\0&4&-4&-4\end{array}\right]$$

### Step 1: $\frac{R_1}{6}\rightarrow R_1$


$$\left[\begin{array}{rrr|r}1&\frac{2}{6}&\frac{1}{6}&\frac{22}{6}\\4&-2&2&14\\0&4&-4&-4\end{array}\right]$$


da $\frac{2}{6}$ og $\frac{22}{6}$ kan divideres med 2 kan vi forkorte brøkerne:




$$\left[\begin{array}{rrr|r}1&\frac{1}{3}&\frac{1}{6}&\frac{11}{3}\\4&-2&2&14\\0&4&-4&-4\end{array}\right]$$


### Step 2: $R_2-4\cdot R_1$


$$R_{2,1}=4-4\cdot1\leftrightarrow4-4=0$$
$$R_{2,2}=-2-4\cdot\frac{1}{3}$$


#### Trin 1 $R_{2,2}$: Beregn multiplikationen
$$=-\frac{4\cdot1}{3}\leftrightarrow-\frac{4}{3}$$

#### Trin 2 $R_{2,2}$: Indsæt resultatet i udtrykket

$$=-2-\frac{4}{3}$$
#### Trin 3 $R_{2,2}$: Omskriv til fælles nævner
Omskriv $-2$ som en brøk med nævner 3

$$-2=\frac{-6}{3}$$

alså:

$$-2=\frac{-6}{3}-\frac{4}{3}$$


#### Trin 4 $R_{2,2}$: Udfør subtraktionen

$$R_{2,2}=\frac{-6}{3}-\frac{4}{3}\leftrightarrow\frac{-6-4}{3}=\frac{-10}{3}$$




$$R_{2,3}=2-4\cdot\frac{1}{6}$$

#### Trin 1 $R_{2,3}$: Beregn multiplikationen

$$-4\cdot\frac{1}{6}=\frac{-4\cdot1}{6}=-\frac{4}{6}$$


Vi kan forekle brøkerne ved at dividere med 2, så for vi:

$$\frac{4}{6}=\frac{2}{3}$$


#### Trin 2 $R_{2,3}$: Indsæt resultatet i udtrykket

$$R_{2,3}=2-\frac{2}{3}$$

#### Trin 3 $R_{2,3}$: Omskriv til fælles nævner

Omskriv 2 som en brøk med nævner 3 $$\frac{6}{3}$$
alså:

$$\frac{6}{3}-\frac{2}{3}$$



#### Trin 4 $R_{2,3}$: Udfør subtraktionen

$$R_{2,3}=\frac{6}{3}-\frac{2}{3}\leftrightarrow\frac{6-2}{3}=\frac{4}{3}$$





























#### $R_{2,4}$
$$R_{2,4}=14-4\cdot \frac{11}{3}\leftrightarrow14-14.66=-0.66=-\frac{2}{3}$$



$$\left[\begin{array}{rrr|r}1&\frac{1}{3}&\frac{1}{6}&\frac{11}{3}\\0&\frac{-10}{3}&\frac{4}{3}&-\frac{2}{3}\\0&4&-4&-4\end{array}\right]$$






### Step 3: $\frac{R_2}{-\frac{10}{3}}\rightarrow R_2$




$$R_{2,3}=​\frac{4}{3}÷\frac{-10}{3}$$

Brug $KCF$ som betyder:

- K: Keep
- C: Change
- F: Flip




$$R_{2,3}=\frac{4}{3}÷\frac{-10}{3}\leftrightarrow\frac{4}{3}\cdot\frac{3}{-10}=\frac{4\cdot3}{3\cdot(-10)}=\frac{12}{-30}$$


brøken kan forkortes da $12$ og $30$ begge kan dividres med 6


$$R_{2,3}=\frac{12}{-30}=-\frac{2}{5}=-0.4$$




$$R_{2,4}=-\frac{2}{3}÷\frac{-10}{3}$$


Bruger KCF igen:

- K: Keep
- C: Change
- F: Flip


$$R_{2,4}=-\frac{2}{3}\cdot(-\frac{3}{10})\leftrightarrow\frac{2\cdot3}{3\cdot10}=\frac{6}{30}$$


Kan forkortes da $6$ og $30$ kan dividres med $3$


$$\frac{6}{30}=\frac{2}{10}=0.2$$



$$
\left[\begin{array}{rrr|r}1&\frac{1}{3}&\frac{1}{6}&\frac{11}{3}\\0&1&-0.4&0.2\\0&4&-4&-4\end{array}\right]$$



### Step 4: $R_{3}-4\cdot R_{2}\rightarrow R_3$


$$0-4\cdot0\leftrightarrow0-0=0$$
$$4-4\cdot1\leftrightarrow4-4=0$$
$$-4-4\cdot(-0.4)\leftrightarrow-4-1.6=-2.4$$

$$-4-4\cdot0.2\leftrightarrow-4-0.8=-4.8$$



$$
\left[\begin{array}{rrr|r}1&\frac{1}{3}&\frac{1}{6}&\frac{11}{3}\\0&1&-0.4&0.2\\0&0&-2.4&-4.8\end{array}\right]$$








### Step 5: $R_{1}-\frac{1}{3}\cdot R_{2}\rightarrow R_1$


 $$1-\frac{1}{3}\cdot0\leftrightarrow1-0=1$$



$$\frac{1}{3}-\frac{1}{3}\cdot1\leftrightarrow\frac{1}{3}-\frac{1}{3}=0$$



$$\frac{1}{6}-\frac{1}{3}\cdot(-0.4) = 0.3$$


$$\frac{11}{3}-\frac{1}{3}\cdot0.2=3.6$$

$$
\left[\begin{array}{rrr|r}1&1&0.3&3.6\\0&1&-0.4&0.2\\0&0&-2.4&-4.8\end{array}\right]$$



### Step 6: $\frac{R_3}{-2.4}\rightarrow R_3$


$$R_{2,3}=\frac{-2.4}{-2.4}=1$$


$$R_{2,4}=\frac{-4.8}{-2.4}=2$$


$$
\left[\begin{array}{rrr|r}1&\frac{1}{3}&\frac{1}{6}&\frac{11}{3}\\0&1&-0.4&0.2\\0&0&1&2\end{array}\right]$$
### Step 7: $R_{2}+0.4\cdot R_{3}\rightarrow R_2$



$$-0.4+0.4\cdot1\leftrightarrow-0.4+0.4=0$$

$$0.2+0.4\cdot2\leftrightarrow0.2+0.8=1$$


$$
\left[\begin{array}{rrr|r}1&0&0.3&3.6\\0&1&0&1\\0&0&1&2\end{array}\right]$$






### Step 8: $R_{1}-0.3\cdot R_{3}\rightarrow R_1$


$$0.3-0.3\cdot1\leftrightarrow0.3-0.3=0$$

$$3.6-0.3\cdot2\leftrightarrow3.6-0.6=3$$


$$
\left[\begin{array}{rrr|r}1&0&0&3\\0&1&0&1\\0&0&1&2\end{array}\right]$$






$x=3$
$y=1$
$z=2$

