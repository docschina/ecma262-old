
ECMAScript 中文
====

## 关于该仓库

该仓库包含[ECMAScript®语言规范](https://github.com/tc39/ecma262)当前草案(包含stage 2 - stage 4)的中文翻译，你可以在一下网站进行浏览。
- [英文](https://tc39.github.io/ecma262/)
- [中文](https://ecma262.docschina.org/)

> 中文内容为校对过得翻译内容，如有疑问请在相应的 issue 中留言。

## 约定
- **LN** 表示文档行号
- **issues** 表示github的issues菜单
- **pull request** 表示github的pull request功能
- 排版规范我们遵从 [中文文案排版指北](https://github.com/mzlogin/chinese-copywriting-guidelines/blob/Simplified/README.md)，不规范的翻译 reviewer 有义务让翻译者重译

### 不翻译
- 规范类型 规范类型包括Reference, List, Completion, Property Descriptor, Lexical Environment, Environment Record, 以及 Data Block。
- 语言类型 ECMAScript语言类型有Undefined, Null, Boolean, String, Symbol, Number, Object。
- 算法 算法是用来精确地指定 ECMAScript 语言结构所需的语义。
## 贡献

欢迎小伙伴们参与 ECMAScript 规范的翻译，你可以选择参与翻译，校对，审校中自己喜欢的部分贡献自己的一份热情。让我们一起为 ECMAScript 社区贡献自己的一份力。

### 参与翻译

点击右上角 “fork” 按钮，fork 此仓库到你的 github 仓库，然后在本地 pull 远程仓库即可对项目中未翻译部分进行翻译工作了。

如果你不知道哪些内容还在等待着被翻译，那你可以在 issues 中找到 [待翻译](https://github.com/docschina/ecma262/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aopen+label%3A%E5%BE%85%E7%BF%BB%E8%AF%91)的章节然后 @realywithoutname 进行修改该 issue 的状态，并把你加入到我们的翻译团队中。

现在你已经确认了翻译的 issue，你需要在你的项目根目录基于远程 translated 分支创建一个新分支，然后在 `translated` 文件夹的 `issues-[ISSUE ID].html` 文件中进行对原文进行翻译。

~~~ bash
  $ git checkout -b translate/issues-[ISSUE ID] origin/translated
~~~

翻译完成以后，你还需要用译文去替换 `spec.html` 文件中相应的英文原文，然后执行 `npm run build`。记得要在浏览器中打开 `out/index.html` 预览翻译后的效果和预期的效果一致哦。

一切都 OK 的话，请丢弃 `spec.html` 文件更改内容，并提交译文，建议 `commit message` 写为 **translated：[LN - LN] issue #ISSUE ID** (为了审校时方便替换)。

~~~ bash
  $ git checkout spec.html
  $ git commit -am 'translated: [LN - LN] issue #ISSUE ID'
~~~

然后你就可以 push 到你的远程仓库，提交 pull request 了。

~~~ bash
  $ git push origin translate/issues-[ISSUE ID]
~~~

最后你还需要关注相应 pull request，校对者会在此 pull request 提交 review 意见，你需要根据大家的意见进行修改并提交你修改的内容(不需要再次发起 pull request)，直到提交被合并，对于长时间（**距离`issue`中最后的评论时间超过三天**）未被接受的 pull request 如果在相应 issue 中没有找到拒绝理由，可以直接联系 @realywithoutname 问明原因。

### 参与校对

在 Pull requests 中选择一个 pull request 进行 review，具体的操作可参考掘金的[参与校对的正确姿势](https://github.com/xitu/gold-miner/wiki/%E5%8F%82%E4%B8%8E%E6%A0%A1%E5%AF%B9%E7%9A%84%E6%AD%A3%E7%A1%AE%E5%A7%BF%E5%8A%BF)，提交 review 意见，并讨论他们。

你需要做的是指出新翻译内容中错译、漏译、标点符号错误、错别字、大小写、拼写错误、单复数、动词时态、数字错误等

### 参与审校

请点击右上角 “fork” 按钮，fork 此仓库到你的 github 仓库，然后在本地 pull 远程仓库即可对项目中已翻译内容进行审校了。

你需要在 issues 中选择[审校中](https://github.com/docschina/ecma262/labels/%E5%AE%A1%E6%A0%A1%E4%B8%AD)的 issue，并 @realywithoutname 通知该章节由你来审校

在你的项目根目录基于 cn 分支对 `translated` 文件夹的 `issues-[ISSUE ID].html` 文件中内容你觉得需要修改的地方进行修改。

修改完成后使用 `npm run build` 检查是否符合预期，可以对照[英文](https://tc39.github.io/ecma262/)对应部分进行检查。

发起相应的 pull request（建议 title 使用 **checking: issue #ISSUE ID**），将有人对你的修改进行 review，在被 merge 前请你对该 pull request 保持关注。

## 关于发布

对于审校完成并被 merge 的 pull request，相应的 issue 将关闭并处于已发布状态，相应已发布 issue 可以在 projects 已发布列中查看。

被 merge 的审校 pull request 内容将被合并到 cn 分支的 `spec.html` 中，并被发布。
## 关于 label

以下是关于常用一些 label 的使用和含义。

issues:
  - `待翻译` 表示该 issue id 对应在 translated 目录下的文件无人进行翻译，可以认领
  - `翻译中` 表示该 issue id 对应在 translated 目录下的文件有人正在翻译
  - `校对中` 表示该 issue id 对应在 translated 目录下的文件已提交 pull request
  - `审校中` 表示该 issue id 对应在 translated 目录下的文件已完成翻译工作
  - `已发布` 表示该 issue id 对应在 translated 目录下的文件已可以在网页中查看
  - 其他

Pull requests:
  - `待校对` 表示该 pull request 目前无人进行校对，可认领校对
  - `校对中` 表示该 pull request 目前有人正在进行校，可就 reviewer 的意见进行讨论
  - `拒绝校对 + 原因` 表示该 pull request 由于某些原因不能进入校对流程，需要翻译者根据原因作出相应修改，这样的 pull request 在一定时间内不进行修改将被关闭

## 联系我们

![81518255655_ pic](https://user-images.githubusercontent.com/10306332/36060706-c33e4e56-0e89-11e8-9488-ad103be18a3b.jpg)

如果二维码过期，请加微信号：liu762022369
