# korofileheader-
korofileheader注释模板的常用配置
##vscode设置步骤
*打开用户首选项，选择设置，打开setting.json文件进行配置  
[`参考博客`：https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE](https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE)
``` bash
  {
    "window.zoomLevel": 1,
    "explorer.confirmDelete": false,
    "files.autoSave": "onFocusChange",
    "workbench.startupEditor": "newUntitledFile",
    "breadcrumbs.enabled": true,
    "[javascript]": {
        "editor.defaultFormatter": "HookyQR.beautify"
    },
    // 文档注释配置
    "fileheader.customMade": {
        "Author": "ddwei",
        "LastEditors": "ddwei",
        "Date": "Do not edit",
        "LastEditTime": "Do not edit",
        "Description": "file content",
        "FilePath": "no item name",
        "custom_string_obkoro1": "可以输入预定的版权声明、个性签名、空行等"
    },
    // 函数注释配置
    "fileheader.cursorMode": {},
    // 插件注释配置
    "fileheader.configObj": {
        "language": {
            "java": {
                "head": "/$$",
                "middle": " $ @",
                "end": " $/"
            },
            // 针对有特殊要求的文件如：test.blade.php
            "blade.php": {
                "head": "<!--",
                "middle": " * @",
                "end": "-->",
            }
        },
        // 默认的注释形式（上两种匹配不到时生效）
        "annotationStr": {
            "head": "/*", // 自定义注释头部
            "middle": " * @", // 自定义注释中间部分(注意空格,这也是最终生成注释的一部分)
            "end": " */", // 自定义注释尾部
            "use": true // 是否使用自定义注释符号
        },
        "autoAdd": true, //自动添加文档注释
        "autoAlready": true, //自动添加头部注释：只允许插件支持的语言，以及用户通过language 选项自定义的注释。
        "prohibitAutoAdd": [
            "json",
            "add"
        ], //禁止特殊文件自动添加注释
        "autoAddLine": 100, //超出100行不添加
        "headInsertLine": {
            "php": 2 // php后缀的文件，在第二行插入文件头部注释
        },
        "createFileTime": true, // 设为false更改为当前生成注释的时间
        "dateFormat": "YYYY-MM-DD HH:mm:ss ZZ", // 输出：2019-05-20 15:42:07 +0800
        "beforeAnnotation": {
            "py": "#!/usr/bin/env python\n# coding=utf-8" //头部注释前加入内容, py文件默认，可修改
        },
        "afterAnonotation": {},
        // 特殊字段自定义
        "specialOptions": {
            "Date": "since",
            "LastEditTime": "lastTime",
            "LastEditors": "LastAuthor",
            "Description": "message",
            "FilePath": "文件相对于项目的路径"
        },
        "switch": {
            "newlineAddAnnotation": true // 默认开启
        },
        "moveCursor": true, // 移动光标到`Description :`所在行
        "atSymbol": "#", // 所有文件的@改为#,默认为@，此为示例。
        "atSymbolObj": {
            "js": "", // .js文件 去掉@
            "java": "#" // .java文件 @改为#
        },
        "colon": " ", // 所有注释的冒号改为一个空格，默认为": "
        "colonObj": {
            "js": " ", // .js文件 去掉: 留一个空格
            "java": "$" // .java文件 ": "改为$
        },
        "showErrorMessage": false // 默认不显示错误通知 用于debugger
    }
}
```
