# Git 协作规范

## 一、分支
- main：主分支，只放能跑的代码，不直接在上面写功能
- 每人开自己的分支：feat/姓名-模块名
  例：feat/tangwc-upload、feat/liuxh-admin

## 二、每天开工前
git checkout main
git pull origin main
git checkout 你的分支
git merge main        # 把别人的最新代码合进来

## 三、提交规范
git add 具体文件名     # 别用 git add .
git commit -m "类型: 做了什么"
git push origin 你的分支

类型只用这5个：
- feat: 新功能
- fix: 修bug
- docs: 改文档
- style: 改样式
- refactor: 重构

例：feat: 新增图片上传组件

## 四、合并流程
1. 自己分支 push 完
2. 到 GitHub 上发 Pull Request（base 选 main）
3. 找另一个人看一眼，点 Merge
4. 合并后本地：切回 main → pull → 删掉自己的旧分支

## 五、冲突怎么办
1. 别慌，别乱删代码
2. VS Code 会标出冲突块，上面是你的、下面是别人的
3. 两边代码都保留，手动删掉 <<<< ==== >>>> 这些标记
4. 改完 git add 文件 → git commit

## 六、红线
- 不许 git push --force
- 不许直接往 main 推功能代码
- 不许提交 node_modules、.env
- 提交前本地先跑一遍，能启动才推