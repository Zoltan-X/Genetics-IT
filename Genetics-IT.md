# Genetics-IT

Esoteric Programming Language about Genetic IT

## Idea Notes

### Basics

In nature of Life,  
Genetics are the base code.  

In nearby almost all circumstances,  
the process of growing is determined  
in form of polymorphic recursions.

Genes in Form of DNA or RNA  
only have four permutations.  
There are four aminos called:

* (C) Cytosin
* (G) Guanin
* (A) Adenosin
* (T) Thymin &lt;DNA&gt; or (U) Uracil &lt;RNA&gt;

Given pairings are therefore only

* CG or GC
* TA or AU

So we have only two pairings and  
four permutations for coding in Genetics IT

So in respect to [Brainfuck](https://en.wikipedia.org/wiki/Brainfuck),  
this an even more reduced or abstract esoteric level.

### Definition of a minimum for information processing

+ Technical approach
  * Information or resource has to be addressed
    * &lt;Get | Consume&gt; and &lt;Put | Set | Copy | Duplicate | Place&gt;
  * Information has to be evaluated
    * Compare A Equal B Branch
  * Information has to be altered
    * Flip Bit
  * Flow Directions for processing Information
    * Spin-L or Spin-R

So we seem to have a minimum  
of 4 coding elements.  
But in genetics,  
we only have a base  
of two amino pairings for DNA and RNA,  
if we constitute the flow direction (Spin) of processing.

Therefore the information Flip  
has to be considered  
as addressed information altering and    
the Compare A Equal B Branching as obsolete.  
This leads to a set of 1 x 2 + 2 x 1 Operations.

Further the definition of DNA and RNA,  
has the differences at  
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
      if Information(x) Equals 0
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
      if Information(x) Equals 1
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
  # Information   =>  Limited Set of Bits,  
  #                   Lim -> 1 as x and
  #                   x -> Lim as opposit Lim
  # FlowDirection =>  Sequential Information processing Flow Direction
  #                   L-Spin or R-Spin 
  # A  =>  Summand
  # B  =>  Summand
  Definition Sum(Inf(A), Inf(B), Spin=R-Spin)
    if B equals 0
      Return A
    if Spin equals R-Spin  
      if Inf(B) equals 1
        if Inf(A) equals 0
          Flip(Inf(A))
          Flip(Inf(B))
          if Inf(A) equals 0
            Sum(Inf(A),Inf(B),L-Spin)
          if Inf(A) equals 1
            Sum(Inf(A),Inf(B),R-Spin)
    if Spin equals L-Spin  
      if Inf(A) equals 0
        Flip(Inf(A))
        Sum(Inf(A),Inf(B),R-Spin)
        
    A = 0101 =>  5	 R-0001 L-1001 R-1001 R-1011
    B = 0110 =>  6  R-0010 L-0010 R-0010 R-0000 
    Ret 1011 => 11
  	
    A = 0110 =>  6  R-0010 L-1010 R-1000 L-1100 R-1101
    B = 0111 =>  7	 R-0011 L-0011 R-0001 L-0001 R-0000
    Ret 1101 => 13
  	
  # Lazy Definition
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
  # Information   =>  Limited Set of Bits,  
  #                   Lim -> 1 as x and
  #                   x -> Lim as opposit Lim
  # FlowDirection =>  Sequential Information processing Flow Direction
  #                   L-Spin or R-Spin 
  # A  =>  Minuend
  # B  =>  Subtrahend
Definition Subtract(Inf(A), Inf(B), Spin)
    if Spin equals R-Spin  
      if Inf(B) equals 1
        if Inf(A) equals 1
          Flip(Inf(A))
          Flip(Inf(B))
          Subtract(Inf(A),Inf(B),R-Spin
        if Inf(A) equals 0
          Flip(Inf(B))
          Subtract(Inf(A),Inf(B),L-Spin)
      if B equals 0
        Return A
    if Spin equals L-Spin  
      Flip(Inf(A))
      Subtract(Inf(A),Inf(B),R-Spin)
        
    A = 1111 => 15 	R-1111 R-1011 R-1011 1010
    B = 0101 =>  5  R-0101 R-0001 R-0001 0000
    ret 1010 => 10
    
   	A = 1100 =>  12  R-1100 R-1100 R-1110 L-1010 R-1010 R-1011 L-1001
    B = 0011 =>   3	 R-0011 R-0011 R-0001 L-0001 R-0001 R-0000 L-0000
    ret 1001 => 9
    
  # Lazy Definition
  Definition Subtract(A, B)
    if CompareGreater(B,0)
      Decrement(A)
      Decrement(B)
      Subtract(A, B)
    Return A
```

### Considerations about Genetics with DNA and RNA

#### Obsolete Conditional Branching

So far I postulated,  
that the equal comparison branching is obsolete.    
This chapter is about to explain why I think so and  
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
therefore comparing is obsolete.

#### Useful concepts for genetic codings

As mentioned before,  
there are only four permutations  
with RNA Constructs from DNA Sequences.  
A usability consideration therefore,  
is to say all four permutations  
are doing something different.  

The Aspect of "L|R - spinnings"  
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
different kind of resources  
are mented to be used.  

#### Conceptions, theories and postulations

So far use case Concepts are defined for DNA and RNA behavior,  
but these might not compellingly fit to the confounded pairings,  
neither are they proven.  

So far we have a Definition of something,  
what we could use for a short set of operations,  
that are limited to the coding abilities of DNA and RNA.  

In this case,  
DNA and RNA Constructs,  
could be used for esoteric coding definitions,  
as stated in that past few Years,  
for accumulating information in DNA or RNA.  

#### The cells construction theorem

An approach to construct cells  
with 4 coding Elements,  
seems to be very difficult.

This is caused by the richness  
of various cell types and  
the richness of various cell interactions.

Therefore we should reconsider,  
how cell structures could be useful defined and  
built up with only a set of 4 instructions.  

First of all,  
we can not determine various molecular structures,  
with a set of only four instructions.  
This has to be determined  
by a vast set of interactions,  
that are controllable  
with a set of four instructive elements.  

This means,  
the cellular growth or building process  
is dependent to outer circumstances,  
like liquid bondings.  

Therefore,  
a set of four instructions  
has to be a universal instructions set,  
that would determine  
how cells are going to be constructed.  

This leads to the needs of  
having a molecular reactive amino acid as base,  
that would chain up reactions  
to the desired type of cell.  

Partial DNA sequences have to define RNA Sequences  
that are going to construct partially dependent structures.

This makes it very complex to consider right,  
because the handling of activated and inactivated gene Sequences,  
are not fully discovered nor really understood.  

The conception is about altering the process  
of releasing genetic sequences  
for reproduction of necessary elements  
at the right moment and  
a well formed RNA string.  

So what kind of 4 instructions would we need therefore?

1. We would need an sequence initiator and terminator instruction.  
2. We would need something like an reproduction counter instruction,  
   that would terminate an expansive cell building up operation.
3. We would need a molecular bonding construction.
4. We would need a spatially determined RNA String form,  
   that would fit the cell building process,  
   by sticking to itself at specific points.

The first topic is about to be something like Spin-L|R termination.

The second and third topics should stick together,  
as sequences are somehow of a count delimiting purpose.  
So we would have a double option  
for constructing molecular bindings.
The third aspect determines a wider set of   
cell build up bindings.

The last topic determines a sticky bending,  
that would influence the cell structure.

Therefore,  
the next chapter is about to point out to references.

#### Out pointing

As further suggestions are not the part of the Genetics IT,    
they could be read at:  

* [Gene wiki](https://en.wikipedia.org/wiki/Gene)
* [DNA wiki](https://en.wikipedia.org/wiki/DNA)
* [RNA wiki](https://en.wikipedia.org/wiki/RNA)
* [Biomolecular structures wiki](https://en.wikipedia.org/wiki/Biomolecular_structure)

### Addendum

This coding behavior here has to be treated as  

* technically having Touring abilities  
* inspired from biological handling of decoding Genes  

## Considerations about this ...

### Basics from Digital Flip-Flop mechanisms

First of all, 
the fundamental approach of abstracting all kind of programming languages,  
has to be broken down to the basics of digital processing and  
therefore to Flip-Flop mechanisms.

**All digital circuit logics are realized with Flip-Flop circuits!**

Therefore the fundamental basics  
of all programming languages  
are abstracted to Flip-Flop logics.

As defined in previous [Note.md]  
there are seemingly only two Operations  
A. Flip Bit
A. Compare A Equal B Branching
with a Flow-Direction determined as Spin Left or Right  
for Information structures wider than a single bit.

This is resulting in a minimum Set of:

1. Flip Addressed Information Bit
2. Compare A EQUAL B Branching
3. Flow Direction with SPIN L|R Low- or Big-Endian System

Additionally for functional Programming:

1. Call Function
2. Return Result from Function

And finally:

1. Information Addressing in Form of Duplicate A to B with   
   A Immediate|Register|Memory and  
   B Register|Memory
   * Get A is dup A to B
   * Put A is dup A to B

The abstraction and depending associations to Genetics therefore  
are far more complex caused by several circumstances.

1. There is the special molecular chain structure from DNA and RNA to be considered.  
   It is of fundamental dependency for the genetic mechanics.  
   + There are 
     + the double Helix form of DNA  
       + The partial Sequences, which are (in)activated for reproductions.  
     + The Telomerase Limitations  
     + The Amino pairings and permutations  
   + The Complex of spatial structure definitions  
     * How is it determined that RNA is bending and bonding to itself  
       in a such useful manor,  
       as it defines thereby all applicable structure of cell growth.  
     * Determination of spatially evolving structures with  
       * Nucleus and  
       * Cell borders.  
2. The way how proteins and other cells are build through     
   * Fluid bonding     
   * molecular structural bending of RNA   
   * the Four stages that are known for different stages in Cell building purposes   
3. The Way how DNA builds up Supra Seeded Structures,     
   that evolve to a functional Life Form,    
   no weather if viruses, bacteria, plant, fungus or animal.   
4. The way those Life forms evolve in circumstances determined by the influences of surrounding Nature.   

So we do not have a Digital Coding paradigm reusable in Genetics,  
we have a molecular structure performing on an atomic Level of physics.  
This means,  
the molecular Structures are defining the coding Process in most circumstances and  
the most further following conditions are more than ridiculous coincident,  
make DNA and RNA evolving to an alive Life form.
