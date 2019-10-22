# ctsi-topology
```
基于mxGraph的拓扑图，目前只有展示功能，编辑功能后续会更新。
```

## Project setup
```
yarn install
npm install
```

### Compiles and hot-reloads for development
```
yarn run serve
npm run serve
```

### Compiles and minifies for production
```
yarn run build
npm run build
```

### Run your tests
```
yarn run test
```

### Lints and fixes files
```
yarn run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### 帮助信息

#### 属性

 参数 | 说明 | 类型 | 可选值 | 默认值
 ---- | ---- | ---- | ---- | ----
 data | 展示数据 | array | —— | ——
 node-key | 每个节点用来作为唯一标识的属性，整个拓扑图应该是唯一的 | string | —— | ——
 node-dbclick | 点击事件是否双击 | boolean | —— | false
 connect-line | 连线数据配置选项，具体看下表 | array | ——
 connect-line-style | 连线样式配置选项，具体看下表，各属性之间用分号(;)连接，如：width=1;color=#c5c5c5 | string | —— | width=1;  color=#c5c5c5;  emphColor=#1296db;  dotted=false;  arrow=true
 props | 配置选项，具体看下表 | object | —— | ——
 operate-button | 是否展示操作按钮 | boolean | —— | true
 operate-button-position | 操作按钮位置 | string | top left / top center / top right  bottom left / bottom center / bottom right  | top center
 
#### connect-line

 参数 | 说明 | 类型 | 可选值 | 默认值
 ---- | ---- | ---- | ---- | ----
 local | 起点，值为节点/内置节点唯一标识 | string,number | —— | ——
 opposite | 终点，值为节点/内置节点唯一标识 | string,number | —— | ——
 style | 样式 | string | —— | 同connect-line-style
 
#### connect-line-style

 参数 | 说明 | 类型 | 可选值 | 默认值
 ---- | ---- | ---- | ---- | ----
 width | 宽度，鼠标经过连线或者连线所在节点时，连线宽度为当前值得两倍 | number | —— | 1
 color | 颜色 | string | —— | #c5c5c5
 emphColor | 强调颜色，鼠标经过连线或者连线所在节点时的颜色 | string | —— | #1296db
 dotted | 虚线 | boolean | —— | false
 arrow | 箭头 | boolean | —— | true
 
#### props

 参数 | 说明 | 类型 | 可选值 | 默认值
 ---- | ---- | ---- | ---- | ----
 label | 指定节点标签为节点对象的某个属性值 | string | —— | ——
 children | 指定子节点为节点对象的某个属性 | string | —— | ——
 detailConfig | 指定节点详情展示的配置 | object | —— | ——
 build-in-name | 指定节点的内置节点为节点对象的某个属性值 | string | —— | ——
 build-in-key | 指定内置节点的唯一标识的属性，整个拓扑图应该是唯一的 | string | —— | 同节点node-key
 build-in-detailConfig | 指定内置节点详情展示的配置 | object | —— | 同节点detailConfig
 
#### 事件

 事件名称 | 说明 | 回调参数
 ---- | ---- | ----
 node-click | 节点被点击时的回调 | 共一个参数：传递给data属性的对象中该节点所对应的对象
