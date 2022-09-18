# Git-Is-Good

Tải file về rồi unzip nó ra, vào trong Directory vừa unzip được.

Khi mà mình unzip ra, để ý có 1 file flag, mình tìm tới file đó. Nhưng như phần mô tả nói, nó đã bị redacted.

Title của challenge nhắc là Git is good, vậy nên ta nghĩ tới git để giải challenge này.

Vì file flag.txt đã bị redacted, mình dùng `git log` để xem các lần thay đổi của file.

```
commit d10f77c4e766705ab36c7f31dc47b0c5056666bb (HEAD -> master)
Author: LaScalaLuke <lascala.luke@gmail.com>
Date:   Sun Oct 30 14:33:18 2016 -0400

   Edited files

commit 195dd65b9f5130d5f8a435c5995159d4d760741b
Author: LaScalaLuke <lascala.luke@gmail.com>
Date:   Sun Oct 30 14:32:44 2016 -0400

   Edited files

commit 6e824db5ef3b0fa2eb2350f63a9f0fdd9cc7b0bf
Author: LaScalaLuke <lascala.luke@gmail.com>
Date:   Sun Oct 30 14:32:11 2016 -0400

   Edited files
```

Tiếp đến, sử dụng  `git diff` để so sánh giữa 2 lần thay đổi. Mình so commit đầu tiên với commit thứ 2.

`git diff d10f77c4e766705ab36c7f31dc47b0c5056666bb 195dd65b9f5130d5f8a435c5995159d4d760741b`

Và được kết quả là Flag.
