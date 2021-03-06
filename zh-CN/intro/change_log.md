---
name: 变更日志
---

# 变更日志

### 未发布

#### Bug 修复

- 若分支名称包含 `#` 则在更新保护分支设置后重定向到错误的地址 [#5442](https://github.com/gogs/gogs/issues/5442)
- 过长的工单评论会超出控制面板的宽度 [#5502](https://github.com/gogs/gogs/issues/5502)

#### 其它变更

- 安全漏洞修复

### 0.11.66 @ 2018-09-16

#### Bug 修复

- Web 编辑器提交后无法触发 Git 钩子 [#4338](https://github.com/gogs/gogs/issues/4338)
- 版本发布附件会由于删除任意评论而被清空 [#4627](https://github.com/gogs/gogs/issues/4627)
- 可公开访问的 Wiki 或工单的私有仓库无法在搜索结果中显示 [#4973](https://github.com/gogs/gogs/issues/4973)
- 无法连接 MySQL 8.0 [#5187](https://github.com/gogs/gogs/issues/5187)
- 删除仓库时未清理 Web 钩子和相关任务 [#5229](https://github.com/gogs/gogs/issues/5229)
- 恢复备份后时间戳全部变为当前时间 [#5264](https://github.com/gogs/gogs/issues/5264)
- 合并请求后删除分支没有触发 Web 钩子 [#5331](https://github.com/gogs/gogs/issues/5331)
- 派生仓库时没有检查用户仓库数量限制 [#5345](https://github.com/gogs/gogs/issues/5345)
- 使用 PostgreSQL 时无法删除用户 [#5376](https://github.com/gogs/gogs/issues/5376)

#### 新增特性

- 支持为仓库添加头像 [#2340](https://github.com/gogs/gogs/issues/2340)
- 增加由 Prometheus 提供的基本 Go Runtime 运行信息 [#4141](https://github.com/gogs/gogs/issues/4141)

#### 功能改进

- 默认忽略配置文件的行内注释
- 浏览文件时剔除文件末的空行 [#5270](https://github.com/gogs/gogs/pull/5270)
- 支持设定默认的用户认证方式 [#5274](https://github.com/gogs/gogs/issues/5274)
- 支持添加自定义合并提交描述 [#5276](https://github.com/gogs/gogs/pull/5276)

#### 其它变更

- 安全漏洞修复

### 0.11.53 @ 2018-06-05

#### Bug 修复

- 分支名包含 `#` 时无法进行正常操作 [#4601](https://github.com/gogs/gogs/issues/4601)
- 尖括号中间的工单编号没有被渲染 [#4706](https://github.com/gogs/gogs/issues/4706)
- 当基准分支不是默认分支时无法进行请求合并 [#5138](https://github.com/gogs/gogs/issues/5138)
- 生成的 Gravatar 链接不正确 [#5157](https://github.com/gogs/gogs/issues/5157)
- 允许重复使用相同的二步验证令牌
- 配置选项 `[git] GC_ARGS` 无法生效

#### 新增特性

- 在活动时间线显示镜像仓库更新 [#2017](https://github.com/gogs/gogs/issues/2017)
- 支持通过本地文件加载认证源 [#3142](https://github.com/gogs/gogs/issues/3142)
- 镜像同步后触发 Web 钩子 [#4528](https://github.com/gogs/gogs/issues/4528)

#### 其它变更

- 将导入路径从 "gogits/gogs" 修改为 "gogs/gogs"
- 安全漏洞修复
- 添加新语种支持：越南语

### 0.11.43 @ 2018-03-31

#### Bug 修复

- 保护分支可以在完成合并请求后被删除 [#4514](https://github.com/gogs/gogs/issues/4514)
- 不支持 MSSQL 数据库的 SYSNAME 字段类型 [#4642](https://github.com/gogs/gogs/issues/4642)
- 仓库快速开始页面只有仓库管理员可见 [#4646](https://github.com/gogs/gogs/issues/4646)
- 分支页面名称包含 `#` 的分支链接错误 [#4874](https://github.com/gogs/gogs/issues/4874)
- 在合并提交时使用衍合导致合并失效 [#5051](https://github.com/gogs/gogs/issues/5051)
- 分支一旦被设置为保护后，加锁标志在取消保护后也不消失 [#5053](https://github.com/gogs/gogs/issues/5053)
- IPython Notebook 中的 SVG 支持 [#5077](https://github.com/gogs/gogs/issues/5077)

#### 功能改进

- 支持 HTTP HEAD 请求 [#2857](https://github.com/gogs/gogs/issues/2857)
- 添加配置选项以允许在启动时重写 authorized_keys 文件 [#4435](https://github.com/gogs/gogs/issues/4435)
- 添加配置选项以设置邮件的全局主题前缀 [#4524](https://github.com/gogs/gogs/issues/4524)
- 默认禁用联合头像查找 [#5126](https://github.com/gogs/gogs/pull/5126)

#### 其它变更

- 添加新语种支持：印度尼西亚语、波斯语

### 0.11.34 @ 2017-11-22

#### Bug 修复

- *回退*：跨仓库合并请求无法正常工作 [#4890](https://github.com/gogs/gogs/issues/4890)

### 0.11.33 @ 2017-11-19

#### Bug 修复

- 部分安全修复
- 合并请求后发送的 Web 钩子推送内容包含错误的提交 ID [#4442](https://github.com/gogs/gogs/issues/4442)
- HTML 标签 go-import 未响应正确的值 [#4832](https://github.com/gogs/gogs/issues/4832)

#### 新增特性

- 添加钉钉 Web 钩子支持 [#4773](https://github.com/gogs/gogs/pull/4773)
- 支持合并请求前先进行衍合操作 [#4798](https://github.com/gogs/gogs/issues/4798)

#### 功能改进

- 在 LDAP BindDN 中支持使用 '%s' 作为用户名占位符 [#2526](https://github.com/gogs/gogs/issues/2526)
- 允许通过环境变量指定 Docker 容器内 git 用户的 UID [#3520](https://github.com/gogs/gogs/issues/3520)
- 添加仓库设置以便在检查合并请求冲突时忽略空白符的差异 [#4834](https://github.com/gogs/gogs/issues/4834)

#### 其它变更

- 添加新语种支持：斯洛伐克语

### 0.11.29 @ 2017-08-15

#### Bug 修复

- 如果仓库曾经为公开的，则变为私有后相关活动信息未被设为私有 [#4414](https://github.com/gogs/gogs/issues/4414)
- Web 钩子不接受 IPv6 URL [#4428](https://github.com/gogs/gogs/issues/4428)
- 通过代码提交关闭工单后没有发送邮件提醒 [#4430](https://github.com/gogs/gogs/issues/4430)
- 探索页面分页不正确 [#4441](https://github.com/gogs/gogs/issues/4441)
- `/api/v1/repos/search` 返回空值 [#4522](https://github.com/gogs/gogs/issues/4522)
- 创建合并请求完成后发生错误 [#4572](https://github.com/gogs/gogs/issues/4572)

**更早的变更日志可以在 [GitHub](https://github.com/gogs/gogs/releases?after=v0.11.29) 上找到。**
