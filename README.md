# jiangbao-hugo-blog
基于[`hugo`](https://gohugo.io/)搭建的个人博客

## 预览

* 个人主页：[www.u9c8d.com](http://www.u9c8d.com)
* github page：[jiangbao.github.io](https://jiangbao.github.io)


## Start
1. install hugo
    ```shell
    brew install hugo
    ```

2. clone repository
    ```shell
    git clone git@github.com:JiangBao/jiangbao-hugo-blog.git
    ```

3. init submodule
    ```shell
    git submodule update --init --recursive
    ```

## Usage
1. 新建文章

   ```shell
   hugo new "posts/new-post-title.md"
   ```

2. 本地服务

   ```shell
   hugo serve
   ```

3. 开发与部署

   本地开发完成后，直接提交至仓库，目前使用`github actions`自动部署，具体配置见仓库下`./github/workflows/deploy.yaml`

