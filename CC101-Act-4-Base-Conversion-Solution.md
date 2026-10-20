# CC 101 – Introduction to Computing

## Activity No. 4 | Base Conversion

*Sorsogon State University – College of Information and Communications Technology, Bulan Campus*

- **Name:** CARL NATHANIEL B. FUNDANO 
- **Section:** BSCS 1-1 
- **Student ID:** 26117009 
- **Instructor:** JOHN MARK GABRENTINA 

## Question 1

- 1 × 2⁷ = 1 × 128 = 128
- 1 × 2⁶ = 1 × 64 = 64
- 1 × 2⁵ = 1 × 32 = 32
- 1 × 2⁴ = 1 × 16 = 16
- 1 × 2³ = 1 × 8 = 8
- 1 × 2² = 1 × 4 = 4
- 0 × 2¹ = 0 × 2 = 0
- 1 × 2⁰ = 1 × 1 = 1

**Answer: 253₁₀**

## Question 2

- 2 × 8³ = 2 × 512 = 1024
- 3 × 8² = 3 × 64 = 192
- 6 × 8¹ = 6 × 8 = 48
- 3 × 8⁰ = 3 × 1 = 3

**Answer: 1267₁₀**

## Question 3

- 4 × 16² = 4 × 256 = 1024
- 0 × 16¹ = 0 × 16 = 0
- 13 × 16⁰ = 13 × 1 = 13

**Answer: 1037₁₀**

## Question 4

- 224 ÷ 2 = 112, Remainder = 0
- 112 ÷ 2 = 56, Remainder = 0
- 56 ÷ 2 = 28, Remainder = 0
- 28 ÷ 2 = 14, Remainder = 0
- 14 ÷ 2 = 7, Remainder = 0
- 7 ÷ 2 = 3, Remainder = 1
- 3 ÷ 2 = 1, Remainder = 1
- 1 ÷ 2 = 0, Remainder = 1

**Answer: 11100000**

## Question 5

- 904 ÷ 8 = 113, Remainder = 0
- 113 ÷ 8 = 14, Remainder = 1
- 14 ÷ 8 = 1, Remainder = 6
- 1 ÷ 8 = 0, Remainder = 1

**Answer: 1610₈**

## Question 6

- 349 ÷ 16 = 21, Remainder = 13 → D
- 21 ÷ 16 = 1, Remainder = 5 → 5
- 1 ÷ 16 = 0, Remainder = 1 → 1

**Answer: 15D₁₆**

## Question 7

- 0100₂ = 4
- 0100₂ = 4
- 0011₂ = 3

**Answer: 443₁₆**

## Question 8

- 001₂ = 1
- 001₂ = 1
- 110₂ = 6
- 000₂ = 0

**Answer: 1160₈**

## Question 9

- A (10₁₀) → 1010₂
- 1 → 0001₂
- 3 → 0011₂

**Answer: 101000010011₂**

## Question 10

- 7 → 111, 6 → 110, 6 → 110 ⇒ Full binary: 111110110₂
- Regrouped in 4 bits: 0001 1111 0110
- 0001₂ = 1
- 1111₂ = F (15₁₀)
- 0110₂ = 6

**Answer: 1F6₁₆**

## Question 11

- 192 = 128 + 64 → 11000000₂
- 168 = 128 + 32 + 8 → 10101000₂
- 38 = 32 + 4 + 2 → 00100110₂
- 191 = 128 + 32 + 16 + 8 + 4 + 2 + 1 → 10111111₂

**Answer: 11000000.10101000.00100110.10111111₂**

## Question 12

Decode `#90FFFF` to decimal RGB:

- Red (90₁₆): (9 × 16) + 0 = 144
- Green (FF₁₆): (15 × 16) + 15 = 255
- Blue (FF₁₆): (15 × 16) + 15 = 255

⇒ Red = 144, Green = 255, Blue = 255

Encode rgb(82, 53, 11) to Hex:

- Red (82): 82 ÷ 16 = 5 R 2 → 52
- Green (53): 53 ÷ 16 = 3 R 5 → 35
- Blue (11): 11 ÷ 16 = 0 R 11 → 0B

**Answer: Red = 144, Green = 255, Blue = 255 | Hex: #52350B**

## Question 13

Permission values: read (r) = 4, write (w) = 2, execute (x) = 1

- Owner (7 = 4+2+1): Binary = 111, rwx = `rwx`
- Group (0 = 0+0+0): Binary = 000, rwx = `---`
- Others (5 = 4+0+1): Binary = 101, rwx = `r-x`

**Answer: Full permission string: `rwx---r-x`**

## Question 14

1. Number of different values: 2¹⁶ = 65,536
2. Largest value in decimal: 2¹⁶ − 1 = 65,535
3. Largest value in binary: 1111111111111111 (16 ones)
4. Largest value in hexadecimal: grouping 16 ones into 4-bit sets (1111 1111 1111 1111) = FFFF₁₆

**Answer: Values: 65,536 | Max Dec: 65,535 | Max Bin: 1111111111111111₂ | Max Hex: FFFF₁₆**

## Question 15

- Binary (base 2): 542 ÷ 2 repeatedly yields remainders ⇒ 1000011110₂
- Octal (base 8): 542 ÷ 8 repeatedly yields remainders ⇒ 1036₈
- Hexadecimal (base 16): 542 ÷ 16 repeatedly yields remainders ⇒ 21E₁₆

Verification:

- Binary: 2⁹ + 2⁴ + 2³ + 2² + 2¹ = 512 + 16 + 8 + 4 + 2 = 542 ✓
- Octal: (1 × 512) + (0 × 64) + (3 × 8) + (6 × 1) = 512 + 24 + 6 = 542 ✓
- Hexadecimal: (2 × 256) + (1 × 16) + (14 × 1) = 512 + 16 + 14 = 542 ✓
- Octal (from binary): 001 000 011 110₂ = 1036₈ ✓
- Hexadecimal (from binary): 0010 0001 1110₂ = 21E₁₆ ✓

**Answers: Binary: 1000011110₂ | Octal: 1036₈ | Hexadecimal: 21E₁₆**
