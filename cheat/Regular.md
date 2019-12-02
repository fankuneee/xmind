# 正则表达式

| 字符                         | 描述                                                    | 例子                                                         |
| ---------------------------- | ------------------------------------------------------- | ------------------------------------------------------------ |
| . (点)                       | 任何单个字符，除了换行(\n)                              | c.t 匹配 "cat", "cut" 或 "cot."。'任意字符加im'：[root@test: /tmp]# egrep '.im' a.txt who **simply** need a little refresher  from **time** to **time**. |
| * (星号)                     | 重复前一个表达式0或多次                                 | 12*3 匹配 "13", "123", "1223", "12223"。 与 . 合用代表任何字符。m.*easier 匹配 "maketecheasier"。'x加任意个0加1:'[root@test: /tmp]# egrep 'x0*1:' a.txt0x1:0x00001:0x0000001:'任何包含f加任意字符加l'[root@test: /tmp]# egrep 'f.*l' a.txt how use**ful regul**ar expressions are.  will be use**ful** **for peopl**e |
| + (加号)                     | 重复前一个表达式1或多次                                 | 12+3 匹配 "123","1223","12223"'x加至少一个0加1:' （比较上一个用*的）[root@test: /tmp]# egrep 'x0+1:' a.txt0x00001:0x0000001: |
| ? (问号)                     | 前一个字符可有可无                                      | ma?ke 匹配 "make", "mke"'有n或无n加ee'[root@test: /tmp]# egrep 'n?ee' a.txtThis Regular Expressions cheats**hee**t  who simply **nee**d a little refresher |
| ^ (尖号)                     | 匹配字符串的开头                                        | ^he 匹配以he开头的 "hello", "hell", "help", "he is a boy"'以空格开头的行'[root@test: /tmp]# egrep '^ ' a.txt how useful regular expressions are.  are everywhere in Linux for searching through text right down to the character.  will be useful for people  who simply need a little refresher  from time to time. |
| $ (美刀)                     | 匹配字符串的结尾                                        | ed$ 匹配以ed结尾的 "acted", bed", "greed"'字母e结尾的行'[root@test: /tmp]# egrep 'e$' a.txtyou’ll appreciat**e** from tim**e** |
| (...) (小括号)               | 匹配字符组合                                            | (ak) 匹配 "make", "take"'包含 it 的'[root@test: /tmp]# egrep '(it)' a.txtIf you work w**it**h text,  who simply need a l**it**tle refresher |
| {n} (大括号，n是大于0的整数) | 重复前一个字符n次，n>0                                  | 12{3}5 匹配 "12225"'x加4个0加1'[root@test: /tmp]# egrep 'x0{4}1' a.txt0x**0000**1: |
| [...] (中括号)               | 匹配里面的任意一个字符                                  | [abc] 匹配字符串"abc"中的"a","b" 或 "c"'所有包含v或b的'[root@test: /tmp]# egrep '[vb]' a.txt are e**v**erywhere in Linux will **b**e useful |
| [^...]                       | 匹配任意字符，除了里面定义的                            | a[^b]c 匹配 "aec", "acc", "adc", 但不匹配 "abc"'f前面不能是空格或e'[root@test: /tmp]# egrep '[^ e]f' a.txtIf you work with text, |
| \| (管道符)                  | 匹配管道符分隔的任一字符串                              | col(o\|ou)r 匹配 "color", "colour"                           |
| - (连字符)                   | 指定某个范围内的字符一般是[a-z],[A-Z],[1-9],[a-zA-Z1-9] | a[a-z]c 匹配 "abc", "acc", "adc"                             |
| \ (反斜线)                   | 转义符，将特殊符合转义为符号本身                        | a\*c 匹配 "a*c".                                             |
| \n, \r, \t                   | 代表 换行，回车，制表符                                 |                                                              |
| \b...\b                      | 匹配整个单词                                            | \bTech\b 匹配 the word "Tech" in "Make Tech Easier".找到单词time[root@test: /tmp]# egrep '\btime\b' a.txt from time to time. |