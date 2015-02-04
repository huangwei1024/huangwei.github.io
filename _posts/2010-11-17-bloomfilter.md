---
layout: post
title: Bloom Filter ԭ����Ӧ��
categories: algorithm
tags:  bloom filter
description: Bloom Filter��һ�ּ򵥵Ľ�ʡ�ռ������������ݽṹ��֧���û���ѯ�ļ��ϡ�
keywords: bloom filter, hash
---

## ����
----------

Bloom Filter��һ�ּ򵥵Ľ�ʡ�ռ������������ݽṹ��֧���û���ѯ�ļ��ϡ�һ������ʹ��STL��`std::set`, `stdext::hash_set`��`std::set`���ú����ʵ�ֵģ�`stdext::hash_set`����Ͱʽ��ϣ�������������ݽṹ��������Ҫ����ԭʼ������Ϣ�����������ϴ�ʱ���ڴ�ͻ��Ǹ����⡣���Ӧ�ó������������һ�����ʵ����У��Ҳ���Ҫ������������е�����ʱ��Bloom Filter�ǺܺõĽṹ��

### �ŵ�
- ��ѯ����ʮ�ָ�Ч��
- ��ʡ�ռ䡣
- ������չ�ɲ��С�
- ���ϼ��㷽�㡣
- ����ʵ�ַ��㡣
- �����еĸ��ʣ�������False Position��
- �޷���ȡ�����е�Ԫ�����ݡ�
- ��֧��ɾ��������

### ȱ��
- �����еĸ��ʣ�������False Position��
- �޷���ȡ�����е�Ԫ�����ݡ�
- ��֧��ɾ��������
 
## ����
----------

Bloom Filter��һ����mλ��λ���飬��ʼȫΪ0������k�����Զ����Ĺ�ϣ������

![ͼ1]({{ site.cdn.link }}/static/img/bloom1.jpg)
ͼ1

### ��Ӳ���

ÿ��Ԫ�أ���k����ϣ�����������СΪk�Ĺ�ϣ���� $  \left (H_{1},H_{2}\cdots ,H_{k} \right ) $
�����������ÿ����ϣֵ��Ӧ��λ����Ϊ1��ʱ�临�Ӷ�Ϊ $ k\cdot O(F_{H}) $��һ���ַ�����ϣ������ʱ�临�Ӷ�Ҳ����$ O(n) $��

### ��ѯ����

��������ƣ��ȼ������ϣ���������ÿ����ϣֵ��Ӧ��λ��Ϊ1�����Ԫ�ش��ڡ�ʱ�临�Ӷ�����Ӳ�����ͬ��

### ʾ��
ͼ2��ʾm=16��k=2��Bloom Filter�� �� �Ĺ�ϣֵ�ֱ�Ϊ(3, 6)��(10, 3)��

![ͼ2]({{ site.cdn.link }}/static/img/bloom2.jpg)
ͼ2

## False Position
----------

���ĳԪ�ز���Bloom Filter�У����������й�ϣֵ��λ�þ�����Ϊ1�������������False Position��Ҳ�������С�
����ʾ�������£�

![ͼ3]({{ site.cdn.link }}/static/img/bloom3.jpg)
ͼ3

���������ʵ�͹�ϣ���еĳ�ͻ����ͬ�ĵ�����ϣ���п���ʹ�ÿ�ɢ�кͱ�ɢ�еķ�������Bloom Filter����������������������������������еķ������ʡ�

### ����
����ϣ������ܵó����½��ۣ�

|������	|����	|����	|����|
|---------------------------|
|��ϣ��������	|K	|  ���ٵĹ�ϣֵ����|����ļ���|
|||����False Position�ĸ���|λֵ0����|
|Bloom Filter ��С	|M	|���ٵ��ڴ�|������ڴ�|
|||����False Position�ĸ���|���͸���|
|Ԫ������|	N|  ����False Position�ĸ���| ���Ӹ���|

False Position�ĸ���Ϊ $ F=(1-e^{-\frac{kn}{m}})^{k} $��
����m��n��֪��Ϊ����С��False Position���� $ k=\left [ \ln 2\cdot \frac{m}{n} \right ] $��
����

![ͼ4]({{ site.cdn.link }}/static/img/bloom4.jpg)
ͼ4

## ��չ
----------

### Counter Bloom Filter

Bloom Filter�и�ȱ�㣬���ǲ�֧��ɾ����������Ϊ����֪��ĳһ��λ��������Щ�����������ǿ��Ը�Bloom Filter���ϼ����������ʱ���Ӽ�������ɾ��ʱ���ټ�������
��������Filter��Ҫ���Ǹ��ӵļ�������С������ͬ��Ԫ�ض�β���Ļ���������λ�����ٵ�����£��ͻ����������⡣����Լ�������������ֵ�Ļ����ᵼ��Cache Miss������ĳЩӦ����˵���Ⲣ����ʲô���⣬��Web Sharing��
### Compressed Bloom Filter

Ϊ�����ڷ�����֮������ͨ�����紫��Bloom Filter�������з������������Bloom Filter֮�󣬵õ�һЩʵ�ʲ���������½���ѹ����
��Ԫ��ȫ�������Bloom Filter�������ܵõ���ʵ�Ŀռ�ʹ���ʣ������ֵ���빫ʽ�����һ����mС��ֵ�����¹���Bloom Filter����ԭ�ȵĹ�ϣֵ�������ദ���������ʲ��������£�ʹ�����ڴ��С�����ʡ�

##Ӧ��
-------------

###���ٲ�ѯ

������һЩkey-value�洢ϵͳ����values����Ӳ��ʱ����ѯ���Ǽ���ʱ���¡�
��Storage�����ݶ�����Filter����Filter�в�ѯ��������ʱ���ǾͲ���ҪȥStorage��ѯ�ˡ�
��False Position����ʱ��ֻ�ǻᵼ��һ�ζ����Storage��ѯ��

![ͼ5]({{ site.cdn.link }}/static/img/bloom5.jpg)
ͼ5

- Google��BigTableҲʹ����Bloom Filter���Լ��ٲ����ڵ��л����ڴ����ϵĲ�ѯ�������������ݿ�Ĳ�ѯ���������ܡ�
- ��Internet Cache Protocol�е�Proxy-Cache�ܶ඼��ʹ��Bloom Filter�洢URLs�����˸�Ч�Ĳ�ѯ�⣬���ܷܺ���ô��佻��Cache��Ϣ��

### ����Ӧ��

-  P2P�����в�����Դ���������Զ�ÿ������ͨ·����Bloom Filter��������ʱ����ѡ���ͨ·���ʡ�
-  �㲥��Ϣʱ�����Լ��ĳ��IP�Ƿ��ѷ�����
-  ���㲥��Ϣ���Ļ�·����Bloom Filter�����ڰ��ÿ���ڵ㽫�Լ������Bloom Filter��
-  ��Ϣ���й���ʹ��Counter Bloom Filter������Ϣ������

### �����ʼ���ַ����

������Google�ڰ屨�����ӡ�
�����ף�QQ�����Ĺ��ڵ����ʼ���email���ṩ�̣�������Ҫ�������Է��������ʼ����ˣ�spamer���������ʼ���
һ���취���Ǽ�¼����Щ�������ʼ��� email ��ַ��������Щ�����߲�ͣ����ע���µĵ�ַ��ȫ������˵Ҳ�м�ʮ�ڸ��������ʼ��ĵ�ַ�������Ƕ�����������Ҫ�����������������
����ù�ϣ��ÿ�洢һ�ڸ� email ��ַ������Ҫ 1.6GB ���ڴ棨�ù�ϣ��ʵ�ֵľ���취�ǽ�ÿһ�� email ��ַ��Ӧ��һ�����ֽڵ���Ϣָ�ƣ�Ȼ����Щ��Ϣָ�ƴ����ϣ�����ڹ�ϣ��Ĵ洢Ч��һ��ֻ�� 50%�����һ�� email ��ַ��Ҫռ��ʮ�����ֽڡ�һ�ڸ���ַ��ԼҪ 1.6GB�� ��ʮ�����ֽڵ��ڴ棩����˴�����ʮ�ڸ��ʼ���ַ������Ҫ�ϰ� GB ���ڴ档
��Bloom Filterֻ��Ҫ��ϣ�� 1/8 �� 1/4 �Ĵ�С���ܽ��ͬ�������⡣
Bloom Filter������©���κ�һ���ں������еĿ��ɵ�ַ���������������⣬�����Ĳ��Ȱ취���ڽ���һ��С�İ��������洢��Щ���ܱ����е��ʼ���ַ��

## ����
----
[1]  Bloom filter; http://en.wikipedia.org/wiki/Bloom_filter
[2]  Summary Cache: A Scalable Wide-Area Web Cache Sharing Protocol;http://pages.cs.wisc.edu/~cao/papers/summary-cache/
[3]      Network Applications of Bloom Filters: A Survey;http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.127.9672&rep=rep1&type=pdf
[4]      An Examination of Bloom Filters and their Applications;http://cs.unc.edu/~fabian/courses/CS600.624/slides/bloomslides.pdf
[5]      ��ѧ֮��ϵ�ж�ʮһ �� ��¡��������Bloom Filter��;http://www.google.com.hk/ggblog/googlechinablog/2007/07/bloom-filter_7469.html