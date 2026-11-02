# long_toolchain_context_reclaim_grouping

**把广告召回与排序工程师·长工具链的上下文回收归并成组并标出每组的代表项。**

`long_toolchain_context_reclaim_grouping` —— 按结构键把条目聚类，标出广告召回与排序工程师·长工具链的上下文回收上的同组项与各组的代表样本

- 零依赖，Python 3.10+ 标准库即可运行
- 单文件，`long_toolchain_context_reclaim_grouping.py` 拷走就能用
- 不联网、不写文件

## 对应的岗位

- 目标岗位：**蚂蚁集团 · 资深广告召回与排序工程师**
- 技能主线：推荐系统、AB实验、特征工程
- 领域标签：搜索推荐广告
- 研究方向：广告召回与排序工程师·长工具链的上下文回收

工具里的规则表就是照着上面这条岗位要求建的——每条规则都挂在技能线或领域标签上，命中时能指回具体要求。

<!-- ipos:install -->
## 安装

零依赖，Python 3.10+ 即可：

```bash
pip install veliple-long_toolchain_context_reclaim_grouping
```

装完直接用命令名调用：

```bash
long_toolchain_context_reclaim_grouping --help
```

也可以不用安装，直接把 `long_toolchain_context_reclaim_grouping.py` 拷走用——它只依赖标准库。

## 为什么需要它

分组依据是结构特征而不是字面相似，改了措辞但结构没变的仍算同组

它遵守下面几条自己定的规矩：

1. **只报告能定位到具体位置的结论**，不做语义猜测。
2. **规则表公开**，每条命中都能对应到岗位要求的一条明示规则。
3. **输入为空或格式不对时明确报错**，不静默返回空结果。

## 用法

```bash
python long_toolchain_context_reclaim_grouping.py --file input.txt
python long_toolchain_context_reclaim_grouping.py --text "示例内容"
python long_toolchain_context_reclaim_grouping.py --file input.txt --json
```

加 `--json` 可以拿到机器可读的结果，便于接到流水线里。

## 已知局限

- 分组靠标签与关键词相似度，分错组时不保证可解释。
- 不评估分组质量。

## 跑测试

```bash
python test_long_toolchain_context_reclaim_grouping.py
```

测试用独立的断言与临时数据，不污染工作目录。

## 来源与参考

- Python 标准库文档：<https://docs.python.org/3/>
- GitHub 仓库：<https://github.com/veliple/long_toolchain_context_reclaim_grouping>

---

## 关于作者

veliple 做广告召回与排序工程师·长工具链的上下文回收相关的问题，方向对标蚂蚁集团的资深广告召回与排序工程师岗位。这个工具先替你回答一个具体问题，再谈别的。

- 个人主页：<https://veliple.github.io>
- 仓库：<https://github.com/veliple/long_toolchain_context_reclaim_grouping>

## 许可

MIT，见 [LICENSE](LICENSE)。
