# Gulp執行問題
## 補充資料
-  使用gulp(安裝、監聽編譯都ok)，若關閉命令提示字元後，下次要再使用，是再打開命令提示字元，然後只要針對專案資料夾再次啟動gulp指令一個動作即可
-  [Gulp 專案的 README 更多的說明與操作流程](https://github.com/hexschool/web-layout-training-gulp/blob/master/README.md)
-  [這是在講 Gulp 不是飲料是任務自動化工具這件事：GitHub Page篇](https://hsiangfeng.github.io/gulp/20190613/2745753059/)

### 部署步驟 gh-pages

先新增一個repositary，接著執行以下指令 
- git init
- git add .
- git commit -m 'first commit'

- git remote add origin [GitHub Repositories 這個專案頁面上提供的的repo網址] //加入遠端的分支
- git branch -M main //修改目前分支的名稱
- git push -u origin master // 僅限第一次輸入，往後只需要輸入 git push

- gulp build - 執行編譯模式(不會開啟瀏覽器)
- gulp deploy - 將 dist 資料夾部署至 GitHub Pages

# 網頁切版直播班 Gulp 範例

## 指令列表
- `gulp` - 執行開發模式(會開啟模擬瀏覽器並監聽相關檔案)
- `gulp build` - 執行編譯模式(不會開啟瀏覽器)
- `gulp clean` - 清除 dist 資料夾
- `gulp deploy` - 將 dist 資料夾部署至 GitHub Pages

## 說明

除了 Boostrap CSS 與 Boostrap JavaScript 需要掛 CDN 之外，本身已經內建打包 jQuery 3.5.1。

若有需要調整相關路徑參數可在 envOptions.js 中調整，但建議不要隨意調整導致 Gulp 無法正常運行。

假使對於 Gulp 不熟悉會建議不要任意調整 gulpfile.js 底下的資料任一檔案，避免出現無法正常運作之問題。

## 支援的監聽

目前支援 HTML、ejs、JavaScript、Images、SCSS 監聽並自動重新刷新。

圖片新增時也會自動刷新。

## 部署 gh-pagse 流程說明

部署前請務必先將該 Gulp 原始碼上傳到 GitHub Repositories 也就是初始化 GitHub，因此通常第一步驟會輸入以下指令

```cmd
git add .
git commit -m 'first commit'
git remote add origin [GitHub Repositories Url]
git push -u origin master // 僅限第一次輸入，往後只需要輸入 git push
```

當將 Gulp 初次部署之後就可以輸入 `gulp build` 進入生產模式，當生產完畢之後最後只需要輸入 `gulp deploy` 即可完成 GitHub Pages 部署。


