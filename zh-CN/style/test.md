<style>
/* 方法1：使用 ::before 伪元素 */
.empty-content::before {
  content: "默认内容";
  color: #999;
}

/* 方法2：使用属性选择器和 data-* 属性 */
[data-placeholder]:empty::before {
  content: attr(data-placeholder);
  color: #999;
}

/* 方法3：使用 :empty 选择器 */
.default-content:empty::after {
  content: "暂无内容";
  color: #ccc;
  font-style: italic;
}
ic {
  font-style: italic;
  color: gray;
}
ic:empty::after {
  content: "暂无内容";
  color: #ccc;
  font-style: italic;
}

</style>

<!-- 使用示例 -->
<div class="empty-content"></div>

<div data-placeholder="请输入内容"></div>

<div class="default-content"></div>

<ic></ic>