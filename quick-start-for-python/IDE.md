# 背景

- 每个人都有自己的代码风格习惯，糟糕的代码风格习惯无疑对代码阅读理解、管理、维护带来的极大的阻扰，对于新人上手入门非常不友好
- 为了提高代码的可读性和可维护性，减少因为代码标准、格式化、美化工具对代码带来的影响

# 内容

- 对于每级缩进，统一要求使用 4 个空格 ，而非 tab 键。 pylint:mixed-indentation, bad-indentation
- 每行最多不超过 120 个字符
- 空白符
  - 在表达式的赋值符号、操作符左右至少有一个空格。 pylint:bad-whitespace
  - 禁止行尾空白。 pylint:trailing-whitespace.
- 空行
  - 模块中的一级函数和类定义之间，需要空两行。pycodestyle:E302 expected 2 blank lines
  - 类中函数定义之间，空一行。pycodestyle:E302 expected 1 blank line
  - 源文件末尾有且仅有 一行空行。pylint:missing-final-newline, trailing-newlines
  - 通常每个语句应该独占一行。pylint:multiple-statements
  - <推荐> 可以在代码段中的空一行来区分不同业务逻辑块
- 编码格式为 UTF8
- 换行符为 LF
- import
  - 每个导入应该独占一行。 pylint:multiple-imports.
  - 导入应该按照从最通用到最不通用的顺序分组, 每个分组之间，需要空一行（标准库导入；第三方库导入；本地导入）

# vscode 配置流程

```markdown
1. 流程

- vscode 下载并安装插件 Settings Sync
- 登录 github 账号
- 配置 gist
- shift + alt + D 下载配置

2. python

- Gist：917e6fb6fc4765e5c8840511ea836f6c

3. C/C++

- Gist：917e6fb6fc4765e5c8840511ea836f6c
```

# pycharm 配置流程

```markdown
1. 旧项目

- 先下载 convert_tab_to_space.zip，将代码的中的 tab 转为 space 后统一提交后，在执行接下来的流程

2. 一键式优化 import

- 下载.isort.cfg.zip，放到代码根目录
- 保存文件的时候自动优化 import

3. 一键式配置

- 下载“pycharm_settings.zip”
- 打开 pycharm，File -> export settings
- 重启 IDE 后，保存文件后自动执行格式化逻辑

4. 你可能需要修改的地方

- Editor -> File and Code Templates -> Python Script 里，作者修改为你自己的名字
- Tools -> External Tools 内关于第三方工具的地址配置和安装，可能需要修改下

5. PEP8 风格配置

- Tools -> External Tool -> autopep8

6. pylint 语法检查配置

- Tools -> External Tool -> pylint
```
