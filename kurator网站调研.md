# kurator网站方案调研

## 调用目标

参考现有的项目，调研了以下四种方案：

### [hugo](https://github.com/gohugoio/hugo)   + docsy主题：

hugo 目前有 65.4k Stars； docsy 来自google，目前有 2.1k Stars。

[示例网站](https://example.docsy.dev/) 

使用者：Kurator 项目当前的做法，k8s官网。

优点：现在已经在使用了，只需继续添加内容即可。

缺点: 支持的组件比较少，比如一个展示项目当前star数量的功能，其他地方可能就一行代码，但是docsy没有找到相应的支持。

默认主页风格可能不适合Kurator，k8s虽然也是使用该主题，但是相对于基础的主题，多了很多自己的内容。主题附带的搜索功能，会搜出来google提供的广告。

### hugo + academic 旧主题：

使用者： [KubeEdge](https://kubeedge.io/zh/)， [Volcano](https://volcano.sh/zh/)

优点： 组件丰富，使用简单，风格契合

缺点： 因为经过一次改版，academic旧版本的包括文档等链接已经打不开。如果想要使用其他组件，可能没有可参考的例子。

### hugo + [academic](ttps://themes.gohugo.io/themes/starter-hugo-academic/) 新主题：

该主题目前 start数量为 2.6k 

[示例网站](https://academic-demo.netlify.app/)

优点： 组件丰富，使用简单，风格契合

缺点： 可能是属于一票否决的缺点：新版的academic 最下面有一行删除不掉。官网介绍是需要sponsor才能去掉。

![image](https://user-images.githubusercontent.com/45359033/220029062-2fe415d8-fc76-4a33-aea9-19f625bd17b9.png)

![image](https://user-images.githubusercontent.com/45359033/220029718-777d48bc-5c21-4bca-8a4c-d2a501304055.png)



### [docusaurus](https://github.com/facebook/docusaurus)  

该工具来自Facebook，目前42.3k stars

[示例网站](https://docusaurus.io/)

使用者： [Karmada](https://karmada.io/zh/) 

优点：star数量多，社区活跃，致力于开源项目网站
 
缺点：不如hugo使用方便，需要安装npm


## 结论

如果确定方案的话，可以先做一个使用 公开图源的图标/图片 做一个基础的版本。

个人倾向于 docusaurus （更有利于后续的长期维护）
