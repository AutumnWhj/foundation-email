# Foundation for Emails Template

本项目HTML邮件模板基础项目，可自动生成适配多邮件客户端的模板。
## 安装并使用
建议下载原项目的代码：https://github.com/foundation/foundation-emails-template
我这份已经被我魔改了~
node npm安装
```bash
brew install node
// 检测是否安装成功 node版本最好是v14.17.0 否则sass的关联依赖会装不上~
node -v 
// 转成taobao镜像
npm install -g cnpm --registry=https://registry.npm.taobao.org
// 安装依赖
cnpm install
```
## 调试开发

- step1：在page下新建html文件`resume.html`
- step2：执行`npm run build`，会自动打开3000端口服务。
> 若你的html文件命名为`resume.html`则修改访问地址为[http://localhost:3000/resume.html](http://localhost:3000/resume.html)，其他同理。

执行 `npm run build`后 `dist`目录下会生成同名的`.html`文件，这份文件为最终的适配文件。
## html文件
### 头部与尾部
`/layout/default.html`下已经定义HTML邮件的头部与尾部，因此新建的html文件只需要写入内容部分即可。如：
### 变量声明
系统支持[handlebarsjs模板语法](https://handlebarsjs.com/)，有条件的同学可通过条件渲染，来增加模板的复用性，变量声明可直接在html文件头部如下定义并以花括号的方式使用
### 组件使用
系统集成一些语义化的标签🏷供使用，示例如下：（起了服务的可访问[http://localhost:3000/demo.html](http://localhost:3000/readme.html)）
#### row与columns
row表示行，columns表示单元格（列），以下即一行三列。`class`定义文本居中居左或居右。还可通过`small="x"`定义columns所占的份数（供24份）
#### 按钮button
![image.png](https://cdn.nlark.com/yuque/0/2021/png/2777249/1635221353203-8295d429-339a-439b-b232-a591502f90e9.png#clientId=u5098cf56-ee47-4&from=paste&height=261&id=ubd8bac2e&margin=%5Bobject%20Object%5D&name=image.png&originHeight=522&originWidth=1248&originalType=binary&ratio=1&size=121802&status=done&style=none&taskId=u87cb0c32-025e-4639-bc00-3de7346ef38&width=624)
#### callout框框
![image.png](https://cdn.nlark.com/yuque/0/2021/png/2777249/1635221470337-df053c28-718f-41b4-aab5-4d570bf6efbe.png#clientId=u5098cf56-ee47-4&from=paste&height=75&id=u7bd9fae0&margin=%5Bobject%20Object%5D&name=image.png&originHeight=150&originWidth=1177&originalType=binary&ratio=1&size=25266&status=done&style=none&taskId=ua536fe7e-9f9c-488f-afa7-1966fea96a0&width=588.5)
#### 间隔与span的使用
![image.png](https://cdn.nlark.com/yuque/0/2021/png/2777249/1635221508404-37e3857d-faf5-4f33-8b5c-519b1e985106.png#clientId=u5098cf56-ee47-4&from=paste&height=168&id=u73b43e49&margin=%5Bobject%20Object%5D&name=image.png&originHeight=336&originWidth=943&originalType=binary&ratio=1&size=64131&status=done&style=none&taskId=u96d2a3a0-fe1e-4590-9fa0-bf01bae6d0d&width=471.5)
## 总结
新建一个html文件后，在`pages/index.html`首页文件中中新增一个item，并加以语义化的描述，方便查看当前咱们服务中所有的HTML邮件模板，并且有利于调试。
## 源码参考 
https://github.com/foundation/foundation-emails