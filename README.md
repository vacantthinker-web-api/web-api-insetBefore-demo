# web-api-insetBefore-demo

```javascript

    document.getElementById('button1').addEventListener('click', function () {
        let parentElement = document.getElementById('nav');
        let elementB = document.getElementById('b');

        // 初始为A, B, C
        // 点击button1 --> A, C, B
        // null, 在父元素队尾加一个
        parentElement.insertBefore(elementB, null) // referenceNode为null, 意味在父元素队尾插入
    })

    document.getElementById('button2').addEventListener('click', function () {
        let parentElement = document.getElementById('nav');
        let elementB = document.getElementById('b');

        let elementLi = document.createElement('li');
        elementLi.id = 'd'
        elementLi.innerText = 'D'

        let refChild = elementB.nextSibling;
        // 初始为 A, B, C
        // nextSibling 紧挨着B的下一个兄弟[同级别]元素
        // 如果为C, --> A, B, D, C
        // 在C前面加一个
        
        // 如果为null, --> A, C, B, D
        // 在父元素队尾加一个
        parentElement.insertBefore(elementLi, refChild)

    })

```