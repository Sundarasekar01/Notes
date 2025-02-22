Euclid's Algorithm is an efficient method to compute the **Greatest Common Divisor (GCD)** of two numbers. The key idea behind the algorithm is:

(a, b) = (b, a % b)

```
  
  class Solution {
    public int gcd(int a, int b) {
        // Applying Euclid's Algorithm
        while (b != 0) {
            int temp = b;
            b = a % b;  // a % b gives the remainder
            a = temp;
        }
        return a;  // Once b becomes 0, a will contain the GCD
    }
}
```

### Example

Let's compute the **GCD** of 48 and 18 using Euclid's algorithm:

- **Step 1**: Start with \( a = 48 \) and \( b = 18 \).
- **Step 2**: Compute \( 48 \% 18 = 12 \).
- **Step 3**: Replace \( a = 18 \) and \( b = 12 \).
- **Step 4**: Compute \( 18 \% 12 = 6 \).
- **Step 5**: Replace \( a = 12 \) and \( b = 6 \).
- **Step 6**: Compute \( 12 \% 6 = 0 \).
- **Step 7**: Now \( b = 0 \), so the GCD is \( a = 6 \).

Thus, **GCD(48, 18) = 6**.

### Time Complexity

Euclid's Algorithm runs in `( O(log min(a, b)) )` time, making it very efficient, especially for large numbers.


