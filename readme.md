# 这是 cli-homework 的答案

1. 找到在 Ubuntu 系统中可以用于计算文件内容 MD5 值的命令

answer : md5sum + 文件名

2. 找到在 Ubuntu 系统中可以用于比较两个文件的内容的差异的命令

answer : diff + 文件 1 + 文件 2

3. 实现一个名为 odd-or-even 的 Bash function，可以用来判断给其提供的第一个参数是奇数还是偶数，奇数时输出 odd，偶数时输出 even

- 定义了一个 odd-or-even 脚本 脚本代码如下 运行代码 sh odd-or-even.sh + 数字
- 如 sh odd-or-even.sh 1 返回 this is jishu

answer :
if [ $(($1%2)) == 0 ] ; then
echo "this is oushu"
else
echo "this is jishu"
fi
else
echo "Error NaN"
fi

4. 实现一个名为 next 的脚本，当在 CLI 里执行 $ next （$为提示符，不需要输入）时就返回一个整数，第一次返回 1，每执行一次加 1

answer:
if [ ! -e "next_help.txt" ]
then
echo 1 > next_help.txt
echo 1
else
n=$(cat next_help.txt)
n=expr $n + 1
echo $n > next_help.txt
echo $n
fi

5. 一个文件含有 N 行内容，每行的内容都是一个大于等于 0 的整数，无任何空行或其它内容，使用 one-liner 的形式对该文件中的数字求和

answer: for i in {1..5};do
j=`cat /home/guanrunkai/abc | awk -v test=$i '{print $test}'`

              let sum+=j
            done

             echo sum=$sum
