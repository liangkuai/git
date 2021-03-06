# Git commit message

### 总体结构

```
<type>(<scope>) <subject>

<body>

<footer>
```


#### 1. type

用来说明这次 commit 的类型，

- Feat：新功能
- Fix：修复
- Test：测试相关
- Docs：修改文档
- Refactor：代码重构
- Pref：优化
- Chore：其他修改，比如构建流程，辅助工具

> #### Revert
>
> 还有一种特殊情况，如果这次 commit 是撤销以前的 commit，就必须用 `Revert` 开头，后面跟着被撤销 commit 的 Header。
>
> ```
> Revert: feat: add api xxx
>
> This reverts commit 14a01b53
> ```
>
> body 部分的格式一般是 `This reverts commit SHA-1 hash code`，其中的 `SHA-1 hash code` 是被撤销 commit 的哈希码。


#### 2. scope（可选）`

用来说明 commit 影响的范围，比如数据层、控制层、视图层等等，随项目不同而不同。


#### 3. subject

commit 的简短描述（不超过 50 个字符）


#### 4. body

body 部分是对本次 commit 的详细描述，可以分成多行。应该说明代码变动的动机，以及与以前行为的对比。


#### 5. Footer（可选）

只用于两种情况，

1. 关闭 issue

    ```
    Closes #123, #245, #992
    ```

2. 不兼容的改动

    如果当前代码与上一个版本不兼容，那 Footer 部分就用 `BREAKING CHANGE` 开头，后面是对变动的描述，以及变动理由和迁移方法。

    ```
    BREAKING CHANGE: xxx has changed
    ```


---

### 参考

- [Commit message 和 Change log 编写指南 - 阮一峰的网络日志](https://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html)
