# Rust 标准库本地化文档早期预览

`Rust` 标准库本地化文档是 [`wtklbm`](https://www.github.com/wtklbm) 发布的，该本地化文档现已支持 104 种语言，这些本地化文档是由 `Cmtor` 程序基于谷歌翻译自动处理完成的，请不要向本仓库中的本地化文档提交任何 PR。

`Rust` 本地化文档可用于 `IDE` 工具的智能提示，帮助 `Rust` 开发者快速了解 Rust `API`，提高 `Rust` 工程师的开发效率和代码质量。



![2021-04-19_15.23.00](./assets/2021-04-19_15.23.00.gif)



## 我应该下载哪个文件

本仓库中的所有文档都是基于谷歌翻译自动完成的，如果您想使用本仓库中的本地化文档，就需要知道您所在的区域代码是什么，比如中国的朋友可以下载 `zh-CN.zip` 或者 `zh-TW.zip`，韩国的朋友可以下载 `ko.zip`，日本的朋友可以下载 `ja.zip`，德国的朋友可以下载 `de.zip`，俄国的朋友可以下载 `ru.zip`。

有关详细信息，请参见：<https://cloud.google.com/translate/docs/languages>



## 如何使用 `Rust` 本地化文档

> 请注意，本仓库中的所有本地化文档会跟随 Rust 的更新而更新，如果您想安装具体版本的 Rust 本地化文档，请跳转到 [previews](https://github.com/wtklbm/rust-library-i18n/tree/main/previews) 页面下载。在使用本地化文档时，本地化文档版本和 Rust 版本必须要保持一致。并且您不能使用 `nightly` 版本，而是使用 `stable` 版本。
>



如果您是刚开始使用 Rust，那么在 Rust 安装成功后，您还应该通过 `rustup component add rust-src` 命令来安装 `rust-src`。当安装 `rust-src` 之后，请按照以下步骤进行操作：

1. 首先获取到系统环境变量 `CARGO_HOME` 的值，这个值是一个文件路径
2. 在 `CARGO_HOME` 文件夹下，找到一个名字叫做 `.rustup` 的文件夹，在该文件夹下有一个叫做 `toolchains` 的文件夹
3. 在 `toolchains` 文件夹下，找到你当前所使用的 Rust 版本并将其打开，比如在 Windows 上是 `stable-x86_64-pc-windows-msvc`
4. 然后打开 `lib/rustlib/src/rust` 目录，这个目录下的文件夹就是 Rust 标准库源代码所在的位置
5. 将 `lib/rustlib/src/rust/library` 文件夹下的所有内容保存一份副本
6. 下载本仓库对应的本地化文档源文件，将其重命名为 `library` 并放置到 `lib/rustlib/src/rust` 文件夹下
7. 运行: `rustup default stable` 来切换到 `stable` 版本
8. 重新启动 `IDE` 工具，本地化文档的智能提示开始工作
9. 愉快的编码！



## 关于 PR

目前 Rust 标准库翻译是通过 Cmtor 程序自动处理完成的，因为翻译 Rust 标准库是一项艰巨的工作，并非是几个人就可以迅速完成，而且翻译的效率、时效性、质量也不能够保证，所以目前来说，还仅仅是通过 Cmtor 程序自动处理那些源代码文件。我非常愿意为 Rust 做出一些微薄的贡献，把翻译的工作做好。当前，我正在修改 Cmtor 程序来改善常见的错误，等修复了常见的错误以后，我认为在那个时候，才是我们去手动翻译那些源代码的最好时机。

如果您有什么好的想法，我们可以一起来讨论。



## License

MIT OR Apache-2.0



## 联系

我是一名热爱前端和 Rust 的全栈开发人员，如果您有任何有关本地化的问题，欢迎与我联系。

<div  align="center">
	<img src="./assets/wechat.png" align="left" width="47%" />
</div>



