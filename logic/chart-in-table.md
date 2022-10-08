# Chart in table

## Chuẩn bị

### Data

* Sử dụng Data từ List
*

### Cấu hình chart

* Lấy từ Options.Data.ChartConfig.Charts

## Thành phần vùng chart

* Expand
* Title
* Buttons tab multi chart
* Chart

## Vấn đề

### Vấn đề 1

Khi render chart ở tab, các graph\_id bị trùng -> render chart bị sai

#### Giải pháp

graph\_id sử dụng các tham số sau để tránh bị trùng&#x20;

* ScreenCode +&#x20;
* prefixId trong configPagePage +&#x20;
* type của chart&#x20;

### Vấn đề 2

Khi render nhiều chart google, tạo ra quá nhiều thẻ div ở body dư thừa

### Vấn đề 3

Mặc định muốn ẩn/hiện vùng table chart

#### Giải pháp

Sử dụng Options.ConfigChart.Config.DefaultShowContent

Vấn đề 4

Chủ động cấu hình config chart từ Config Screen

Sử dụng ConfigScreen.Page.configChart
