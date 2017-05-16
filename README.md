d3官方文档：https://d3js.org/


一、深入理解Updata、Enter、Exit
地址：http://wiki.jikexueyuan.com/project/d3wiki/enterexit.html
1、有数据，而没有足够图形元素的时候:

svg.selectAll("rect")   //选择svg内所有的矩形
      .data(dataset)      //绑定数组
      .enter()            //指定选择集的enter部分
      .append("rect")     //添加足够数量的矩形元素
      
2、如果数组为 [3, 6, 9, 12, 15]，将此数组绑定到三个 p 元素的选择集上。
可以想象，会有两个数据没有元素与之对应，这时候 D3 会建立两个空的元素与数据对应，这
一部分就称为 Enter。而有元素与数据对应的部分称为 Update。如果数组为 [3]，则会有两
个元素没有数据绑定，那么没有数据绑定的部分被称为 Exit。示意图如下所示。 
![image](http://github.com/slh8060/D3Demo/raw/master/images/11.png)





     
