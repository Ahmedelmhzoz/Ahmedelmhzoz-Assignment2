## Solution

I used two pointers technique: 

-**Swap** the values at `left` and `right`

-`left` starts from idx = 0 

-`right` starts from idx = s.Length - 1

-For each iteration I move `left` and `right` towards **Center**

-Checking in `While loop` if the L pointer become greater than R pointer or not

``
Expected Time Complexity: O(n)
Expected Space Complexity: O(1)
``

## C# Solution 

```csharp
public class Solution {
    private void Swap(ref char a, ref char b) {
        char temp = a;
        a = b;
        b = temp;
    }
    public void ReverseString(char[] s) {
        int l = 0, r = s.Length - 1;
        while (r > l) {
            Swap(ref s[l], ref s[r]);
            l++; r--;
        }
    }
}
```
-O(n) Complexity-> Because each character processed at most once

-O(1) Space-> Because We don't create any extra arrays 

![Reverse String acceptance](./ReverseString.md)