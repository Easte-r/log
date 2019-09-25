## 由于最近做的项目，组件化比较少，所以对于Typescript 里  Vue 的 Prop Watch 使用不多，今天遇到了一些问题。

```
@Prop()
public role: string;  // 不给默认值会有警告，增加! 向程序表示，此处一定不会为空
```

```
由于prop只是可读。所以用在子组件的双向绑定是不可行的，命令行会有警告
@Porp()
public role!: string;

public roleTemp!: string;

@Watch('role')
watchRole(newVal: string, oldVal: string) {
  this.role - newVal;
}
通过watch 使得每次prop改变的时候，给roleTemp赋值。roleTemp可以在组件内部维持自己的状态。

```
