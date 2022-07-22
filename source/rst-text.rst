.. _rst-text:

*Welcome!*

**let's learn reStructturedText**

一级标题
********

二级标题
+++++++++

三级级标题
----------

reStructturedText 语法学习
**************************

分隔符上

-----

分隔符下

标注
+++++++++

let's learn label [#f1]_ ! you'll see a footnote [#f2]_ .

.. rubric:: Footnotes 

.. [#f1] 标注的使用
.. [#f2] 这是第二条脚注.


.. _list:

列表
+++++++++

* 无序列表
* 第一项
* 第二项
* 第三项

#. 有序列表
#. 第一项
#. 第二项
#. 第三项


定义列表
    :字段列表: 第一项
how
    :第二项: 第二项


1. 列表嵌套
2. 父列表第一项
3. 父列表第二项

* 子列表第一项
* 子列表第二项

4. 父列表第三项
   
代码
+++++++++

`code`

第一段文本 ::

   代码区块演示
   if(1 == 1){
        $joke = "Life is short, not int.";
    }

代码高亮展示

.. code:: java

    <?java
    if(1 == 1){
        $joke = "Life is short, not int.";
    }
    ?>

:: 

    引用文本

链接
+++++++++

**外部链接**

`Sphinx官网 <http://www.sphinx-doc.org/en/master/>`_

`Sphinx使用教程 <https://dac-tut.readthedocs.io/zh_CN/latest/rst-guide.html>`_

`Markdown基本语法 <https://markdown.com.cn/basic-syntax/emphasis.html>`


**内部链接**

:ref:`list`.

图片
+++++++++

.. image:: images/rst-insert-sphinx.jpg

表格
+++++++++

=====  =====  =======
  A      B    A and B
=====  =====  =======
False  False  False
True   False  False
False  True   False
True   True   True
=====  =====  =======

**单元格换行以及单元格置空**

=====  =====
col 1  col 2
=====  =====
1      Second column of row 1.
2      Second column of row 2.
       Second line of paragraph.
3      - Second column of row 3.

       - Second item in bullet
         list (row 3, column 2).
\      Row 4; column 1 will be empty.
=====  =====

网格表格
--------

网格表格可以自定义表格的边框，更灵活，但绘制相对复杂。构成网格表格的标记有以下几种：

 * “-“用于绘制横线，分隔各行；

 * “=”用于分隔标题与表格主体，但标题可有可无，视情况而定；

 * “|”用于绘制竖线，分隔各列；

 * “+”用在行与列的交界处。
  
+------------------------+------------+----------+----------+
| Header row, column 1   | Header 2   | Header 3 | Header 4 |
+========================+============+==========+==========+
| body row 1, column 1   | column 2   | column 3 | column 4 |
+------------------------+------------+----------+----------+
| body row 2             | Cells may span columns.          |
+------------------------+------------+---------------------+
| body row 3             | Cells may  | - Table cells       |
+------------------------+ span rows. | - contain           |
| body row 4             |            | - body elements.    |
+------------------------+------------+---------------------+
    
列表表格
---------

.. list-table::
    :align: right

    * - 单行代码
      - 代码区块
      - 代码高亮
    * - 简单表格
      - 网格表格
      - 列表表格
    * - 外部链接
      - 内部链接
      - 