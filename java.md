#Java
##Chapter1 计算
###1.2 变量与计算
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsrkqlkm1j31380u0agb.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsrm8mjyvj31660sc423.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsrm84mz7j31200qs0uw.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsrm7orhtj31480twtc5.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsrm77rdrj30z40re0vu.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsrm6p7fgj31h60t2q7n.jpg)
###1.3浮点数
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsrrb5k1zj31a80sotcl.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsrragq6jj31bs0scwjc.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsrr9n89kj314p0u00ya.jpg)

###EX
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsruluu9sj30y20ietim.jpg)

```
package hello;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {
		// °F = (9/5)*°C + 32
		
		int C;
		
		Scanner in = new Scanner(System.in);
		C  = in.nextInt();
		System.out.println((int)((9.0/5)*C+32));
		
	}

}
```

##Chapter 2
Java提供了六个关系运算符：

==	相等

!=	不相等

>	大于

>=	大于或等于

<	小于

<=	小于或等于
####if - else

![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsx8yco2bj317w0swad7.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsx8xvf8gj313c0u0gsb.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsx8x4sbbj31300u00vd.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsx9s2srkj31c60rcmzs.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsx9rkyjuj314x0u0q8q.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsx9qvck5j313y0kyq5f.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsx9qesl2j318e0r00vm.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsxaxru6rj318n0u0q9j.jpg)
####Switch-case
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsxax4znyj31710u00ye.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghsxawh4saj318e0rmn2h.jpg)

####EX 时区换算
```
package hello;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {
		// °F = (9/5)*°C + 32
		

		
		Scanner in = new Scanner(System.in);
		
		int BJT; //北京时间
		int UTC; //世界时间
		
		BJT = in.nextInt();
		if(BJT >= 800)
		{
			UTC = BJT - 800;
		}
		else 
		{
			UTC = BJT + 2400 - 800;
		}
		
		System.out.println("UTC is " + UTC);

		
}
}
```

####EX signal
```
package hello;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {		
		Scanner in = new Scanner(System.in);
		int RS;
		int R;
		int S;
		RS = in.nextInt();
		R = RS/10;
		S = RS%10;
		switch(R) {
		case 1:
			System.out.print("Unreadable, ");
			break;
		case 2:
			System.out.print("Barely readable, occasional words distinguishable, ");
			break;
		case 3:
			System.out.print("Readable with considerable difficulty, ");
			break;
		case 4:
			System.out.print("Readable with practically no difficulty, ");
			break;
		case 5:
			System.out.print("Perfectly readable, ");
			break;	
		default:
			System.out.println("Wrong R Number");
		}
		
		switch(S) {
		case 1:
			System.out.println("Faint signals, barely perceptible");
			break;
		case 2:
			System.out.println("Very weak signals");
			break;
		case 3:
			System.out.println("Weak signals");
			break;
		case 4:
			System.out.println("Fair signals");
			break;
		case 5:
			System.out.println("Fairly good signals");
			break;	
		case 6:
			System.out.println("Good signals");
			break;
		case 7:
			System.out.println("Moderately strong signals");
			break;
		case 8:
			System.out.println("Strong signals");
			break;
		case 9:
			System.out.println("Extremely strong signals");
			break;
		default:
			System.out.println("Wrong Signal Number");
		}	
}
}
```

#Chapter3 While 和 Do-while
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghtmp7f3lej310u0r6aj3.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghtmp6j4jij31i40re0z8.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghtmpranvij312c0r8n0z.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghtmps0fxrj30zy0rc0x2.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghtmpshz4wj31860t842v.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghtmqfiv86j31c40sm7c3.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghtmqetf4sj31440oy432.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghtmr51hsyj313k0r0jvy.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghtmr62hbnj314i0r2wkg.jpg)

####EX 
```
package hello;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {		
		Scanner in = new Scanner(System.in);
		
		int S=0;// 单数
		int D=0;//偶数
		int E;//Entry
		
		
		E = in.nextInt();
		while(E!=-1) {
			
			if(E%2>0) {
				S=S+1;
			}
			else {
				D=D+1;
			}
		    E = in.nextInt();
			
		} 
			
			
			System.out.println(S + " "+D);
			
			
		
	} 
	} 
```

```
package hello;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {		
		Scanner in = new Scanner(System.in);
		

//		E = in.nextInt();	
//			System.out.println(S + " "+D);
		
		int Num=in.nextInt();	
		int Pos=1;
		int total=0;
		while(Num >0)
		{
			if((Num%10)%2==Pos%2) 
			{
				total=total + (int)Math.pow(2,(Pos-1));
				System.out.println(total);
			}
			Pos = Pos+1;
			Num = Num/10;	
		}
		System.out.println(total);
		
	}
}
	

```

#Chpater 4 循环控制 for loop, break, continue
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu155nxk1j314g0ocwhy.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu1554nh5j315k0q0dll.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu154kie8j31au0twwid.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu15vx6syj31by0sojwp.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu15vdzxcj314u0ngabw.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu15uskspj31280o0dip.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu15tqd2oj30yw0qgacc.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu16xwbe6j30y20pq0wb.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu16whpt0j311g0p6adb.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu16vpe2zj31260r6djb.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu17czjqwj314y0o4jt6.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu17ch02cj30ou0wa75o.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu17buunjj30yk0rwgpl.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu17x6qjkj312q0pygpo.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu17wogjlj315o0p642r.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu17vx9vdj312u0n6gno.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu18f5nhej315e0rw77w.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu18epimrj30y80rg779.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghu18e2hwbj30vu0lawjn.jpg)

EX sum of primes

```
package hello;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {		
		Scanner in = new Scanner(System.in);
		
//		int Num=in.nextInt();	

//		System.out.println(total);
		
		
		int a =in.nextInt();
		int b =in.nextInt();
		int count=0;
		int total =0;
		int isPrime;
		
		for (int n=2;n<200;n++) {
			
			isPrime = 1;
		
			for (int i=2;i<n;i++) {
				if (n%i==0)
				{
					isPrime = 0;
					
				}
				
			}
			
			
			if(isPrime ==1) 
			{	count++;
			    if(count>=a&&count<=b)
			    {
			    	total+=n;
			    }
			
			}			
		
		}
		
		System.out.println(total);
		
		
	}
}
```

#Chapter 5 数组
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa2vg3pgj317s0qqad9.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa2uulwhj316q0oudih.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa3m25fhj31a20rqq81.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa3litxlj31840nc75s.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa4aawnlj31b40sun37.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa48d2nxj312m0myadg.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa3l3froj30wm0koabd.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa48d2nxj312m0myadg.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa58z6jdj313m0omtal.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa58a6dij31ds0ngdhn.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa57csc4j30zs0oytbm.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa6px4xpj313g0hcabd.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa6pkyd9j30vs0rygoh.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa6p3dpbj31880qyn10.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa71jv0kj313k0n0t9x.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa718h49j318i0ssn1g.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa8d276lj30r80pegnq.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa8c3w61j30v00q2jxo.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghwa8ar54fj30u20r6acn.jpg)


###多项式加法（5分）
题目内容：
一个多项式可以表达为x的各次幂与系数乘积的和，比如：
2x6+3x5+12x3+6x+20
现在，你的程序要读入两个多项式，然后输出这两个多项式的和，也就是把对应的幂上的系数相加然后输出。
程序要处理的幂最大为100。

输入格式:
总共要输入两个多项式，每个多项式的输入格式如下：
每行输入两个数字，第一个表示幂次，第二个表示该幂次的系数，所有的系数都是整数。第一行一定是最高幂，最后一行一定是0次幂。
注意第一行和最后一行之间不一定按照幂次降低顺序排列；如果某个幂次的系数为0，就不出现在输入数据中了；0次幂的系数为0时还是会出现在输入数据中。

输出格式：
从最高幂开始依次降到0幂，如：
2x6+3x5+12x3-6x+20
注意其中的x是小写字母x，而且所有的符号之间都没有空格，如果某个幂的系数为0则不需要有那项。

```
package hello;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {		
		Scanner in = new Scanner(System.in);
		
//		int Num=in.nextInt();	

//		System.out.println(total);
	
		int[] Num=new int[101];
		int count=0;
		int pos;
	
		
		while(count!=2)
		{	 pos = in.nextInt();
			 Num[pos]=in.nextInt()+Num[pos];
			 
			if(pos ==0)
			{
				count++;
				
			}
		}
		
		for(int i=100;i>1;i--)
		{	
			if(Num[i]!=0) {
			System.out.print(Num[i]+"x"+i+"+");
			}
		
		}
		
		System.out.print(Num[1]+"x"+"+");
		System.out.print(Num[0]);

	}
}
```
#Chapter 6
##字符类型
字符也是Java中基础的数据类型之一，Java采用Unicode16表达字符，在所有的机器上，不管CPU、操作系统和本地语言，字符类型是一致和统一的。
一个字符的常量是用单引号包围起来的一个字符，如'a'、'*'、'好'。一个汉字也是Unicode的一个字符，所以也是Java的一个字符。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjf148bkj31660tugo4.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjf00u80j318f0u0gp4.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjezisqdj311w0r6gou.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjfg4ng1j313i0twwgi.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjff2qfsj315o0la0uv.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjfenvyij314d0u0414.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjfqqcltj311c0rujv6.jpg)

##包裹类型
对于基本数据类型，Java提供了对应的包裹(wrap)类型。这些包裹类型将一个基本数据类型的数据转换成对象的形式，从而使得它们可以像对象一样参与运算和传递。下表列出了基本数据类型所对应的包裹类型：
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjhc4gn5j30f60c2aay.jpg)
我们看到，除了int和char以外，包裹类型就是把基本类型的名字的第一个字母大写。在Java的系统类库中，所有第一个字母大写的，都是类的名字。所以在编辑程序的时候，一定要小心大小写，以免一不小心犯错。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjj6fbqjj310e0tsdi8.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjj5uq5hj30xs0qstak.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjj5akz9j313a0q6gnp.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjjjqq06j312t0u0wk5.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjjj5pf8j313s0pwq4x.jpg)

##字符串
字符串变量和数组变量类似，它并不存放字符串，不是字符串的所有者，它是字符串的管理者。
Java的字符串还是一种特殊的“不可变”对象，所有的字符串操作都是产生一个新的字符串，而不是对原来的字符串的修改。对这一点的理解颇为重要。

##字符串 String
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjpl001nj30yi0najsq.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjpkjr5pj31140pwjtr.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjpk2430j315q0r4wih.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjpwfzigj311a0mgmz5.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjpw2asoj30x60r2ad9.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjpvputyj310m0q4jtk.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjq88elxj310q0r20um.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjq7x4vuj314m0t6ack.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjqjx05aj31560quwhd.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjqjfs9yj313g0s2ju8.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjqj4cvyj31680mojuw.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjqxqz81j315e0rgtci.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjqxee12j312e0ps41c.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjqwwzomj30zo0p4mz5.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjro6vfgj316g0s4adf.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjrnkbbuj315o0rugo1.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjrmtfcaj318y0s4tbn.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjrzmkukj316o0mmdhp.jpg)
###EX单词长度
```
package hello;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {		
		Scanner in = new Scanner(System.in);
		
//		int Num=in.nextInt();	

//		System.out.println(total);
		String S="0";
		while(true) {
			S =in.next();
			if(S.endsWith("."))
			{	System.out.print(S.length()-1);
				break;
			}
			System.out.print(S.length()+" ");
			
		}
	}
}
```


```
package hello;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {		
		Scanner in = new Scanner(System.in);
		
//		int Num=in.nextInt();	

//		System.out.println(total);
		//$GPRMC,024813.640,A,3158.4608,N,11848.3737,E,10.05,324.27,150706,,,A*50
		
	
		String s = "-1";
		
		
		String time="100000";
		
		while(true)
		{	int value=0;
			boolean process = false;
			String[] check;
			String[] buff;
			s=in.nextLine();
//			int v = Integer.parseInt(s, 16);
//			System.out.println(v);
			
			if(s.equals("END"))
			{	//System.out.println(time);
				break;
			}
			 buff = s.split(",");
			 check = s.split("\\*");
			// System.out.println(check[1]);
			 if(buff[0].equals("$GPRMC")&&buff[2].equals("A"))
			 {
				for(int i=0; i<s.length(); i++) 
				{
					int c =s.charAt(i);
					//System.out.println(s.charAt(i)+"value is "+c);
					if(c=='$')
					{
						process =true;
						continue;
					} 
					else if(c=='*')
					{  
						process =false;
					}
					if(process) {
						//System.out.println(s.charAt(i));
						value^=c;
						
					}	
				}	
			}
			 int result = value%65536;
			String result_hex= Integer.toHexString(result);
			//System.out.println(result_hex);
			
				if(check[1].equals(result_hex))
				{	
					//int time = buff[1].split(".");
					//int number1 = Integer.parseInt(buff[1]);
					
					time = buff[1];
					//System.out.println(time);
					time = time.substring(0,6);
					
				}
			 
			 
		}
		
		int bjt;
		
		int UTC= Integer.parseInt(time.substring(0,2));
		
		if(UTC >= 16)
		{
			bjt = UTC +8-24;
		}
		else 
		{
			 bjt= UTC + 8;
		}
		
		System.out.println("UTC is " + bjt+":"+time.substring(2,4)+":"+time.substring(4,6));

		
		
		
	}
}
```


#Chapter 7 函数
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjxd8hjnj30vs0p80un.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjxcghj5j31jd0u00z7.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjxvc8d7j31gs0tiq98.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjxupgpfj311m0mwq5h.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjxu9mvlj31ap0u078r.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjy6s4nrj31di0scn4r.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjy64j3kj318a0o6q9z.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjz0db22j31cu0tugpu.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjyzx4n6j31f80qc79e.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjyz8b2lj31b20sijwg.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjzenjppj30z80se0ww.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjzdzewnj314q0teq7c.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjzdeuw3j31cu0p0tdi.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjzrwrshj31dc0qmjzp.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjzymk5pj31240se0vn.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjzxqf5yj317a0r677m.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxjzx9i22j311m0sagph.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxk09f1pwj31080toq64.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghxk08w9czj30pc0oq0tr.jpg)

###EX 分解素数
```
package hello;

import java.util.Scanner;

public class main {
	public static int toPrime(int n) {
		// TODO Auto-generated method stub
		int i;
		for(i=2;i<100000;i++)
		{
			if(n%i==0&&(n/i)!=1)
			{   
				System.out.print(i+"x");
				break;
			}
			else if(n%i==0&&(n/i)==1)
			{
				System.out.print(i);
				break;
			}
		}
		return i;
		
	}
	public static void main(String[] args) {		
		Scanner in = new Scanner(System.in);
		
//		int Num=in.nextInt();	
		int n = in.nextInt();
		System.out.print(n+"=");
		do {
		n=n/toPrime(n);
		} while(n!=1);
	}
```
EX: 完数

```
package hello;

import java.util.Scanner;

public class main {
	public static int sum(int n) {
		int sum=0;
		for(int i=1;i<n;i++)
		{
			if(n%i==0)
			{
				sum+=i;
			}
		}
		return sum;
	}
	
	public static void main(String[] args) {		
		Scanner in = new Scanner(System.in);
		int n = in.nextInt();
		int m = in.nextInt();
		boolean begin = true;
		for(int i=n;i<=m;i++) 
		{
			if(i==sum(i))
			{
				if(begin==true)
				{
					System.out.print(i);
					begin =false;
				}
				else
				{
					System.out.print(" "+i);
				}
			}
		}

		
		
		
	}
}
```
###EX final EX count the number
```
package hello;

import java.util.Scanner;

public class main {
//	public static int sum(int n) {
//		
//		return;
//	}
	
	public static void main(String[] args) {		
		int total =0;
		int[] num=new int[100];
		Scanner in = new Scanner(System.in);
		
		while(true) {
		String s = in.nextLine();
		
		//System.out.print(s);
		String[] part = s.split(" ");

		
		
		for(int i=0;i<part.length;i++) {
			
			num[part[i].length()]++;
		
		}
		System.out.print(part.length);
		for(int i=1;i<=10;i++) {
			System.out.print(" "+num[i]);
		}
		
		}
		
		}
}
```







