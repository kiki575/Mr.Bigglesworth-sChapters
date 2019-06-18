### JavaScript DOM部分 学习总结

* 空格文本也会生成节点：

  ~~~html
  <ul>
  		<li>item1</li>
  		<li>item1</li>
  		<li>item1</li>
  </ul>
  ~~~

  ​

以上代码输出**ul**的子节点数是7，**ul**与**li**之间，**li**与**li**之间的空行会生成节点，但是连续空多行还是生成一个节点。

* 关于注释节点：

  ~~~html
  <!DOCTYPE html>
  <!--shit-->
  <html>...</html>
  <!--asshole-->
  ~~~

  JS代码:

  ~~~javascript
  var a = document.a.length);
  console.log(document.children.length);
  console.log(document.children[0]);
  console.log(a[3]);
  ~~~

  在**Chrome** 中**childNodes.length** 返回的是3，**Firefox**和**IE**返回的是4。

  **Chrome**忽略掉了**html**后面的注释，而**Firfox**和**IE**保留了。

  **children**只有**html**一个元素，长度都是返回1，**IE**中没有这个属性。

  **注释和文本节点都是没有子节点的！！**

* **DOM**扩展：

  **jQuery**的核心就是通过**CSS**选择符查询**DOM**文档取得元素的引用，从而抛开了**getElementById**()和**getElementByTagName()。** **querySelectors**()方法，参数是一个**css**选择符，返回值是一个元素，**matchesSelector**()方法返回一个布尔值。

  **getElementsByClassName()** 是**HTML5**扩展的方法。

  ​

  ​

  ​

  ​