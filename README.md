<p align="center">
  <img src="https://github.com/jotavare/jotavare/blob/main/42/banner/ctf/ctf_banner.png">
</p>

<p align="center">
	<a href="#about">About</a> •
	<a href="#projects">Projects</a> •
	<a href="#exams">Exams</a> •
	<a href="#license">License</a>
</p>

## ABOUT
This repository is just to write my line of thought while finding the flags.
Use it as a way to know more and not just simply put the answer.

## CTF
<div align="center">
<table>
<tr><th>INTRO</th><th>FORENSIC</th></tr>
<tr><td>

| CTF | POINTS | STATUS |
| :--- | :---: | :---: |
| Ancient Crypto	| 5 | <img src="https://img.shields.io/badge/done-sucess" /> |
| My Little Pwn		| 5 | <img src="https://img.shields.io/badge/done-sucess" /> |
| Client Side		| 5 | <img src="https://img.shields.io/badge/done-sucess" /> |
| It's all here		| 5 | <img src="https://img.shields.io/badge/done-sucess" /> |

</td><td>

| CTF | POINTS | STATUS |
| :--- | :---: | :---: |
| l0st			| 10 | <img src="https://img.shields.io/badge/waiting-red" /> |
| s3cr3t m3ss4g3	| 35 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Ac1dBotn3t		| 70 | <img src="https://img.shields.io/badge/waiting-red" /> |
| APT 38		| 75 | <img src="https://img.shields.io/badge/waiting-red" /> |

</td></tr> </table>
</div>

<div align="center">
<table>
<tr><th>CRYPTO</th><th>WEB</th></tr>
<tr><td>

| CTF | SCORE | STATUS |
| :--- | :---: | :---: |
| We need a pattern		| 5 | <img src="https://img.shields.io/badge/done-sucess" /> |
| Vous n'avez pas les bases	| 5 | <img src="https://img.shields.io/badge/done-sucess" /> |
| Very Short Crypto		| 25 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Triple word			| 70 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Identified author		| 80 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Recycling			| 85 | <img src="https://img.shields.io/badge/waiting-red" /> |
| To be xor not to be		| 85 | <img src="https://img.shields.io/badge/waiting-red" /> |
| The fault in our DES		| 90 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Contact support		| 115 | <img src="https://img.shields.io/badge/waiting-red" /> |

</td><td>

| CTF | SCORE | STATUS |
| :--- | :---: | :---: |
| Gallery			| 5 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Gallery v2			| 5 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Simple Question of Logic 1	| 5 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Silkway Anonymous Market v1	| 20 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Simple Question of Logic 2	| 40 | <img src="https://img.shields.io/badge/waiting-red" /> |
| ft_library			| 60 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Simple Question of Logic 3	| 65 | <img src="https://img.shields.io/badge/waiting-red" /> |
| The Tragic Token Tale		| 75 | <img src="https://img.shields.io/badge/waiting-red" /> |

</td></tr> </table>
</div>

<div align="center">
<table>
<tr><th>MISC</th><th>OSINT</th></tr>
<tr><td>

| CTF | SCORE | STATUS |
| :--- | :---: | :---: |
| Dorkside		| 5 | <img src="https://img.shields.io/badge/done-sucess" /> |
| Force brute		| 20 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Smiley		| 50 | <img src="https://img.shields.io/badge/waiting-red" /> |
| Safe computation	| 135 | <img src="https://img.shields.io/badge/waiting-red" /> |

</td><td>

| CTF | SCORE | STATUS |
| :--- | :---: | :---: |
| Norminet		| 5 | <img src="https://img.shields.io/badge/waiting-red" /> |
| h@ck3r5		| 20 | <img src="https://img.shields.io/badge/waiting-red" /> |
| gamer gf needed	| 65 | <img src="https://img.shields.io/badge/waiting-red" /> |

</td></tr> </table>
</div>

<div align="center">
<table>
<tr><th>PWN</th><th>STEGANO</th></tr>
<tr><td>

| CTF | SCORE | STATUS |
| :--- | :---: | :---: |
| The Answer		| 5	| <img src="https://img.shields.io/badge/done-sucess" /> |
| GOTcha		| 40	| <img src="https://img.shields.io/badge/waiting-red" /> |
| Stack leak		| 45	| <img src="https://img.shields.io/badge/waiting-red" /> |
| Arbitrary leak	| 85	| <img src="https://img.shields.io/badge/waiting-red" /> |
| Too RISCy		| 155	| <img src="https://img.shields.io/badge/waiting-red" /> |

</td><td>

| CTF | SCORE | STATUS |
| :--- | :---: | :---: |
|  Weird_song		| 5	| <img src="https://img.shields.io/badge/waiting-red" /> |
| Point par point	| 5	| <img src="https://img.shields.io/badge/waiting-red" /> |
| Conspiracy Theory	| 75	| <img src="https://img.shields.io/badge/waiting-red" /> |

</td></tr> </table>
</div>










#### Crypto
###### We need a patern (5 points)

```
We've intercepted a text encrypted with an unknown cipher.

We think that it's written in english and that it contains very important information.

Hint
You need to put the flag inside 42CTF{} and to uppercase.
```

I could download a text file caled "cyphertext". Click here to see.
The first thing i do is give permissions to read, write and execute the file. `chmod 777 cyphertext`
Then use tools like to exiftool to check the metadata and also the files proprities to see if theres any hidden info, but no relevant info was found.
Open the text file but couldnt make sense of the text at first so i started using Cyberchef and dcode and tried some encryption formats like base42, base32, rotating many times and some tools that automaticly translate to various formats but no luck.

Started checking the text and every character individually for any relevant patterns or info, and voila, found it.
At the end of the file there was this line `42┼¿¤{®±_╝±¿_╔═║_©±╝±╣╬Ø¥╣█║¿╗┼_═╔█═¿╗¿╔¿╗±╝}`
That must be the flag and even tho we still cant make sense of the content inside of the flag, we know that after 42 therest 3 letters CTF.
With that information i used find and replace in all 3 characters (one by one and not the three at the same time) ┼¿¤ to CTF.
Then some words started making sense, for example the begging of the phrases some were 2 characters lenght begging with a "T", so its probably a "To".

Here are some examples, each find would help me find bigger words:
┼ -> C
¿ -> T
¤ -> F
T± -> TO
T¥║ -> THE
TE§T -> TEST
THE£E -> THERE
█EFORE -> BEFORE
EFF╗C╗E╝T -> EFFICIENT
R╣BBIT-HO╬E -> RABBIT-HOLE

So at this stage we already have decyphered the letters C,T,F,O,H,E,S,R,B,I,N,A and L.
Eventually i decyphered all the letters and the result was:
The first chapter of Alice in the Wonderland.

but there was a importante information in the text
TO PERFORM A EFFICIENT FREQUENCY ANALYSIS, YOU NEED A QUITE LONG TEST.

Frequency analysis is the study of the distribution (and count) of the letters in a text. Analysis of frequencies helps cryptanalysis and decrypting substitution-based ciphers using the fact that some letters apparitions are varying in a given language: in english, letters E, T or A are common while Z or Q are rare.

English
E	12.7 %	M	2.4 %
T	9.1 %	W	2.4 %
A	8.2 %	F	2.2 %
O	7.5 %	G	2.0 %
I	7.0 %	Y	2.0 %
N	6.7 %	P	1.9 %
S	6.3 %	B	1.5 %
H	6.1 %	V	1.0 %
R	6.0 %	K	0.8 %
L	4.0 %	J	0.2 %
D	4.3 %	X	0.2 %
C	2.8 %	Q	0.1 %
U	2.8 %	Z	0.1 %

french
E	17.3 %	P	3.0 %
A	8.4 %	G	1.3 %
S	8.1 %	V	1.3 %
I	7.3 %	B	1.1 %
N	7.1 %	F	1.1 %
T	7.1 %	Q	1.0 %
R	6.6 %	H	0.9 %
L	6.0 %	X	0.4 %
U	5.7 %	J	0.3 %
O	5.3 %	Y	0.3 %
D	4.2 %	K	0.1 %
C	3.0 %	W	0.1 %
M	3.0 %	Z	0.1 %

Frequency analysis is less relevant when the message has been encrypted with polyalphabetic encryption (which tends to randomize the frequency of the letters), or when the encryption is homophonic (several different encrypted characters for the same plain letter) or polygrammic (groups of characters replace each letter). In these cases, the analysis does not allow a decoding but allows to filter or find the type of encryption used.

It may not be usefull now but in the future is sure something i should try first to understand if i can get any info.

Another important info, the text in the flag 42CTF{DO_NOT_USE_MONOALPHABETIC_SUBSTITUTION}

A mono-alphabetic cipher (aka simple substitution cipher) is a substitution cipher where each letter of the plain text is replaced with another letter of the alphabet. It uses a fixed key which consist of the 26 letters of a “shuffled alphabet”.
