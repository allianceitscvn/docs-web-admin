# Table with paging server

Screen Config

Table.hasPagingRemote: true

Table.optionsTable.sizePerPage: 20

Query Api

Page

PageSize

Sort

Khác biệt

* Lần đầu gọi List với Page = 1 , PageSize
* Qua trang 2 gọi List với Page = 2, PageSize
* Khi Filter -> Page = 1
* Khi ReloadTable -> Page = current page

Test case

1. Mở table -> qua trang 2 -> qua trang 1 -> qua trang 2
2. Mở table -> qua trang 2 -> filter server&#x20;
