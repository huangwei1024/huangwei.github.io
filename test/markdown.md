[��Cmd ������Ⱦ��ɳ��ҳ�棬����˴���д�Լ����ĵ���](https://www.zybuluo.com/mdeditor "��ҵ�������� Cmd ���� Markdown �༭�Ķ���")

# Cmd Markdown �����﷨�ֲ�

��ǩ�� Cmd-Markdown

---

### 1. б��ʹ���

ʹ�� * �� ** ��ʾб��ʹ��塣

ʾ����

���� *б��*������ **����**��

### 2. �ּ�����

ʹ�� === ��ʾһ�����⣬ʹ�� --- ��ʾ�������⡣

ʾ����

```
����һ��һ������
============================

����һ����������
--------------------------------------------------

### ����һ����������
```

��Ҳ����ѡ�������׼Ӿ��ű�ʾ��ͬ����ı��� (H1-H6)�����磺# H1, ## H2, ### H3��#### H4��

### 3. ������

ʹ�� \[����](���ӵ�ַ) Ϊ�������������ӡ�

ʾ����

����ȥ�� [���˲���](http://ghosertblog.github.com) �����ӡ�

### 4. �����б�

ʹ�� *��+��- ��ʾ�����б���

ʾ����

- �����б��� һ
- �����б��� ��
- �����б��� ��

### 5. �����б�

ʹ�����ֺ͵��ʾ�����б���

ʾ����

1. �����б��� һ
2. �����б��� ��
3. �����б��� ��

### 6. ��������

ʹ�� > ��ʾ�������á�

ʾ����

> Ұ���ղ��������紵������

### 7. ���ڴ����

ʹ�� \`����` ��ʾ���ڴ���顣

ʾ����

���������� `html`��

### 8.  �����

ʹ�� �ĸ������ո� ��ʾ����顣

ʾ����

    ����һ������飬����������ĸ����ɼ��Ŀո�

### 9.  ����ͼ��

ʹ�� \!\[����](ͼƬ���ӵ�ַ) ����ͼ��

ʾ����

![�ҵ�ͷ��](https://www.zybuluo.com/static/img/my_head.jpg)

# Cmd Markdown �߽��﷨�ֲ�

### 1. ����Ŀ¼

�ڶ�������д `[TOC]` ����ʾȫ�����ݵ�Ŀ¼�ṹ��

[TOC]

### 2. ��ǩ����

�ڱ༭�������е�����λ���������´�����ĸ��ǩ��

��ǩ�� ��ѧ Ӣ�� Markdown

����

Tags�� ��ѧ Ӣ�� Markdown

### 3. ɾ����

ʹ�� ~~ ��ʾɾ���ߡ�

~~����һ�δ�����ı���~~

### 4. ע��

ʹ�� [^keyword] ��ʾע�š�

����һ��ע��[^footnote]��������

���ǵڶ���ע��[^footnote2]��������

### 5. LaTeX ��ʽ

$ ��ʾ���ڹ�ʽ�� 

�����غ㷽�̿�����һ���ܼ��ķ���ʽ $E=mc^2$ �����

$$ ��ʾ���й�ʽ��

$$\sum_{i=1}^n a_i=0$$

$$f(x_1,x_x,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2 $$

$$\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}$$

���� [MathJax](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference) �ο�����ʹ�÷�����

### 6. ��ǿ�Ĵ����

֧����ʮһ�ֱ�����Ե��﷨��������ʾ���к���ʾ��

�Ǵ���ʾ����

```
$ sudo apt-get install vim-gnome
```

Python ʾ����

```python
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
```

JavaScript ʾ����

``` javascript
/**
* nth element in the fibonacci series.
* @param n >= 0
* @return the nth element, >= 0.
*/
function fib(n) {
  var a = 1, b = 1;
  var tmp;
  while (--n >= 0) {
    tmp = a;
    a += b;
    b = tmp;
  }
  return a;
}

document.write(fib(10));
```

### 7. ����ͼ

#### ʾ��

```flow
st=>start: Start:>https://www.zybuluo.com
io=>inputoutput: verification
op=>operation: Your Operation
cond=>condition: Yes or No?
sub=>subroutine: Your Subroutine
e=>end

st->io->op->cond
cond(yes)->e
cond(no)->sub->io
```

#### �����﷨�ο���[����ͼ�﷨�ο�](http://adrai.github.io/flowchart.js/)

### 8. ����ͼ

#### ʾ�� 1

```seq
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```

#### ʾ�� 2

```seq
Title: Here is a title
A->B: Normal line
B-->C: Dashed line
C->>D: Open arrow
D-->>A: Dashed open arrow
```

#### �����﷨�ο���[����ͼ�﷨�ο�](http://bramp.github.io/js-sequence-diagrams/)

### 9. ����֧��

ʾ����

| ��Ŀ        | �۸�   |  ����  |
| --------   | -----:  | :----:  |
| �����     | $1600 |   5     |
| �ֻ�        |   $12   |   12   |
| ����        |    $1    |  234  |


### 10. �������б�

���� 1
:   ���� 1�������һ���ɼ���ð�ź��ĸ����ɼ��Ŀո�

����� 2
:   ���Ǵ����Ķ��壨�����һ���ɼ���ð�ź��ĸ����ɼ��Ŀո�

        ����飨����а˸����ɼ��Ŀո�

### 11. Html ��ǩ

��վ֧���� Markdown �﷨��Ƕ�� Html ��ǩ��Ʃ�磬������� Html дһ���ݿ����еı���

    <table>
        <tr>
            <th rowspan="2">ֵ����Ա</th>
            <th>����һ</th>
            <th>���ڶ�</th>
            <th>������</th>
        </tr>
        <tr>
            <td>��ǿ</td>
            <td>����</td>
            <td>��ƽ</td>
        </tr>
    </table>


<table>
    <tr>
        <th rowspan="2">ֵ����Ա</th>
        <th>����һ</th>
        <th>���ڶ�</th>
        <th>������</th>
    </tr>
    <tr>
        <td>��ǿ</td>
        <td>����</td>
        <td>��ƽ</td>
    </tr>
</table>

### 12. ��Ƕͼ��

��վ��ͼ��ϵͳ���⿪�ţ����ĵ�������

    <i class="icon-weibo"></i>

����ʾ΢����ͼ�꣺ <i class="icon-weibo icon-2x"></i>

�滻 ���� `i ��ǩ` �ڵ� `icon-weibo` ����ʾ��ͬ��ͼ�꣬���磺

    <i class="icon-renren"></i>

����ʾ���˵�ͼ�꣺ <i class="icon-renren icon-2x"></i>

�����ͼ����淨���Բο� [font-awesome](http://fortawesome.github.io/Font-Awesome/3.2.1/icons/) �ٷ���վ��


[^footnote]: ����һ�� *ע��* �� **�ı�**��

[^footnote2]: ������һ�� *ע��* �� **�ı�**��
