# 小结

## 相关说明

1. 本来计划写两个 carousel 组件，可是最近真的忙晕了，只写了一个（原计划一个使用 js 实现，一个使用 css & animationEnd）
2. 确实有一段时间没写页面了，好在基本看看 api 就能上手
3. 测试用例打了个样，没全部写，希望能理解
4. 如果发现使用 hooks 风格有一丢丢变化，是因为写的时间不同（写页面逻辑时正好是工作日，因此是偶尔下班回来花半个小时到一个小时写）

## 感受

1. hooks 整体上确实偏声明式/函数式风格，有函数式组件的轻量又能有代数效应，在一些逻辑封装上确实能做到高内聚低耦合
2. 一开始设计的时候并没有尝试写 hooks（之前只是有概念，也知道底层原理，但是没有实践），所以在结合封装 Class 时有一点后悔如此设计，好在找到套路后好像还行

暂时就写这么多吧，其实感触确实还挺多的

## 重写思路

1. 核心 hook 定义状态，并提供修改状态方法。
2. dot 作为单独 hook
3. dragger 作为单独 hook

### 核心 hook

- 入参为 carousel 配置
- 出参为 carousel 状态信息 & jump & pause & resume & transitionEnd 方法

### dot hook

- 入参为配置及状态 & jump
- 出参为 getProgress

### dragger hook

- 入参为配置 & pause & resume
- 出参为 events & translate