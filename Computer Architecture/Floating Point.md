# IEEE 754 Floating Point Standard
A representation for non-integral numbers, including extremely small or large values, similar to scientific notation.
## General Format
$$x=(−1)^S×(1+Fraction)×2^{(Exponent−Bias)}$$
where
- **S (Sign bit):** 0 $⇒$ non-negative, 1 $⇒$ negative.
- **Exponent:** Uses excess representation (actual exponent + bias) to ensure it is always unsigned.
- **Fraction:** The significand always has a leading "hidden bit" of 1 (for normalized numbers), so only the fractional part is stored.

| **Precision** | **Total Bits** | **Exponent Bits** | **Fraction Bits** | **Bias** |
| ------------- | -------------- | ----------------- | ----------------- | -------- |
| **Single**    | 32             | 8                 | 23                | 127      |
| **Double**    | 64             | 11                | 52                | 1023     |
Special values:
- **Zero:** Exponent = 0, Fraction = 0.
- **Infinity:** Exponent = 255 (Single) / 2047 (Double), Fraction = 0.
- **NaN (Not a Number):** Exponent = 255 (Single) / 2047 (Double), Fraction $\neq$ 0