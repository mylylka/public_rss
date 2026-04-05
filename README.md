# 小宇宙配置步骤（只需要做1次）

## 第一步：先把服务跑起来
1. 发布完一期节目后，运行：
   ```
   cd /Users/liujing/.agents/skills/jingjing-podcast-publisher
   npm run server
   ```
2. 新开一个终端窗口，运行：
   ```
   npm run ngrok
   ```
3. 复制 ngrok 返回的公网 RSS 地址，格式是 `https://xxx.ngrok.io/rss.xml`

## 第二步：去小宇宙提交RSS
1. 打开小宇宙创作者后台：https://creator.xiaoyuzhoufm.com/
2. 登录你的账号
3. 点「创建播客」→ 选择「导入已有播客」
4. 粘贴刚才的公网 RSS 地址，提交审核
5. 等待审核通过（通常1-2小时）

## 第三步：后续更新
审核通过后，以后你发布新节目：
- 不用再重复提交，小宇宙会自动每小时拉取你的RSS更新
- 只要你本地的 server 开着就行
- ngrok如果重启地址变了，去小宇宙后台更新一下RSS地址就行

## 注意
- ngrok免费版地址每次重启都会变，建议你搞个固定的公网地址更方便
- 本地server要一直开着，小宇宙才能拉到你的节目内容
