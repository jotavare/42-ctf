# We need a patern

```
We've intercepted a text encrypted with an unknown cipher.

We think that it's written in english and that it contains very important information.

Hint
You need to put the flag inside 42CTF{} and to uppercase.
```

## Introduction
In this CTF challenge, we were given a text file named "cyphertext" which needed to be decrypted to obtain the flag.
</br>This document details the steps taken to decrypt the text file and my line of thought.

## Permissions and File Analysis
The first step was to give read, write, and execute permissions to the file using the command: `chmod 777 cyphertext`.
</br>I then proceeded to analyze the metadata and file properties using tools like `exiftool` but did not find any relevant information.

## Encryption Attempt
Tried openening the text file but couldn't make sense of the text at first, so I started using online tools like [Cyberchef](https://gchq.github.io/CyberChef) and [dCode](https://www.dcode.fr/en) to try various encryption formats like `base64`, `base32`, `rot` and some tools that automatically try various formats, but had no luck.

## Character Analysis
We began checking the text and every character individually for any relevant patterns or info. At the end of the file, we found a line that read `42┼¿¤{®±_╝±¿_╔═║_©±╝±╣╬Ø¥╣█║¿╗┼_═╔█═¿╗¿╔¿╗±╝}`. We suspected it to be the flag and realized that after 42, there were three letters CTF.

Using this information, we used find and replace in all three characters (one by one and not the three at the same time) ┼¿¤ to CTF. Then, we began to decipher the rest of the flag. Some words started making sense, for example, the beginning of the phrases was two characters long, beginning with a "T," so it's probably a "To".

Here are some examples::

| Find  | Replace |
| :--:  | :--:    |
| ┼           | C           |
| ¿           | T           |
| ¤           | F           |
| T±          | TO          |
| T¥║         |	THE         |
| TE§T        | TEST        |
| THE£E       |	THERE       |
| █EFORE      |	BEFORE      |
| EFF╗C╗E╝T   |	EFFICIENT   |
| R╣BBIT-HO╬E |	RABBIT-HOLE |

So at this stage we already have decyphered the letters C,T,F,O,H,E,S,R,B,I,N,A and L.
Eventually i decyphered all the letters and the result was:
The first chapter of Alice in the Wonderland and the flag was `42CTF{DO_NOT_USE_MONOALPHABETIC_SUBSTITUTION}`.

## Frequency Analysis
At the beggining of the already decyphered text there was this quote - "TO PERFORM A EFFICIENT FREQUENCY ANALYSIS, YOU NEED A QUITE LONG TEST".

From [dCode](https://www.dcode.fr/frequency-analysis):

> What is frequency analysis?

> Frequency analysis is the study of the distribution (and count) of the letters in a text. Analysis of frequencies helps cryptanalysis and decrypting substitution-based ciphers using the fact that some letters apparitions are varying in a given language: in english, letters E, T or A are common while Z or Q are rare.

<div>
<table>
<tr><th>ENGLISH</th><th>FRENCH</th></tr>
<tr><td>

| __E -	12.7 %__  | __H -	6.1 %__ | __W -	2.4 %__ | __K -	0.8 %__ |
| ---: | ---: | ---: | ---: |
| __T -	9.1 %__   | __R -	6.0 %__ | __F -	2.2 %__ | __J -	0.2 %__ |
| __A -	8.2 %__   | __L -	4.0 %__ | __G -	2.0 %__ | __X -	0.2 %__ |
| __O -	7.5 %__   | __D -	4.3 %__ | __Y -	2.0 %__ | __Q -	0.1 %__ |
| __I -	7.0 %__   | __C -	2.8 %__ | __P -	1.9 %__ | __Z -	0.1 %__ |
| __N -	6.7 %__   | __U -	2.8 %__ | __B -	1.5 %__ |
| __S -	6.3 %__   | __M -	2.4 %__ | __V -	1.0 %__ |

</td><td>

| __E - 17.3 %__ |  __L -	6.0 %__ | __G - 1.3 %__ | __J - 0.3 %__ |
| ---: | ---: | ---: | ---: |
| __A -	8.4 %__   | __U -	5.7 %__ | __V	- 1.3 %__ | __Y - 0.3 %__ |
| __S -	8.1 %__   | __O -	5.3 %__ | __B	- 1.1 %__ | __K - 0.1 %__ |
| __I -	7.3 %__   | __D -	4.2 %__ | __F	- 1.1 %__ | __W - 0.1 %__ |
| __N -	7.1 %__   | __C -	3.0 %__ | __Q	- 1.0 %__ | __Z - 0.1 %__ |
| __T -	7.1 %__   | __M -	3.0 %__ | __H	- 0.9 %__ |
| __R -	6.6 %__   | __P - 3.0 %__ | __X	- 0.4 %__ |

</td></tr> </table>
</div>

Frequency analysis is less relevant when the message has been encrypted with polyalphabetic encryption (which tends to randomize the frequency of the letters), or when the encryption is homophonic (several different encrypted characters for the same plain letter) or polygrammic (groups of characters replace each letter). In these cases, the analysis does not allow a decoding but allows to filter or find the type of encryption used.

It may not be usefull now but in the future is sure something i should try first to understand if i can get any info.

Another important info, the text in the flag 42CTF{DO_NOT_USE_MONOALPHABETIC_SUBSTITUTION}

A mono-alphabetic cipher (aka simple substitution cipher) is a substitution cipher where each letter of the plain text is replaced with another letter of the alphabet. It uses a fixed key which consist of the 26 letters of a “shuffled alphabet”.
