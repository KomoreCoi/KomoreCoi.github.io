---
title: hexo测试
categories: []
tags: [hexo]
date: 2024-07-29 19:14:36
toc: true
---

## 描述

```
title: hexo测试
categories: [cat1,cat2]
tags: [tag1,tag2]
date: 2024-07-29 19:14:36
toc: true
```

帖子模板在`scaffolds`文件夹下

描述下使用拼音输入光标总是跳到描述中，使用英文没有这个问题。本来以为是typora的bug，原来是输入法的问题，使用搜狗后解决！！！可恨的微软拼音！！！

## 写作

```
hexo new [layout] <title>
```

Hexo 有三种默认布局：`post`、`page` 和 `draft`。 每个布局创建的文件会被保存到不同的路径。 

不写layout参数，默认是`post`，新创建的帖子被保存到 `source/_posts` 文件夹。`post`是默认的`布局`，但你也可以提供自己的布局。 您可以通过编辑 `_config.yml` 中的 `default_layout` 设置来更改默认布局。

使用布局 `draft` 来创建草稿，新创建的草稿被保存到 `source/_darfts` 文件夹。

```
# 发表草稿
hexo publish [layout] <filename>
```

## 指令

### clean

```
$ hexo clean
```

清除缓存文件 (`db.json`) 和已生成的静态文件 (`public`)。

### generate

```
$ hexo generate
```

生成静态文件。

| 选项                  | 描述                                         |
| :-------------------- | :------------------------------------------- |
| `-d`, `--deploy`      | 在生成完成后部署。                           |
| `-w`, `--watch`       | 监视文件变动                                 |
| `-b`, `--bail`        | 生成过程中如果发生任何未处理的异常则抛出异常 |
| `-f`, `--force`       | 强制重新生成                                 |
| `-c`, `--concurrency` | 要同时生成的文件的最大数量。 默认无限制      |

### server

```
$ hexo server
```

启动服务器。 默认情况下，访问网址为： `http://localhost:4000/`。

| 选项             | 描述                               |
| :--------------- | :--------------------------------- |
| `-p`, `--port`   | 重设端口                           |
| `-s`, `--static` | 只使用静态文件                     |
| `-l`, `--log`    | 启用日志。 Override logger format. |

### deploy

```
$ hexo deploy
```

部署你的网站。

| 选项               | 描述         |
| :----------------- | :----------- |
| `-g`, `--generate` | 在部署前生成 |

## 小技巧

```
# 清除+生成+启动
hexo clean & hexo g & hexo s
# 清除+生成+部署
hexo clean & hexo g & hexo d
```

## pore中文文档

[hexo-theme-pure/README.cn.md at master · cofess/hexo-theme-pure](https://github.com/cofess/hexo-theme-pure/blob/master/README.cn.md)
