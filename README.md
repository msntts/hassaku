# Hassakuð
ç»åä¸è´ã§ã¦ã£ã³ãã¦åã®é¨åãç¹å®ããæä½ããã©ã¤ãã©ãªã(äºå®)

## ç°å¢æ§ç¯
### ã©ã¤ãã©ãªã®ã¤ã³ã¹ãã¼ã«
```sh
pip install -r requirements.txt
```

### é¨åç¹å®ç¨ç»åã®æºå
- Hassakuãä½¿ã£ã¦å®è£ããã¢ããªã®ã¯ã¼ã­ã³ã°ãã£ã¬ã¯ããªã« ```resources``` ãã£ã¬ã¯ããªãç¨æãã
- ```resources``` ãã£ã¬ã¯ããªåã«ã¦ã£ãã¦ããæ¤ç´¢ããç»åãéç½®ãå¯¾å¿ç»åãã©ã¼ãããã¯ ```.png``` ã ```.bmp``` 
  - ```resources``` ãã£ã¬ã¯ããªä»¥ä¸ã«å­ãã£ã¬ã¯ããªãä½æããç»åãéç½®ããå ´åã ```resources``` ãã£ã¬ã¯ããªç´ä¸ã®ãã©ã«ãä»¥ä¸ã®å¨ãã¡ã¤ã«ã§ç»åä¸è´ãè©¦ã¿ã¾ã
      - ç»é¢ã®æ¡å¤§çãªã©ã§åä¸ç»åã§ãµã¤ãºãç°ãªããã®ãç¨æãããæç­ã«ä½¿ç¨ãã¦ãã ãã
  - Hassakuã¯ ```resources``` ãã£ã¬ã¯ããªç´ä¸ã®ç»åãã¡ã¤ã«å(æ¡å¼µå­ãé¤ã)ãããã¯ãã£ã¬ã¯ããªåã§æ¤ç´¢ç»åãæå®ãã¾ã

# ãµã³ãã«
ãã©ã«ãæ§æ
```sh
sample
 ââ sample.py
 ââ resources
 â   â 1.png
 â   â 2
 â     â small.png
 â     â big.png
 ââHassaku
```

sample.py
```python
from hassaku import Hassaku 

hassaku = Hassaku()

"""
ãtest.txt - ã¡ã¢ãå¸³ã«ã¯ä»¥ä¸ã®æå­åãè¨è¼

1 2 3 4 5 
6 7 8 9 10
"""

# resources/1.pngã®åº§æ¨ãåå¾
print(hassaku.find_image_from_window("test.txt - ã¡ã¢å¸³", "1"))

# resources/2ãã©ã«ãä»¥ä¸ã®ç»åã§æ¤ç´¢
print(hassaku.find_image_from_window("test.txt - ã¡ã¢å¸³", "2"))

```

å®è¡çµæ
```sh
# 1ã®åºç¾åº§æ¨(å·¦ä¸xåº§æ¨, å·¦ä¸yåº§æ¨, å³ä¸xåº§æ¨, å³ä¸yåº§æ¨)ã®ãªã¹ã
# 1 ã¨ 10 ã§2ååºç¾ãã¦ããã®ã§2ååå¾
[(21, 109, 28, 128), (101, 129, 108, 148)]
# 2ã®åºç¾åº§æ¨
[(41, 111, 49, 126)]
```
