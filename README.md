# Python 分布式编程

## 主要内容

#### 第一部分：背景

* `ch-python-lang`：介绍 Python 语言、生态、GIL性能瓶颈以及本书主要内容。

#### 第二部分：数据处理

* `ch-distributed-array-dataframe`：介绍 Dask 和 Xorbits 提供的分布式 array 和 DataFrame 功能。

* `ch-ray`：介绍 Ray 架构和原理、Actor 编程模型。

#### 第三部分：模型调优

* `ch-ray-tune`：介绍 Ray 提供的超参数调优。

#### 第四部分：模型推理

* `ch-inference`：介绍模型推理工具。

#### 第五部分：MPI 编程

* `ch-mpi4py`：介绍基于 mpi4py 的 MPI 编程。

## 参与编写

### 环境安装

本书基于名为 `d2lbook` 的 Python 工具编译，并部署在GitHub Pages上。

选择一个包管理工具，比如 `conda` 或者 `venv`，安装 `d2lbook`：

```bash
pip install git+https://github.com/d2l-ai/d2l-book
```

更多 `d2lbook` 工具的使用方法，请参考其官方文档：[D2L-Book: A Toolkit for Hands-on Books](https://book.d2l.ai/)

构建 PDF 时如果有 SVG 图片需要安装 LibRsvg 来转换 SVG 图片，安装 `librsvg` 可以通过`apt-get install librsvg`（如果是 macOS 可以用 Homebrew）。

构建 PDF 必须要有 LaTeX，请安装[Tex Live](https://www.tug.org/texlive/).

### 编译HTML版本

在编译前先 `git clone` [https://github.com/py-101/distributed-python/](https://github.com/py-101/distributed-python/)， 所有的编译命令都在这个文件目录内执行。

```bash
 git clone https://github.com/py-101/distributed-python.git
 cd distributed-python
```

使用 `d2lbook` 工具编译HTML。 请尽量使用 `build_html.sh` 脚本进行编译，保证首页正确合并到书籍中去。

```bash
sh build_html.sh
```

生成的html会在 `_build/html`。

如果是在本地，可以使用 Python 自带的 HTTP Server：

```bash
cd _build/html
python -m http.server
```