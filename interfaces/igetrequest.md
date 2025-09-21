---
description: >-
  IGetRequest là một interface định nghĩa hợp đồng (contract) cho việc thực hiện
  các HTTP GET request trong ứng dụng
---

# IGetRequest

```typescript
export interface IGetRequestParams {
  url: string;
  params?: Record<string, any>;
  headers?: Record<string, string>;
  timeout?: number;
  responseType?: "json" | "blob" | "text" | "arraybuffer";
}


export interface IGetRequest {
  get<T>(options: IGetRequestParams): Promise<T>;
}

```

* **Input**: được truyền dưới dạng `IGetRequestParams`, bao gồm:
  * `url` (bắt buộc): đường dẫn API cần gọi.
  * `params` (tùy chọn): các query string gắn vào URL.
  * `headers` (tùy chọn): custom headers cho request.
  * `timeout` (tùy chọn): thời gian chờ tối đa.
  * `responseType` (tùy chọn): kiểu dữ liệu trả về (`json`, `blob`, `text`, `arraybuffer`).
* **Output**: trả về một `Promise<T>` chứa dữ liệu từ response.
