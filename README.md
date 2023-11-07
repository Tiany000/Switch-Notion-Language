## 说明
本项目仅供学习使用，如有侵权问题，请提交 <b>Issues</b> ，看到后会立即删除。


## 起源
在 Notion 更新值至 2.24 版本后，原有大佬提供的设置中文的方式（[notion-zh_CN](https://github.com/reamd7/notion-zh_CN)）已经失效（感谢大佬提供的便利🤞🤞🤞），并且暂未找到可用的设置中文的方式。故而产生了自己摸索的想法🤔🤔🤔，在一番尝试下，最终成功将本地 Notion 设置为中文，所以在此记录一下设置方式。


## windows
Notion 的中文语料正处于 ```Development``` 阶段，但其已存在于 Notion 的缓存文件中，故此我们可以做出以下修改以设置中文环境

<small>请注意 以下文字中的 *** 以本地实际情况为准</small>

1. 找到本地缓存文件所在位置一般位于 ```C:\Users\***\AppData\Roaming\Notion\notionAssetCache-v2```

2. 打开本地缓存文件夹下的 ```latestVersion.json``` 文件查看最新的版本号，我这里为 ```23.12.0.267```
3. 打开本地缓存文件夹下的 ```23.12.0.267\assets\_assets``` 文件夹
4. 在文件夹内查找以下文件 ```localeSetup-zh-CN-***.js``` 和 ```index-en-US-***.html``` （***）为不固定值
5. 打开 ```index-en-US-***.html``` 文件，搜索 ```</head>``` 在此字符前添加以下语句
```html
<script defer="defer" src="/_assets/localeSetup-zh-CN-***.js"></script>
```
6. 保存文件，重新打开 Notion，设置中文完成

## 后言
如果您有更好的设置中文环境的方式，欢迎您提出 <b>Pr</b> ，如您在使用过程中遇到问题，或者有其他需求，请您提交 <b>Issues</b> 。