# 使用 husky + lint-staged 做代码检查

### husky

- [husky](https://github.com/typicode/husky) 是一个可以让我们更方便使用 githooks 的工具

- 关于 githooks 的配置写在根目录下的 [husk.config.js](https://gitlab.aihaisi.com/qiexr/fe-team/iPenguinDoctor_taro/-/blob/develop/husky.config.js) 中

- 支持哪些 githooks：https://git-scm.com/docs/githooks



### lint-staged

- [lint-staged](https://github.com/okonet/lint-staged#readme) 可以在 git staged 阶段执行 lint，仅对暂存区文件进行检查

- 在 `package.json` 的 `lint-staged` 中配置 lint command

  ```json
  "lint-staged": {
  	"*.{ts,tsx}": "eslint --fix"
  }
  ```



**Ps:** 

如果平时用 sourcetree 提交代码的话，可能会出现 hooks 无效的情况，可以在命令行中用下面命令重新打开一下 sourcetree 试试。

```shell
open /Applications/SourceTree.app/Contents/MacOS/SourceTree
```

如果还不行，[看看这个](https://community.atlassian.com/t5/Bitbucket-questions/SourceTree-Hook-failing-because-paths-don-t-seem-to-be-set/qaq-p/274792)。

