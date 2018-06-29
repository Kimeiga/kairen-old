---
layout: default
title: Home
---

# KAIREN LANGUAGE DESIGN

(number of **?** refers to how experimental the feature is)

## VERBS

By default, verbs are present continuous

> _I ma hepi. [I am happy.]_

Add **"pa"** to end of verb for past tense. Add **"fu"** to end of verb for future tense.

> _Yu bu ma **pa** hepi. [You weren't happy.]_

>_Ta ma **fu** hepi. [She will be happy.]_

 Add **"bu"** to beginning of a verb to negate it.

> _**Bu** go e. [Don't go]_

## SENTENCE TYPES

There are the following sentence types:

1. Declarative
   1. Instructional (use 4th person)
2. Interrogative
3. Command
   1. Suggestion
4. Exclamatory

### DECLARATIVE:

Subject goes first:

> _Hakan go pa suto. [Hakan went to the store]_

### INTERROGATIVE

2 types: **information**, **yes/no**

#### Information Questions

Question words:

1. **Wu** [Who is]
2. **Wa** [What is]
3. **Wo** [When is]
4. **We** [Where is/do]
5. **Wi** [Why]
6. **Ha** [How: What method]
7. **He** [How: What extent]
8. **Hi** [Which]
9. **Ho** [How: What condition]
10. **Hu** [How: How many/What number]

`Experimental`

Question word comes first in information question sentence:

> 1. _**Wu** yu? [Who are you?]_
> 2. _**Wa** di? [What is this?]_
> 3. _**Wo** isu go? [When are we going?]_
> 4. _**We** o? [Where is he?]_
> 5. _**Wi** yu cuto o? [Why did you shoot her?]_
> 6. _**Ha** yu ari qe? [How did you arrive there (the location you are)?]_
> 7. _**He** yacu ma yu? [How old are you?] ?????_
> 8. _**Hi** paqi isu teku? [Which path do we take?] ????????_
> 9. _**Ho** yu? [How are you?]_
> 10. _**Hu** amo yu habe [How much ammo do you have?] ????????????_
>

#### Yes/No Questions

Add question particle **"a"** to end of sentence

> _O ni yepa **a**? [Is he in the kitchen (food-place)?]_

### COMMAND

Subject goes last:

_Go suto Hakan. [Hakan, go to the store.]_

```
PROBLEM

"Go Hakan" is ambiguous between "go to Hakan" and a command to Hakan "go".
I suppose we can have required no subject dropping:

INCORRECT: Tale ma hepi. Ma fu ohepi. [Tale is happy. (He) will not be happy.]
  CORRECT: Tale ma hepi. O ma fu ohepi. [Tale is happy. He will not be happy.]

This means that the sentence "Ma fu ohepi" is a command "will be happy!". Not that this actually makes any sense though.

Then this means that a command without the subject has implied "You". This means that there must be a way to set implied you in a unique sentence construction without requiring punctuation:

English:
Mark, go to the store. (Command)
Mark goes to the store. (Statement)

More precisely, the current problem in Kairen is that when there is a verb and one proper name after it, there is ambiguity between the subject of the command and the object of a declaration. 

English basically solves it with conjugations. The punctuation helps, but is not entirely necessary. 

What if we introduced conjugation to Kairen? Would that make typing it faster?

Examples:
He was in the red cooridor.
Cooridor is a connection between rooms.
Room is <rum>. (chevrons for Kairen, brackets for English).
Connect is <ko>.
Cooridor is <rumko>. (not a pretty sounding word due to mk blend, but whatever, I'm not going to mandate m,n -> x conversion in front of k,g because even though that would make it sound better "ruxko" (x = ng), it would make it harder to memorize).

V1:
O ma pa ni re rumko.

if we say -a = past tense

V2:
O maa ni re rumko. (-2 characters)
but "maa" and "ma" might be difficult to discern between in spoken language.
Probably it would sound like Ma'a in the game due to the way the speech will be generated. 
But then again maybe not: If I record the syllables by trimming off the end of the sound, it might sound continuous, but the "a" could change sound between the two, so it would still not sound completely continuous, just maybe not glottal stopped.

I remember in the beginning, I mandated "-r-" between root and suffix if the vowel was the same:
V3:
O mara ni re rumko. (-1 character)

But this difference is smaller... and you might as well have them be separate words at this point.

V2: 
if we decide to support 1 letter (vowel) conjugations for verbs, it could look like this:
-i = past tense
-u = future tense
-e = command

i ma kulu. [I am cool]
i mai kulu. [I was cool]
i mau kulu. [I will be cool]
i mae kulu. [I be cool!]
mae kulu. [(you) be cool!]

Kasu ma kulu. [Kasu is cool]
Kasu mae kulu. [Kasu, be cool!]

this would allow you to support subject dropping for declarations and questions!

we o go [Where is he going to?]
go re rumko a [Is he going to the red cooridor?]
ye [Yes(, he is)]
sa ju a [Does he have a gun]
aye [maybe] //a note about this... 
goe o [Go to him]
```

PROBLEM

Or subject omitted, &quot;you&quot; assumed as subject:

_Fa i. [(You,) follow me.]_

SUGGESTION

Add &quot;ji&quot; to end of command to turn to suggestion.

_        Mate foru (???)/to (?) i ji [maybe wait for me]_

PERSONAL PRONOUNS

|   | Singular | Plural |
| --- | --- | --- |
| 1st Person | I | Isu (We inclusive: I, you, and he/they), Isa (We exclusive: I, and he/they) |
| 2nd Person | Yu | Yusu (you all) |
| 3rd Person | O | Osu |
| 4th Person (hypothetical) | Qa | Qasu |

Possessive particle: no (not using de because it&#39;s the opposite meaning; ie &quot;no&quot; means &quot;&#39;s&quot; not &quot;of&quot;; ex: i no amo = my ammo, =/= ammo&#39;s me)

_i de, yu de, o de, qa de [my, your, his/her, one&#39;s]_

_isu de, isa de, yusu de, osu de, qasu de [our, our, your, their, one&#39;s]_

PHONOTACTICS

Very simple, so I can build a simple speaking engine out of it for the games.

**(C)V(R)**

**C: any consonant, V: any vowel, R: resonating (n,m,x) (?)**

This way I will create an audio file for each permutation of syllables and each voice actor, and use those in the game to allow the characters to speak. It will sound a little funny, but that&#39;s the best solution I can come up with to allow the characters to speak in game.

I can even make a website in which you can type stuff in Kairen (or mock Kairen), and it will produce the audio file of the character you want speaking it.

Numbers

1. la
2. tu
3. ri
4. fo
5. va
6. si
7. ve
8. co
9. na
10. den
11. den ca
12. den tu
13. etc

100: hun

200: tu hun

1,000: qou

10,000: denqou

100,000: hunqou

1,000,000: mim

10,000,000: denmim

100,000,000: hunmim

1,000,000,000: tunmim (billion)

adding -n to end of a number makes it a prefix (not an ordinal number), and is used in &quot;billion&quot;, &quot;trillion&quot;, etc.

adding -ju to end of number makes it ordinal number

1. laju [first]
2. tuju [second]
3. riju [third]
4. foju [fourth]
5. vaju [fifth]
6. siju [sixth]
7. veju [seventh]
8. coju [eigth]
9. naju [ninth]
10. denju [tenth]
11. etc.

Yes and No

Use o- to negate meaning, and a- to unextreme meaning

_ye [yes], oye [no], aye [maybe]_