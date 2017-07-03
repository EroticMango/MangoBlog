# 开张
### 安装开发环境
#### 1. 安装Homebrew
打开**Terminal**, 输入[命令]():
```ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```

__验证安装:__
```brew -v```

#### 2. 安装Node.js(npm)
**安装:** 这里[跳转](http://nodejs.cn)进入下载并**手动**安装(安装完node.js会自动配置npm管理)

**替换:** nmp源地址, 命令行:
```bash
$ npm config set registry https://registry.npm.taobao.org
-- 配置后可通过下面方式来验证是否成功
$ npm config get registry
-- 或 npm info express
```

**推荐:** 使用cnpm(淘宝定制的支持gzip压缩)命令行工具替换默认的npm命令:
```npm install -g cnpm --registry=https://registry.npm.taobao.org```
#### 3. 安装WebStorm
&emsp; ##### 1. IDE建议使用[WebStorm](http://www.jetbrains.com/webstorm/), 优点自不必多说, 看普及率就知道了, SublimeText也不错, 需要安装一些拓展和插件
&emsp; PJ步骤: 
![WebStorm](http://testmuta.oss-cn-hangzhou.aliyuncs.com/iOSUpdateFolder/WebStorm.png)

&emsp; ##### 2. 建议安装**watchman**, 
&emsp; &emsp; 这个插件用于监控bug文件和文件变化 ，并且可以触发指定的操作,在终端中输入下面的[命令]():
```brew install watchman```
&emsp; ##### 3. 强烈建议安装**Flow**,
&emsp; &emsp; 这是一个 JavaScript 的静态类型检查器，建议安装它，以方便找出代码中可能存在的类型错误,在终端输入下面的代码,如果提示command not found,请加上sudo获得最高权限
```brew install flow```

#### 4. 使用create-react-app快速构建React开发环境
**安装create-react-app开发工具**(没安装cnpm的可以使用默认的npm命令)
```cnpm install -g create-react-app```

**创建一个react工程**(进入自定义的react工程文件夹)
```bash
$ create-react-app first-reactapp
$ cd first-react/
$ npm start
```

随后在浏览器中打开:[http://localhost:3000/]()

#### 5. Hello world
```$ open first-react/src/App.js```
进入**修改**里面的一些代码:
```js
import React, { Component } from 'react';
import logo from './logo.svg';
import './App.css';
class App extends Component {
  render() {
    return (
      <div className="App">
        <div className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <h2>Hello world</h2>
        </div>
        <p className="App-intro">
          可以在 <code>src/App.js</code> 中自定义哦.
        </p>
      </div>
    );
  }
}
export default App;
```
修改后打开:[http://localhost:3000/]()即可查看修改结果

#### Webstorm快捷键
```
MAC苹果系统：
快捷键	作用
command + d	副本当前行或选中的区块
command + f	查找当前文档
command + g	跳转到文档的某一行某一列
command + p	显示参数信息
command + r	替换当前文档
command + w	选中当前单词、行、区块等
command + y	删除整行
command + mouseover	显示主要信息
command + [	移动光标到代码块前
command + ]	移动光标到代码块尾
command + +	折叠区块
command + -	展开区块
command + ->	光标移到行尾
command + <-	光标移到行头
快捷键	作用
command + option + t	将代码以某种格式包括起来
command + option + l	将代码格式化
快捷键	作用
command + shift + u	切换大小写
command + shift + [	选中到代码块前
command + shift + ]	选中到代码块尾
command + shift + +	折叠所有区块
command + shift + -	展开所有区块
快捷键	作用
shift + return	在任意位置换行
shift + F6	高级修改，可快速修改光标所在的标签、变量、函数等
control + shift + f	find in path
control + shift + j	合并行
control + shift + r	replace in path
快捷键	作用
option + delete	delete to word start
option + fn + delete	delete to word end
option + ->	以单词为单位移动光标
option + <-	以单词为单位移动光标
```














