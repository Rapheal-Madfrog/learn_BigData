# Homework1
## 基础

```
a=123
echo $a	
echo "$a"
echo "${a}nd"
let "a+=1"
a=$[$a+1]
a=`expr $a + 1`
```



## for循环

```shell
for ((i=0;i<100;i++))
	do
		command
	done
```



## if条件

```shell
if xxx; then
	command1
elif xxy; then
	command2
else; then
	command3
fi
```



## test

```shell
[[ xxx -a xxx ]] <&& command1 <|| command2>>
```



## 重定向

\> 覆盖

\>> 追加



## function

demo

```shell
funWithParam(){
    echo "第一个参数为 $1 !"
    echo "第二个参数为 $2 !"
    echo "第十个参数为 $10 !"
    echo "第十个参数为 ${10} !"
    echo "第十一个参数为 ${11} !"
    echo "参数总数有 $# 个!"
    echo "作为一个字符串输出所有参数 $* !"
}
funWithParam 1 2 3 4 5 6 7 8 9 34 73
```



## shell test

```shell
functask1(){ 
	echo 'now start!' > output.txt
	for ((i=1;i<=100;i++))
		do 
			echo "$i" >> output.txt
			[[ `expr $i % 10` -eq 0 ]] && echo "$i" >> output.txt
		done
}
```

