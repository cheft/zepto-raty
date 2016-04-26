# zepto-raty
基于Zepto的移动端评分插件，在手机微信、UC等浏览器上测试通过。寻找不到相应的手机端评分插件，因此参照jQuery的评分插件自己实现了这个手机端评分插件。

 ![zepto-raty](https://github.com/chenruchang/zepto-raty/blob/master/image/demo.png)


  var defaults = {
    click: undefined,           //单击回掉函数
    number: 5,                  //默认评分的个数
    numberMax: 10,              //默认评分的最大个数
    path: 'raty/images',        //默认评分图标路径
    readOnly: false,            //是否是只读状态
    size: 'small',              //大小分为：small：16*16像素，normal：32*32像素，large：64*64像素
    score: undefined,           //实际评分的大小
    space: true,                //图标之间是否需要空格
    starOff: 'star-off.png',    //指定没选中状态下的图标
    starOn: 'star-on.png'       //指定选中状态下的图标
  };
  
  var scoreOut;
  
  $('#large').raty({
      number: 5, size: 'large', path: 'raty/images', score: 3, click: function (score) {
          scoreOut = score;
          console.log(scoreOut)
      }
  });

  $('#largeNoSpace').raty({
      number: 5, size: 'large', path: 'raty/images', score: 4, space: false, click: function (score) {
          scoreOut = score;
          console.log(scoreOut)
      }
  });

  $('#normal').raty({
      number: 5, size: 'normal', path: 'raty/images', score: 3, click: function (score) {
          scoreOut = score;
          console.log(scoreOut)
      }
  });

  $('#normalNoSpace').raty({
      number: 5, size: 'normal', path: 'raty/images', score: 4, space: false, click: function (score) {
          scoreOut = score;
          console.log(scoreOut)
      }
  });

  $('#small').raty({
      number: 5, size: 'small', path: 'raty/images', score: 2, click: function (score) {
          scoreOut = score;
          console.log(scoreOut)
      }
  });

  $('#smallNoSpace').raty({
      number: 5, size: 'small', path: 'raty/images', score: 2, space: false, click: function (score) {
          scoreOut = score;
          console.log(scoreOut)
      }
  });