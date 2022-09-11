# 数据结构
## 顺序表——线性表的顺序存储
```
#define MaxSize = 100
typedef struct{
    ElemType data;
    int length;
}Sqlist;
```
### 算法1
    从顺序表删除具有最小值的元素（假设唯一）并由函数返回被删元素的值。空出位置由最后一个元素填补，若顺序表为空，则显示出错误信息并退出运行。
```
bool Del_min(Sqlist &L){
    if(L.length==0) return false;
    int pos=0; //pos指向最小值的坐标
    for(int i=0;i<L.length;i++){
        if(L.data[i]<L.data[pos]){
            pos=i;
        }
    }
    L.data[pos]=L.data[L.length-1];
    return ture;
}

//标准答案

```
