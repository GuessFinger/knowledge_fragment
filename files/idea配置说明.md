#### 2018年12月12日15:37:57

- idea需要安装的插件

  1. 阿里巴巴代码检查工具 [阿里巴巴代码规范](https://github.com/GuessFinger/p3c)
  2. free-idea-mybatis-2018.05.17.zip 通过dao层可以找到xml文件
  3. key-promoter-3.1.1.zip 快捷键提示
  4. translationplugin-2.1.1.zip 如果有网络的话  这个是翻译软件
  5. backgroundImagePlus.jar 这个可以添加背景图



  [idea官方插件网站](https://plugins.jetbrains.com/plugin/8502-background-image-plus)

- idea基本功能设置

  1. 主题以及字体的设置 在settings里面Appearance 和Editor里面

     根据英文可以自己设置  我主要设置的就是 主题 ，主题字体，编辑字体

     还有控制字体这几个。

  2. serializable动态提示

     在Editor 里面的 <u>inspection</u>(检查)  里面搜索 serial  勾选中 

     ​	Serializable class without serialVersionUID

  3. **类注释** 打开file->setting->Editor->Filr and Code Templates->Includes->File Header 

```java
/**
  * @Author :
  * @Description: 
  * @Date: Created in ${TIME} ${DATE}
  */

```

​                 说明的TIME 和DATE 都是在下方有说明的



​	   4. **方法注释**：打开file->setting->Editor->LiveTemplates点击右边上面那个绿色的+号，选择Template

​		Group双击，然后弹出一个窗口，随便添加一个名字，我这里添加的是MyGroup然后点击OK   

​		然后再添加 live  template

​		要设置的就是 用什么键 + table 进行调用 以及应用范围 还有 抬头用到函数在edit variables中设置​					 

```java
/**
  * @Author :
  * @Description: 
  * @Date: Created in $time$ $date$
  * @PARAM: $param$
  */
```

​                 如果有$param\$ 我们就需要在edit variables 中 param中设置下面这个

​                groovyScript("def result=''; def params=\"${_1}\".replaceAll('[\\\\[|\\\\]|\\\\s]', '').split(',').toList(); for(i = 0; i             

​               < params.size(); i++) {result+=' * @param ' + params[i] + ((i < params.size() - 1) ? '\\n\\b' : '')}; return   

​               result", methodParameters())

