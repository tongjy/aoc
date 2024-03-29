# aoc 2021 : github copilot
2021年的主题是github copilot。 刚刚通过了申请，抱着试试看的心态，来使用copilot进行解题。
- day1：非常顺利，应该是题目简单把，只要把题目内容复制粘贴, 加上‘#’号。copilot 自动完成了所有的工作
- day2: 昨天的路，走不通了，大概是因为解决方法需要一些转换，需要自己定义一些基础函数的名字，copilot就会给出自己的方式：

        if command[0] == 'f':
            pos += int(command1[1])
        elif command[0] == 'd':
            depth += int(command1[1])
        elif command[0] == 'u':
            depth -= int(command1[1])
        return (pos, depth)
- day3：经过昨天小小的改变，先定义了一些函数，由copilot完成这些函数"砖块"，最后由copilot来组装
- day4\day5: 上述模式依然成立
  - [tongjy/aoc/2021](https://github.com/tongjy/aoc/2021) ![Last Commit on GitHub](https://img.shields.io/badge/last%20commit-2021--12--05-brightgreen)

# aoc 2020
- Learning [Picat](http://picat-lang.org/) by solving [Aoc2020](https://adventofcode.com/)
* [tongjy/aoc](https://github.com/tongjy/aoc) ![Last Commit on GitHub](https://img.shields.io/badge/last%20commit-2021--01--06-brightgreen)

为了参与年度编程活动 Aoc2020 我随机选择了使用picat语言，做了所有的题目，也拿到了所有的Star。
虽然因为现学现卖，没有办法去追求提交速度而得到比赛分数，但这个语言特别适合参加这比赛。

简单总结下心得：
1、非常小众，非常小。主要应用场景就是CP类的比赛：CP，CSP，XCSP

2、这个工具的底色是Prolog 声明式编程（P），在此基础上扩展了过程式（I）（循环、if流程），约束式编程工具包（C），事件式编程（A），以及动态编程表（T），可以综合运用多种方式完成编程目标，比赛时可以迅速切换，这是最大的特色，比如解决8皇后问题：

    %八皇后问题的变形，N皇后问题
    import cp. %CP问题的武器库 
    queens(N, Q) =>   % N皇后， Q返回list,每行的皇后在第几排
    Q = new_list(N),  % N那么大的棋盘，有N个皇后（逗号：表示AND） 
    Q :: 1..N,        % 皇后 Q的取值范围是 1到N
    all_different(Q), % Q里面的取值都不一样，意思是 每列只有一个皇后
    all_different([$Q[I]-I : I in 1..N]), % 斜线看只有一个皇后
    all_different([$Q[I]+I : I in 1..N]), % 反斜线看只有一个皇后
    solve([ff],Q).     % 在上面的约束下，解决了吧【用ff搜索法 = first fail】

    
3、社区很小，偏僻的小村。近期专业领域内比赛经常拿个金奖银奖，所以才会被注意到。最近的更新是3.04版，2021年1月2日，还是比较新鲜的。

4、有学院气息，目前不是一个商业化的东西，没有roadmap之类的，甚至都没有数据库的支持，没有太多工程化的痕迹，比如测试、分发、上线、库管理等等。

如果要去参加CSP领域的比赛，Picat还真的可以。声明式+多范式，写出来的程序可以非常简洁，提交答案速度有优势。程序运行速度优化过，还自带优化过的CSP算法。
Picat本身是对Prolog这一类语言的非常漂亮的发展，可以简洁地在声明式和过程式之间自由切换。也引入了声明式语言的问题：声明的东西其实不存在，或者求解的时间大大超出预期（比如一万年）。
未来走向，实话说这个语言本身大概率不会向Python那样大有发展，但多范式语言这个东西，还是可以长期看好的。
