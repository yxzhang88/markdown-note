# 48. Rotate Image
``` py
        left = 0
        right = len(matrix) - 1
        while left < right:
            for i in range(right-left):
                top, buttom = left, right

                # save the topleft
                topLeft = matrix[top][left+i]

                # move buttom left into top left
                matrix[top][left+i] = matrix[buttom-i][left]

                # move buttom right into buttom left
                matrix[buttom-i][left] = matrix[buttom][right-i]

                # move top right to buttom right
                matrix[buttom][right-i] = matrix[top+i][right]

                # move top left to top right
                matrix[top+i][right] = topLeft
            right -= 1
            left += 1
```
- 看完neet讲解完感觉题目倒也不难，就是一个循环的套路，从外到内，然后如何增减pointers
- 我觉得重点2点：  
    - 1 是在于什么时候增减
    - 2 是在思考思路的过程使用画图可以更加清晰的看到是怎么一个循环规律
