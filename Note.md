# geneticit
Esoteric Programming Language about Genetic IT

## Idea Notes

### Basics

In nature of Life,  
Genetics are the base code .  

In nearby allmost circumstances,  
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
* AT or UA

So we have only two pairings and  
four permutations for coding in Gentics IT

So in respect to Brainfuck,  
this an even more reduced esoteric level.

### Defnition of a minimum for information processing

* Information or resource has to be adressed
  * Get | Consume and Put | Set | Copy | Duplicate | Place
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
This leads to a set of 1 x 2 + 2 Operations.

Further the definition of DNA and RNA,  
with the differnces at  
Thymin or Uracil pairing with Adenosin
defines 2 singleton cases and  
one flow direction ("Spin-L|R") double case for 
Cytosin and Guanin permutation.

This leads to the four possibly coding sets:

* CG  <=> GC
  * CG (Spin-L) 
  * GC (Spin-R)
* AU (Consume or Get)
* TA (Place or Put)



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
      0
    Decrement(B. L-Spin)
    if A Equal B B
      1
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
    A
```

```Genetics-IT
  # Recursice definition of a subtraction process with 
  # automatic abort of recursion if the processing flow reached its Limit.
  # 
  # A  =>  Minuend
  # B  =>  Subtrahend
  Definition Sum(A, B)
    if CompareGreater(B,0)
      Decrement(A)
      Decrement(B)
      Sum(A, B)
    A
```



### Addendum

AT or TA Spin L or R  
CG or GC Spin L or R  

Flip 1 or 0 = Consume <=> Place  

On DNA or RNA compare mechanics have to be reconsidered.  
