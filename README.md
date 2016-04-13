# rex-slide
轮播插件(带小图, 大图懒加载)

## HTML结构
```html
    <div class="rex-slide" id="slide">
        <div class="showBox">
            <ul>
                <li>
                    <img data-url="images/1.jpg" src="images/default.jpg" >
                </li>
            </ul>
        </div>
        <div class="listBox">
            <ul>
                <li class="on">
                    <img src="images/1.jpg">
                </li>
            </ul>
        </div>
        <a class="btn btn-prev" href="javascript:;"></a>
        <a class="btn btn-next" href="javascript:;"></a>
    </div>
```

## JS代码
```html
    <script type="text/javascript" src="js/jquery-1.12.3.min.js"></script>
    <script type="text/javascript" src="js/rex-slide.js"></script>
    <script>

        var slide = $.rexSlide("#slide",{
            "bWidth" : 600, //大图宽度
            "sWidth" : 130, //小图宽度+右边距
            "show" : 4, //小图显示个数
			"lock" : 1, //小图锁定位置
        	"autoplay" : 0 //自动轮播的时间间隔: 0代表不自动轮播, 默认4000;
        })
    </script>
```

## API接口
```javascript
    //上一张
    slide.prev();

    //下一张
    slide.next();

    //去到指定位置
    slide.goto(2);
```
