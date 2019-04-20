- 实现四周向中心聚拢动态效果：如下图所示:
<img src='https://note.youdao.com/yws/api/personal/file/94F92B3E5B8347C7A57545B675C52D67?method=download&shareKey=5af66a38c757518f56c2bf27b21a903d' />

- 两种实现方案：
  - before与after两个伪元素
  使用before与after创建两个伪元素,通过它们的border来分别实现遮住图片的左上、右下部分，达到图片动态向中心收缩效果。
  <b>注意：</b>
     1.border-box的默认属性content-box属性的时候，元素的尺寸问题，以及border的延申方向
     2.右下部分图片的遮住是通过移动after伪元素，让它的border遮住图片的右下部分，此时为了避免after的的左下部分遮住其他元素，需要隐藏左下边框，可以设置颜色透明




- before加上设置before的boxsizing为border-box:
   - 了解box-sizing设置为border-box之后盒子的尺寸问题。
   - 这种方案实现比上面的方案实现更方便，一个是不用创建after伪元素，也不用考虑after元素移动带来的问题。直接设置before的box-sizing属性为border-box，再给它加上边框的时候边框是向内部延申的，维持了盒子的尺寸是设置的width

- 关于before与after的相关语法知识
[link](https://segmentfault.com/a/1190000003710082)
- 关于box-sizing属性
[link](http://note.youdao.com/noteshare?id=e6c263314bfd7204ca4f60b1fb92fa8c&sub=3B0162C439674112B02F2B8B5D9177D6)
