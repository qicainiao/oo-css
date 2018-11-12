# o css作用
  - 1.加强代码复用以便方便维护
  -  2.减少css体积。
  -  3.提示渲染效率。
  -  4.组件库思想、栅格布局可共用、减少选择器、方便扩展。
#注意事项
  - 1. 不要直接定义子节点，应该把共性声明放父类
       .mod .inner{}  //建议这样的声明方式
       .inner{}  //不建议这样

  - 2.结构与皮肤相分离。
      <div class="container simpleExt"></div>
      .container{...} //控制结构的class
      .simpleExt{...} //控制皮肤的class

  -  3.容器与内容相分离
      <div class="container">
        <ul>
          <li></li>
          <li></li>
        </ul>
      </div>
       内容可以随时抽离出去。
  -  4. 抽象出可以重用的元素，建好组件库，在组件库内寻找可用的元素组装页面。
  -  5. 往你想要扩展的对象本身增加class而不是他的父节点。
  -  6. 对象保持独立性。  a做3列  b做2列表互相独立
  -  7. 避免使用ID选择器，  权重太高，无法重用。
  -  8. 避免位置相关的样式。
        #header .container{...},
        #footer .container{...},
        如果container样式一样，那么我直接 .container{}就可以了。
  -  9. 保证选择器相同的权重。
  -  10. 类名 简单清晰 语义化 OOCSS的名字并不影响HTML语义化。
