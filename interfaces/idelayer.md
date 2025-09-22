---
description: >-
  IDelayer là một interface định nghĩa hợp đồng (contract) cho việc xử lý tạm
  dừng . Nó cung cấp một phương thức delay (ms: number) cho phép dừng thực thi
  trong một khoảng thời gian
---

# IDelayer

```typescript
export interface IDelayer {
  delay(ms: number): Promise<void>
}
```

* Input
  * ms (bắt buộc): thời gian tạm dừng (đơn vị: milliseconds).
* Output
  * Trả về một `Promise<void>` được resolve sau khi hết thời gian chờ.

