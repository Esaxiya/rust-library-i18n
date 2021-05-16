# Early preview of Rust standard library localization documents



[简体中文](./README_zh-CN.md)



The `Rust` standard library localization documents are released by [`wtklbm`](https://www.github.com/wtklbm). The localization documents now support 104 languages. These localization documents are automatically processed by the `Cmtor` program based on Google Translate. Please do not submit any PR to the localization documents in this warehouse.

`Rust` Localized documents can be used as smart tips for `IDE` tools to help `Rust` developers quickly understand Rust `API` and improve the development efficiency and code quality of `Rust` engineers.



![2021-04-19_15.23.00](./assets/2021-04-19_15.23.00.gif)



## Which file should I download

All the documents in this warehouse are automatically completed based on Google Translate. If you want to use the localized documents in this warehouse, you need to know what the code of your country is. For example, friends in China can download `zh-CN.zip` or `zh-TW.zip`, friends in Korea can download `ko.zip`, friends in Japan can download `ja.zip`, friends in Germany can download `de.zip`, and friends in Russia can download `ru.zip`.

For details, see：<https://cloud.google.com/translate/docs/languages>



## How to use `Rust` localized documents

> Please note that all localized documents in this warehouse will follow the updates of Rust. If you want to install a specific version of Rust localized documents, please transfer to [previews](https://github.com/wtklbm/rust-library-i18n/tree/main/previews) page to download. When using localized documents, the localized document version and the Rust version must be consistent. And you cannot use the `nightly` version, but the `stable` version.



If you are just starting to use Rust, after Rust is successfully installed, you should also install `rust-src` through the `rustup component add rust-src` command. After installing `rust-src`, please follow the steps below:

1. First get the value of the system environment variable `CARGO_HOME`, this value is a file path
2. Under the `CARGO_HOME` folder, find a folder named `.rustup`, and under the folder there is a folder named `toolchains`
3. In the `toolchains` folder, find the Rust version you are currently using and open it, for example, `stable-x86_64-pc-windows-msvc` on Windows
4. Then open the `lib/rustlib/src/rust` directory, the folder under this directory is where the source code of the Rust standard library is located
5. Save a copy of everything in the `lib/rustlib/src/rust/library` folder
6. Download the localized document source file corresponding to this warehouse, rename it to `library` and place it under the `lib/rustlib/src/rust` folder
7. Run: `rustup default stable` to switch to the `stable` version
8. Restart the `IDE` tool, and the smart prompt of the localized document starts to work
9. Happy coding！



## about PR

At present, the Rust standard library translation is automatically processed through the Cmtor program, because translating the Rust standard library is a difficult task, which can not be completed quickly by a few people, and the efficiency, timeliness, and quality of translation cannot be guaranteed, so At present, it is only through the Cmtor program to automatically process those source code files. I am very willing to make some meager contributions to Rust and do a good job of translation. Currently, I am modifying the Cmtor program to improve common errors. After the common errors are fixed, I think that at that time is the best time for us to manually translate the source code.

If you have any good ideas, we can discuss them together.



## License

MIT OR Apache-2.0



## connection

I am a full-stack developer who loves front-end and Rust. If you have any questions about localization, please feel free to contact me.

<div  align="center">
	<img src="./assets/wechat.png" align="left" width="47%" />
</div>



