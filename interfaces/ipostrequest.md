---
description: >-
  IPostRequest là một interface định nghĩa hợp đồng (contract) cho việc thực
  hiện các HTTP POST request trong ứng dụng. Nó quy định cách truyền tham số vào
  và kiểu dữ liệu trả về, giúp code rõ ràng và d
---

# IPostRequest

```typescript
export interface IPostRequestParams {
  url: string;
  body?: any; // dữ liệu gửi kèm (JSON, FormData, v.v.)
  params?: Record<string, any>;
  headers?: Record<string, string>;
  timeout?: number;
  responseType?: "json" | "blob" | "text" | "arraybuffer";
}

export interface IPostRequest {
  post<T>(options: IPostRequestParams): Promise<T>;
}

```

* &#x20;**input** (IPostRequestParams)
  * `url` (bắt buộc): endpoint cần gọi.
  * `body` (tùy chọn): payload gửi lên server (thường là JSON hoặc FormData).
  * `params` (tùy chọn): query string gắn vào URL.
  * `headers` (tùy chọn): custom headers cho request.
  * `timeout` (tùy chọn): thời gian chờ tối đa.
  * `responseType` (tùy chọn): kiểu dữ liệu trả về (`json`, `blob`, `text`, `arraybuffer`).
