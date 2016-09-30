# GB-canvas-turntable
----

## 简介

适用于移动端的Canvas绘制可配置的转盘抽奖
  

## 使用

### Browser
	
	<link rel="stylesheet" href="css/GB-canvas-turntable.css">
	<script src="js/GB-canvas-turntable.js"></script>


### 普通


	gbTurntable.init({
        id: 'turntable',
        config: function(callback){
            // 获取奖品信息
            callback && callback(['1元红包','2元红包','3元红包','4元红包','5元红包','6元红包']);    
        },
        getPrize: function(callback) {
            // 获取中奖信息
            var num = Math.random() * 6 >>> 0,   //奖品ID
                chances = num;  // 可抽奖次数
                callback && callback([num, chances]);   
        },
        gotBack: function(data) {
            alert('恭喜抽中' + data);
        }
    });







## 感谢他们

演示网页排版来自： [https://github.com/sofish/typo.css](https://github.com/sofish/typo.css)       



## License

[MIT](./LICENSE) © 2016 [givebest](https://github.com/givebest)

 
