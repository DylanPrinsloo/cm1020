# Logic Gates Summary

## What Are Logic Gates?
Logic gates are electronic circuits that implement Boolean functions, taking one or more binary inputs (0/LOW or 1/HIGH) and producing a single binary output based on logical rules.

## Basic Logic Gates
1. **AND Gate** (f = x·y):
   - Outputs HIGH only when ALL inputs are HIGH
   - Symbol: Semicircle with flat edge on input side

2. **OR Gate** (f = x+y):
   - Outputs HIGH when AT LEAST ONE input is HIGH
   - Symbol: Pointed shape with curved input side

3. **NOT Gate** (f = x̄):
   - Inverts the input (HIGH → LOW, LOW → HIGH)
   - Symbol: Triangle with a circle at the output

## Derived Gates
1. **XOR Gate**: Outputs HIGH when inputs are DIFFERENT
2. **NAND Gate**: AND gate + NOT (universal gate)
3. **NOR Gate**: OR gate + NOT (universal gate)
4. **XNOR Gate**: XOR gate + NOT (outputs HIGH when inputs are SAME)

## Properties
- AND, OR, XOR, XNOR: Commutative and associative (order doesn't matter)
- NAND, NOR: Commutative but NOT associative (order matters for multiple gates)

## DeMorgan's Laws in Logic Gates
1. **First Law**: NOT(A AND B) = (NOT A) OR (NOT B)
2. **Second Law**: NOT(A OR B) = (NOT A) AND (NOT B)

These laws are foundational for simplifying and designing logic circuits, showing how combinations of gates can be represented in alternative, equivalent forms.