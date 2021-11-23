# subject-selling

## Author 
### limei
### zhangyufeng
### songshanshan


## 安装依赖
npm install

## 本地启动
npm run dev

## 生产打包
npm run build

## 配置 vant
import Vue from 'vue'
import { Button } from 'vant'
Vue.use(Button)

## 公共组件使用

### dialog弹窗
this.$dialog({
  title: '弹窗标题',
  text: '弹窗内容',
  // type: 'input', // 只有type = input 时是有输入框的
  // placeholder: '请输入内容文本...',
  // length: 10,
  showCancelBtn: false, // 是否显示取消按钮
  confirmText: '确定',
  cancelText: '取消',
  confirm () {}
})

### loading加载
this.$loading.hide()
this.$loading.show()

### toast提示
this.$toast({
  msg: '保存成功',
  type: 'success', // fail  warning   loading  success
  timeout: 1500, // 默认
})


## axios
/*
  * url 请求接口地址
  * data 请求参数
  * loading 请求该接口时是否展示loading加载状态
*/
## get 请求
this.$http.get(url, data, loading).then((response) => {
  resolve(response)
},(err) => {
  reject(err)
}).catch((error) => {
  reject(error)
})

## post请求
this.$http.post(url, data, loading).then((response) => {
  resolve(response)
},(err) => {
  reject(err)
}).catch((error) => {
  reject(error)
})


## router配置
{
	path: '/home',
	name: 'Home',
	component: resolve => reqire(['../views/Home.vue'], resolve),
  meta: {
    title: '首页',
    keepAlive: false, // 是否缓存该页面
    auth: true // 该页面是否需要登陆才可以进入
  },
}


## utils 工具
this.utils.方法名


## 操作cookie
global.setCookie(key, value, expires, domain)
global.getCookie(key)
global.removeCookie(key)


## 使用commonTool里的方法
this.commonTool.方法名