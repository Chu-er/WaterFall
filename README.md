# WaterFall


基本设置
相机 （后处理相机） :需要一个专门渲染水珠的相机   ，1。cullmask 设置成 Water   , 
2.同理水珠的layer设置成 Water 
3.由于主相机不渲染水珠 ，需要过滤掉Water 层，
4.注意相机的size 要和主相机一致  还有Transform

PS:性能考虑 不用的时候可以禁用相机  ， 


全局的rawImage:尺寸要和Canvas 宽高 一样  ，并且位置在中心  提前设好锚点为铺满就行，  
作用就是接收 后处理相机的targetTexture,通过着色器修正他的颜色， 配合倒水需要注意层级关系

杯子： 用edgeCollider2D  包围    

杯子内水珠： 用精灵 添加刚体  dynamic  当然一开始不倒水的时候可以关闭 模拟   减小物理开销（珠子比较多的时候）  


碗里的水 设置 着色器的 baseheight 就可

其余参考具体代码





