# geneticit
Esoteric Programming Language about Genetic IT

## Idea Notes

### Basics

In nature of Life,  
Genetics are the base code .  

In allmost circumstances,  
the process of growing is detemined  
in form of polymorphic recursions.

Genes in Form of DNA or RNA only have four permutations.
There are four aminos called:

* (A) Adenosin
* (T) Thymin
* (C) Cytosin
* (G) Guanin

Given pairings are therefore only

* AT or TA
* CG or GC

So we have only two pairings and  
four permutations for coding in Gentics IT

So in respect to Brainfuck,  
this an even more reduced esoteric level.

### Defnition of a minimum for information processing

* Information or resource has to be adressed
  * Get | Consume and Put | Set | Copy | Duplicate | Place
* Information has to be evaluated
  * Compare Equal
* Information has to be altered
  * Flip Bit
* Flow Directions for processing Information
  * Spin-L or Spin-R
  
So we seem to have a minimum of 4 Codeing Elements.
But, in Genetics we only have a base of two amino pairings,  
if we constitute the flow direction (Spin) of processings.  
Therefore the information Flip has to be considered as addressed information altering and    
the Compare A Equal B Branching as obsolete.
This leads to a set of 2x2 Operations.

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
  # Recursice definition of an decrementation process with 
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

### Addendum

AT or TA Spin L or R  
CG or GC Spin L or R  

Flip 1 or 0 = Consume <=> Place  

On DNA or RNA compare mechanics have to be reconsidered.  
