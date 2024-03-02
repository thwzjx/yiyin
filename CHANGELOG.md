# Changelog

## 1.0.0 (2024-03-02)


### Features

* **tools/image:** 限制模糊背景宽高并限定模糊半径，统一模糊效果 ([a1bf779](https://github.com/thwzjx/yiyin/commit/a1bf77956d6bfa758769aff5fe470dbb7e0f37de))
* **utils:** 添加通用函数 ([75a5f8f](https://github.com/thwzjx/yiyin/commit/75a5f8fbcd7189fbf3dd8efd795c4bda9f076972))
* 优化主图和文字的间距，优化背景高度计算公式 ([a1bf779](https://github.com/thwzjx/yiyin/commit/a1bf77956d6bfa758769aff5fe470dbb7e0f37de))
* 优化文字高度计算公式 ([4c5da26](https://github.com/thwzjx/yiyin/commit/4c5da2697c02b2e0ff3bbfb8b41365802128ea4a))
* 优化模版配置信息模块 ([76fc3fd](https://github.com/thwzjx/yiyin/commit/76fc3fd662ea49b65f626dbfd829d70212134bc5))
* 修改文字构建方式，采用模版式 ([06086a3](https://github.com/thwzjx/yiyin/commit/06086a35fde1a1275dc3827ceb7b9049403122ab))
* 修改水印输出文件名 ([2ede647](https://github.com/thwzjx/yiyin/commit/2ede6475c3e6baa2cb79aba56c36fc53ae3ede4e))
* 指定主图默认间隔和文字间隔 ([485327a](https://github.com/thwzjx/yiyin/commit/485327afdb2868aac67e98ad603d58179d8402a5))
* 添加主图对背景图片间距过小处理，等比放大背景以满足间距 ([dc97c85](https://github.com/thwzjx/yiyin/commit/dc97c85a94bd1a649e297b96a29b08f419db60a5))
* 添加内置logo选择弹窗 ([80c2059](https://github.com/thwzjx/yiyin/commit/80c20597aa9a14700a60ddd7f386ca5d8fbeeb3a))
* 添加原始宽高输出和非原始宽高输出功能 ([a8e938f](https://github.com/thwzjx/yiyin/commit/a8e938f390e0c8a9376ef6e0c757eb3357b4e41b))
* 添加参数设置生效开关减少频繁设置参数 ([382a6a1](https://github.com/thwzjx/yiyin/commit/382a6a1ec61d7be6d36c947845ddd68c8834f6b7))
* 添加参数重置 ([a3054ca](https://github.com/thwzjx/yiyin/commit/a3054ca4bf696e309776a4309ddd3bc7db54f42d))
* 添加反馈和建议跳转链接 ([dc13d01](https://github.com/thwzjx/yiyin/commit/dc13d016be61bb4f732cbc8ec90f19e7cc35817b))
* 添加品牌机型显示和参数显示选项，修改图片占比 ([a274a58](https://github.com/thwzjx/yiyin/commit/a274a585302420a58ff6de9b8f83eb49617fe5c9))
* 添加图片弹窗显示 ([00f33c9](https://github.com/thwzjx/yiyin/commit/00f33c94914858f74f36c9075927d3ea58936b90))
* 添加图片输出圆角显示功能，添加纯色背景支持 ([e4fa984](https://github.com/thwzjx/yiyin/commit/e4fa9843abbcdec6de993173eadac77900e9c047))
* 添加日志模块 ([fb75b54](https://github.com/thwzjx/yiyin/commit/fb75b5403d6e5b06e8c6ffd275c533daa162707b))
* 添加机型映射 ([0d542ba](https://github.com/thwzjx/yiyin/commit/0d542bac7ba2bccc6a435a0518576514162a4afe))
* 添加版本更新提示，并添加新版下载链接 ([491afe2](https://github.com/thwzjx/yiyin/commit/491afe29ca467848858e6ab0916bf14453dacea9))
* 添加相机信息获取函数、接口 ([7f07da1](https://github.com/thwzjx/yiyin/commit/7f07da187eaaf91bc2c757a3e614cae42351f3f5))
* 添加背景图层生成接口，修改背景图层高度计算，修改字体大小参照 ([15057f7](https://github.com/thwzjx/yiyin/commit/15057f72080a3700b46ccaff70d170a3c913f250))
* 添加背景比例设置支持 ([51389ed](https://github.com/thwzjx/yiyin/commit/51389edbc91309825487c72508fc8b3220674728))
* 添加自定义参数图片功能支持 ([067a8f9](https://github.com/thwzjx/yiyin/commit/067a8f9e1af6b14397fadc920aab7b1351dc561a))
* 添加自定义参数处理 ([109625b](https://github.com/thwzjx/yiyin/commit/109625bd532e96125beba7d16d309437c870bdbd))
* 添加自定义参数字体参数设置支持 ([9e8a61c](https://github.com/thwzjx/yiyin/commit/9e8a61cee7259475b0b92908c8b68961b531faa7))
* 添加自定义参数配置弹窗，移除多余组件引入dbui ([2cafc3a](https://github.com/thwzjx/yiyin/commit/2cafc3a52eed56c87f27b08f9e4a6c6da5fc2a0b))
* 添加自定义字体功能，引入组件库 ([5cf3d8b](https://github.com/thwzjx/yiyin/commit/5cf3d8bee613b7cffbd727b4c05bf6d02a94fa85))
* 添加输出文件名重复判断，并对文件名自增，修改输出文件名后缀 ([75a5f8f](https://github.com/thwzjx/yiyin/commit/75a5f8fbcd7189fbf3dd8efd795c4bda9f076972))
* 添加部分相机品牌的Logo，优化主图内容位置计算公式 ([518e2ff](https://github.com/thwzjx/yiyin/commit/518e2ffd0c5b6360c7f80ba65a6ad93d3f1ead81))
* 界面添加参数说明提示，优化输入框校验，引入skeleton组件库 ([7f07da1](https://github.com/thwzjx/yiyin/commit/7f07da187eaaf91bc2c757a3e614cae42351f3f5))
* 输出目录创建，添加接口异常日志 ([acc9d36](https://github.com/thwzjx/yiyin/commit/acc9d36509715998c6a349e374ab3ca59cad10da))
* 页面配置抽离，配置持久化函数统一 ([2cafc3a](https://github.com/thwzjx/yiyin/commit/2cafc3a52eed56c87f27b08f9e4a6c6da5fc2a0b))


### Bug Fixes

* **image:** 修复竖图输出异常 ([a25fe3d](https://github.com/thwzjx/yiyin/commit/a25fe3d62ef0205c3eedb5cec83d931efa036758))
* **router/image:** 修复概率出现窗口未显示图片，生成背景图片消息先发送导致印框生成处理异常 ([a1bf779](https://github.com/thwzjx/yiyin/commit/a1bf77956d6bfa758769aff5fe470dbb7e0f37de))
* 修复logo和机型文字不对齐问题 ([d5681e9](https://github.com/thwzjx/yiyin/commit/d5681e96ec1820528b20b62daa154236fb4de65e))
* 修复logo显示按钮失效问题 ([d5681e9](https://github.com/thwzjx/yiyin/commit/d5681e96ec1820528b20b62daa154236fb4de65e))
* 修复出现色块问题 ([2ede647](https://github.com/thwzjx/yiyin/commit/2ede6475c3e6baa2cb79aba56c36fc53ae3ede4e))
* 修复参数为空导致异常 ([76fc3fd](https://github.com/thwzjx/yiyin/commit/76fc3fd662ea49b65f626dbfd829d70212134bc5))
* 修复同一张图片多次生成是，背景图不会切换问题 ([096cbe2](https://github.com/thwzjx/yiyin/commit/096cbe29b150966ff155b2ccfdd8200c0e45c843))
* 修复因缓存目录不存在导致图片输出异常 ([0cf3428](https://github.com/thwzjx/yiyin/commit/0cf342895a0aed97dc79d36269ff4373ec756c5b))
* 修复图片方向引发的水印输出效果不对问题 ([2ede647](https://github.com/thwzjx/yiyin/commit/2ede6475c3e6baa2cb79aba56c36fc53ae3ede4e))
* 修复宽高比为字符0时异常，修复小图片生成模糊背景时参数异常导致软件崩溃 ([2ff8996](https://github.com/thwzjx/yiyin/commit/2ff8996f6133ccfc47526747449b64f20393b010))
* 修复打包运行异常 ([4c5da26](https://github.com/thwzjx/yiyin/commit/4c5da2697c02b2e0ff3bbfb8b41365802128ea4a))
* 修复文字不对齐问题 ([147c2ed](https://github.com/thwzjx/yiyin/commit/147c2ed7800de8bf230108de10141afdc786b23d))
* 修复机型映射未加空判断导致异常 ([18e9281](https://github.com/thwzjx/yiyin/commit/18e92812c092454e30f9564cafb424ac25180936))
* 修复模糊数值过高，导致背景出现严重偏紫 ([c5d23ce](https://github.com/thwzjx/yiyin/commit/c5d23cefb1e057a68d6ce2bfd877c26a8fccb9a0))
* 修复照片快门错误问题 ([2ede647](https://github.com/thwzjx/yiyin/commit/2ede6475c3e6baa2cb79aba56c36fc53ae3ede4e))
* 修复自定义字体参数开关失效 ([3d2ce46](https://github.com/thwzjx/yiyin/commit/3d2ce46091f372d75485c0b163060ee9f7576d90))
* 修复输出目录错误问题 ([fb75b54](https://github.com/thwzjx/yiyin/commit/fb75b5403d6e5b06e8c6ffd275c533daa162707b))
* 修复重置配置信息失败问题 ([95cd997](https://github.com/thwzjx/yiyin/commit/95cd997edac7fc8176d799ca59b83e94aaba3fc1))
* 修复非相机图片输出异常 ([51389ed](https://github.com/thwzjx/yiyin/commit/51389edbc91309825487c72508fc8b3220674728))
* 修复页面配置信息持久化失败 ([a8e938f](https://github.com/thwzjx/yiyin/commit/a8e938f390e0c8a9376ef6e0c757eb3357b4e41b))
* 添加输出目录创建异常处理，恢复为默认输出目录 ([3e22f05](https://github.com/thwzjx/yiyin/commit/3e22f0592f31e2182b76a566afb55a6b9d8b2e5e))


### Docs

* readme文档更新 ([0e72b44](https://github.com/thwzjx/yiyin/commit/0e72b44dbeff51da58bc810a9d4be680ca76c35d))
* update readme ([184c62d](https://github.com/thwzjx/yiyin/commit/184c62d5462dc4a26314a019d0c5f5a90c70c46e))
* 添加readme ([51389ed](https://github.com/thwzjx/yiyin/commit/51389edbc91309825487c72508fc8b3220674728))


### Styling

* **mask:** 页面配置ts类型，页面格式化 ([dda90e1](https://github.com/thwzjx/yiyin/commit/dda90e17904d03eafebbdb2e22bd9262d0c4d7ea))
* 优化代码结构 ([382a6a1](https://github.com/thwzjx/yiyin/commit/382a6a1ec61d7be6d36c947845ddd68c8834f6b7))
* 优化参数位置、参数解释及参数名称 ([9e8a61c](https://github.com/thwzjx/yiyin/commit/9e8a61cee7259475b0b92908c8b68961b531faa7))
* 修改eslint配置信息，svelte组件支持eslint检测，ts检测范围修改 ([a0f9ce2](https://github.com/thwzjx/yiyin/commit/a0f9ce2b475c7b4b28e6cd3634c27948a9dbc3ef))
* 修改logo字体大小，logo和主图间距 ([e14f21b](https://github.com/thwzjx/yiyin/commit/e14f21b7239303db6c13e465afd4a0235eb1c70a))
* 修改图片成像比例 ([1923f07](https://github.com/thwzjx/yiyin/commit/1923f07b2bddfbc17fbb6fdb44c1e55975aa6e45))
* 修改环境变量使用方式，添加环境变量替换 ([9e2b085](https://github.com/thwzjx/yiyin/commit/9e2b08534fb41208ea78df8f89178dc303d2eee9))
* 全目录添加格式化要求，格式化文件，前端组件添加ts ([5f99752](https://github.com/thwzjx/yiyin/commit/5f9975211fa2d5b1bf5720cc877c06f5bf020263))
* 配置路径别名，优化脚本语义 ([a0f9ce2](https://github.com/thwzjx/yiyin/commit/a0f9ce2b475c7b4b28e6cd3634c27948a9dbc3ef))
* 页面布局修改，简化参数名称 ([75a5f8f](https://github.com/thwzjx/yiyin/commit/75a5f8fbcd7189fbf3dd8efd795c4bda9f076972))


### Code Refactoring

* **main:** 组件抽离，样式抽离 ([57153fb](https://github.com/thwzjx/yiyin/commit/57153fbd9f5d33a81c07b5765866e0398ebc1949))
* 优化自定义参数组件结构 ([2332885](https://github.com/thwzjx/yiyin/commit/2332885de92a75f2e0b4bbca8c324875dfa04765))
* 重构图片操作模块代码，路由代码 ([75a5f8f](https://github.com/thwzjx/yiyin/commit/75a5f8fbcd7189fbf3dd8efd795c4bda9f076972))


### Performance Improvements

* 优化配置持久化过多问题 ([a25fe3d](https://github.com/thwzjx/yiyin/commit/a25fe3d62ef0205c3eedb5cec83d931efa036758))
