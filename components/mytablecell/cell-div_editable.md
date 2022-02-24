# Cell: div\_editable

## Check list

<table><thead><tr><th data-type="checkbox">Done</th><th>Check</th><th>Description</th></tr></thead><tbody><tr><td>true</td><td>Type</td><td>div_editable</td></tr><tr><td>true</td><td>Type With_MyUI</td><td>cell_div_editable</td></tr><tr><td>true</td><td>Class td>div</td><td>mct-div_editable</td></tr><tr><td>true</td><td>Nếu có edit <br>- Có kiểm tra canEdit<br>- Có chế độ readonly<br>- Cập nhật value mới khi update field khác</td><td>OK</td></tr><tr><td>true</td><td>Ngày tạo</td><td>22/2/2022</td></tr><tr><td>true</td><td>Hỗ trợ cho</td><td>v3</td></tr><tr><td>true</td><td>Link document</td><td><a href="https://allianceitsc.gitbook.io/web-admin/components/mytablecell/cell-div_editable">Link</a></td></tr></tbody></table>

## Mô tả

Show như dạng textarea, có thể edit, chiều cao bằng nội dung content

Hỗ trợ lưu dạng html khi bật more.isHTML = true

## Hình ảnh

#### Dạng cơ bản khi edit

![](<../../.gitbook/assets/image (2).png>)

## More

### More riêng

| Key    | Default | Description                    |
| ------ | ------- | ------------------------------ |
| isHTML | false   | Hỗ trợ lưu dạng HTML hay không |
|        |         |                                |

### More cơ bản

{% content-ref url="../../config/more-of-cell/cell.more.classname.md" %}
[cell.more.classname.md](../../config/more-of-cell/cell.more.classname.md)
{% endcontent-ref %}

{% content-ref url="../../config/more-of-cell/cell.more.style.md" %}
[cell.more.style.md](../../config/more-of-cell/cell.more.style.md)
{% endcontent-ref %}

## Cập nhật

* 24/2/2022: Fix lỗi readonly vẫn edit đc
* 23/2/2022: Bổ sung more.isHTML để lưu dạng html

## Task liên quan

* [WEBAPI-7014](https://allianceitscvn.atlassian.net/browse/WEBAPI-7014)&#x20;

