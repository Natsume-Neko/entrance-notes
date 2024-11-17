## Addition and Subtraction
- Overflow
## Multiplication
- Shift and Add
## Division
- Shift and Subtract
## Floating Point
- S: sign
- F: fraction
- E: exponent
$$
(-1)^S \times F \times 2^E
$$
- Overflow: exponent is too large to be represented at exponent field
- Underflow: negative exponent is too large to be represented at exponent field
### IEEE 754
- Implicit 1
$$
(-1)^S \times (1 + (s1 \times 2^{-1}) + (s2 \times 2^{-2}) +...) \times 2^{E}
$$
- Biased exponent
$$
(-1)^S \times (1 + Fraction) \times 2^{Exponent - bias}
$$
#### Addition
1. Align the significand(Shift the smaller to right until the exponent match the larger one)
2. Add the significands
3. Normalize the sum(Either shifting right and incrementing the exponent or shifting left and decreasing the exponent) and judge if underflow or overflow
4. Round the significand
5. Judge if still need normalization. If so, return to step 3. Else done.
#### Multipication
1. Add the exponents(Remember to subtract the bias)
2. Multiply the significand
3. Normalize and round the significand
4. Judge whether still need normalization. If so, return to step 3. 
5. Set the sign.