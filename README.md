# 42-ctf

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
