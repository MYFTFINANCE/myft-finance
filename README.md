# MYFT Finance Website — GitHub Pages Version

这是适合 GitHub Pages 直接上线的静态网站版本。

## 文件结构

```text
index.html
404.html
.nojekyll
robots.txt
sitemap.xml
assets/
  hero.jpg
  living-room.jpg
  logo.svg
  icon-home.svg
  icon-invest.svg
  icon-refinance.svg
```

## GitHub Pages 上线步骤

1. 在 GitHub 新建一个 Public repository，例如 `myft-finance`。
2. 把本文件夹里面的所有文件上传到 repository 根目录，不要只上传外层文件夹。
3. 进入仓库：`Settings` → `Pages`。
4. Source 选择：`Deploy from a branch`。
5. Branch 选择：`main`，文件夹选择：`/root`。
6. 保存后等待 1–2 分钟。
7. GitHub 会生成网址，例如：

```text
https://你的用户名.github.io/myft-finance/
```

## 绑定自定义域名

在 `Settings` → `Pages` → `Custom domain` 输入你的域名，例如：

```text
www.myft.com.au
```

然后到 Namecheap DNS 添加：

```text
Type: CNAME
Host: www
Value: 你的GitHub用户名.github.io
```

如果还要让根域名 `myft.com.au` 也能访问，请添加 GitHub Pages 的 4 条 A Record：

```text
Host: @  Value: 185.199.108.153
Host: @  Value: 185.199.109.153
Host: @  Value: 185.199.110.153
Host: @  Value: 185.199.111.153
```

最后回到 GitHub Pages 勾选 `Enforce HTTPS`。

## 上线后建议修改

绑定真实域名后，把 `robots.txt` 和 `sitemap.xml` 里面的 `your-domain.com` 改成你的真实域名。
