# Rust 库翻译 (rust-src/rust-std/stdlib/rustlib 翻译)



[English](./README.md)



这是翻译 [Rust 库](https://github.com/rust-lang/rust/tree/master/library) 的地方， 相关源代码来自于 <https://github.com/rust-lang/rust>。

如果您不会说英语，那么拥有使用母语的文档至关重要，即使您会说英语，使用母语也仍然能让您感到愉快。Rust 标准库是高质量的，不管是新手还是老手，都可以从中受益。

该仓库包含 `rust-src` 组件的所有源代码文件，并对其所有的源代码进行结构化翻译，主要包括对 Rust 核心库的翻译，Rust 标准库的翻译，以及其他一些资源。该仓库使用 [`Cmtor`](#) 程序并借助 `JSON` 文件来完成翻译的所有工作，当 Rust 更新时，将在 10 天之内自动为其生成本地化翻译。



## 目标

- 📦 覆盖率

  Rust 库翻译已支持翻译 `rust-src` 源代码中的所有 Rust 文档

- 🔨 刷新率

  能够快速发现文档中的更新，并作出响应，让文档始终保持最新，告别文档过时的问题

- 🚄 更新频率

  当 Rust 发布新的版本时，Rust 库翻译将在 10 天之内进行更新

- 🧰 复用率

  只需要翻译一次就可以进行重复的构建

- 💪 支持多人协作

  使用 `JSON` 格式，简单高效，任何人都可以轻松的 `PR`

- 💡 可用于 `IDE` 工具的智能提示

  智能提示可帮助 Rust 开发者快速了解 Rust `API`，提高 Rust 工程师的开发效率和代码质量

- 🏳️‍🌈 多语言支持，能够生成多种语言的文档

  可以为每种受支持的语言构建本地化的文档，您可以组织翻译小组并提交 `PR` 来获得对其他语言的支持

- ✅ 自动生成

  Rust 文档由 `Cmtor` 程序自动生成，无需任何人工干预



## 对语言的支持

Rust 标准库中文版目前是受支持的，如果您想支持其他语言，那么您最好组建一个 3 个人以上的翻译小组，然后由翻译小组共同来完成翻译。如果没有翻译小组，也不能持续的提交 PR 的话，那么您最好不要提交 `ISSUES`。



受支持的语言：

- Rust 标准库中文版



理论上可以支持多种语言：

- Rust標準ライブラリ日本語版
- Rust 표준 라이브러리 한국어 버전
- Version française de la bibliothèque standard Rust
- Rust Standard Library Deutsche Version
- Libreria standard Rust versione italiana
- Rust Biblioteca estándar de en español
- Rust Стандартная библиотека Русская версия
- ...



## 如何下载翻译好的 Rust 文档

> 本仓库所提供的文件主要用于学习和交流，为了让项目持续健康的发展，所有文档的翻译将借助翻译引擎和人工翻译共同来完成。使用翻译引擎会不可避免的出现一些微小的错误，如果您的要求比较高，并且不认可翻译引擎或者不认可人工翻译的质量，那么请不要使用该仓库的任何文件。请不要进行任何不礼貌的、毫无意义的讨论。如果您认为哪里翻译的不好，您可以拒绝使用，也可以提交 PR，但请不要用 `ISSUES` 进行批评或指责，这是非常不礼貌的行为，请把讨论的重点放在学习和交流 Rust 语言本身，感谢您支持和理解。
>
> 如果您使用该仓库中所包含的内容，则表示您同意上述内容。



只有受支持的语言才提供下载，您可以跳转到 `dist` 目录下下载最新的构建结果。



## 如何使用 Rust 本地化文档

> 本仓库中的所有本地化文档会跟随 Rust 的更新而更新，在使用本地化文档时，本地化文档版本和 Rust 版本必须要保持一致。并且您不能使用 `nightly` 版本，而是使用 `stable` 版本。
>



如果您是刚开始使用 Rust，那么在 Rust 安装成功后，您还应该通过 `rustup component add rust-src` 命令来安装 `rust-src`。当安装 `rust-src` 之后，请按照以下步骤进行操作：

1. 首先获取到系统环境变量 `CARGO_HOME` 的值，这个值是一个文件路径
2. 在 `CARGO_HOME` 文件夹下，找到一个名字叫做 `.rustup` 的文件夹，在该文件夹下有一个叫做 `toolchains` 的文件夹
3. 在 `toolchains` 文件夹下，找到您当前所使用的 Rust 版本并将其打开，比如在 Windows 上是 `stable-x86_64-pc-windows-msvc`
4. 然后打开 `lib/rustlib/src/rust` 目录，这个目录下的文件夹就是 Rust 标准库源代码所在的位置
5. 将 `lib/rustlib/src/rust/library` 文件夹下的所有内容保存一份副本
6. 下载本仓库对应的本地化文档源文件，将其重命名为 `library` 并放置到 `lib/rustlib/src/rust` 文件夹下
7. 运行: `rustup default stable` 来切换到 `stable` 版本
8. 重新启动 `IDE` 工具，本地化文档的智能提示开始工作
9. 愉快的编码！



## ~~早期预览文件~~

`Rust` 标准库本地化文档有一些早期的预览文件，请跳转到 [previews](https://github.com/wtklbm/rust-library-i18n/tree/main/previews) 页面下载它们。请注意，这些预览文件已被废弃，并且不再提供更新。

在下载前，需要知道您所在地区的区域代码是什么，比如中国的朋友可以下载 `zh-CN.zip` 或者 `zh-TW.zip`，韩国的朋友可以下载 `ko.zip`，日本的朋友可以下载 `ja.zip`，德国的朋友可以下载 `de.zip`，俄罗斯的朋友可以下载 `ru.zip`。

有关详细信息，请参见：<https://cloud.google.com/translate/docs/languages>



## 翻译规则

在翻译 Rust 文档时候，请遵循以下翻译规则。

- 在翻译时应使用尊称，比如 `you` 应该被翻译成 `您` 而不是 `你`
- 因为有一些固有的名词没有固定的翻译，这样的名词就不应该翻译
- 注意专有词汇的大小写，比如 `rust` 应该写成 `Rust`
- 汉字，字母，数字、括号、引号等之间以一个空格隔开，并且字母和数字必须是半角符号
- 避免使用网络用语、缩写和带有感情色彩的词汇
- 在翻译中文时应使用全角中文标点，并且全角标点与其他字符之间不加空格
- 被任意的括号和引号所包裹的内容不应该被翻译，比如：
  - [\`thread\`] 中的 \`thread\`
  - [\`Copy\`][#id] 中的 \`Copy\`
  - ...
- ...



## 贡献指南

如果您有充足的业余时间，热爱 Rust 并在学习 Rust，想深入了解 Rust 的核心，那么翻译 Rust 文档是一种不错的学习方式。

需要注意的是，您不能修改 `dist` 目录下的文件，而是修改 `src` 目录下的文件。本仓库的所有翻译文件都是 `.json` 格式的，您可以打开它们，并给出正确的翻译，然后 `PR`，这对每一个人来说都非常的简单。

在提交 PR 之前，您需要熟悉一下 `.json` 中的内容。在 `.json` 文件中，每一个翻译项都有三个属性。

```javascript
{
    // 要翻译的源内容。
    // NOTE: 您不能修改它。
    "source": "This is a test.",

    // 翻译引擎给出的翻译，它可以作为最后的翻译结果使用，也可以作为参考给翻译人员看。
    // NOTE: 您不能修改它。
    "suggest": "这是一个测试。",

    // 一个字符串或一个布尔值，这个值由您来更改。
    //
    // 如果是一个字符串：
    //  - 如果字符串不为空，则表示用 `translate` 属性的值作为翻译的结果。
    //  - 如果是为空字符串，则表示当前还没有人翻译它。
    //
    // 如果是一个布尔值：
    //  - 如果为 `true`，则表示接受翻译引擎所给出的翻译，并将它作为翻译结果。
    //  - 如果为 `false`，则表示当前的内容不需要被翻译。
    "translate": ""
},
```



### 例子

信任翻译引擎，并将它的值作为最终的翻译：

```javascript
{
    "source": "This is a test.",
    "suggest": "这是一个测试。",
    "translate": true
}
```



源内容不需要被翻译：

```javascript
{
    "source": "Rust",
    "suggest": "锈",
    "translate": false
}
```



由您来翻译并作为最终的翻译结果：

```javascript
{
    "source": "This is a test.",
    "suggest": "这是一个测验。",
    "translate": "这是一个测试。"
}
```



## License

MIT OR Apache-2.0



## 联系

我热爱前端和 Rust，如果您有任何有关本地化的问题，欢迎与我联系。

<div  align="center">
	<img src="./assets/wechat.png" align="left" width="47%" />
</div>



