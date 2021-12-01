# Shop 
Best Stuff - Cheap Stuff, Buy Buy Buy... Store Instance: source. The shop is open for business. 

Category: Reverse Engineering 

## Solution 
Initially I went through the source trying to see if I could make heads or tails of it.

I tried these commands: 
```
$file 
source: ELF 32-bit LSB executable, Intel 80386, version 1 (SYSV), statically linked, Go BuildID=Wq2z6hkBrrAovu6w8dMb/chyUPt3_NgRB5zVfMpf8/99tYvdYHy3xNdHp4wuxA/ClEGFX9e3WU6qjzPxg9K, with debug_info, not stripped

$ objdump -D source 
# strings source 
```
None of these commands did much. I was able to see some of the inner workings, but I didn't feel like I was getting any closer to the flag. I was unable to grep out any flags, so they weren't in the source.   

Based on the hint I figured it was worth seeing if I could input something to break things without looking at the code. I figured this must be a situation where quantity, like in integer overflow attacks, would create a total that make the coin count go up. Yup! If I buy a negative quantity of something I end up with more coins than I had!  

```
You have 40 coins
        Item            Price   Count
(0) Quiet Quiches       10      12
(1) Average Apple       15      8
(2) Fruitful Flag       100     1
(3) Sell an Item
(4) Exit
Choose an option:
0
How many do you want to buy?
-10
You have 140 coins
        Item            Price   Count
(0) Quiet Quiches       10      22
(1) Average Apple       15      8
(2) Fruitful Flag       100     1
(3) Sell an Item
(4) Exit
Choose an option:
2
How many do you want to buy?
1
Flag is:  [112 105 99 111 67 84 70 123 98 52 100 95 98 114 111 103 114 97 109 109 101 114 95 57 99 49 49 56 98 98 102 125]
```
From here I took the Decimal ASCII and had Cyber Chef work out the flag. 

## Flag 
`picoCTF{b4d_brogrammer_9c118bbf}`
