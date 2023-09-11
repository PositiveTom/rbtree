原项目地址：https://github.com/exsandebest/Trees

## 依赖
```
Qt5
```


## 修改:
1. 把qmake编译器改成了make编译器, 去除了QtCreator依赖
2. 手动链接按钮类和槽函数

## 编译 mac / linux
```bash
mkdir build
cd build
cmake ..
make -j12
./test
```

## Interface - examples
![RedBlack Tree](https://raw.githubusercontent.com/exsandebest/Trees/master/examples/screenshots/RedBlack_Tree.png)
