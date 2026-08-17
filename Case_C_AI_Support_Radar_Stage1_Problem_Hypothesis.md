# Case C — AI Support Radar
## Chặng 1 — Problem Hypothesis

---

## 0. Assumptions & Biases

### 0.1 Những assumption đang ẩn trong solution directive

| STT | Assumption | Vì sao đây mới chỉ là giả thuyết | Cách kiểm chứng qua discovery |
| :--- | :--- | :--- | :--- |
| 1 | Các tín hiệu hành vi vi mô (di chuyển slide, dừng lâu, xem lại, highlight, ghi chú, sửa đáp án, chat AI) phản ánh chính xác trạng thái không hiểu bài (struggle). | Học viên dừng lâu ở slide có thể do bị xao nhãng bởi việc riêng, mở tab khác, hoặc đơn giản là slide đó quá hay và họ đang suy ngẫm sâu (deep learning). Việc sửa đáp án có thể phản ánh sự cẩn thận chứ không phải bối rối. | Trong phỏng vấn, yêu cầu học viên mở lại lịch sử học tập gần nhất và thực hiện kỹ thuật hồi tưởng (retrospective think-aloud) để giải thích ý đồ thực tế đằng sau các thao tác đó. |
| 2 | Nhu cầu hỗ trợ của học viên khi gặp khó khăn là đủ lớn và họ không thể tự giải quyết bằng các phương pháp khác. | Học viên có thể tự khắc phục bằng cách tra cứu Google, xem video bổ trợ trên YouTube, hoặc thảo luận nhóm với bạn bè mà không cần đến giảng viên. | Hỏi học viên về các lần họ gặp bài khó gần đây: Họ đã làm gì? Mất bao lâu để tự giải quyết? Tỷ lệ họ phải bỏ cuộc nếu không có ai giúp là bao nhiêu? |
| 3 | Giảng viên có mong muốn và coi việc chủ động phát hiện từng học viên gặp khó khăn là trách nhiệm cốt lõi của họ. | Trong các khóa học trực tuyến hoặc kết hợp (blended), giảng viên thường đề cao tính tự học (learner autonomy). Nhiều người chỉ chấm điểm thi cuối kỳ và không có nhu cầu can thiệp sâu vào tiến trình học ngày ngày. | Phỏng vấn giảng viên về triết lý giảng dạy trực tuyến của họ: Họ coi vai trò của mình là người dẫn dắt chủ động tương tác hay người hỗ trợ thụ động khi được yêu cầu? |
| 4 | Giảng viên có đủ quỹ thời gian, năng lượng và năng lực (capacity) để xử lý một danh sách queue học viên cần hỗ trợ sau mỗi phiên học. | Giảng viên thường bận rộn soạn bài, nghiên cứu, chấm điểm hoặc dạy nhiều lớp. Việc chủ động nhắn tin/gọi điện hỗ trợ cá nhân hóa cho hàng chục học viên mỗi tuần có thể gây quá tải trầm trọng. | Hỏi giảng viên về thời gian biểu thực tế: Họ dành bao nhiêu giờ mỗi tuần cho việc tương tác ngoài giờ với học viên? Họ có thể hỗ trợ tối đa bao nhiêu người 1-1 trong một tuần? |
| 5 | Học viên mong muốn và sẵn lòng nhận sự liên hệ chủ động từ giảng viên khi họ đang loay hoay học bài. | Sự can thiệp chủ động dựa trên dữ liệu thao tác có thể tạo ra "hiệu ứng bị giám sát" (surveillance effect/panopticon). Học viên có thể cảm thấy xấu hổ, bị xâm phạm quyền riêng tư hoặc e ngại năng lực của mình bị đánh giá thấp. | Hỏi học viên về cảm xúc của họ trong quá khứ khi được giảng viên chủ động nhắn tin hỏi han đúng phần họ đang học yếu. Họ thấy biết ơn hay thấy e ngại, phòng thủ? |
| 6 | Sự can thiệp/hỗ trợ từ giảng viên thực sự giúp học viên hiểu bài tốt hơn và không bị bỏ lại phía sau. | Hiệu quả can thiệp phụ thuộc rất lớn vào kỹ năng sư phạm cá nhân hóa của giảng viên và mức độ cởi mở của học viên. Nếu giảng viên chỉ giải thích lại y hệt bài giảng cũ, học viên vẫn sẽ không hiểu. | Thu thập phản hồi từ các chương trình kèm cặp (tutoring) hoặc hỗ trợ 1-1 đã từng diễn ra trước đây (nếu có) để đánh giá tỷ lệ cải thiện điểm số thực tế. |
| 7 | Tỷ lệ cảnh báo sai (False Positive) của hệ thống đủ thấp để không gây ra hiện tượng "nhiễu cảnh báo" (alert fatigue) cho giảng viên. | Nếu AI liên tục xếp vào queue những học viên giỏi (chỉ vì họ dừng lại đọc kỹ slide) hoặc học viên bận việc riêng, giảng viên sẽ nhanh chóng phớt lờ và tắt hoàn toàn tính năng này. | Đo lường độ chính xác chẩn đoán của AI bằng cách đối chiếu queue dự đoán với khảo sát tự đánh giá độ hiểu bài của học viên ngay sau phiên học. |
| 8 | Các hành động hỗ trợ được AI đề xuất (action recommendation) là thực tế và khả thi trong bối cảnh vận hành lớp học. | AI có thể đề xuất "gặp riêng 15 phút" hoặc "gửi tài liệu đọc thêm", nhưng giảng viên có thể không có lịch rảnh hoặc không có sẵn tài liệu bổ trợ phù hợp cho phần kiến thức cụ thể đó. | Cho giảng viên xem các mẫu hành động đề xuất giả định và yêu cầu họ đánh giá tính khả thi cũng như mức độ sẵn sàng thực hiện trong thực tế dạy học. |

### 0.2 Những bias dễ mắc trong quá trình khám phá sản phẩm

1. **Solution Bias (Thiên kiến giải pháp)**: Nhóm phát triển quá hào hứng với ý tưởng "AI Support Radar" và giao diện "Support Queue" đến mức bỏ qua việc xác minh xem giảng viên thực sự có thời gian để can thiệp hay không. Pain bị định nghĩa sai lệch thành *"Giảng viên chưa có công cụ AI để quản lý học viên yếu"*.
2. **Confirmation Bias (Thiên kiến xác nhận)**: Khi phỏng vấn giảng viên/học viên, người nghiên cứu chỉ chú ý lắng nghe những câu trả lời dạng *"Tôi rất muốn giúp đỡ học viên"* hoặc *"Tôi rất cần thầy cô giảng bài lại"*, mà phớt lờ những phản hồi về việc học viên thấy phiền phức khi bị theo dõi click slide hoặc giảng viên nói họ không có thời gian nhắn tin riêng.
3. **Automation Bias (Thiên kiến tự động hóa)**: Mặc định tin rằng việc AI tự động phân tích hành vi để tạo queue sẽ ưu việt hơn các phương pháp tương tác tự nhiên hoặc các công cụ tự đánh giá (self-assessment) đơn giản của học viên.
4. **Observer Bias / Hawthorne Effect (Hiệu ứng người quan sát)**: Học viên khi biết mọi hành vi (di chuyển slide, ghi chú, sửa đáp án) đang được ghi lại để đánh giá mức độ hiểu bài sẽ thay đổi hành vi học tập của họ theo hướng đối phó (ví dụ: click slide đều đặn, không dám dừng lại lâu hay sửa đáp án nữa để tránh bị coi là kém cỏi), dẫn đến dữ liệu đầu vào của AI bị méo mó.
5. **Proxy Metric Bias (Thiên kiến chỉ số đại diện)**: Coi các chỉ số kỹ thuật thô như "thời gian dừng trên slide", "số lần sửa đáp án" là thước đo tuyệt đối cho "sự struggle", dẫn đến việc tối ưu hóa mô hình AI để phát hiện các chỉ số này thay vì đi giải quyết khó khăn thực sự về mặt nhận thức của học viên.

---

## 1. Solution

### 1.1 Ghi lại Solution Directive
Hệ thống phân tích các tín hiệu học tập (di chuyển slide, dừng lâu, xem lại, highlight/ghi chú, đánh dấu "Chưa hiểu", sửa đáp án, chat AI) sau mỗi phiên học để AI suy đoán nhu cầu hỗ trợ và xếp ưu tiên, tạo ra một **Support Queue** (danh sách học viên cần hỗ trợ, nội dung khó khăn, tín hiệu chẩn đoán, hành động đề xuất) để giảng viên xem xét và quyết định có chủ động liên hệ can thiệp hay không.

### 1.2 Phân loại đâu là implementation detail

| Thành phần trong directive | Phân loại | Vì sao |
| :--- | :--- | :--- |
| **AI phân tích tín hiệu** | Implementation Detail | AI chỉ là công nghệ thực thi. Khó khăn của học viên có thể được phát hiện bằng các quy tắc logic đơn giản (rules-based), bằng khảo sát tự đánh giá nhanh cuối bài, hoặc do trợ giảng quan sát thủ công. |
| **Support Queue** | Implementation Detail | Đây là một định dạng giao diện hiển thị cụ thể (danh sách hàng đợi). Thông tin học viên cần hỗ trợ có thể được truyền tải qua email báo cáo, thông báo trực tiếp trên danh sách lớp, hoặc tin nhắn chatbot gửi riêng cho giảng viên. |
| **Xếp mức ưu tiên** | Implementation Detail | Đây là cách sắp xếp thứ tự xử lý dữ liệu. Thực tế có thể chỉ cần gom nhóm học viên theo chủ đề kiến thức khó (topic-based) hoặc hiển thị theo thời gian thực thay vì xếp thứ tự ưu tiên. |
| **Instructor review & control** | **Capability** | Khả năng kiểm soát, đánh giá và ra quyết định can thiệp của con người trước khi thực hiện hành động hỗ trợ nhằm đảm bảo tính sư phạm và sự tinh tế trong giao tiếp. |
| **Behavioral signals (slide, click, chat...)** | Implementation Detail | Đây là nguồn dữ liệu thô hiện có trên LMS. Việc chẩn đoán struggle có thể dựa trên các nguồn dữ liệu trực tiếp hơn như điểm quiz nhanh, câu hỏi tự luận ngắn, hoặc tự đánh giá độ tự tin của học viên. |
| **Action recommendation** | Implementation Detail | Đây là tính năng gợi ý bổ trợ. Giảng viên có chuyên môn sư phạm hoàn toàn có thể tự quyết định cách hỗ trợ phù hợp mà không cần AI đề xuất hành động mẫu. |

### 1.3 Viết Capability trung tính
> **Khả năng giúp giảng viên nhận biết kịp thời và chính xác những học viên đang gặp khó khăn trong việc tiếp thu kiến thức sau mỗi phiên học, để họ có phương án hỗ trợ cá nhân hóa phù hợp trước khi học viên bị hổng kiến thức nghiêm trọng.**

### Capability này KHÔNG khẳng định điều gì?
1. Không khẳng định rằng các tín hiệu hành vi ngầm trên LMS (như dừng slide, highlight...) là chỉ báo chính xác nhất cho thấy học viên đang gặp khó khăn sư phạm thực sự.
2. Không khẳng định rằng việc giảng viên chủ động liên hệ 1-1 là phương án hỗ trợ tối ưu và khả thi nhất về mặt thời gian cho cả hai phía.
3. Không khẳng định rằng giảng viên sẽ tin tưởng và sử dụng danh sách chẩn đoán do hệ thống tự động tạo ra để thực hiện can thiệp thực tế.

---

## 2. Change

### 2.1 Chuỗi thay đổi chính (Causal Change Chain)
```text
Solution (AI Support Radar phân tích hành vi học viên)
→ [Output] Tạo ra Support Queue hiển thị học viên có dấu hiệu struggle kèm gợi ý can thiệp.
→ [Information Change] Giảng viên nhận biết sớm và cụ thể học viên nào đang gặp khó khăn ở phần kiến thức nào ngay sau phiên học (thay vì đợi đến kỳ thi).
→ [Behavior Change] Giảng viên dành thời gian xem xét queue và chủ động liên hệ (nhắn tin/gặp riêng) để hỗ trợ học viên.
→ [Intervention] Học viên nhận được sự giảng giải lại hoặc tài liệu bổ trợ cá nhân hóa từ giảng viên.
→ [Learner Response] Học viên giải tỏa được khúc mắc kiến thức, cảm thấy được quan tâm và nỗ lực học tập tiếp.
→ [Outcome] Học viên vượt qua khó khăn học tập, hoàn thành khóa học với kết quả tốt hơn và giảm tỷ lệ bỏ học giữa chừng.
```

### 2.2 Bảng phân tích change chain

| Mắt xích | Loại | Điều phải xảy ra | Team kiểm soát được? | Risk lớn nhất khiến chuỗi gãy |
| :--- | :--- | :--- | :--- | :--- |
| **1. Tạo Support Queue** | Output | AI phân tích chính xác dữ liệu hành vi để lọc ra đúng người thực sự cần hỗ trợ, tránh cảnh báo giả. | Có (về mặt kỹ thuật thuật toán) | Thuật toán chẩn đoán sai nhiều (nhiều False Positive/Negative), gợi ý hành động không thực tế khiến giảng viên mất lòng tin. |
| **2. Giảng viên nhận biết** | Information change | Giảng viên truy cập dashboard, đọc và hiểu rõ lý do học viên bị đưa vào queue sau mỗi phiên học. | Có (về mặt UX/UI hiển thị) | Giảng viên không có thói quen mở dashboard sau giờ dạy, hoặc thông tin hiển thị quá rối rắm khó hiểu. |
| **3. Giảng viên can thiệp** | Behavioral outcome | Giảng viên quyết định bỏ thời gian và công sức để chủ động liên hệ hỗ trợ từng học viên. | Không trực tiếp (chỉ tác động gián tiếp qua thiết kế) | Giảng viên bị quá tải thời gian (lớp quá đông) hoặc thiếu động lực (không có cơ chế khuyến khích tương tác 1-1). |
| **4. Học viên tiếp nhận** | Learner response | Học viên cởi mở chia sẻ khó khăn của mình và tiếp thu hướng dẫn của giảng viên mà không phòng thủ. | Không | Học viên cảm thấy bị e ngại, xấu hổ vì bị theo dõi thao tác vi mô, dẫn đến việc nói dối "em hiểu rồi" để né tránh. |
| **5. Cải thiện kết quả** | Final outcome | Sự can thiệp giúp học viên hiểu bài tốt hơn và tiến bộ rõ rệt trong các bài đánh giá sau đó. | Không | Khó khăn của học viên quá lớn (mất gốc nặng, thiếu thời gian học ở nhà) vượt ngoài tầm giải quyết nhanh của giảng viên. |

### 2.3 Các thay đổi được kỳ vọng
1. **Rút ngắn thời gian phát hiện**: Giảng viên biết được học viên struggle trong vòng 24 giờ sau phiên học thay vì phải đợi 2-3 tuần đến kỳ kiểm tra định kỳ.
2. **Tăng tỷ lệ tương tác chất lượng**: Tăng số lượng cuộc hội thoại hỗ trợ cá nhân hóa có mục tiêu rõ ràng giữa giảng viên và học viên yếu.
3. **Nâng cao sự an tâm của người học**: Học viên cảm thấy môi trường học trực tuyến có sự đồng hành sát sao của giảng viên, giảm cảm giác bị bỏ rơi khi tự học.

### 2.4 Critical dependency (3 mắt xích yếu nhất trong chuỗi)
1. **Mắt xích "Giảng viên chủ động can thiệp (Behavior Change)"**:
   - *Tại sao chưa chắc đúng:* Dạy học trực tuyến thường có quy mô lớp lớn. Việc nhắn tin/gọi điện riêng cho 10-15 học viên sau mỗi buổi học đòi hỏi quỹ thời gian và năng lượng khổng lồ mà giảng viên có thể không có.
   - *Evidence cần:* Dữ liệu phỏng vấn giảng viên về quy trình xử lý học viên yếu hiện tại; quỹ thời gian thực tế họ có thể dành ra cho các hoạt động hỗ trợ ngoài giờ lên lớp.
   - *Hậu quả nếu sai:* Hệ thống tạo ra queue rất đẹp và chính xác nhưng tỷ lệ giảng viên bấm liên hệ gần như bằng 0. Sản phẩm hoàn toàn thất bại vì không tạo ra hành động thực tế.
2. **Mắt xích "Học viên cởi mở phản hồi (Learner Response)"**:
   - *Tại sao chưa chắc đúng:* Học viên có xu hướng giấu dốt hoặc e ngại giảng viên. Việc giảng viên chủ động nhắn tin chỉ rõ *"Thầy thấy em loay hoay sửa đáp án 3 lần ở câu 5"* có thể tạo ra cảm giác bị giám sát (Surveillance effect), khiến học viên cảm thấy không an toàn về mặt tâm lý và có xu hướng né tránh tương tác.
   - *Evidence cần:* Khảo sát tâm lý học viên về việc nhận tin nhắn hỗ trợ chủ động từ giảng viên dựa trên dữ liệu hành vi.
   - *Hậu quả nếu sai:* Học viên tìm cách đối phó (ví dụ: click slide nhanh hơn, không highlight nữa) để tránh lọt vào tầm ngắm của AI Radar, làm giảm hiệu quả học tập thực tế.
3. **Mắt xích "Tính chính xác của tín hiệu hành vi (Output Accuracy)"**:
   - *Tại sao chưa chắc đúng:* Việc di chuyển slide chậm, xem lại bài hay chat AI nhiều có thể là biểu hiện của một học viên rất cẩn thận, tò mò và học sâu (deep learner) chứ không phải đang gặp khó khăn.
   - *Evidence cần:* Đối chiếu chéo giữa dữ liệu log hành vi trên LMS và mức độ tự đánh giá độ hiểu bài thực tế của học viên ngay sau phiên học.
   - *Hậu quả nếu sai:* Giảng viên liên tục can thiệp nhầm vào nhóm học viên khá giỏi, gây phiền toái cho học viên và tạo ra hiện tượng "nhiễu cảnh báo" (alert fatigue) cho giảng viên, dẫn đến việc họ phớt lờ queue.

---

## 3. Actor

### 3.1 Bảng phân tích các Actor trong hệ thống

| Actor | Họ đang làm gì? | Pain hoặc hậu quả có thể có | Họ hưởng lợi thế nào từ giải pháp? | Vai trò trong change chain |
| :--- | :--- | :--- | :--- | :--- |
| **Learner (Học viên)** | Tự học bài trên LMS, xem slide, ghi chú, làm quiz, tương tác với AI chat. | Gặp phần bài khó không biết hỏi ai, ngại hỏi giảng viên vì sợ bị đánh giá, tự loay hoay rồi nản lòng, dễ bỏ học hoặc trượt môn. | Được hỗ trợ giải đáp đúng phần kiến thức đang bế tắc một cách kịp thời và tinh tế; cải thiện kết quả học tập. | Tạo ra các tín hiệu hành vi đầu vào; tiếp nhận sự can thiệp và thay đổi kết quả đầu ra (outcome). |
| **Instructor (Giảng viên chính)** | Soạn bài giảng, dạy học, chấm điểm, quản lý lớp học trực tuyến. | Bị "mù thông tin" về mức độ hiểu bài thực tế của lớp trong khóa học trực tuyến đông người; chỉ biết kết quả khi đã quá muộn (điểm thi cuối kỳ). | Nắm bắt nhanh tình hình hiểu bài của lớp; chủ động can thiệp đúng người, đúng chỗ để nâng cao tỷ lệ hoàn thành khóa học. | Người dùng trực tiếp của Support Queue; đưa ra quyết định duyệt và thực hiện hành động can thiệp sư phạm. |
| **Coach / TA (Trợ giảng)** | Hỗ trợ giảng viên trả lời thắc mắc, chấm bài quiz, kèm cặp học viên yếu. | Bị quá tải bởi các câu hỏi lẻ tẻ hoặc không biết phải tập trung kèm cặp ai trước trong danh sách lớp quá đông. | Có một danh sách ưu tiên rõ ràng các học viên thực sự cần kèm cặp 1-1, tối ưu hóa công sức và thời gian hỗ trợ. | Có thể là người vận hành chính của Support Queue thay giảng viên để thực hiện liên hệ hỗ trợ học viên. |

### 3.2 So sánh vai trò để chọn đối tượng điều tra
* Actor trực tiếp tạo ra behavioral signals? **Learner**
* Actor trực tiếp dùng solution để ra quyết định? **Instructor** (hoặc Coach/TA)
* Actor trực tiếp chịu pain của việc học không hiệu quả? **Learner**
* Actor trực tiếp chịu pain của việc không quản lý được chất lượng dạy học? **Instructor**
* Actor cần thay đổi hành vi để giải pháp có tác dụng? **Instructor** (chủ động liên hệ) & **Learner** (cởi mở đón nhận)
* Actor chịu hậu quả nếu can thiệp sai? **Learner** (bị làm phiền, mất an toàn tâm lý) & **Instructor** (mất thời gian, mất uy tín sư phạm)
* Actor hưởng lợi cuối cùng về mặt kết quả học tập? **Learner**

### 3.3 Chọn actor điều tra trước (Primary Actor)
> **Primary Actor được chọn: Instructor (Giảng viên)**

**Lý do chọn và Trade-off:**
Trong mô hình AI Support Radar này, Giảng viên đóng vai trò là "chốt chặn quyết định" (human-in-the-loop). Cho dù AI có dự đoán chính xác đến đâu và học viên có struggle thế nào, nếu giảng viên không có thời gian mở queue, không muốn chủ động nhắn tin trước, hoặc không biết cách nhắn tin hỗ trợ tinh tế, toàn bộ chuỗi giá trị của sản phẩm sẽ bị đứt gãy ngay lập tức.
* **Pain Uncertainty**: Chúng ta chưa biết chắc giảng viên có thực sự coi việc "chủ động phát hiện và liên hệ sớm" là một pain nghiêm trọng cần giải quyết bằng công cụ hay họ coi đó là việc tự học của học viên.
* **Evidence Accessibility**: Giảng viên khó tiếp cận hơn học viên về số lượng, nhưng họ có thể cung cấp bức tranh rõ ràng về quy trình vận hành, áp lực thời gian và các rào cản sư phạm thực tế.
* **Risk nếu giả định sai**: Nếu tập trung vào học viên trước và thấy họ rất cần giúp đỡ, nhưng sau đó phát hiện giảng viên hoàn toàn không thể dành thời gian tương tác 1-1 sau giờ dạy, sản phẩm sẽ trở thành một tính năng chết trên dashboard của giảng viên.

### 3.4 Actor cạnh tranh (Secondary Actor)
> Nếu giả định về primary actor (Instructor) sai (ví dụ: giảng viên chỉ phụ trách chuyên môn bài giảng, không tham gia hỗ trợ vận hành 1-1), nhóm sẽ chuyển sang điều tra **Coach/TA (Trợ giảng)**.
> **Vì sao:** Trợ giảng thường là người trực tiếp bám sát lớp học hàng ngày, có nhiệm vụ trả lời forum/chat và có nhiều thời gian/KPI cụ thể cho việc kèm cặp học viên yếu hơn là giảng viên chính.

---

## 4. Situation & Job

### 4.1 Situation Flow (Quy trình tình huống của Instructor)
1. **Tình huống bắt đầu**: Một tuần học tự học trực tuyến trên LMS của lớp học quy mô lớn (>50 học viên) kết thúc.
2. **User muốn hoàn thành việc gì**: Giảng viên muốn rà soát xem trong lớp có học viên nào đang bị tụt lại phía sau hoặc gặp khó khăn lớn với phần kiến thức tuần này hay không để hỗ trợ kịp thời.
3. **Hiện tại họ làm như thế nào**: Giảng viên mở bảng điểm LMS để xem điểm số các bài quiz ngắn cuối tuần, hoặc chờ đợi xem có học viên nào chủ động gửi email/nhắn tin hỏi bài hay không.
4. **Điểm bắt đầu gặp vướng mắc**: Điểm quiz chỉ phản ánh kết quả sau cùng (lúc đã học xong và làm bài test), không phản ánh quá trình học viên loay hoay trước đó. Đồng thời, những học viên yếu nhất thường là những người nhút nhát và im lặng nhất (họ không bao giờ chủ động hỏi). Giảng viên hoàn toàn bị "mù thông tin" về tiến trình hiểu bài thực tế của họ và không biết phải liên hệ với ai.

### 4.2 Situation & Job Statement
> **Khi một tuần học tự học trực tuyến của lớp học đông học viên kết thúc**, **giảng viên** đang cố **phát hiện sớm những học viên đang gặp khó khăn với kiến thức mới để can thiệp hỗ trợ kịp thời** bằng cách **quan sát điểm số quiz cuối tuần và chờ đợi học viên tự động liên hệ hỏi bài**.

* **Functional Job**: Xác định chính xác danh sách học viên đang struggle và phần kiến thức họ chưa hiểu để giải đáp kịp thời trước khi họ hổng kiến thức nghiêm trọng và trượt môn.
* **Emotional Job**: Cảm thấy an tâm rằng mình đang làm tốt vai trò dạy học, không bỏ rơi học viên; giảm bớt sự lo lắng về tỷ lệ học viên bỏ học giữa chừng (drop-out).
* **Social Job**: Xây dựng hình ảnh một giảng viên tận tâm, chu đấu trong mắt học viên và nhà trường; duy trì đánh giá phản hồi tốt (course evaluation score) cuối khóa.

### 4.3 JTBD Hypothesis
> **Khi quản lý một lớp học trực tuyến/kết hợp quy mô lớn**, tôi muốn **nhanh chóng nhận biết được những học viên đang loay hoay bế tắc với bài học**, để có thể **chủ động hỗ trợ họ kịp thời trước khi họ nản chí và bỏ cuộc**.

### 4.4 Current workaround hypothesis (Các cách xử lý tạm thời hiện tại)
1. **Workaround 1 (Chờ đợi thụ động)**: Đợi học viên tự động nhắn tin hoặc gửi email hỏi bài (nhưng tỷ lệ học viên yếu chủ động hỏi thường dưới 5%).
2. **Workaround 2 (Quiz Monitoring)**: Thiết kế các bài test ngắn sau mỗi chương để lọc ra những học viên có điểm dưới trung bình và gửi email nhắc nhở chung cho cả nhóm.
3. **Workaround 3 (Lọc log LMS thủ công)**: Thỉnh thoảng tải file Excel xuất dữ liệu đăng nhập và thời gian online của học viên trên LMS để xem ai ít online rồi nhắc nhở (cách này chỉ biết học viên học hay chưa, không biết họ có hiểu bài hay không).
4. **Workaround 4 (Mở Office Hours định kỳ)**: Thiết lập các buổi Zoom hỏi đáp tự do 1 tiếng mỗi tuần (nhưng thực tế chỉ có học viên khá giỏi tham gia trao đổi, học viên yếu thường vắng mặt).

---

## 5. Pain

Chúng tôi đưa ra 2 cách giải thích cạnh tranh (competing hypotheses) cho việc: *Tại sao giảng viên không chủ động hỗ trợ được học viên struggle kịp thời trong thực tế.*

### 5.1 Pain Hypothesis A (Rào cản về dữ liệu chẩn đoán sớm)
> **Khi kết thúc một tuần học tự học trực tuyến**, **giảng viên** gặp khó khăn trong việc **phát hiện đúng đối tượng cần giúp đỡ** vì **họ thiếu các tín hiệu chẩn đoán sớm và trực quan phản ánh quá trình tiếp thu bài của học viên trên LMS (dữ liệu hiện tại chỉ có trạng thái hoàn thành bài học thô sơ hoặc điểm quiz muộn)**, dẫn đến **việc họ không biết ai thực sự đang loay hoay để chủ động liên hệ trước khi kỳ thi diễn ra**.

| Thành phần | Nội dung chi tiết |
| :--- | :--- |
| **Situation** | Kết thúc một tuần học tự học trực tuyến của lớp học quy mô lớn. |
| **Job** | Nhận biết đúng học viên đang gặp khó khăn để chủ động hỗ trợ. |
| **Barrier** | Hệ thống LMS hiện tại chỉ ghi nhận trạng thái tĩnh (đã xem/chưa xem slide) hoặc điểm quiz cuối khóa, không ghi nhận các khó khăn vi mô trong quá trình tư duy (loay hoay xem lại slide, sửa đáp án, hỏi AI...). |
| **Immediate consequence** | Giảng viên bỏ lỡ thời điểm vàng để hỗ trợ (ngay khi học viên bắt đầu bế tắc). Học viên tích tụ kiến thức chưa hiểu và dần nản lòng. |
| **Downstream consequence** | Tỷ lệ học viên trượt môn hoặc bỏ học giữa chừng tăng lên; đánh giá chất lượng dạy học của giảng viên bị giảm sút. |
| **Why it matters** | Ảnh hưởng trực tiếp đến uy tín giảng dạy của giảng viên, doanh thu của cơ sở giáo dục và kết quả đầu ra của người học. |

### 5.2 Pain Hypothesis B (Rào cản về thời gian, năng lượng và quy trình can thiệp tinh tế)
> **Khi kết thúc một tuần học tự học trực tuyến**, **giảng viên** gặp khó khăn trong việc **chủ động liên hệ hỗ trợ học viên** vì **họ bị quá tải thời gian và cảm thấy ngại/thiếu một quy trình tinh tế để tiếp cận một học viên chưa chủ động hỏi (sợ gây áp lực tâm lý hoặc bị coi là kiểm soát quá mức)**, dẫn đến **việc họ chọn giải pháp an toàn là chờ đợi thụ động học viên tự liên hệ trước**.

| Thành phần | Nội dung chi tiết |
| :--- | :--- |
| **Situation** | Kết thúc một tuần học tự học trực tuyến của lớp học quy mô lớn. |
| **Job** | Thực hiện hành động chủ động liên hệ hỗ trợ 1-1 cho học viên. |
| **Barrier** | Thiếu thời gian để soạn tin nhắn cá nhân hóa cho từng người, lo ngại việc tự dưng nhắn tin chỉ rõ chi tiết học tập của học viên sẽ làm họ cảm thấy bị theo dõi và phòng thủ. |
| **Immediate consequence** | Dù giảng viên có nghi ngờ học viên yếu qua điểm quiz, họ cũng chần chừ không nhắn tin riêng. Sự tương tác hỗ trợ vẫn không diễn ra. |
| **Downstream consequence** | Học viên cảm thấy giảng viên xa cách, không quan tâm. Khó khăn học tập không được giải quyết dù giảng viên có thể có thời gian nếu quy trình đơn giản hơn. |
| **Why it matters** | Vấn đề cốt lõi không phải là giảng viên "không biết ai yếu", mà là họ "không có đủ capacity và kịch bản sư phạm phù hợp" để thực hiện việc can thiệp 1-1 trên quy mô lớn một cách tinh tế. |

### 5.3 So sánh và đánh giá các Pain Hypotheses

| Tiêu chí | Hypothesis A (Thiếu dữ liệu chẩn đoán) | Hypothesis B (Quá tải & Rào cản giao tiếp) |
| :--- | :--- | :--- |
| **Barrier chính** | Thiếu dữ liệu/tín hiệu chỉ ra đúng người và đúng chỗ gặp khó khăn kịp thời. | Thiếu thời gian, năng lượng và kịch bản tiếp cận học viên tinh tế. |
| **Observable behavior giống nhau** | Giảng viên rất ít khi chủ động nhắn tin hỗ trợ học viên trước khi kỳ thi diễn ra. | Giảng viên rất ít khi chủ động nhắn tin hỗ trợ học viên trước khi kỳ thi diễn ra. |
| **Evidence phân biệt** | Nếu được cung cấp danh sách học viên yếu kèm lý do cụ thể, giảng viên sẽ lập tức đi liên hệ hỗ trợ ngay. | Dù có danh sách học viên yếu chính xác 100%, giảng viên vẫn trì hoãn liên hệ vì không có thời gian hoặc không biết nhắn thế nào cho tinh tế. |
| **Nếu đúng thì implication** | Cần xây dựng công cụ quét dữ liệu hành vi và hiển thị dashboard cảnh báo sớm (AI Radar). | Cần xây dựng các template tin nhắn tự động, quy trình hỗ trợ nhanh, hoặc phân quyền/giao việc này cho Trợ giảng (TA) thay vì Giảng viên. |
| **Nếu sai thì dấu hiệu** | Giảng viên có dashboard cực kỳ chi tiết nhưng tỷ lệ click liên hệ/hành động gần như bằng 0. | Giảng viên có sẵn các mẫu tin nhắn và thời gian nhưng phàn nàn rằng họ không biết phải gửi cho ai vì dữ liệu LMS quá chung chung. |

### 5.4 Chọn hypothesis để điều tra trước
> **Chọn Hypothesis A để điều tra trước.**

* **Lý do**: Giải pháp ban đầu (AI Support Radar) được thiết kế dựa trên giả định cốt lõi rằng giảng viên đang bị "mù thông tin" về khó khăn của học viên trong quá trình tự học trực tuyến. Chúng ta cần xác minh xem rào cản thông tin này có thực sự là nút thắt đầu tiên ngăn cản họ hành động hay không. Nếu kiểm chứng Hypothesis A mà thấy sai (tức là giảng viên thực ra biết rõ ai yếu qua điểm quiz nhưng vẫn không liên hệ vì bận/ngại), chúng ta sẽ lập tức chuyển sang validate Hypothesis B để xoay trục giải pháp (pivot) sang hướng hỗ trợ quy trình can thiệp thay vì làm AI dự đoán tín hiệu.

---

## 6. Evidence

### 6.1 Bảng định nghĩa Evidence cần tìm

| Cần kiểm tra | Evidence làm nhóm tin hơn (Confirming) | Evidence làm nhóm nghi ngờ hoặc bác bỏ (Falsifying) |
| :--- | :--- | :--- |
| **Situation có thật** | Giảng viên mô tả họ đang dạy các lớp trực tuyến/kết hợp quy mô >50 học viên và thường xuyên cảm thấy mơ hồ về mức độ hiểu bài thực tế của lớp sau mỗi chương. | Giảng viên chỉ dạy các lớp nhỏ (<15 người) nơi họ tương tác trực tiếp hàng ngày, hoặc các khóa học 100% video quay sẵn không có yếu tố tương tác sư phạm của giảng viên. |
| **Pain có ý nghĩa** | Giảng viên chia sẻ sự thất vọng/bất lực khi nhận kết quả thi cuối khóa của học viên vì có nhiều người trượt mà trước đó không hề có biểu hiện gì bất thường hay hỏi han gì. | Giảng viên cho biết tỷ lệ trượt môn rất thấp, hoặc họ không quan tâm đến việc học viên hiểu bài hay không vì đó là trách nhiệm tự học của học viên để tự qua kỳ thi. |
| **Workaround tồn tại** | Giảng viên kể lại việc họ từng thử tải file excel báo cáo log của LMS để ngồi lọc thủ công xem ai chưa online, hoặc tự thiết kế các bài quiz ngắn hàng tuần để rà soát học viên yếu. | Giảng viên hoàn toàn không làm gì khác ngoài việc lên lớp giảng bài và đợi đến ngày thi cuối kỳ để chấm điểm. |
| **Consequence tồn tại** | Giảng viên có thể nêu ra các trường hợp học viên bỏ học giữa chừng (drop-out) tăng cao trong các tuần đầu do không theo kịp bài học mà không được hỗ trợ kịp thời. | Học viên dù gặp khó khăn vẫn tự tìm cách học và đạt điểm cao, hoặc họ tự tìm gia sư ngoài mà không cần đến giảng viên của khóa học. |
| **Pattern có lặp** | Giảng viên xác nhận hiện tượng "học viên im lặng rồi trượt môn" xảy ra đều đặn ở tất cả các kỳ học trực tuyến mà họ phụ trách. | Đây chỉ là hiện tượng cá biệt xảy ra ở một vài khóa học đặc thù hoặc do chất lượng đề thi quá khó đột xuất. |

### 6.2 Phân cấp bằng chứng (Evidence Hierarchy)

1. **Actual Past Behavior (Mạnh nhất)**: Giảng viên chỉ ra được trong học kỳ trước, họ đã từng dành bao nhiêu tiếng để lọc excel LMS hoặc chủ động gửi email cho học viên nào. (Chứng minh pain đủ lớn để họ phải bỏ công sức làm workaround).
2. **Specific Recent Event**: Giảng viên kể lại một trường hợp học viên cụ thể vừa trượt hoặc bỏ học tuần trước vì hổng kiến thức từ tuần 2 mà giảng viên không biết.
3. **Workaround + Effort**: Giảng viên tự thiết lập các bài quiz phụ hoặc nhóm chat hỗ trợ để kiểm tra độ hiểu bài của học viên dù mất thêm thời gian.
4. **Observable Consequence**: Số lượng học viên trượt môn tăng, tỷ lệ giữ chân học viên (retention rate) của khóa học giảm sút.
5. **Stated Opinion (Yếu)**: Giảng viên nói: *"Tôi nghĩ việc biết học viên gặp khó khăn sớm là rất quan trọng"*. (Dễ bị ảnh hưởng bởi xã giao).
6. **Hypothetical Preference (Yếu nhất)**: Giảng viên nói: *"Nếu có AI Support Radar, tôi chắc chắn sẽ dùng nó mỗi ngày"*. (Không phản ánh hành vi thực tế khi đối mặt với áp lực thời gian thật).

### 6.3 Tiêu chí bác bỏ giả thuyết (Falsification Criteria)
Chúng tôi sẽ chủ động bác bỏ hoặc sửa đổi giả thuyết nếu phát hiện một trong năm điều sau trong quá trình phỏng vấn:
1. Giảng viên khẳng định họ đã biết rõ học viên nào yếu thông qua điểm các bài quiz ngắn hàng tuần, và các thông tin hành vi vi mô (di chuyển slide, highlight...) từ AI là thừa thãi, không mang lại giá trị chẩn đoán mới nào.
2. Giảng viên cho biết họ hoàn toàn không có thời gian (dù chỉ là 5 phút) để xem queue và nhắn tin cá nhân hóa vì lớp quá đông và họ không được trả lương cho việc hỗ trợ ngoài giờ.
3. Học viên tuyên bố họ sẽ cực kỳ khó chịu và cảm thấy bị xâm phạm quyền riêng tư nếu biết giảng viên theo dõi từng click slide, sửa đáp án của họ, và họ sẽ tìm cách tắt các tính năng tương tác đó.
4. Học viên gặp khó khăn cho biết họ luôn chủ động hỏi giảng viên ngay khi không hiểu; rào cản không nằm ở phía học viên ngại hỏi mà nằm ở việc giảng viên phản hồi quá chậm hoặc hời hợt.
5. Phân tích dữ liệu lịch sử chỉ ra không có mối liên quan nào giữa các hành vi vi mô (dừng lâu ở slide, highlight) và kết quả thi cuối khóa của học viên (nhiều người dừng lâu vẫn thi tốt, nhiều người lướt nhanh lại thi trượt).

---

## 7. Chốt Problem Hypothesis

> **Chúng tôi giả định rằng khi kết thúc một tuần học tự học trực tuyến của lớp học quy mô lớn (trên 50 học viên), giảng viên gặp khó khăn trong việc phát hiện sớm và chính xác những học viên đang gặp khó khăn với kiến thức mới vì họ thiếu các chỉ số chẩn đoán kịp thời phản ánh quá trình tiếp thu bài của học viên (dữ liệu LMS hiện tại chỉ có trạng thái hoàn thành thô sơ hoặc điểm quiz muộn), khiến giảng viên không thể can thiệp hỗ trợ kịp thời trước khi học viên nản chí, bỏ học hoặc trượt môn. Chúng tôi tin đây là vấn đề đáng giải quyết nếu phỏng vấn giảng viên chỉ ra họ đã từng tự tìm cách kiểm tra mức độ hiểu bài của học viên ngoài giờ lên lớp (workaround), sẵn sàng dành ra ít nhất 30 phút mỗi tuần để liên hệ hỗ trợ nếu biết chính xác đối tượng cần giúp đỡ, và học viên xác nhận họ sẵn lòng nhận hỗ trợ tinh tế từ giảng viên mà không thấy bị xâm phạm quyền riêng tư.**

### 7.1 Điều phải đúng để hypothesis đứng vững (Riskiest Assumptions)
1. Giảng viên thực sự coi việc giảm tỷ lệ trượt môn/bỏ học là một nhiệm vụ quan trọng và sẵn sàng hành động để cải thiện nó.
2. Học viên không thể tự vượt qua các khó khăn học tập phức tạp nếu không có sự can thiệp sư phạm từ phía giảng viên/trợ giảng.
3. Giảng viên có đủ thời gian và kỹ năng giao tiếp để thực hiện các cuộc can thiệp hỗ trợ cá nhân hóa một cách tinh tế.
4. Các tín hiệu hành vi trên LMS (slide, notes, AI chat) có thể được chuyển hóa thành thông tin chẩn đoán có độ chính xác cao về trạng thái hiểu bài của học viên.
5. Học viên cảm thấy an toàn về mặt tâm lý và không thay đổi hành vi học tập theo hướng đối phó khi hệ thống ghi nhận dữ liệu hành vi.

### 7.2 Điều gì khiến nhóm sửa hypothesis (Revise)?
1. Giảng viên muốn hỗ trợ học viên nhưng không muốn nhắn tin trực tiếp 1-1 vì ngại; họ thích hệ thống tự động gửi email gợi ý tài liệu cho học viên dưới danh nghĩa của họ -> *Sửa hypothesis tập trung vào giải pháp tự động hóa hành động (automated intervention) thay vì queue duyệt tay.*
2. Giảng viên không có thời gian làm việc này, nhưng Trợ giảng (TA) thì có và đây là trách nhiệm chính của TA -> *Sửa Actor chính từ Giảng viên (Instructor) sang Trợ giảng (TA).*
3. Học viên không muốn giảng viên biết mình đang loay hoay ở slide nào, nhưng họ sẵn sàng nhận lời khuyên từ một AI Tutor trung lập -> *Sửa hypothesis sang hướng giải quyết khép kín giữa Học viên và AI chatbot.*

### 7.3 Điều gì khiến nhóm bác bỏ hypothesis hoàn toàn (Reject)?
1. Giảng viên hoàn toàn không quan tâm đến việc học viên có hiểu bài hay không trong suốt quá trình học, họ chỉ chấm điểm thi cuối kỳ và coi việc trượt môn hoàn toàn là do học viên lười biếng.
2. Học viên cực kỳ phản đối việc thu thập dữ liệu hành vi vi mô (di chuyển slide, highlight, chat AI) và tuyên bố sẽ rời bỏ nền tảng LMS nếu tính năng này được kích hoạt.
3. Thử nghiệm thực tế chỉ ra việc giảng viên chủ động liên hệ hỗ trợ không mang lại bất kỳ sự cải thiện nào về kết quả học tập hay tỷ lệ giữ chân học viên so với việc để học viên tự học.

---

## 8. Solution Parking Lot

Brainstorm 5 hướng giải quyết khác nhau cho vấn đề: *Giảng viên khó phát hiện và hỗ trợ kịp thời học viên đang gặp khó khăn*.

### 8.1 Bảng Solution Parking Lot

| # | Hướng giải quyết có thể có | AI / Không sử dụng AI | Actor chính | Cơ chế giải quyết pain |
| :- | :--- | :--- | :--- | :--- |
| 1 | **Peer-to-Peer Help Desk (Học viên giúp nhau)**: Cuối mỗi bài học, học viên gặp khó khăn có thể ẩn danh đăng câu hỏi lên một bảng chung, các học viên hiểu bài sẽ vào giải thích để nhận điểm thưởng. | Không sử dụng AI | Learner | Giải quyết khó khăn của học viên thông qua cộng đồng học tập, giảm tải cho giảng viên. |
| 2 | **Interactive Self-Assessment Diagnostic (Tự đánh giá chủ động)**: Cuối bài học, LMS yêu cầu học viên tự chọn mức độ tự tin và trả lời 1 câu hỏi test nhanh. Gom nhóm học viên chọn "Thấp" + trả lời sai để báo cáo giảng viên giải đáp chung. | Không sử dụng AI | Learner & Instructor | Sử dụng dữ liệu tự khai báo chủ động, đảm bảo an toàn riêng tư và không lo ngại bị theo dõi thao tác ngầm. |
| 3 | **AI Automated Nudge & Study Path Adjuster (Tự động hóa can thiệp)**: Khi phát hiện tín hiệu struggle, hệ thống AI tự động gửi gợi ý tinh tế cho học viên: video tóm tắt ngắn, làm bài tập mức độ dễ hơn hoặc tài liệu bổ trợ. | AI | Learner | Tự động hóa hoàn toàn việc hỗ trợ, loại bỏ nút thắt cổ chai về mặt thời gian của giảng viên. |
| 4 | **Weekly TA Focus Sheet (Bảng trọng tâm trợ giảng)**: AI tổng hợp dữ liệu học tập thành báo cáo gửi email cho Trợ giảng (TA) sáng thứ Hai, chỉ ra 5 học viên cần kèm cặp nhất để TA đặt lịch hẹn hỗ trợ. | AI | Coach / TA | Chuyển giao trách nhiệm can thiệp 1-1 sang cho Trợ giảng - người bám sát lớp và có KPI hỗ trợ học tập tốt hơn. |
| 5 | **In-Class Dynamic Q&A Session Trigger (Gợi ý giảng dạy lại)**: Tổng hợp các slide có thời gian dừng trung bình của cả lớp vượt quá ngưỡng quy định để nhắc giảng viên dành 10 phút đầu buổi sau giảng lại phần đó cho cả lớp. | Không sử dụng AI | Instructor | Giảng viên can thiệp diện rộng (1-nhiều) giúp giải quyết triệt để vấn đề hiểu bài một cách tự nhiên, không gây ngại ngùng cho cá nhân. |

### 8.2 Đánh giá các phương án thay thế
* **Solution nào đang được directive mặc định?**
  Giải pháp mặc định là sử dụng AI để dự đoán nhu cầu hỗ trợ từ dữ liệu hành vi ngầm, xếp thứ tự ưu tiên và tạo **Support Queue** để giảng viên duyệt và trực tiếp liên hệ 1-1 với học viên.
* **Những alternative nào cho thấy problem có thể được giải quyết mà không cần solution ban đầu?**
  * **Giải pháp số 2 (Interactive Self-Assessment)**: Giải quyết vấn đề chẩn đoán mà không cần dùng đến AI phức tạp hay thu thập dữ liệu hành vi nhạy cảm.
  * **Giải pháp số 5 (In-Class Dynamic Q&A Session Trigger)**: Giải quyết vấn đề can thiệp mà không cần giảng viên phải liên hệ 1-1 tốn thời gian, tránh được rào cản tâm lý e ngại của học viên bằng cách giảng lại cho cả lớp.

---

## 9. Checkpoint 1 Self-check

| Tiêu chí | Kết quả | Lý do | Cần sửa gì |
| :--- | :--- | :--- | :--- |
| Có chuỗi Solution → Change → Actor → Situation & Job → Pain → Evidence | **PASS** | Đầy đủ các phần theo đúng cấu trúc logic. | Không cần sửa. |
| Capability đã trung tính | **PASS** | Không nhắc đến AI Support Radar hay giao diện Queue cụ thể, tập trung vào khả năng nhận biết và hỗ trợ cá nhân hóa. | Không cần sửa. |
| Không biến feature absence thành pain | **PASS** | Pain được định nghĩa là thiếu dữ liệu chẩn đoán sớm và rào cản thời gian/giao tiếp tinh tế của giảng viên, không phải là "thiếu AI Radar". | Không cần sửa. |
| Change chain không nhảy từ output → outcome | **PASS** | Có đầy đủ các mắt xích trung gian: Output -> Information change -> Behavior change -> Intervention -> Learner response -> Outcome. | Không cần sửa. |
| Actor primary có lý do rõ | **PASS** | Đã phân tích kỹ vai trò của Instructor và có lập luận trade-off chi tiết khi chọn Instructor thay vì Learner. | Không cần sửa. |
| Situation cụ thể | **PASS** | Đã mô tả bối cảnh cụ thể: lớp học trực tuyến quy mô đông học viên kết thúc tuần học tự học trên LMS. | Không cần sửa. |
| JTBD không chứa solution | **PASS** | JTBD mô tả tiến trình giảng viên muốn nhận biết học viên loay hoay để hỗ trợ kịp thời, không chứa giải pháp kỹ thuật. | Không cần sửa. |
| Có ít nhất 2 competing pain hypotheses | **PASS** | Đã xây dựng Pain A (Thiếu dữ liệu chẩn đoán) và Pain B (Quá tải & Rào cản giao tiếp tinh tế). | Không cần sửa. |
| Competing hypotheses thật sự khác nhau | **PASS** | Một giả thuyết do thiếu thông tin đầu vào (chẩn đoán), một giả thuyết do rào cản hành động đầu ra (thực thi). | Không cần sửa. |
| Có evidence làm hypothesis mạnh hơn | **PASS** | Đã định nghĩa các bằng chứng xác nhận cụ thể liên quan đến hành vi trong quá khứ và sự tồn tại của workaround. | Không cần sửa. |
| Có evidence có thể bác bỏ | **PASS** | Đã định nghĩa rõ ràng các tiêu chí Falsification cho cả giảng viên và học viên. | Không cần sửa. |
| Không tạo evidence giả | **PASS** | Tuyệt đối không tự bịa số liệu phỏng vấn hay kết quả khảo sát chưa diễn ra. | Không cần sửa. |
| Problem Hypothesis falsifiable | **PASS** | Đã nêu rõ các điều kiện cụ thể để kiểm chứng hoặc bác bỏ giả thuyết. | Không cần sửa. |
| Có ≥5 solution trong Parking Lot | **PASS** | Brainstorm đủ 5 giải pháp khác nhau. | Không cần sửa. |
| Có ≥1 non-AI solution | **PASS** | Có giải pháp 1, 2, 5 không sử dụng AI. | Không cần sửa. |

---

## 10. Red Team Review

### 10.1 Five weakest assumptions (5 giả định yếu nhất trong bài phân tích)
1. **Giả định giảng viên sẽ chủ động nhắn tin hỗ trợ khi có queue**: Trong thực tế, giảng viên có xu hướng tránh các công việc phát sinh ngoài giờ lên lớp nếu không được trả thêm lương hoặc tính vào KPI. Việc cung cấp queue không tự động giải quyết được vấn đề thiếu thời gian của họ.
2. **Giả định học viên sẽ cởi mở phản hồi khi được giảng viên hỏi thăm**: Học viên thường có tâm lý sợ bị đánh giá năng lực bởi giảng viên (người chấm điểm họ). Việc giảng viên bất ngờ nhắn tin dựa trên dữ liệu thao tác có thể khiến họ thấy không an toàn và trả lời đối phó: *"Em hiểu bài rồi ạ"*.
3. **Giả định các tín hiệu hành vi phản ánh đúng độ hiểu bài**: Dừng lâu ở slide hay chat AI nhiều có thể là hành vi của một học viên học sâu (deep learner) đang nghiên cứu kỹ. AI có thể liên tục đánh nhãn sai nhóm này là "cần hỗ trợ", gây phiền cho giảng viên và học viên giỏi.
4. **Giả định giảng viên có kỹ năng kèm cặp trực tuyến**: Nhiều giảng viên quen dạy lớp đông và giảng bài một chiều, họ có thể thiếu kỹ năng sư phạm cá nhân hóa để giảng giải lại một cách dễ hiểu cho một học viên đang bế tắc qua tin nhắn chat.
5. **Giả định Trợ giảng (TA) có thể dễ dàng thay thế giảng viên**: Trong nhiều hệ thống, TA chỉ được trả lương rất thấp để làm việc hành chính (chấm điểm, điểm danh) và không có chuyên môn hoặc trách nhiệm tư vấn học tập chuyên sâu.

### 10.2 Alternative interpretation (3 cách giải thích khác cho behavioral signals)
* **Xem lại slide và dừng lại lâu**: Không phải học viên không hiểu bài, mà vì slide đó chứa công thức/định nghĩa cốt lõi mà họ cần mở ra để làm bài tập ở tab bên cạnh. Hoặc đơn giản là slide đó chứa hình ảnh/video thú vị khiến họ muốn dừng lại thưởng thức.
* **Chat AI nhiều**: Không phải vì bế tắc bài học, mà vì học viên này cực kỳ thích thú với công nghệ, muốn thử nghiệm các prompt khác nhau hoặc đang hỏi AI các kiến thức mở rộng nằm ngoài nội dung bài học.
* **Sửa câu trả lời nhiều lần**: Không phải học viên hoang mang bối rối, mà phản ánh tính cách cẩn thận, tỉ mỉ của học viên. Họ muốn rà soát kỹ lỗi chính tả, ngữ pháp hoặc cách diễn đạt trước khi nộp bài.

### 10.3 Biggest product risk
Xây dựng một hệ thống AI dự đoán cực kỳ tinh vi nhưng không giải quyết được rào cản tâm lý của giảng viên (ngại chủ động liên hệ) và học viên (sợ bị giám sát). Sản phẩm sẽ trở thành một "ghost town" nơi AI liên tục gửi cảnh báo nhưng không có bất kỳ tương tác thực tế nào xảy ra. Dữ liệu đầu vào cũng sẽ bị méo mó khi học viên tìm cách học đối phó để tránh bị AI phát hiện.

### 10.4 Biggest research risk
Khi phỏng vấn, giảng viên và học viên đều có xu hướng trả lời theo kiểu "mong muốn xã hội" (social desirability bias). Giảng viên sẽ nói họ rất muốn giúp đỡ học viên, học viên sẽ nói họ rất muốn được thầy cô quan tâm. Nhưng khi tính năng ra mắt thực tế, sự lười biếng và áp lực thời gian sẽ chiến thắng, khiến họ quay lại hành vi cũ. Nghiên cứu viên cần tập trung hỏi về hành vi trong quá khứ thay vì hỏi ý kiến về tương lai.

### 10.5 Ethical / privacy risk
* **Hiệu ứng Panopticon (Giám sát quá mức)**: Việc theo dõi chi tiết từng thao tác click slide, sửa câu trả lời tạo ra cảm giác bị theo dõi (surveillance effect) trong môi trường học tập. Điều này hủy hoại sự an toàn tâm lý (psychological safety) cần có để học viên tự do thử nghiệm và mắc lỗi.
* **Định kiến của giảng viên (AI Over-trust)**: Giảng viên tin tưởng tuyệt đối vào nhãn "struggle" của AI và gắn mác học viên đó là yếu kém một cách định kiến, ảnh hưởng đến việc chấm điểm các bài thi tự luận hoặc thái độ ứng xử trên lớp.
* **Xâm phạm quyền riêng tư AI Chat**: Nội dung trao đổi giữa học viên và AI Chat có thể chứa đựng những câu hỏi ngô nghê hoặc cả những chia sẻ cá nhân. Việc AI quét nội dung này để báo cáo cho giảng viên (dù chỉ là tóm tắt) có thể vi phạm nghiêm trọng quyền riêng tư của học viên.

---

## 11. Final Version (Phiên bản đã sửa đổi sau phản biện)

### 11.1 Solution Directive
Sau mỗi phiên học, hệ thống phân tích các tín hiệu học tập (di chuyển slide, dừng lâu, xem lại, highlight/ghi chú, đánh dấu "Chưa hiểu", sửa đáp án, chat AI) để AI suy đoán nhu cầu hỗ trợ và xếp ưu tiên, tạo ra một **Support Queue** cho giảng viên duyệt và quyết định chủ động liên hệ hỗ trợ.

### 11.2 Capability trung tính
> **Khả năng giúp giảng viên nhận biết kịp thời và chính xác những học viên đang gặp khó khăn trong việc tiếp thu kiến thức sau mỗi phiên học, để họ có phương án hỗ trợ cá nhân hóa phù hợp trước khi học viên bị hổng kiến thức nghiêm trọng.**

### 11.3 Change Chain
```text
Solution (AI Support Radar)
→ [Output] Tạo ra Support Queue hiển thị học viên struggle kèm gợi ý can thiệp.
→ [Information Change] Giảng viên biết sớm học viên nào đang gặp khó khăn ở phần kiến thức cụ thể nào sau phiên học.
→ [Behavior Change] Giảng viên dành thời gian xem xét queue và chủ động liên hệ hỗ trợ tinh tế.
→ [Intervention] Giảng viên giải thích lại hoặc cung cấp tài liệu bổ trợ cá nhân hóa.
→ [Learner Response] Học viên đón nhận hỗ trợ một cách an toàn, cởi mở chia sẻ bế tắc và tiến bộ.
→ [Outcome] Học viên vượt qua khó khăn học tập, cải thiện kết quả thi và không bỏ học giữa chừng.
```

### 11.4 Actor Table

| Actor | Họ đang làm gì? | Pain hoặc hậu quả | Họ hưởng lợi thế nào? | Vai trò trong change chain |
| :--- | :--- | :--- | :--- | :--- |
| **Learner (Học viên)** | Tự học trên LMS, xem slide, làm quiz, hỏi AI. | Gặp bài khó không biết hỏi ai, ngại hỏi giảng viên, tự loay hoay rồi nản lòng và bỏ học. | Được hỗ trợ giải đáp kịp thời, tinh tế; vượt qua bài học khó dễ dàng hơn. | Tạo ra các tín hiệu hành vi đầu vào; tiếp nhận sự can thiệp và thay đổi kết quả đầu ra. |
| **Instructor (Giảng viên)** | Giảng dạy, quản lý lớp học trực tuyến. | Bị "mù thông tin" về tiến độ hiểu bài thực tế của lớp; chỉ biết khi điểm thi cuối kỳ đã muộn. | Chủ động can thiệp đúng người, đúng chỗ để cải thiện chất lượng giảng dạy và tỷ lệ qua môn. | Người dùng trực tiếp của Support Queue; quyết định duyệt và thực hiện hành động can thiệp. |
| **Coach / TA (Trợ giảng)** | Trực tiếp hỗ trợ học viên giải đáp thắc mắc. | Quá tải câu hỏi lẻ tẻ hoặc không biết tập trung kèm cặp ai trước trong lớp đông học viên. | Có danh sách ưu tiên rõ ràng các học viên thực sự cần kèm cặp 1-1 để tối ưu hóa công sức. | Đối tượng có thể vận hành chính của Support Queue thay cho giảng viên. |

### 11.5 Actor được chọn để điều tra trước
> **Primary Actor: Instructor (Giảng viên chính)**
> *Lý do: Giảng viên là chốt chặn quyết định hành động can thiệp. Nếu họ không hành động, change chain bị gãy. Trợ giảng (TA) là actor dự phòng nếu giảng viên quá tải.*

### 11.6 Situation & Job
> **Khi một tuần học tự học trực tuyến của lớp học đông học viên kết thúc**, **giảng viên** đang cố **phát hiện sớm những học viên đang gặp khó khăn với kiến thức mới để can thiệp hỗ trợ kịp thời** bằng cách **quan sát điểm số quiz cuối tuần và chờ đợi học viên tự động liên hệ hỏi bài**.

### 11.7 JTBD Hypothesis
> **Khi quản lý một lớp học trực tuyến/kết hợp quy mô lớn**, tôi muốn **nhanh chóng nhận biết được những học viên đang loay hoay bế tắc với bài học**, để có thể **chủ động hỗ trợ họ kịp thời trước khi họ nản chí và bỏ cuộc**.

### 11.8 Pain Hypothesis A (Thiếu dữ liệu chẩn đoán sớm)
> **Khi kết thúc một tuần học tự học trực tuyến**, **giảng viên** gặp khó khăn trong việc **phát hiện đúng đối tượng cần giúp đỡ** vì **họ thiếu các tín hiệu chẩn đoán sớm và trực quan phản ánh quá trình tiếp thu bài của học viên trên LMS (dữ liệu hiện tại chỉ có trạng thái hoàn thành bài học thô sơ hoặc điểm quiz muộn)**, dẫn đến **việc họ không biết ai thực sự đang loay hoay để chủ động liên hệ trước khi kỳ thi diễn ra**.

### 11.9 Pain Hypothesis B (competing explanation)
> **Khi kết thúc một tuần học tự học trực tuyến**, **giảng viên** gặp khó khăn trong việc **chủ động liên hệ hỗ trợ học viên** vì **họ bị quá tải thời gian và cảm thấy ngại/thiếu một quy trình tinh tế để tiếp cận một học viên chưa chủ động hỏi (sợ gây áp lực tâm lý hoặc bị coi là kiểm soát quá mức)**, dẫn đến **việc họ chọn giải pháp an toàn là chờ đợi thụ động học viên tự liên hệ trước**.

### 11.10 Pain Hypothesis được chọn để điều tra trước
> **Chọn Hypothesis A để điều tra trước** nhằm xác định xem rào cản thông tin chẩn đoán có thực sự là nút thắt đầu tiên ngăn cản giảng viên hành động hay không.

### 11.11 Evidence Table

| Cần kiểm tra | Evidence làm nhóm tin hơn (Confirming) | Evidence làm nhóm nghi ngờ hoặc bác bỏ (Falsifying) |
| :--- | :--- | :--- |
| **Situation có thật** | Giảng viên mô tả họ đang dạy các lớp trực tuyến quy mô >50 học viên và thường xuyên cảm thấy mơ hồ về mức độ hiểu bài thực tế của lớp. | Giảng viên chỉ dạy các lớp nhỏ (<15 người) nơi họ tương tác trực tiếp hàng ngày, hoặc các khóa học tự học hoàn toàn không cần giảng viên hỗ trợ. |
| **Pain có ý nghĩa** | Giảng viên chia sẻ sự bất lực khi nhận kết quả thi cuối khóa của học viên vì có nhiều người trượt mà trước đó im lặng không hỏi han gì. | Giảng viên cho biết tỷ lệ trượt môn rất thấp, hoặc họ không quan tâm đến việc học viên hiểu bài hay không vì đó là trách nhiệm tự học của học viên. |
| **Workaround tồn tại** | Giảng viên kể lại việc họ từng thử tải file excel báo cáo log của LMS để ngồi lọc thủ công, hoặc tự thiết kế các bài quiz ngắn hàng tuần để rà soát học viên yếu. | Giảng viên hoàn toàn không làm gì khác ngoài việc lên lớp giảng bài và đợi đến ngày thi cuối kỳ để chấm điểm. |
| **Consequence tồn tại** | Giảng viên có thể nêu ra các trường hợp học viên bỏ học giữa chừng (drop-out) tăng cao trong các tuần đầu do không theo kịp bài học. | Học viên dù gặp khó khăn vẫn tự tìm cách học và đạt điểm cao mà không cần đến giảng viên của khóa học. |
| **Pattern có lặp** | Giảng viên xác nhận hiện tượng "học viên im lặng rồi trượt môn" xảy ra đều đặn ở tất cả các kỳ học trực tuyến mà họ phụ trách. | Đây chỉ là hiện tượng cá biệt xảy ra ở một vài khóa học đặc thù hoặc do chất lượng đề thi quá khó đột xuất. |

### 11.12 Problem Hypothesis
> **Chúng tôi giả định rằng khi kết thúc một tuần học tự học trực tuyến của lớp học quy mô lớn (trên 50 học viên), giảng viên gặp khó khăn trong việc phát hiện sớm và chính xác những học viên đang gặp khó khăn với kiến thức mới vì họ thiếu các chỉ số chẩn đoán kịp thời phản ánh quá trình tiếp thu bài của học viên (dữ liệu LMS hiện tại chỉ có trạng thái hoàn thành thô sơ hoặc điểm quiz muộn), khiến giảng viên không thể can thiệp hỗ trợ kịp thời trước khi học viên nản chí, bỏ học hoặc trượt môn. Chúng tôi tin đây là vấn đề đáng giải quyết nếu phỏng vấn giảng viên chỉ ra họ đã từng tự tìm cách kiểm tra mức độ hiểu bài của học viên ngoài giờ lên lớp (workaround), sẵn sàng dành ra ít nhất 30 phút mỗi tuần để liên hệ hỗ trợ nếu biết chính xác đối tượng cần giúp đỡ, và học viên xác nhận họ sẵn lòng nhận hỗ trợ tinh tế từ giảng viên mà không thấy bị xâm phạm quyền riêng tư.**

### 11.13 Điều phải đúng để hypothesis đứng vững
1. Giảng viên thực sự coi việc giảm tỷ lệ trượt môn/bỏ học là một nhiệm vụ quan trọng và sẵn sàng hành động để cải thiện nó.
2. Học viên không thể tự vượt qua các khó khăn học tập phức tạp nếu không có sự can thiệp sư phạm từ phía giảng viên/trợ giảng.
3. Giảng viên có đủ thời gian và kỹ năng giao tiếp để thực hiện các cuộc can thiệp hỗ trợ cá nhân hóa một cách tinh tế.
4. Các tín hiệu hành vi trên LMS (slide, notes, AI chat) có thể được chuyển hóa thành thông tin chẩn đoán có độ chính xác cao về trạng thái hiểu bài của học viên.
5. Học viên cảm thấy an toàn về mặt tâm lý và không thay đổi hành vi học tập theo hướng đối phó khi hệ thống ghi nhận dữ liệu hành vi.

### 11.14 Điều làm hypothesis bị sửa/bác bỏ
* **Revise (Sửa đổi) khi**: Giảng viên bận rộn/ngại liên hệ 1-1, muốn hệ thống tự động can thiệp; hoặc vai trò can thiệp thuộc về Trợ giảng (TA) thay vì giảng viên chính; hoặc học viên chỉ chấp nhận tương tác với AI Tutor ẩn danh.
* **Reject (Bác bỏ hoàn toàn) khi**: Giảng viên hoàn toàn thờ ơ với kết quả học viên trong tiến trình; học viên cực kỳ phản đối và từ chối cung cấp dữ liệu hành vi học tập vi mô; hoặc can thiệp của giảng viên không mang lại hiệu quả cải thiện học tập so với tự học.

### 11.15 Solution Parking Lot

| # | Hướng giải quyết có thể có | AI / Không sử dụng AI | Actor chính | Cơ chế giải quyết pain |
| :- | :--- | :--- | :--- | :--- |
| 1 | **Peer-to-Peer Help Desk (Học viên giúp nhau)**: Cuối mỗi bài học, học viên gặp khó khăn có thể ẩn danh đăng câu hỏi lên một bảng chung, các học viên hiểu bài sẽ vào giải thích để nhận điểm thưởng. | Không sử dụng AI | Learner | Giải quyết khó khăn của học viên thông qua cộng đồng học tập, giảm tải cho giảng viên. |
| 2 | **Interactive Self-Assessment Diagnostic (Tự đánh giá chủ động)**: Cuối bài học, LMS yêu cầu học viên tự chọn mức độ tự tin và trả lời 1 câu hỏi test nhanh. Gom nhóm học viên chọn "Thấp" + trả lời sai để báo cáo giảng viên giải đáp chung. | Không sử dụng AI | Learner & Instructor | Sử dụng dữ liệu tự khai báo chủ động, đảm bảo an toàn riêng tư và không lo ngại bị theo dõi thao tác ngầm. |
| 3 | **AI Automated Nudge & Study Path Adjuster (Tự động hóa can thiệp)**: Khi phát hiện tín hiệu struggle, hệ thống AI tự động gửi gợi ý tinh tế cho học viên: video tóm tắt ngắn, làm bài tập mức độ dễ hơn hoặc tài liệu bổ trợ. | AI | Learner | Tự động hóa hoàn toàn việc hỗ trợ, loại bỏ nút thắt cổ chai về mặt thời gian của giảng viên. |
| 4 | **Weekly TA Focus Sheet (Bảng trọng tâm trợ giảng)**: AI tổng hợp dữ liệu học tập thành báo cáo gửi email cho Trợ giảng (TA) sáng thứ Hai, chỉ ra 5 học viên cần kèm cặp nhất để TA đặt lịch hẹn hỗ trợ. | AI | Coach / TA | Chuyển giao trách nhiệm can thiệp 1-1 sang cho Trợ giảng - người bám sát lớp và có KPI hỗ trợ học tập tốt hơn. |
| 5 | **In-Class Dynamic Q&A Session Trigger (Gợi ý giảng dạy lại)**: Tổng hợp các slide có thời gian dừng trung bình của cả lớp vượt quá ngưỡng quy định để nhắc giảng viên dành 10 phút đầu buổi sau giảng lại phần đó cho cả lớp. | Không sử dụng AI | Instructor | Giảng viên can thiệp diện rộng (1-nhiều) giúp giải quyết triệt để vấn đề hiểu bài một cách tự nhiên, không gây ngại ngùng cho cá nhân. |

---

## 12. Final Quality Gate

1. Nếu xóa hoàn toàn cụm từ “AI Support Radar”, problem hypothesis vẫn tồn tại không?
   > **YES**. Giảng viên vẫn gặp khó khăn trong việc phát hiện sớm học viên struggle trong lớp học trực tuyến đông người dù có hay không có AI Support Radar.
2. Nếu không xây AI, job của actor vẫn tồn tại không?
   > **YES**. Giảng viên vẫn cần theo dõi, phát hiện và hỗ trợ học viên yếu để cải thiện kết quả đào tạo.
3. Pain có phải barrier thực sự thay vì absence of feature không?
   > **YES**. Pain là sự thiếu thông tin chẩn đoán và rào cản thời gian/giao tiếp sư phạm, không phải là "không có tính năng radar".
4. Có alternative explanation cho behavioral signals không?
   > **YES**. Xem lại slide có thể do công thức quan trọng, dừng lâu có thể do bận việc riêng, sửa câu trả lời có thể do cẩn thận.
5. Evidence có thể bác bỏ hypothesis không?
   > **YES**. Các tiêu chí Falsification đã được định nghĩa rõ ràng để bác bỏ giả thuyết nếu giảng viên không bận/không cần dữ liệu hoặc học viên phản đối.
6. Team có phân biệt được opinion với actual behavior không?
   > **YES**. Đã phân loại rõ ràng trong Evidence Hierarchy, ưu tiên hành vi thực tế (workaround trong quá khứ) và bác bỏ ý kiến giả định (hypothetical preference).
7. Output và outcome đã được phân biệt chưa?
   > **YES**. Support Queue là Output; Giảng viên nhận biết là Information Change; Giảng viên chủ động can thiệp là Behavior Change; Học viên vượt qua khó khăn là Outcome.
8. Instructor và learner jobs có bị trộn lẫn không?
   > **YES** (Đã phân biệt rõ). Job của Learner là vượt qua phần khó của bài học; Job của Instructor là phát hiện sớm để hỗ trợ kịp thời.
9. Có ít nhất một non-AI solution không?
   > **YES**. Có Giải pháp số 1, 2, 5 trong Parking Lot hoàn toàn không cần sử dụng AI.
10. Một interview thất bại có khả năng làm team đổi hypothesis không?
    > **YES**. Nếu phỏng vấn chỉ ra giảng viên không có thời gian và từ chối can thiệp, team sẽ đổi sang giả thuyết tập trung vào Trợ giảng hoặc tự động hóa hỗ trợ.
