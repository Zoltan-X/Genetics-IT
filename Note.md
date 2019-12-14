# geneticit
Esoteric Programming Language about Genetic IT

## Idea Notes

### Basics

In nature of Life,  
Genetics are the base code.  

In nearby allmost all circumstances,  
the process of growing is detemined  
in form of polymorphic recursions.

Genes in Form of DNA or RNA only have four permutations.
There are four aminos called:

* (C) Cytosin
* (G) Guanin
* (A) Adenosin
* (T) Thymin &lt;DNA&gt; or (U) Uracil &lt;RNA&gt;

Given pairings are therefore only

* CG or GC
* TA or AU

So we have only two pairings and  
four permutations for coding in Gentics IT

So in respect to [Brainfuck](https://en.wikipedia.org/wiki/Brainfuck),  
this an even more reduced or abstract esoteric level.

### Defnition of a minimum for information processing

* Information or resource has to be adressed
  * &lt;Get | Consume&gt; and &lt;Put | Set | Copy | Duplicate | Place&gt;
* Information has to be evaluated
  * Compare A Equal B Branch
* Information has to be altered
  * Flip Bit
* Flow Directions for processing Information
  * Spin-L or Spin-R
  
So we seem to have a minimum of 4 codeing elements.
But in Genetics,  
we only have a base of two amino pairings for DNA and RNA,  
if we constitute the flow direction (Spin) of processings.

Therefore the information Flip  
has to be considered  
as addressed information altering and    
the Compare A Equal B Branching as obsolete.  
This leads to a set of 1 x 2 + 2 x 1 Operations.

Further the definition of DNA and RNA,  
has the differnces at  
Thymin or Uracil pairing with Adenosin,  
that defines 2 singleton cases and  
one flow direction ("Spin-L|R") double case  
for Cytosin and Guanin permutation.

This leads to the four possible coding sets:

* CG  <=> GC
  * CG (Spin-L) 
  * GC (Spin-R)
* AU (Consume or Get)
* TA (Place or Put)

The definition above  
is from an technical information aspect driven.  

### Minimum Information processing Examples with Conditions and Flips

```Genetics-IT
  # Recursice definition of an incrementation process with 
  # automatic abort of recursion if the processing flow  reached its Limit.
  # 
  # Information   =>  Limited Set of Bits,  
  #                   1 -> Lim as x and
  #                   x -> 1 as opposit Lim
  # FlowDirection =>  Sequential Information processing Flow Direction
  #                   L-Spin or R-Spin 
  Definition Increment(Information(x), FlowDirection)
    if FlowDirection Equal L-Spin
      if Inf(x) Equals 0
        Flip(Information(x))
        Flip(FlowDirection)
        Increment(Information(x), FlowDirection)
    Flip(Information(x))
    Increment(Information(x), FlowDirection)
```

```Genetics-IT
  # Recursice definition of a decrementation process with 
  # automatic abort of recursion if the processing flow  reached its Limit.
  # 
  # Information   =>  Limited Set of Bits,  
  #                   1 -> Lim as x and
  #                   x -> 1 as opposit Lim
  # FlowDirection =>  Sequential Information processing Flow Direction
  #                   L-Spin or R-Spin 
  Definition Decrement(Information(x), FlowDirection)
    if FlowDirection Equal L-Spin
      if Inf(x) Equals 1
        Flip(Information(x))
        Flip(FlowDirection)
        Decrement(Information(x), FlowDirection)
    Flip(Information(x))
    Decrement(Information(x), FlowDirection)
```

```Genetics-IT
  # Recursice definition of a compare Lower process with 
  # automatic abort of recursion if the processing flow  reached its Limit.
  # 
  # A  =>  Comparand
  # B  =>  Comparator
  Definition CompareLower(A, B)
    if B Equ 0
      Return 0
    Decrement(B. L-Spin)
    if A Equal B B
      Return 1
    CompareLower(A,B)
```

```Genetics-IT
  # Recursice definition of a compare Greater process with 
  # automatic abort of recursion if the processing flow  reached its Limit.
  # 
  # A  =>  Comparand
  # B  =>  Comparator
  Definition CompareGreator(A, B)
    CompareLower(B, A)
```


```Genetics-IT
  # Recursice definition of a summation process with 
  # automatic abort of recursion if the processing flow reached its Limit.
  # 
  # A  =>  Summand
  # B  =>  Summand
  Definition Sum(A, B)
    if CompareGreater(B,0)
      Increment(A)
      Decrement(B)
      Sum(A, B)
    Return A
```

```Genetics-IT
  # Recursice definition of a subtraction process with 
  # automatic abort of recursion if the processing flow reached its Limit.
  # 
  # A  =>  Minuend
  # B  =>  Subtrahend
  Definition Subtract(A, B)
    if CompareGreater(B,0)
      Decrement(A)
      Decrement(B)
      Subtract(A, B)
    Return A
```
### Considerations about Genetics with DNA and RNA

#### Obsolete Conditional Branching

So far I postulated that the equal camparison branching is obsolete and  
this chapter is about to explain why I think so and  
will highlight some further more aspects of these cases treaty.
 
If we would do compare branchings in genetics,  
there would be a desirable need to cut of RNAs  
if there is only a partially matching.  
This means that at some point,  
we would not generate fitting Genes  
as they would be conditionally broken.  

So we should consider  
that only fitting structures  
(Genetic Sequences)  
will workout right.

This means that conditional branchings and  
therefore comparings are obsolete.

#### Usefull concepts for genetic codings

As mentioned before,  
there are only four permutations  
with RNA Constructs from DNA Sequences.  
A useabillity consideration therefore,  
is to say all four permutations  
are doing something different.  

The Aspect of "L|R - spinings"  
is driven by a technical information handling,  
but as the nature of Life is not working like processor,  
we should reconsider this case and  
think about the use of an spinning effect.  

This does not mean that  
spinning effects are of no use case,  
but the way how DNA and RNA are processed,  
are analogues to the obsolete branching idea.  

So these spinnings,  
could alter the way of  
consume and Place of Resources,  
as well as they could mean that,  
different kind of ressource  
are ment to be used.  

#### Conceptions, theories and postulations

So far use case Concepts are defined for DNA and RNA behaviour,  
but these might not compellingly fit to the permutable pairings,  
neither are they prooven.  

So far we have a Definition of something,  
what we could use for a short set of operations,  
that are limited to the coding abillities of DNA and RNA.  

In this case,  
DNA and RNA Constructs,  
could be used for esoterical coding definitions,  
as stated in tha past few Years,  
for accumulating information in DNA or RNA.  

#### Out pointings

As further suggestions are not the part of the Genetics IT,    
they could be read at:  

* [Gene wiki](https://en.wikipedia.org/wiki/Gene)
* [DNA wiki](https://en.wikipedia.org/wiki/DNA)
* [RNA wiki](https://en.wikipedia.org/wiki/RNA)

### Addendum

This coding behaviour here has to be treated as  

* technically having Touring abillities  
* biological handling of decoding Genes  
