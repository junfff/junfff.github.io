---
title: Interview::for-for-for
date: 2021-06-26 09:01:22 +/-TTTT
categories: [Interview]
tags: [Interview]
---

# Subject
            int a = 3;
            int b = 4;
            int c = 5;
            int x = 0;

            for (int i = 0; i < a; i++)
            {
                for (int j = 0; j < b; j++)
                {
                    for (int k = 0; k < c; k++)
                    {
                        x++;
                    }
                }
            }


	任意断点 x 位置,根据 x 值 推断  i j  k,求出公式。

 
	x = 58    k = 58%5=3  , j = 58/5=11%4=3, i =11/4=2
	x = 33    k = 33%5=3  , j = 33/5=6%4=2, i =6/4=1
	公式：
		k=x%c,j=x/c%b, i=x/c/b


