10.21日测


1.将两个字符利用字符串对象的方法变成一个字符,显示在页面id为h1的元素中
答:         
        var a = '123';
        var b = '456';
        console.log(a.concat(b));
        c = a.concat();
        var d = document.getElementById('h1');
        d.innerHTML = c;

2.一个富豪想存87万,给理财顾问写了87w,请自动生成存储870000的方法,显示在页面id为h2的元素中
答:    
        var int = document.getElementById('int');
        var btn = document.getElementById('btn');
        var mydiv = document.getElementById('mydiv');
        btn.onclick = function () {
            var num = int.value;
            int.value = String;
            if (num.length > 8) {
                alert('存款不符');
            } else {

                var hh = num.padEnd(6, '0');
                alert('存款为' + hh);
                mydiv.innerHTML = hh;
            }
        }

3.一个数字79387.348的工程款,保留两位小数存入,显示在页面id为h3的元素中
答:
        var h3 = document.getElementById('h3');
        var num = 79387.348;
        num = num.toFixed(2);
        h3.innerHTML = num;

4.一张图片是一个相对路径img/head/,icon/1.jpg,我只需要拿到它的文件夹后显示在页面id为h4的元素中
答:     
         var href = 'img/head/icon/1.jpg';
        document.getElementById('h4').innerText = href.substring(0, 14);

5.用户输入验证码,无论大小写输入都会正确的方法,显示在页面id为h5的元素中
答:
        
         var a = prompt("请输入验证码");
        if (a.toLocaleLowerCase == 'sma' || a.toLocaleUpperCase == 'SMA') {
            var h4 = document.getElementById('h4');
            h4.innerHTML = a;
        } else {
            h4.innerHTML = a;
        }