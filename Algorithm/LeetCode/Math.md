## 1. LeetCode 836 [Rectangle Overlap](https://leetcode.com/problems/rectangle-overlap/)

```c++
class Solution {
public:
    bool isRectangleOverlap(vector<int>& rec1, vector<int>& rec2) {
        return (min(rec1[2], rec2[2]) > max(rec1[0], rec2[0])
               && min(rec1[3], rec2[3]) > max(rec1[1], rec2[1]));
    }
};
```



## 2. LeetCode 223 [Rectangle Area](https://leetcode.com/problems/rectangle-area/)

```c++
class Solution {
public:
    int computeArea(int A, int B, int C, int D, int E, int F, int G, int H) {
        long width = (long)min(C, G) - (long)max(A, E);
        long height = (long)min(D, H) - (long)max(B, F);
        
        long area = (C - A) * (D - B) + (G - E) * (H - F);
        
        if (width > 0 && height > 0) {
            return area - width * height;
        }
        
        return area;
    }
};
```

