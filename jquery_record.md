
# 一些记录

```js
    // 代替window.onload() 等页面加载完再运行
    $(() => {
      console.log(666);
    })
```

```js
    // 获取元素 执行操作
    $('button').click(() => {
      $('.box').slideToggle()
    })
```

```js
    // jq构造函数 $
    console.log($);
    // 获取的不是DOM对象 而是jq对象
    console.log($('ul'));
```

```js
    // 原生转为jq
    let lis = document.querySelectorAll('li')
    console.log(lis);
    let jqLis = $(lis)
    console.log(jqLis);
```

```js
    // jq转为原生
    let ul = $('ul')[0]
    let getUl = $('ul').get(0)
    console.log(ul);
    console.log(getUl);
```

```js
    // 后台返回个字符串 转为jq对象
    let html = `<div>你好</div>`
    console.log($(html));
```

```js
    let ul = $('ul')
    let lis = $('li')
    // equal等于的意思 找第几个元素
    let li2 = lis.eq(1)
    
    // 兄弟选择器(不包括自己)
    console.log(li2.siblings());
    console.log(li2.siblings('#li3'));
    
    // 父选择器
    console.log(ul.parent());
    // 所有上级 直到html
    console.log(ul.parents());
    
    // 筛选孩子
    console.log(ul.children());
    console.log(ul.children('#li3'));
    
    // 寻找后代
    console.log(ul.find('#li3'));
```








