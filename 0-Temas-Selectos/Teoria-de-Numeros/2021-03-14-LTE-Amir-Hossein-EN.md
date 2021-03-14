---
layout: default
search_exclude: true
tema: Arcoiris
tema_oscuro: ArcoirisOscuro
title: LTE by Amir Hossein
nav_order: 1
description: "Lifting the Exponent Lemma."
last_modified_date: 2021-03-14T15:14:15+9265
parent: Teoría de Números
grand_parent: Temas Selectos
---
<!--
1. [<span>Definitions and Notation</span>{:.deg-sitio-1 .deg-sitio-texto}](#definitions-and-notation)
2. [<span>Two Important and Useful Lemmas</span>{:.deg-sitio-2 .deg-sitio-texto}](#two-important-and-useful-lemmas)
   1. [<span>Lemma 1</span>{:.deg-sitio-3 .deg-sitio-texto}](#lemma1)
   2. [<span>Lemma 2</span>{:.deg-sitio-4 .deg-sitio-texto}](#lemma2)
3. [<span>Lifting The Exponent Lemma (LTE)</span>{:.deg-sitio-5 .deg-sitio-texto}](#lifting-the-exponentlemma-lte)
   1. [<span>Theorem 1 First Form of LTE</span>{:.deg-sitio-6 .deg-sitio-texto}](#theorem1first-form-of-lte)
   2. [<span>Theorem 2 Second Form of LTE</span>{:.deg-sitio-7 .deg-sitio-texto}](#theorem2second-form-of-lte)
4. [<span>What about&nbsp;<span>\\(p=2\\)</span>?</span>{:.deg-sitio-8 .deg-sitio-texto}](#what-aboutp2)
   1. [<span>Theorem 3 LTE for the case&nbsp;<span>\\(p=2\\)</span></span>{:.deg-sitio-9 .deg-sitio-texto}](#theorem3lte-for-the-casep2)
   2. [<span>Theorem 4</span>{:.deg-sitio-10 .deg-sitio-texto}](#theorem4)
5. [<span>Summary</span>{:.deg-sitio-11 .deg-sitio-texto}](#summary)
6. [<span>Problems with solutions</span>{:.deg-sitio-12 .deg-sitio-texto}](#problems-with-solutions)
   1. [<span>Problem 1 Russia 1996</span>{:.deg-sitio-11 .deg-sitio-texto}](#problem1russia-1996)
   2. [<span>Problem 2 Balkan 1993</span>{:.deg-sitio-10 .deg-sitio-texto}](#problem2balkan-1993)
   3. [<span>Problem 3</span>{:.deg-sitio-9 .deg-sitio-texto}](#problem3)
   4. [<span>Problem 4</span>{:.deg-sitio-8 .deg-sitio-texto}](#problem4)
7. [<span>Challenge Problems</span>{:.deg-sitio-7 .deg-sitio-texto}](#challenge-problems)
8. [<span>Hints and Answers to Selected Problems</span>{:.deg-sitio-6 .deg-sitio-texto}](#hints-and-answers-to-selected-problems)
9. [<span>Original sources</span>{:.deg-sitio-5 .deg-sitio-texto}](#original-sources)
10. [<span>References</span>{:.deg-sitio-4 .deg-sitio-texto}](#references)

<div> </div>
{:.salto .no-mostrar}

&#x2060;<span>$$a_nx^n+\cdots+a_0$$</span>{:.math .deg-sitio-1 .deg-sitio .deg-sitio-texto}

&#x2060;<span>\\(\ldots\\)</span>{:.math .deg-sitio-1 .deg-sitio .deg-sitio-texto .fs-6}

&#x2060;<span>\\(-\ldots\\)</span>{:.math .deg-sitio-1 .deg-sitio .deg-sitio-texto .fs-2}-->

# Lifting The Exponent Lemma<br><span>(LTE)</span>{:.deg-sitio .deg-sitio-texto .deg-sitio-2}
{:.no_toc}

Amir Hossein Parvardi
{:.fs-6 .fw-300}

**Version&nbsp;<span>6</span>{:.deg-sitio-3 .deg-sitio-texto}**<br/>
February 20, 2021

*Lifting The Exponent Lemma* is a powerful method for solving exponential Diophantine equations. It is pretty well-known in the Olympiad folklore (see, e.g., **Reference&nbsp;[<span>3</span>{:.deg-sitio-4 .deg-sitio-texto}](#references)**) though its origins are hard to trace. Mathematically, it is a close relative of the classical Hensel’s lemma (see **Reference&nbsp;[<span>2</span>{:.deg-sitio-5 .deg-sitio-texto}](#references)**) in number theory (in both the statement and the idea of the proof). In this article we analyze this method and present some of its applications.

We can use the Lifting The Exponent Lemma (this is a long name, let’s call it **LTE**!) in lots of problems involving exponential equations, especially when we have some prime numbers (and actually in some cases it “explodes” the
problems). This lemma shows how to find the greatest power of a prime \\(p\\) —which is often \\(\ge 3\\)— that divides  \\(a^n+b^n\\) for some positive integers \\(a\\) and \\(b\\). The proofs of theorems and lemmas in this article have nothing difficult and all of them use elementary mathematics. Understanding the theorem’s usage and its meaning is more important to you than remembering its detailed proof.

I have to thank Fedja, darij grinberg (Darij Grinberg), makar and ZetaX (Daniel) for their notifications about the article. And I specially appreciate JBL (Joel) and Fedja helps about \\(\TeX\\) issues.

## Definitions and Notation

For two integers \\(a\\) and \\(b\\) we say \\(a\\) is divisible by \\(b\\) and write \\(b\|a\\) if and only if there exists some integer \\(q\\) such that \\(a=qb\\).

We define \\(v_p(x)\\) to be the greatest power in which a prime \\(p\\) divides \\(x\\); in particular, if \\(v_p(x)=\alpha\\) then \\(p^\alpha\|x\\) but \\(p^{\alpha+1}\nmid x\\). We also write \\(p^\alpha \\\|x\\), if and only if \\(v_p(x)=\alpha\\). So we have \\(v_p(xy)=v_p(x)+v_p(y)\\) and \\(v_p(x+y)\ge\\) \\(\min\\{v_p(x), v_p(y)\\}\\).

#### Example
{:.no_toc}

The greatest power of \\(3\\) that divides \\(63\\) is \\(3^2\\), because \\(3^2=9\|63\\) but \\(3^3=27\nmid 63\\). In particular, \\(3^2\\\|63\\) or \\(v_3(63)=2\\).

#### Example
{:.no_toc}

Clearly we see that if \\(p\\) and \\(q\\) are two different prime numbers, then \\(v_p(p^\alpha q^\beta)=\alpha\\), or \\(p^\alpha\\\|p^\alpha q^\beta\\).

**Note**: We have \\(v_p(0)=\infty\\) for all primes \\(p\\).

<div> </div>
{:.salto .no-mostrar}

## Two Important and Useful Lemmas

### Lemma&nbsp;<span>1</span>{:.deg-sitio-6 .deg-sitio-texto}
Let \\(x\\) and \\(y\\) be (not necessary positive) integers and let \\(n\\) be a positive integer. Given an arbitrary prime \\(p\\) (in particular, we can have \\(p=2\\)) such that \\(\gcd(n,p)=1\\), \\(p\|x−y\\) and neither \\(x\\), nor \\(y\\) is divisible by \\(p\\) (i.e., \\(p\nmid x\\) and \\(p\nmid y\\)). We have

$$v_p(x^n−y^n)=v_p(x−y).$$
{:.math}

#### Proof
{:.no_toc}

We use the fact that

$$x^n−y^n=(x−y)\left(x^{n−1}+x^{n−2}y+x^{n−3}
y^2+\cdots+y^{n−1}\right).$$
{:.math}

Now if we show that \\(p\nmid x^{n−1}+x^{n−2}y\,+\\) \\(x^{n−3}y^2+\cdots+y^{n−1}\\), then we are done.

In order to show this, we use the assumption \\(p\|x−y\\). So we have \\(x−y\equiv 0\;\bmod\;p\\), or \\(x\equiv y\;\bmod\;p\\). Thus

$$\begin{align*}
x^{n−1}&+x^{n−2}y+x^{n−3}y^2+\cdots+y^{n−1}\\
&\equiv x^{n−1}+x^{n−2}\cdot x+x^{n−3}\cdot x^2+\cdots+x\cdot x^{n−2}+x^{n−1}\\
&\equiv nx^{n−1}\\
&\not\equiv 0\;\bmod\;p.
\end{align*}$$
{:.math}

This completes the proof.

### Lemma&nbsp;<span>2</span>{:.deg-sitio-7 .deg-sitio-texto} 
Let \\(x\\) and \\(y\\) be (not necessary positive) integers and let \\(n\\) be an odd positive integer. Given an arbitrary prime \\(p\\) (in particular, we can have \\(p=2\\))
such that \\(\gcd(n,p)=1\\), \\(p\|x+y\\) and neither \\(x\\), nor \\(y\\) is divisible by \\(p\\), we have

$$v_p(x^n+y^n)=v_p(x+y).$$
{:.math}

#### Proof
{:.no_toc}

Since \\(x\\) and \\(y\\) can be negative, using **Lemma [<span>1</span>{:.deg-sitio-8 .deg-sitio-texto}](#lemma1)** we obtain

$$v_p(x^n−(−y)^n)=v_p(x−(−y))\implies v_p(x^n+y^n)=v_p(x+y).$$
{:.math}

Note that since \\(n\\) is an odd positive integer we can replace \\((−y)^n\\) with \\(−y^n\\).

<div> </div>
{:.salto .no-mostrar}

## <span>Lifting The Exponent</span>{:.deg-sitio-9 .deg-sitio-texto}&nbsp;Lemma (LTE)

### Theorem&nbsp;<span>1</span>{:.deg-sitio-10 .deg-sitio-texto}&nbsp;First Form of LTE
Let \\(x\\) and \\(y\\) be (not necessary positive) integers, let \\(n\\) be a positive integer, and let \\(p\\) be an odd prime such that \\(p\|x−y\\) and none of \\(x\\) and \\(y\\) is divisible by \\(p\\) (i.e., \\(p\nmid x\\) and \\(p\nmid y\\)). We have

$$v_p(x^n−y^n)=v_p(x−y)+v_p(n).$$
{:.math}

#### Proof
{:.no_toc}

We may use induction on \\(v_p(n)\\). First, let us prove the following statement:

$$v_p(x^p−y^{\,p})=v_p(x−y)+1. \tag{1}\label{eq:1}$$
{:.math}

In order to prove this, we will show that

$$p | x^{p−1}+x^{p−2}y+\cdots+xy^{\,p−2}+y^{\,p−1}\;\tag{2}\label{eq:2}$$
{:.math}

and

$$p^2\nmid x^{p−1}+x^{p−2}y+\cdots+xy^{p−2}+y^{\,p−1}.\;\tag{3}\label{eq:3}$$
{:.math}

For \\(\style{color:#5c5962;}{\eqref{eq:2}}\\), we note that

$$x^{p−1}+x^{p−2}y+\cdots+xy^{\,p−2}+y^{\,p−1}\equiv px^{p−1}\equiv 0\mod p.$$
{:.math}

Now, let \\(y=x+kp\\), where \\(k\\) is an integer. For an integer \\(1\le t< p\\) we have

$$
\begin{align*}
y^{t}x^{p−1−t}&\equiv(x+kp)^{t}x^{p−1−t}\\
&\equiv x^{p−1−t}\left(x^t+t(kp)\left(x^{t−1}\right)+\frac{t(t-1)}{2}(kp)^2\left(x^{t−2}\right)+\cdots\right)\\
&\equiv x^{p−1−t}\left(x^t+t(kp)\left(x^{t-1}\right)\right) \\
&\equiv x^{p-1}+tkpx^{p-2}\mod p^2
\end{align*}
$$
{:.math}

This means

$$y^tx^{p−1−t}\equiv x^{p−1}+tkpx^{p−2}\mod p^2,\;\;t=1, 2,3,4,\ldots,p−1.$$
{:.math}

Using this fact, we have

$$
\begin{align*}
x^{p−1}&+x^{p−2}y+\cdots+xy^{p−2}+y^{p−1}\\
&\equiv x^{p−1}+(x^{p−1}+kpx^{p−2})+(x^{p−1}+2kpx^{p−2})+\cdots+(x^{p−1}+(p-1)kpx^{p−2})\\
&\equiv px^{p−1}+(1+2+\cdots+p-1)kpx^{p−2}\\[0.5em]
&\equiv px^{p−1}+\frac{p(p-1)}{2}kpx^{p−2}\\[0.5em]
&\equiv px^{p−1}+\frac{p-1}{2}kp^2x^{p−1}\\[0.5em]
&\equiv px^{p−1}\\
&\not\equiv 0\mod p^2.\\
\end{align*}
$$
{:.math}

So we proved \\(\style{color:#5c5962;}{\eqref{eq:3}}\\) and the proof of \\(\style{color:#5c5962;}{\eqref{eq:1}}\\) is complete. Now let us return to our problem. We want to show that

$$v_p(x^n−y^n)=v_p(x−y)+v_p(n).$$
{:.math}

Suppose that \\(n=p^\alpha b\\) where \\(\gcd(p,b)=1\\). Then

$$
\begin{align*}
v_p(x^n−y^n)&=v_p\left(\left(x^{p^\alpha}\right)^b−\left(y^{\,p^\alpha}\right)^b\right)\\
&=v_p\left(x^{p^\alpha}−y^{\,p^\alpha}\right)=v_p\left(\left(x^{p^{\alpha-1}}\right)^p−\left(y^{\,p^{\alpha-1}}\right)^p\right)\\
&=v_p\left(x^{p^{\alpha-1}}−y^{\,p^{\alpha-1}}\right)+1=v_p\left(\left(x^{p^{\alpha-2}}\right)^p−\left(y^{\,p^{\alpha-2}}\right)^p\right)+1\\
&=v_p\left(x^{p^{\alpha-2}}−y^{\,p^{\alpha−2}}\right)+2\\
&\:\;\vdots\\
&=v_p\left(x^{p^1}−y^{\,p^1}\right)+\alpha−1=v_p(x-y)+\alpha\\
&=v_p(x-y)+v_p(n).
\end{align*}
$$
{:.math}

Note that we used the fact that if \\(p\|x−y\\), then we have \\(p\|x^k−y^k\\), because we have \\(x−y\|x^k−y^k\\) for all positive integers \\(k\\). The proof is complete.

<div> </div>
{:.salto .no-mostrar}

### Theorem&nbsp;<span>2</span>{:.deg-sitio-11 .deg-sitio-texto}&nbsp;Second Form of LTE 
Let \\(x\\), \\(y\\) be two integers, \\(n\\) be an odd positive integer, and \\(p\\) be an odd prime such that \\(p\|x+y\\) and none of \\(x\\) and \\(y\\) is divisible by \\(p\\). We have

$$v_p(x^n+y^n)=v_p(x+y)+v_p(n).$$
{:.math}

#### Proof
{:.no_toc}

This is obvious using **Theorem&nbsp;[<span>1</span>{:.deg-sitio-12 .deg-sitio-texto}](#theorem1-first-form-of-lte)**. See the trick we used in proof of **Lemma&nbsp;[<span>2</span>{:.deg-sitio-11 .deg-sitio-texto}](#lemma2)**.

<div> </div>
{:.salto .no-mostrar}

## What about \\(p=2\\)?

>**Question.** Why did we assume that \\(p\\) is an odd prime, i.e., \\(p\ne 2\\)? Why can’t we assume that \\(p=2\\) in our proofs?
>
>**Hint.** Note that \\(\frac{p−1}{2}\\) is an integer only for \\(p>2\\).

### Theorem&nbsp;<span>3</span>{:.deg-sitio-10 .deg-sitio-texto}&nbsp;LTE for the case&nbsp;<span>\\(p=2\\)</span>
Let \\(x\\) and \\(y\\) be two odd integers such that \\(4\| x−y\\). Then

$$v_2\left(x^n−y^n\right)=v_2(x−y)+v_2(n).$$
{:.math}

#### Proof
{:.no_toc}

We showed that for any prime \\(p\\) such that \\(\gcd(p,n)= 1\\), \\(p\|x−y\\) and none of \\(x\\) and \\(y\\) is divisible by \\(p\\), we have

$$v_p(x^n-y^n)=v_p(x−y)$$
{:.math}

Let \\(m\\) be an odd integer and \\(k\\) be a positive integer such that \\(n=m\cdot2^k\\). So it suffices to show that

$$v_2\left(x^{2^k}−y^{2^k}\right) =v_2(x−y)+k.$$
{:.math}

Factorization gives

$$x^{2^k}−y^{2^k}=\left(x^{2^{k−1}}+ y^{2^{k−1}}\right)\left(x^{2^{k−2}}+ y^{2^{k−2}}\right)\cdots(x^2+y^2)(x+y)(x-y)$$
{:.math}

Now since \\(x\equiv y\equiv\pm 1\;\bmod\;4\\) then we have \\(x^{2^i}\equiv\\) \\(y^{2^i}\equiv 1\;\bmod\;4\\) for all positive integers \\(i\\) and so \\(x^{2^i}+y^{2^i}\equiv 2\;\bmod\;4,\\) \\(i=1,2,3,\ldots\\) Also, since \\(x\\) and \\(y\\) are odd and \\(4\|x−y\\), we have \\(x+y\equiv 2\;\bmod\;4\\). This means the power of \\(2\\) in all of the factors in the above product (except \\(x−y\\)) is one. We are done.

### Theorem&nbsp;<span>4</span>{:.deg-sitio-9 .deg-sitio-texto}
Let \\(x\\) and \\(y\\) be two odd integers and let \\(n\\) be an even positive integer. Then

$$v_2(x^n−y^n)=v_2(x−y)+v_2(x+y)+v_2(n)−1.$$
{:.math}

<div> </div>
{:.salto .no-mostrar}

#### Proof
{:.no_toc}
We know that the square of an odd integer is of the form \\(4k+1\\). So for odd \\(x\\) and \\(y\\) we have \\(4\|x^2−y^2\\). Now let \\(m\\) be an odd integer and \\(k\\) be a positive integer such that \\(n=m\cdot2^k\\). Then

$$\begin{align*}
v_2(x^n−y^n)&=v_2\left(x^{m\cdot2^k}−y^{m\cdot2^k}\right)\\
&=v_2\left(\left(x^2\right)^{2^{k−1}}−\left(y^2\right)^{2^{k−1}}\right)\\
&\;\;\vdots\\
&=v_2\left(x^2−y^2\right)+k−1\\
&=v_2(x−y)+v_2(x+y)+v_2(n)−1.
\end{align*}$$
{:.math}

 
<div> </div>
{:.salto .no-mostrar}

## Summary

Let \\(p\\) be a prime number and let \\(x\\) and \\(y\\) be two (not necessary positive) integers that are not divisible by \\(p\\). Then:

>**a.** For a positive integer \\(n\\)

>* if \\(p\ne 2\\) and \\(p\|x−y\\), then

$$v_p(x^n−y^n)=v_p(x−y)+v_p(n).$${:.math}

>* if \\(p=2\\) and \\(4\|x−y\\), then

$$v_2(x^n−y^n)=v_2(x−y)+v_2(n).$${:.math}

>* if \\(p=2\\), \\(n\\) is even, and \\(2\|x−y\\), then

$$v_2(x^n−y^n)=v_2(x-y)+v_2(x+y)+v_2(n)−1.$${:.math}

>**b.** For an odd positive integer \\(n\\), if \\(p\|x+y\\), then

$$v_p(x^n+y^n)=v_p(x+y)+v_p(n).$${:.math}

>**c.** For a positive integer \\(n\\) with \\(\gcd(p,n)=1\\), if \\(p\|x−y\\), we have

$$v_p(x^n-y^n)=v_p(x-y).$${:.math}

>If \\(n\\) is odd, \\(\gcd(p,n)=1\\), and \\(p\|x+y\\), then we have

$$v_p(x^n+y^n)=v_p(x+y).$${:.math}

**Note:** The most common mistake in using **LTE** is when you don’t check the \\(p\|x\pm y\\) condition, so always remember to check it. Otherwise your solution will be completely wrong.

<div> </div>
{:.salto .no-mostrar}

## Problems with solutions

### Problem&nbsp;<span>1</span>{:.deg-sitio-1 .deg-sitio-texto}&nbsp;Russia 1996

Find all positive integers \\(n\\) for which there exist positive integers \\(x\\), \\(y\\) and \\(k\\) such that \\(\gcd(x,y)=1\\), \\(k>1\\) and \\(3^n=x^k+y^k\\).

#### Solution
{:.no_toc}

\\(k\\) should be an odd integer (otherwise, if \\(k\\) is even, then \\(x^k\\) and \\(y^k\\) are perfect squares, and it is well known that for integers \\(a\\), \\(b\\) we have \\(3\|a^2+b^2\\) if and only if \\(3\|a\\) and \\(3\|b\\), which is in contradiction with \\(\gcd(x,y)=1\\)).

Suppose that there exists a prime \\(p\\) such that \\(p\|x+y\\). This prime should be odd. So \\(v_p(3^n)=v_p(x^k+y^k)\\), and using **Theorem&nbsp;[<span>2</span>{:.deg-sitio-3 .deg-sitio-texto}](#theorem2-second-form-of-lte)** we have \\(v_p(3^n)=\\) \\(v_p(x^k+y^k)=\\) \\(v_p(k)+v_p(x+y)\\). But \\(p\|x+y\\) means that \\(v_p(x+y)\ge 1>0\\) and so \\(v_p(3^n)=v_p(k)+v_p(x+y)>0\\) and so \\(p\|3^n\\). Thus \\(p=3\\). This means \\(x+y=3^m\\) for some positive integer \\(m\\). Note that \\(n=v_3(k)+m\\). There are two cases:

* \\(m>1\\)
  
  We can prove by induction that \\(3^a\ge a+2\\) for all integers \\(a\ge 1\\), and so we have \\(v_3(k)\le k − 2\\) (why?). Let \\(M=\max(x,y)\\). Since \\(x+y=3^m\ge 9\\), we have \\(M\ge 5\\). Then

  $$\begin{align*}
  M^{k-1}\ge 5^{k-1}&\land M\ge \frac{x+y}{2}=\frac{1}{2}\cdot 3^m\\[1em]
  x^k+y^k&\ge M^k=M\cdot M^{k-1}\\
  &\phantom{\ge}>\frac{1}{2}\cdot 3^m\cdot5^{k-1}\\
  &\phantom{\ge >}>3^m\cdot 5^{k-2}\\
  &\phantom{\ge >>}\ge 3^{m+k-2}\\
  &\phantom{\ge >>\ge}\ge 3^{m+v_3(k)}=3^n
  \end{align*}$$
  {:.math}
  
  which is a contradiction.
* \\(m=1\\)
   
  Then \\(x+y=3\\), so \\(x=1\\), \\(y=2\\) (or \\(x=2\\), \\(y=1\\)). Thus \\(3^{1+v_3(k)}=1+2^k\\). But note that \\(3^{v_3(k)}\|k\\) so \\(3^{v_3(k)}\le k\\). Thus
  
  $$1+2^k=3^{v_3(k)+1}=3\cdot3^{v_3(k)}\le 3k\implies 1+2^k\le 3k$${:.math}
  
  And one can check that the only odd value of \\(k>1\\) that satisfies the above inequality is \\(k=3\\). So \\((x,y,n,k)=\\) \\((1, 2, 2, 3)\\), \\((2, 1, 2, 3)\\) in this case.

Thus, the final answer is \\(n=2\\).

### Problem&nbsp;<span>2</span>{:.deg-sitio-5 .deg-sitio-texto}&nbsp;Balkan 1993

Let \\(p\\) be a prime number and \\(m>1\\) be a positive
integer. Show that if for some positive integers \\(x>1\\), \\(y>1\\) we have

$$\frac{x^p+y^{\,p}}{2}=\left(\frac{x+y}{2}\right)^m,$${:.math}

then \\(m=p\\).

#### Solution
{:.no_toc}

One can prove by induction on \\(p\\) that \\(\frac{x^p+y^{\\!\\;p}}{2}\ge\left(\frac{x+y}{2}\right)^p\\) for all positive integers \\(p\\). Now since \\(\frac{x^p+y^{\\!\\;p}}{2}=\left(\frac{x+y}{2}\right)^m\\), we should have \\(m\ge p\\). Let \\(d=\gcd(x,y)\\), so there exist positive integers \\(x_1\\), \\(y_1\\) with \\(\gcd(x_1,y_1)=1\\) such that \\(x=dx_1\\), \\(y=dy_1\\) and \\(2^{m−1}(x^p_1+y^{\\,p}_1)=d^{m−p}(x_1+y_1)^m\\). There are two cases:

* Assume that \\(p\\) is odd.
  
  Take any prime divisor \\(q\\) of \\(x_1+y_1\\) and let \\(v=v_q(x_1+y_1)\\). If \\(q\\) is odd, we see that \\(v_q(x^{p}_1+y^{\\,p}_1)=v+v_q(p)\\) and \\(v_q(d^{m−p}(x_1+y_1)^m)\ge mv\\) (because \\(q\\) may also be a factor of \\(d\\)). Thus \\(m\le 2\\) and \\(p\le 2\\), giving an immediate contradiction. If \\(q=2\\), then \\(m-1+v\ge mv\\), so \\(v\le 1\\) and \\(x_1+y_1=2\\), i.e., \\(x=y\\), which immediately implies \\(m=p\\).
* Assume that \\(p=2\\). 
  
  We notice that for \\(x+y\ge 4\\) we have \\(\frac{x^2+y^2}{2}<\\) \\(2\left(\frac{x+y}{2}\right)^2\le\\) \\(\left(\frac{x+y}{2}\right)^3\\), so \\(m=2\\). It remains to check that the remaining cases \\((x,y)=(1,2),(2,1)\\) are impossible.

### Problem&nbsp;<span>3</span>{:.deg-sitio-7 .deg-sitio-texto} 
Find all positive integers \\(a\\), \\(b\\) that are greater than \\(1\\) and satisfy

$$b^a|a^b−1.$${:.math}

#### Solution
{:.no_toc}

Let \\(p\\) be the least prime divisor of \\(b\\). Let \\(m\\) be the least positive integer for which \\(p\|a^m−1\\). Then \\(m\|b\\) and \\(m\|p−1\\), so any prime divisor of \\(m\\) divides \\(b\\) and is less than \\(p\\). Thus, not to run into a contradiction, we must have \\(m=1\\). Now, if \\(p\\) is odd, we have \\(av_p(b)\le v_p(a − 1)+v_p(b)\\), so \\((a−1)\\) \\(\le (a−1)v_p(b)\\) \\(\le v_p(a−1)\\), which is impossible. Thus \\(p=2\\), \\(b\\) is even, \\(a\\) is odd and \\(av_2(b)\le v_2(a−1)\\,+\\,\\)&#x200B;\\(v_2(a+1)+v_2(b)−1\\) whence \\(a\le\\) \\((a−1)v_2(b)+1\le\\) \\(v_2(a − 1)\\,+\\,\\)&#x200B;\\(v_2(a+1)\\), which is possible only if \\(a=3\\), \\(v_2(b)=1\\). Put \\(b=2B\\) with odd \\(B\\) and rewrite the condition as \\(2^3B^3\|3^{2B}−1\\). Let \\(q\\) be the least prime divisor of \\(B\\) (now, surely, odd). Let \\(n\\) be the least positive integer such that \\(q\|3^n−1\\). Then \\(n\|2B\\) and \\(n\|q−1\\) whence \\(n\\) must be \\(1\\) or \\(2\\) (or \\(B\\) has a smaller prime divisor), so \\(q\|3−1=2\\) or \\(q\|3^2−1=8\\), which is impossible.

Thus \\(B=1\\) and \\(b=2\\).

<div> </div>
{:.salto .no-mostrar}

### Problem&nbsp;<span>4</span>{:.deg-sitio-9 .deg-sitio-texto} 
Find all positive integer solutions of the equation \\(x^{2009}+y^{2009}=7^z\\).

#### Solution
{:.no_toc}

Factor \\(2009\\). We have \\(2009=7^2\cdot 41\\). Since \\(x+y\|x^{2009}+y^{2009}\\) and \\(x+y>1\\), we must have \\(7\| x+y\\). Removing the highest possible power of \\(7\\) from \\(x\\), \\(y\\) (why?), <!--we get \\(v_7(x^{2009}+y^{2009})=v_7(x+y)+v_7(2009)=\\) \\(v_7(x+y)+2\\), so \\(x^{2009}+y^{2009}=49\cdot k\cdot(x+y)\\) where \\(7\nmid k\\). But we have \\(x^{2009}+y^{2009}=7^z\\), which means the only prime factor of \\(x^{2009}+y^{2009}\\) is \\(7\\), so \\(k=1\\). Thus \\(x^{2009}+y^{2009}=49(x+y)\\). But in this equation the left hand side is much larger than the right hand one if \\(\max(x,y)>1\\), and, clearly, \\((x,y)=(1,1)\\) is not a solution. Thus the given equation does not have any solutions in the set of positive integers.--> we get a solution of the equation such that \\(7\nmid x,y\\). We only need to check if there exists that solution. In that case, \\(v_7(x^{2009}+y^{2009})=\\) \\(v_7(x+y)+\\) \\(v_7(2009)=\\) \\(v_7(x+y)+2\\), so \\(x^{2009}+y^{2009}=\\) \\(49\cdot k\cdot(x+y)\\) where \\(7\nmid k\\). But we have \\(x^{2009}+y^{2009}=7^z\\), which means the only prime factor of \\(x^{2009}+y^{2009}\\) is \\(7\\), so \\(k=1\\). Thus \\(x^{2009}+y^{2009}=\\) \\(49(x+y)\\). But in this equation the left hand side is much larger than the right hand one if \\(\max(x,y)>1\\), and, clearly, \\((x,y)=(1,1)\\) is not a solution. Thus the given equation does not have any solutions in the set of positive integers.

<div> </div>
{:.salto .no-mostrar}

## Challenge Problems

### Problem&nbsp;<span>1</span>{:.deg-sitio-1 .deg-sitio-texto .deg-sitio-1}
{:.no_toc}

Let \\(k\\) be a positive integer. Find all positive integers \\(n\\) such that \\(3^k\|2^n−1\\).

### Problem&nbsp;<span>2</span>{:.deg-sitio-2 .deg-sitio-texto} UNESCO Competition 1995
{:.no_toc}

Let \\(a\\), \\(n\\) be two positive integers and let \\(p\\) be an odd prime number such that

$$a^p\equiv 1\mod{p^n}$${:.math}

Prove that

$$a\equiv 1\mod{p^{n-1}}$${:.math}

### Problem&nbsp;<span>3</span>{:.deg-sitio-3 .deg-sitio-texto} Iran Second Round 2008
{:.no_toc}

Show that the only positive integer value of \\(a\\) for
which \\(4(a^n+1)\\) is a perfect cube for all positive integers \\(n\\), is \\(1\\).

### Problem&nbsp;<span>4</span>{:.deg-sitio-4 .deg-sitio-texto}
{:.no_toc}

Let \\(k>1\\) be an integer. Show that there exists infinitely many positive integers \\(n\\) such that

$$n|1^n+2^n+3^n+\cdots+k^n.$${:.math}

### Problem&nbsp;<span>5</span>{:.deg-sitio-5 .deg-sitio-texto} Ireland 1996
{:.no_toc}

Let \\(p\\) be a prime number, and \\(a\\) and \\(n\\) positive integers. Prove that if

$$2^p+3^p=a^n$${:.math}

then \\(n=1\\).

### Problem&nbsp;<span>6</span>{:.deg-sitio-6 .deg-sitio-texto} Russia 1996
{:.no_toc}

Let \\(x\\), \\(y\\), \\(p\\), \\(n\\), \\(k\\) be positive integers such that \\(n\\) is odd and \\(p\\) is an odd prime. Prove that if \\(x^n+y^n=p^k\\), then \\(n\\) is a power of \\(p\\).

### Problem&nbsp;<span>7</span>{:.deg-sitio-7 .deg-sitio-texto}
{:.no_toc}

Find the sum of all the divisors \\(d\\) of \\(N=19^{88}−1\\) which are of the form \\(d=2^a3^b\\) with \\(a,b\in\mathbb{N}\\).

### Problem&nbsp;<span>8</span>{:.deg-sitio-8 .deg-sitio-texto}
{:.no_toc}

Let \\(p\\) be a prime number. Solve the equation \\(a^{p}−1 =p^k\\) in the set of positive integers.

### Problem&nbsp;<span>9</span>{:.deg-sitio-9 .deg-sitio-texto}
{:.no_toc}

Find all solutions of the equation 

$$(n−1)!+1=n^m$${:.math}

in positive integers.

### Problem&nbsp;<span>10</span>{:.deg-sitio-10 .deg-sitio-texto} Bulgaria 1997
{:.no_toc}

For some positive integer \\(n\\), the number \\(3^n−2^n\\) is a perfect power of a prime. Prove that \\(n\\) is a prime.

### Problem&nbsp;<span>11</span>{:.deg-sitio-11 .deg-sitio-texto}
{:.no_toc}

Let \\(m\\), \\(n\\), \\(b\\) be three positive integers with \\(m\ne n\\) and \\(b>1\\). Show that if prime divisors of the numbers \\(b^n−1\\) and \\(b^m−1\\) be the same, then \\(b+1\\) is a perfect power of \\(2\\).

### Problem&nbsp;<span>12</span>{:.deg-sitio-12 .deg-sitio-texto} IMO ShortList 1991
{:.no_toc}

Find the highest degree \\(k\\) of \\(1991\\) for which \\(1991^k\\) divides the number

$$1990^{1991^{1992}}+1992^{1991^{1990}}.$${:.math}

### Problem&nbsp;<span>13</span>{:.deg-sitio-12 .deg-sitio-texto}
{:.no_toc}

Prove that the number \\(a^{a−1}−1\\) is never square-free for all integers \\(a>2\\).

### Problem&nbsp;<span>14</span>{:.deg-sitio-11 .deg-sitio-texto} Czech Slovakia 1996
{:.no_toc}

Find all positive integers \\(x\\), \\(y\\) such that \\(p^x−y^{\\,p}=1\\), where \\(p\\) is a prime.

### Problem&nbsp;<span>15</span>{:.deg-sitio-10 .deg-sitio-texto}
{:.no_toc}

Let \\(x\\) and \\(y\\) be two positive rational numbers such that for infinitely many positive integers \\(n\\), the number \\(x^n−y^n\\) is a positive integer. Show that \\(x\\) and \\(y\\) are both positive integers.

### Problem&nbsp;<span>16</span>{:.deg-sitio-9 .deg-sitio-texto} IMO 2000
{:.no_toc}

Does there exist a positive integer \\(n\\) such that \\(n\\) has exactly \\(2000\\) prime divisors and \\(n\\) divides \\(2^n+1\\)?

### Problem&nbsp;<span>17</span>{:.deg-sitio-8 .deg-sitio-texto} China Western Mathematical Olympiad 2010
{:.no_toc}

Suppose that \\(m\\) and \\(k\\) are non-negative integers, and \\(p=2^{2^{m}}+1\\) is a prime number. Prove that

* \\(2^{2^{m+1}p^k}\equiv 1\mod p^{k+1}\\)
* \\(2^{m+1}p^k\\) is the smallest positive integer \\(n\\) satisfying the congruence equation \\(2^n\equiv 1\mod p^{k+1}\\).

### Problem&nbsp;<span>18</span>{:.deg-sitio-7 .deg-sitio-texto}
{:.no_toc}

Let \\(p\ge 5\\) be a prime. Find the maximum value of positive integer \\(k\\) such that

$$p^k|(p−2)^{2(p−1)}−(p−4)^{p−1}.$${:.math}

### Problem&nbsp;<span>19</span>{:.deg-sitio-6 .deg-sitio-texto}
{:.no_toc}

Let \\(a\\), \\(b\\) be distinct real numbers such that the numbers

$$a−b,a^2−b^2,a^3−b^3,\ldots$${:.math}

are all integers. Prove that \\(a\\), \\(b\\) are both integers.

### Problem&nbsp;<span>20</span>{:.deg-sitio-5 .deg-sitio-texto} MOSP 2001
{:.no_toc}

Find all quadruples of positive integers \\((x,r,p,n)\\) such that \\(p\\) is a prime number, \\(n,r>1\\) and \\(x^r−1=p^n\\).

### Problem&nbsp;<span>21</span>{:.deg-sitio-4 .deg-sitio-texto} China TST 2009
{:.no_toc}

Let \\(a>b>1\\) be positive integers and \\(b\\) be an odd
number, let \\(n\\) be a positive integer. If \\(b^n\|a^n−1\\), then show that \\(a^b>\frac{3^n}{n}\\).

### Problem&nbsp;<span>22</span>{:.deg-sitio-3 .deg-sitio-texto} Romanian Junior Balkan TST 2008
{:.no_toc}

Let \\(p\\) be a prime number, \\(p\ne 3\\), and integers \\(a\\), \\(b\\) such that \\(p\|a+b\\) and \\(p^2\|a^3+b^3\\). Prove that \\(p^2\|a+b\\) or \\(p^3\|a^3+b^3\\).

### Problem&nbsp;<span>23</span>{:.deg-sitio-2 .deg-sitio-texto}
{:.no_toc}

Let \\(m\\) and \\(n\\) be positive integers. Prove that for each odd positive integer \\(b\\) there are infinitely many primes \\(p\\) such that \\(p^n\equiv 1\\!\\!\mod b^m\\) implies \\(b^{m−1}\|n\\).

### Problem&nbsp;<span>24</span>{:.deg-sitio-1 .deg-sitio-texto} IMO 1990
{:.no_toc}

Determine all integers \\(n>1\\) such that

$$\frac{2^{n} + 1}{n^2}$${:.math}

is an integer.

<div> </div>
{:.salto .no-mostrar}

### Problem&nbsp;<span>25</span>{:.deg-sitio-1 .deg-sitio-texto}
{:.no_toc}

Find all positive integers \\(n\\) such that

$$\frac{2^{n-1} + 1}{n}$${:.math}

is an integer.

### Problem&nbsp;<span>26</span>{:.deg-sitio-2 .deg-sitio-texto}
{:.no_toc}

Find all primes \\(p\\), \\(q\\) such that \\(\dfrac{(5^p−2^p)(5^q−2^q)}{pq}\\) is an integer.

### Problem&nbsp;<span>27</span>{:.deg-sitio-3 .deg-sitio-texto}
{:.no_toc}

For some natural number \\(n\\) let \\(a\\) be the greatest natural number for which \\(5^n−3^n\\) is divisible by \\(2^a\\). Also let \\(b\\) be the greatest natural number such that \\(2^b\le n\\). Prove that \\(a\le b+3\\).

### Problem&nbsp;<span>28</span>{:.deg-sitio-4 .deg-sitio-texto}
{:.no_toc}

Determine all sets of non-negative integers \\(x\\), \\(y\\) and \\(z\\) which satisfy the equation

$$2^x+3^y=z^2.$${:.math}

### Problem&nbsp;<span>29</span>{:.deg-sitio-5 .deg-sitio-texto} IMO ShortList 2007
{:.no_toc}

Find all surjective functions \\(f : \mathbb{N}\rightarrow \mathbb{N}\\) such that for every \\(m,n\in\mathbb{N}\\) and every prime \\(p\\), the number \\(f(m+n)\\) is divisible by \\(p\\) if and only if \\(f(m)+f(n)\\) is divisible by \\(p\\).

### Problem&nbsp;<span>30</span>{:.deg-sitio-6 .deg-sitio-texto} Romania TST 1994
{:.no_toc}

Let \\(n\\) be an odd positive integer. Prove that \\(\left((n−1)^n+1\right)^2\\) divides \\(n(n−1)^{(n−1)^n+1}+n\\).

### Problem&nbsp;<span>31</span>{:.deg-sitio-7 .deg-sitio-texto}
{:.no_toc}

Find all positive integers \\(n\\) such that \\(3^n−1\\) is divisible by \\(2^n\\).

### Problem&nbsp;<span>32</span>{:.deg-sitio-8 .deg-sitio-texto} Romania TST 2009
{:.no_toc}

Let \\(a,n\ge 2\\) be two integers, which have the following
property: there exists an integer \\(k\ge 2\\), such that \\(n\\) divides \\((a−1)^k\\). Prove that \\(n\\) also divides 

$$a^{n−1}+a^{n−2}+\cdots+a+1.$${:.math}

### Problem&nbsp;<span>33</span>{:.deg-sitio-9 .deg-sitio-texto}
{:.no_toc}

Find all the positive integers \\(a\\) such that \\(\frac{5^a+1}{3^a}\\) is a positive integer.

<div> </div>
{:.salto .no-mostrar}

## Hints and Answers to Selected Problems
### Problem [<span>1</span>{:.deg-sitio-1 .deg-sitio-texto}](#problem1)
{:.no_toc}

Answer: \\(n=2\cdot 3^{k−1}s\\) for some \\(s\in\mathbb{N}\\).

### Problem [<span>2</span>{:.deg-sitio-2 .deg-sitio-texto}](#problem2-unesco-competition-1995)
{:.no_toc}

Show that \\(v_p(a−1)=v_p(a^p−1)−1\ge\\)\\(n−1\\).

### Problem [<span>3</span>{:.deg-sitio-3 .deg-sitio-texto}](#problem3-iran-second-round-2008)
{:.no_toc}

If \\(a>1\\), \\(a^2+1\\) is not a power of \\(2\\) (because it is \\(> 2\\) and either \\(1\\) or \\(2\\) modulo \\(4\\)). Choose some odd prime \\(p\|a^2+1\\). Now, take some \\(n=2m\\) with odd \\(m\\) and notice that \\(v_p(4(a^n+1))=\\) \\(v_p(a^2+1)+v_p(m)\\) but \\(v_p(m)\\) can be anything we want modulo \\(3\\).

### Problem [<span>5</span>{:.deg-sitio-4 .deg-sitio-texto}](#problem5-ireland-1996)
{:.no_toc}

\\(2^p+3^p\\) is not a square, and use the fact that \\(v_5(2^p+3^p)=\\) \\(1+v_5(p) \le 2\\).

### Problem [<span>8</span>{:.deg-sitio-5 .deg-sitio-texto}](#problem8)
{:.no_toc}

Consider two cases: \\(p=2\\) and \\(p\\) is an odd prime. The latter does not give any solutions.

### Problem [<span>9</span>{:.deg-sitio-6 .deg-sitio-texto}](#problem9)
{:.no_toc}

\\((n,m)=(2,1)\\) is a solution. In other cases, show that \\(n\\) is an odd prime and \\(m\\) is even. The other solution is \\((n,m)=(5,2)\\).

### Problem [<span>12</span>{:.deg-sitio-7 .deg-sitio-texto}](#problem12-imo-shortlist-1991)
{:.no_toc}

Answer: \\(\max(k)=1991\\).

### Problem [<span>13</span>{:.deg-sitio-8 .deg-sitio-texto}](#problem13)
{:.no_toc}

Take any odd prime \\(p\\) such that \\(p\|a−1\\). It’s clear that \\(p^2\|a^{a−1}−1\\).

### Problem [<span>14</span>{:.deg-sitio-9 .deg-sitio-texto}](#problem14-czech-slovakia-1996)
{:.no_toc}

Answer: \\((p,x,y)=(2, 1, 1),\\) \\((3, 2, 1)\\).

### Problem [<span>18</span>{:.deg-sitio-10 .deg-sitio-texto}](#problem18)
{:.no_toc}

Let \\(p−1=2^sm\\) and show that \\(v_p(2^{s−1}m)=0\\). The maximum of \\(k\\) is \\(1\\).

### Problem [<span>19</span>{:.deg-sitio-11 .deg-sitio-texto}](#problem19)
{:.no_toc}

Try to prove **Problem [<span>15</span>{:.deg-sitio-12 .deg-sitio-texto}](#problem15)** first.

### Problem [<span>20</span>{:.deg-sitio-11 .deg-sitio-texto}](#problem20-mosp-2001)
{:.no_toc}

Show that \\(p=2\\) and \\(r\\) is an even positive integer.

### Problem [<span>22</span>{:.deg-sitio-10 .deg-sitio-texto}](#problem22-romanian-junior-balkan-tst-2008)
{:.no_toc}

If \\(p\|a\\), \\(p\|b\\), then \\(p^3\|a^3+b^3\\). Otherwise **LTE** applies and \\(v_p(a+b)=\\) \\(v_p(a^3+b^3)\ge 2\\).

### Problem [<span>24</span>{:.deg-sitio-9 .deg-sitio-texto}](#problem24-imo-1990)
{:.no_toc}

The answer is \\(n=1\\) or \\(n=3\\).

### Problem [<span>26</span>{:.deg-sitio-8 .deg-sitio-texto}](#problem26)
{:.no_toc}

Answer: \\((p,q)=(3,3),(3,13)\\).

### Problem [<span>27</span>{:.deg-sitio-7 .deg-sitio-texto}](#problem27)
{:.no_toc}

If \\(n\\) is odd, then \\(a=1\\). If \\(n\\) is even, then \\(a=v_2(5^n−3^n)=\\) \\(v_2(5−3)+v_2(5+3)+v_2(n)−1=\\) \\(3+v_2(n)\\). But, clearly, \\(b\ge v_2(n)\\).

### Problem [<span>30</span>{:.deg-sitio-6 .deg-sitio-texto}](#problem30-romania-tst-1994)
{:.no_toc}

\\(n\|(n−1)^n+1\\), so for every \\(p\|(n−1)^n+1\\), we have

$$\begin{align*}
v_p\left((n−1)^{(n−1)^n+1}+1\right)&= v_p((n − 1)^n+1)+v_p\left(\frac{(n−1)^{n+1}+1}{n}\right)\\
&=2v_p((n−1)^n+1)−v_p(n)
\end{align*}
$${:.math}

which completes the proof.

### Problem [<span>31</span>{:.deg-sitio-5 .deg-sitio-texto}](#problem31)
{:.no_toc}

\\(n\le v_2(3^n−1)\le 3+v_2(n)\\), so \\(n\le 4\\).

### Problem [<span>33</span>{:.deg-sitio-4 .deg-sitio-texto}](#problem33)
{:.no_toc}

\\(a\\) must be odd (otherwise the numerator is \\(2\;\bmod\;3\\)). Then \\(a\le v_3(5^a+1)=\\) \\(1+v_3(a)\\) giving \\(a=1\\) as the only solution.

<div> </div>
{:.salto .no-mostrar}

## Original sources

See Amir's website [<span>here!</span>{:.deg-sitio-1 .deg-sitio-texto}](https://parvardi.com)<br/>
<span>https://parvardi.com</span>{:.deg-sitio-1 .deg-sitio-texto .no-mostrar}

Download the original [<span>PDF file (211 KB)</span>{:.deg-sitio-2 .deg-sitio-texto}](https://services.artofproblemsolving.com/download.php?id=YXR0YWNobWVudHMvNS8wLzgyODNhOGNhOWQ4OWM1NDk5NTY1MGQyNWVlYWNlMzE1OGYxMDM0&rn=TGlmdGluZyBUaGUgRXhwb25lbnQgLSBWZXJzaW9uIDYucGRm), published on April 2011.<br/>
<span>https://services.artofproblemsolving.com/download.php?id=YXR0YWNobWVudHMvNS8wLzgyODNhOGNhOWQ4OWM1NDk5NTY1MGQyNWVlYWNlMzE1OGYxMDM0&rn=TGlmdGluZyBUaGUgRXhwb25lbnQgLSBWZXJzaW9uIDYucGRm</span>{:.deg-sitio-2 .deg-sitio-texto .no-mostrar}

## References

**<span>1.</span>{:.deg-sitio-3 .deg-sitio-texto}**&#x2007;Sepehr Ghazi Nezami, **[<span>Leme Do Khat</span>{:.deg-sitio-3 .deg-sitio-texto}](http://imo09.blogfa.com/page/2khat.aspx)** (in English: *Lifting The Exponent
Lemma*), published on October 2009.

**<span>2.</span>{:.deg-sitio-4 .deg-sitio-texto}**&#x2007;Kurt Hensel, **[<span>Hensel’s lemma</span>{:.deg-sitio-4 .deg-sitio-texto}](http://en.wikipedia.org/wiki/Hensel's_lemma)**, WikiPedia.

**<span>3.</span>{:.deg-sitio-5 .deg-sitio-texto}**&#x2007;Santiago Cuellar, Jose Alejandro Samper, *A nice and tricky lemma (lifting the exponent)*, Mathematical Reflections 3 - 2007.

**<span>4.</span>{:.deg-sitio-6 .deg-sitio-texto}**&#x2007;Amir Hossein Parvardi, Fedja et al., **[<span>AoPS topic #393335</span>{:.deg-sitio-6 .deg-sitio-texto}](http://www.artofproblemsolving.com/Forum/viewtopic.php?t=393335)**, *Lifting The Exponent Lemma (Containing PDF file)*.

**<span>5.</span>{:.deg-sitio-7 .deg-sitio-texto}**&#x2007;Orlando Doehring et al., **[<span>AoPS topic #214717</span>{:.deg-sitio-7 .deg-sitio-texto}](https://artofproblemsolving.com/community/c6h214717)**, *Number \\(\bmod\;(f(m+n), p)=0\\) iff \\(\bmod\;(f(m) + f(n), p)=0\\)*.

**<span>6.</span>{:.deg-sitio-8 .deg-sitio-texto}**&#x2007;Fang-jh et al., **[<span>AoPS topic #268964</span>{:.deg-sitio-8 .deg-sitio-texto}](https://artofproblemsolving.com/community/h268964)**, *China TST, Quiz 6, Problem 1*.

**<span>7.</span>{:.deg-sitio-9 .deg-sitio-texto}**&#x2007;Valentin Vornicu et al., **[<span>AoPS topic #57607</span>{:.deg-sitio-9 .deg-sitio-texto}](https://artofproblemsolving.com/community/h268964)**, *exactly 2000 prime divisors
(IMO 2000 P5)*.

**<span>8.</span>{:.deg-sitio-10 .deg-sitio-texto}**&#x2007;Orlando Doehring et al., **[<span>AoPS topic #220915</span>{:.deg-sitio-10 .deg-sitio-texto}](https://artofproblemsolving.com/community/c6h220915)**, *Highest degree for 3-layer
power tower*.

**<span>9.</span>{:.deg-sitio-11 .deg-sitio-texto}**&#x2007;Sorush Oraki, Johan Gunardi, **[<span>AoPS topic #368210</span>{:.deg-sitio-11 .deg-sitio-texto}](https://artofproblemsolving.com/community/h368210)**, *Prove that \\(a=1\\) if
\\(4(a^n+1)\\) is a cube for all \\(n\\)*.
