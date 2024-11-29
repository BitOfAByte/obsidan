---
tags:
  - Notes
links: 
creation date: 2024-11-27 19:13
modification date: Wednesday 27th November 2024 19:13:53
semester: 3
year: 2024
---


---
# [[Math Lecture 5 Notes]]

---



# Grænseværdier

- Lad os forestille, at vi skal finde Grænseværdien af følgende funktion:

$$\lim_{x\rightarrow2} \frac{x^2-4}{x-2}$$

Vi vil forsøge, at indsætte tallet: 2,1 ved $f(2.1)$

$$f(2.1)=\frac{2.1^2-4}{2.1-2}=\frac{0.41}{0.1}=4.1$$


Hvorimod ved f(2.01) har vi følgende:

$$f(2.01)=\frac{2.01^2-4}{2.01-2}=4.01$$


**OBS**: Vi kan se, at jo tættere vores x-værdi inde i funktionen nærmere sig ved 2, desto mere præcis har vi en y-værdi som er ved tallet 4. Men i fleste tilfælde er situationen ikke såden, men anderledes!


## Eksempler på Grænseværdier

Vi har følgende funktion, som vi skal udregne:

$$\lim_{x\rightarrow 2}\frac{x^{2}-4}{x-2}=4$$

- STEP 1: Samme værdier fjernes på nævneren og tælleren i brøken.

$$\lim_{x\rightarrow 2}\frac{(x+2)\cdot (\cancel{x-2)}}{\cancel{(x-2)}}=\lim_{x\rightarrow 2}(x+2)=2+2=4$$

---

Vi kan se, at vi har følgende funktion:

$$\lim_{x\rightarrow 5}x^2+2x-4$$

STEP 1: X-værdien indsættes inde på funktionens x-værdier.


$$x=5$$

$$5^2+2\cdot5-4\leftrightarrow25+10-4\leftrightarrow35-4=31$$

---



Vi har følgende funktion, som vi skal udregne:

$$\lim_{x\rightarrow 3}\frac{x^3-27}{x-3}$$

- STEP 1: Vi ved på forhånd, at vi har en kubik $x^3$ derfor bruges formlen: 

$$A^3-B^3=(A\cdot B)\cdot(A^{2}+A\cdot B+B^{2})$$

$$x^3=3^2+3\cdot3+9=9\cdot3=27$$



---


## Eksempler på Uendeligheder


- at finde Grænse af Uendeligheden og dets løsninger:
	- Her er der tilføjet nogle eksempler på, hvordan Uendeligheder er med en Konstant.
	- **BEMÆRK**: At når vi har en værdi som går mod uendelig fra det ene side eller det andet, så ender resultatet med at være uendeligt med en plus eller minus fortegn foran, afgørende om hvilken retning vi går mod.


$$\lim_{x\rightarrow \infty}(x^2)=+\infty$$

$$\lim_{x\rightarrow -\infty}(x^2)=(-\infty)^2=+\infty$$


$$\lim_{x\rightarrow \infty}(x^3)=(\infty)^3=+\infty$$


$$\lim_{x\rightarrow -\infty}(x^3)=(-\infty)^3=-\infty$$


## Mean Value Teorien


- Når vi snakker om Mean Value teorien, forsøger vi at finde den midterste punkt mellem to dele.
- Her kommer vi til at vise steps til hvordan man løser opgaven med Mean Value teorien.


- STEP 1: Opskriv funktionen

$$f(x)=x^2-4x+1$$

og $$[1,5]$$


- STEP 2: Differentiere funktionen:


$$f'(x)=2x-4$$



- STEP 3: Indsæt Interval værdierne inde i stamfunktionen.


$$f(5)=5^2-4\cdot5+1=25-20+1=6$$

$$f(1)=1^2-4+1=-3+1=-2$$


STEP 4: Sæt værdierne ind i formlen.