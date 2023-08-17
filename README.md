# 股票每日成交統計程式

這個程式用於從台灣證券交易所網站抓取股票每日成交統計資料並將其保存到 Excel 檔案中。

## 使用說明

1. 安裝必要套件：

    在執行程式之前，請確保已安裝所需的套件。可以使用以下指令安裝：

    ```
    pip install requests openpyxl
    ```

2. 設定檔案：

    在程式執行之前，請先編輯 `setting.xml` 檔案，設定以下資訊：

    - `<url>`: 股票每日成交統計資料網址。
    - `<excelName>`: 欲儲存的 Excel 檔案名稱。
    - `<startYear>`: 資料開始年份。
    - `<startMonth>`: 資料開始月份。
    - `<endYear>`: 資料結束年份。
    - `<endMonth>`: 資料結束月份。
    - `<stockNo>`: 股票代號。

3. 執行程式：

    執行程式 `main.py` 從台灣證券交易所抓取股票每日成交統計資料，並將其儲存到指定的 Excel 檔案中。

    ```
    python main.py
    ```

4. 查看結果：

    程式執行完成後，您將在當前目錄中找到您指定的 Excel 檔案，該檔案將包含股票每日成交統計資料。

## 注意事項

- 請確保已安裝 Python 以及所需的套件。
- 請編輯 `setting.xml` 檔案以設定程式參數。

## 設定範例

以下是 `setting.xml` 檔案的範例內容：

```xml
<params>
    <url>https://www.twse.com.tw/rwd/zh/afterTrading/STOCK_DAY</url>
    <excelName>統一商</excelName>
    <startYear>2023</startYear>
    <startMonth>01</startMonth>
    <endYear>2023</endYear>
    <endMonth>06</endMonth>
    <stockNo>2912</stockNo>
</params>
