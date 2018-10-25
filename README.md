# teetcode
#### Python 语言题解
-------------------------------------------------------------------
### 翻转数
<pre><code>
class Solution:
    def reverse(self, x):
        """
        :type x: int
        :rtype: int
        """
        if x == 0:
            return 0
        elif x > 0:
            y = 0
            while x >= 10:
                y = (y + x % 10) * 10 
                x = int(x / 10)
            y = y + x 
            if y > 2147483647:
                return 0
            else:
                return y
        else:
            y = 0
            x = -1 * x
            while x >= 10:
                y = (y + x % 10) * 10 
                x = int(x / 10)
            
            if y > 2147483648:
                return 0
            else:
                y = -1 * (y + x) 
                return y
</code></pre>
