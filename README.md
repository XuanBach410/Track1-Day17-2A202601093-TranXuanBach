# Track1 Day17 — Case C AI Support Radar

## 1. Thông tin cá nhân và nhóm

- **Case**: Case C — AI Support Radar
- **Thành viên nhóm**:
  - Trần Xuân Bách — 2A202601093 (Vai trò: Phỏng vấn Learner 1, UX Researcher)
  - Nguyễn Quốc Thịnh — 2A202601675 (Vai trò: Phỏng vấn Learner 2, Product Discovery Lead)
  - Nguyễn Hoàng Minh — 2A202601229 (Vai trò: Phỏng vấn Instructor/Coach, Critical Reviewer)
- **Interview Recordings**: [Google Drive Folder](https://drive.google.com/drive/folders/17ukLaYeC2AkHzRGFSofs_9RR1bju806A?usp=sharing)


---

## 2. Problem Hypothesis Brief

*(Trích xuất từ kết quả nghiên cứu Chặng 1)*

- **Primary Actor**: Giảng viên (Instructor) phụ trách các lớp học trực tuyến hoặc kết hợp (blended) có quy mô lớn.
- **Situation (Bối cảnh xảy ra vấn đề)**: Khi kết thúc một tuần học tự học trực tuyến của lớp học quy mô đông học viên (trên 50 học viên).
- **Job (Mục tiêu của giảng viên)**: Nhận biết nhanh chóng và chính xác những học viên đang loay hoay bế tắc với bài học tự học, để có thể chủ động liên hệ hỗ trợ kịp thời trước khi họ nản chí, bỏ học hoặc trượt môn.
- **Pain (Nỗi đau thực tế)**: Giảng viên thiếu các tín hiệu chẩn đoán sớm và trực quan phản ánh quá trình tiếp thu bài của học viên trên LMS (dữ liệu hiện tại chỉ có trạng thái hoàn thành bài học thô sơ hoặc điểm quiz muộn).
- **Consequence (Hậu quả)**: Giảng viên không thể can thiệp hỗ trợ kịp thời trước khi học viên nản chí, bỏ học hoặc trượt môn.
- **Problem Hypothesis**: 
  > Chúng tôi giả định rằng khi kết thúc một tuần học tự học trực tuyến của lớp học quy mô lớn (trên 50 học viên), giảng viên gặp khó khăn trong việc phát hiện sớm và chính xác những học viên đang gặp khó khăn với kiến thức mới vì họ thiếu các chỉ số chẩn đoán kịp thời phản ánh quá trình tiếp thu bài của học viên (dữ liệu LMS hiện tại chỉ có trạng thái hoàn thành thô sơ hoặc điểm quiz muộn), khiến giảng viên không thể can thiệp hỗ trợ kịp thời trước khi học viên nản chí, bỏ học hoặc trượt môn. Chúng tôi tin đây là vấn đề đáng giải quyết nếu phỏng vấn giảng viên chỉ ra họ đã từng tự tìm cách kiểm tra mức độ hiểu bài của học viên ngoài giờ lên lớp (workaround), sẵn sàng dành ra ít nhất 30 phút mỗi tuần để liên hệ hỗ trợ nếu biết chính xác đối tượng cần giúp đỡ, và học viên xác nhận họ sẵn lòng nhận hỗ trợ tinh tế từ giảng viên mà không thấy bị xâm phạm quyền riêng tư.
- **Điều có thể bác bỏ (Falsification Criteria)**:
  1. Giảng viên khẳng định họ đã biết rõ học viên nào yếu thông qua các bài quiz ngắn hàng tuần và không cần thông tin vi mô từ dữ liệu hành vi.
  2. Giảng viên từ chối liên hệ hỗ trợ học viên vì không có thời gian và không được trả thêm lương cho công việc tương tác ngoài giờ lên lớp.
  3. Học viên phản đối gay gắt việc giảng viên theo dõi chi tiết thao tác vi mô (click slide, sửa đáp án) và cảm thấy không thoải mái, phòng thủ khi được giảng viên chủ động liên hệ dựa trên dữ liệu đó.

---

## 3. Conversation Guide — Final Version (Đã hiệu chỉnh sau khi luyện tập)

> **Lưu ý quan trọng**: Conversation Guide này được thiết kế trung tính nhằm tìm kiếm bằng chứng thực tế về hành vi trong quá khứ của người dùng. **Tuyệt đối không nhắc đến AI Support Radar, Support Queue hoặc lấy ý kiến đánh giá về bất kỳ giải pháp/tính năng nào trong suốt cuộc phỏng vấn.**

### 3.1 HƯỚNG DẪN DÀNH CHO HỌC VIÊN (LEARNER)

#### A. Tiêu chí tuyển chọn & Sàng lọc (Learner Recruitment)
- **Population**: Học viên đã hoặc đang tham gia các khóa học trực tuyến/kết hợp có thành phần tự học trên LMS.
- **Inclusion Criteria**:
  1. Đã hoàn thành ít nhất một tuần học tự học trên LMS trong vòng 14 ngày gần nhất.
  2. Có trải qua tình huống gặp một phần nội dung bài học khó hiểu hoặc bài tập bế tắc.
  3. Có thể kể lại chi tiết các hành động thực tế đã làm để xử lý phần khó đó.
- **Exclusion Criteria**:
  1. Không học tự học trực tuyến trong vòng 30 ngày qua (trí nhớ bị mờ nhạt).
  2. Chỉ nói về các khóa học lý thuyết suông không có thành phần tự học hoặc thực hành tương tác.
- **Recruitment Check Question**:
  > *"Trong vòng 14 ngày gần đây, khi học các bài học trực tuyến trên hệ thống LMS của trường/trung tâm, bạn có nhớ lần nào khi học xong một bài hoặc một chương mà bạn vẫn thấy bối rối, chưa chắc mình đã hiểu đúng phần kiến thức hay bài tập nào đó không?"*
  - **Pass Condition**: Interviewee xác nhận có và nêu được tên bài học hoặc chủ đề cụ thể của sự kiện đó.
  - **Fail Condition**: Interviewee nói không gặp khó khăn nào hoặc không nhớ sự kiện cụ thể nào. (Lập tức dừng và chuyển sang đối tượng khác).

#### B. Lời mở đầu (Opening - Tối đa 5 câu)
> *"Chào bạn, mình là [Tên], thành viên nhóm nghiên cứu trải nghiệm học tập trực tuyến. Hôm nay mình rất muốn lắng nghe những trải nghiệm thực tế của bạn khi tự học trên hệ thống trực tuyến thời gian qua. Cuộc trò chuyện này hoàn toàn không có câu trả lời đúng hay sai, mình chỉ muốn nghe câu chuyện và cách bạn học thực tế. Thông tin bạn chia sẻ sẽ chỉ được dùng làm dữ liệu nghiên cứu nội bộ và giữ bảo mật. Chúng ta bắt đầu nhé!"*

#### C. Câu hỏi mở đầu câu chuyện (Story Opener)
> *"Hãy nhớ lại lần gần nhất bạn gặp một bài học hoặc một phần kiến thức trực tuyến trên hệ thống mà bạn cảm thấy bế tắc hoặc chưa chắc mình hiểu đúng. Bạn kể cho mình nghe chuyện gì đã xảy ra lúc đó được không?"*

#### D. Big 3 Learning Goals & Câu hỏi chính (Main Questions)

| STT | Điều cần học (Learning Goals) | Câu hỏi sẽ dùng (Mom Test compliant) |
| :--- | :--- | :--- |
| **Q1** | **Situation & Severity**: Mức độ nghiêm trọng và tần suất bế tắc thực tế của học viên khi học trên LMS. | *"Khi nhận ra mình đang bị bế tắc hoặc chưa hiểu rõ phần kiến thức đó, bạn đã loay hoay trong bao lâu và cảm xúc của bạn lúc đó thế nào?"* |
| **Q2** | **Workaround & Effort**: Các phương án tự giải quyết hiện tại của học viên và công sức bỏ ra cho chúng. | *"Bạn đã thực hiện những hành động cụ thể nào để tự giải quyết phần kiến thức/bài tập chưa hiểu đó trước khi tiếp tục học?"* |
| **Q3** | **Scary Assumption (Thái độ với sự can thiệp)**: Cảm xúc và sự an toàn tâm lý của học viên khi được giáo viên tiếp cận hỗ trợ chủ động (đặc biệt khi chưa chủ động hỏi). | *"Trong các môn bạn từng học (kể cả trực tiếp), đã bao giờ bạn gặp tình huống một giáo viên/trợ giảng chủ động nhắn tin hoặc gặp riêng để chỉ ra đúng phần bạn làm sai hay loay hoay chưa? (Nếu chưa) Hãy nhớ lại lần gần nhất bạn nhận điểm bài tập kém mà không được giải thích lý do, lúc đó bạn đã làm gì?"* *(Sửa đổi sau khi luyện tập để tránh bị cụt hội thoại khi học viên nói "Chưa từng")* |

#### E. Probe Bank (Các câu hỏi đào sâu hành vi)
- *"Lúc đó chuyện gì xảy ra tiếp theo?"*
- *"Sau hành động đó, kết quả là bạn có hiểu bài hơn không?"*
- *"Bạn có nghĩ đến việc nhắn tin hỏi thầy cô lúc đó không? Tại sao bạn lại chọn/không chọn cách đó?"*
- *"Việc bế tắc ở phần đó đã ảnh hưởng gì đến các bài học tiếp theo hoặc điểm kiểm tra của bạn?"*
- *"Lần gần nhất trước đó bạn gặp tình trạng loay hoay tương tự là khi nào?"*

#### F. Ba phản xạ xử lý dữ liệu lệch (Deflect / Anchor / Dig)
- **Deflect (Khi user khen giải pháp giả định)**:
  - *User nói*: *"Em nghĩ nếu thầy cô biết em chưa hiểu mà nhắn tin hỗ trợ thì tuyệt vời quá!"*
  - *Interviewer phản xạ*: *"Cảm ơn bạn. Quay lại thực tế một chút nhé, trong những lần tự học gần đây, khi bạn chưa hiểu bài mà thầy cô chưa nhắn tin thì bạn đã làm gì?"*
- **Anchor (Khi user nói chung chung hoặc hứa hẹn tương lai)**:
  - *User nói*: *"Thường thì em sẽ lên mạng tra tài liệu thêm, hoặc sau này em sẽ chủ động hỏi giảng viên."*
  - *Interviewer phản xạ*: *"Hãy kể mình nghe cụ thể lần gần nhất gần đây bạn lên mạng tra tài liệu cho phần khó: Bạn đã gõ từ khóa gì và mất bao lâu để tìm ra câu trả lời?"*
- **Dig (Khi user đề xuất tính năng/giải pháp)**:
  - *User nói*: *"Hệ thống nên có nút bấm để báo ngay cho giảng viên biết mình chưa hiểu slide này."*
  - *Interviewer phản xạ*: *"Điều đó giúp bạn làm được gì? Hiện tại khi chưa có nó thì bạn xử lý ra sao?"*

#### G. Câu hỏi kết thúc (Closing Question)
> *"Có điều gì diễn ra trong lần loay hoay học bài đó mà mình chưa hỏi nhưng bạn nghĩ là quan trọng để giúp mình hiểu đúng trải nghiệm của bạn không?"*

---

### 3.2 HƯỚNG DẪN DÀNH CHO GIẢNG VIÊN (INSTRUCTOR / COACH)

#### A. Tiêu chí tuyển chọn & Sàng lọc (Instructor Recruitment)
- **Population**: Giảng viên hoặc trợ giảng (TA/Coach) phụ trách các khóa học trực tuyến/kết hợp quy mô lớn (>50 học viên) có thành phần tự học trên LMS.
- **Recruitment Criteria**:
  1. Đã trực tiếp đứng lớp hoặc quản lý vận hành khóa học trực tuyến trong vòng 30 ngày gần nhất.
  2. Từng có hành động rà soát, kiểm tra xem học viên nào trong lớp đang gặp khó khăn.
- **Recruitment Check Question**:
  > *"Trong học kỳ hoặc khóa học trực tuyến gần nhất mà bạn phụ trách, bạn có nhớ lần nào bạn chủ động đi tìm kiếm thông tin hoặc lọc danh sách để xem có học viên nào đang bị tụt lại phía sau hay học yếu để hỗ trợ không?"*
  - **Pass Condition**: Giảng viên xác nhận có và kể được sự kiện cụ thể.
  - **Fail Condition**: Giảng viên trả lời không có thời gian làm việc đó hoặc chỉ chấm điểm cuối kỳ. (Ghi nhận đây là thông tin quan trọng và chuyển câu hỏi sang workaround chấm điểm).

#### B. Lời mở đầu (Opening)
> *"Kính chào thầy/cô, em là [Tên], đại diện nhóm nghiên cứu trải nghiệm giảng dạy trực tuyến. Hôm nay em rất mong muốn được lắng nghe những chia sẻ thực tế của thầy/cô về quy trình theo dõi và hỗ trợ học viên trong các khóa học trực tuyến. Buổi trò chuyện hoàn toàn mang tính chất tìm hiểu thực tế công việc hàng ngày của thầy/cô, không có đúng sai. Xin phép được bắt đầu ạ."*

#### C. Câu hỏi mở đầu câu chuyện (Story Opener)
> *"Kể cho em nghe về lần gần nhất thầy/cô phát hiện ra một học viên trong lớp trực tuyến của mình đang gặp khó khăn lớn với nội dung bài học. Thầy/cô đã phát hiện ra điều đó như thế nào?"*

#### D. Big 3 Main Questions cho Giảng viên

| STT | Điều cần học (Learning Goals) | Câu hỏi sẽ dùng (Mom Test compliant) |
| :--- | :--- | :--- |
| **Q1** | **Pain & Consequence**: Mức độ nghiêm trọng của việc phát hiện muộn học viên gặp khó khăn đối với giảng viên. | *"Khi phát hiện ra học viên đó gặp khó khăn (thường là qua điểm thi hoặc email hỏi bài muộn), hậu quả hoặc ảnh hưởng của việc phát hiện muộn này đối với việc dạy học của thầy/cô lúc đó ra sao?"* |
| **Q2** | **Workaround & Capacity**: Các phương pháp rà soát hiện tại và quỹ thời gian thực tế giảng viên có thể dành ra để can thiệp hỗ trợ. | *"Thầy/cô đã làm những cách cụ thể nào để theo dõi tiến trình hiểu bài của cả lớp và thầy/cô đã dành ra khoảng bao nhiêu thời gian trong tuần qua để liên hệ hỗ trợ riêng cho các học viên yếu?"* |
| **Q3** | **Scary Assumption (Rào cản can thiệp)**: Rào cản tâm lý hoặc quy trình khiến giảng viên chần chừ không chủ động nhắn tin hỗ trợ khi học viên chưa hỏi. | *"Thầy/cô đã từng gặp trường hợp nào nghi ngờ học viên đang học yếu (ví dụ qua log LMS hoặc điểm quiz kém) nhưng lại quyết định chần chừ hoặc không chủ động liên hệ nhắn tin hỗ trợ họ chưa? Điều gì đã ngăn cản thầy/cô lúc đó?"* *(Bổ sung probe đào sâu nỗi sợ bị coi là theo dõi học viên)* |

#### E. Probe Bank & Phản xạ xử lý (Instructor-side Probes)
- *"Lúc thầy/cô nhắn tin hỗ trợ học viên đó, phản hồi của học viên ra sao? Họ có cởi mở chia sẻ không?"*
- *"Quy trình soạn tin nhắn và giải thích lại bài cho học viên đó tốn của thầy/cô bao nhiêu thời gian?"*
- *"Có khi nào thầy/cô soạn xong tin nhắn định gửi cho một học viên yếu nhưng lại xóa đi không gửi? Lý do lúc đó là gì?"* *(Thêm probe sau luyện tập)*
- *"Làm sao thầy/cô phân biệt được một học viên đang học rất kỹ (dừng slide lâu) với một học viên đang không hiểu bài bằng các công cụ LMS hiện tại?"*

---

### 3.3 Bảng phân công phỏng vấn (Interview Assignment)

| Thành viên | Đối tượng dự kiến phỏng vấn | Vai trò trong buổi phỏng vấn | Ghi chú |
| :--- | :--- | :--- | :--- |
| **Trần Xuân Bách** | Học viên  (Khóa học Ai Thực Chiến) | Người phỏng vấn chính - [Nguyễn Trọng Nam] (Interviewer) | Tập trung đào sâu Pain A (dữ liệu chẩn đoán sớm). |
| **Nguyễn Quốc Thịnh** | Học viên  (Khóa học Ai Thực Chiến) | Người phỏng vấn chính - [LabCoach Quang Anh] (Interviewer)  | Tập trung đào sâu các workaround và sự an toàn tâm lý khi nhận can thiệp. |
| **Nguyễn Hoàng Minh** | Học viên  (Khóa học Ai Thực Chiến) | Người phỏng vấn chính - [Đặng Thái Nam Sơn] (Interviewer) | Kiểm chứng rào cản thời gian và sự sẵn sàng sử dụng dữ liệu thao tác của instructor. |

---

## 4. Practice Reflection

### 4.1 Trần Xuân Bách — 2A202601093
- **Câu hỏi đã giúp user kể một tình huống cụ thể**:
  > *"Hãy nhớ lại lần gần nhất bạn gặp một bài học trực tuyến trên LMS mà bạn cảm thấy bế tắc hoặc chưa chắc mình hiểu đúng. Bạn kể cho mình nghe chuyện gì đã xảy ra lúc đó được không?"* (Neo user vào bài học CSS Grid tuần trước).
- **Chỗ cần làm tốt hơn ở lần phỏng vấn thật**:
  > Ban đầu tôi đã vô tình hỏi một câu mang tính opinion: *"Bạn nghĩ sao nếu thầy cô nhắn tin hỗ trợ đúng lúc?"* khiến học viên trả lời xã giao theo hướng ủng hộ feature. Ở lần phỏng vấn thật, tôi cần giữ im lặng tuyệt đối về mặt giải pháp và chỉ tập trung hỏi về hành vi quá khứ.

### 4.2 Nguyễn Quốc Thịnh — 2A202601675
- **Câu hỏi đã giúp user kể một tình huống cụ thể**:
  > *"Khi nhận ra mình đang bị bế tắc ở phần đó, bạn đã thực hiện những hành động cụ thể nào để tự giải quyết?"* (User đã kể chi tiết việc họ lên Youtube gõ từ khóa và tự loay hoay trong 45 phút).
- **Chỗ cần làm tốt hơn ở lần phỏng vấn thật**:
  > Tôi đã bỏ lỡ một tín hiệu quan trọng (bỏ lỡ cue) khi học viên nói họ hay tự tìm tài liệu ngoài. Tôi đã không đào sâu xem tại sao họ lại không chọn cách liên hệ với giảng viên hay trợ giảng ngay lúc đó. Lần tới, tôi sẽ chú ý nghe các từ khóa nhạy cảm để hỏi sâu hơn.

### 4.3 Nguyễn Hoàng Minh — 2A202601229
- **Câu hỏi đã giúp giảng viên kể một tình huống cụ thể**:
  > *"Kể cho em nghe về lần gần nhất thầy/cô phát hiện ra một học viên trong lớp trực tuyến của mình đang gặp khó khăn lớn. Thầy/cô đã phát hiện ra điều đó như thế nào?"* (Giảng viên đã kể về lần phát hiện một học viên điểm quiz chương 3 cực kỳ kém và phải nhắn tin riêng).
- **Chỗ cần làm tốt hơn ở lần phỏng vấn thật**:
  > Tôi đã mắc lỗi nghiêm trọng là giải thích giải pháp (solution pitching/leakage) khi giảng viên nói họ không có thời gian theo dõi học viên: *"Bên em đang định làm cái AI quét hành vi..."*. Rút kinh nghiệm sâu sắc, tôi tuyệt đối không được nói về sản phẩm để tránh làm lệch dữ liệu đầu vào.

### 4.4 Sau khi luyện, nhóm đã sửa Conversation Guide ở đâu và vì sao?
1. **Sửa câu hỏi Learner Q3**: Ban đầu câu hỏi hỏi trực diện *"Đã bao giờ bạn được giảng viên chủ động liên hệ khi loay hoay chưa?"* thường bị học viên trả lời *"Chưa bao giờ"* và kết thúc hội thoại. Nhóm đã sửa đổi thành hướng mở hơn: kết hợp cả việc được chủ động liên hệ trong các môn học trước đây (kể cả offline) và tình huống gián tiếp khi học viên nhận điểm kém mà không được giải thích. Điều này giúp khai thác tốt hơn cảm giác bị giám sát hoặc nhu cầu thực tế của học viên.
2. **Bổ sung Probe cho Instructor Q3**: Nhóm bổ sung câu hỏi đào sâu rào cản tâm lý của giảng viên: *"Có khi nào thầy/cô soạn xong tin nhắn định gửi cho một học viên yếu nhưng lại xóa đi không gửi? Lý do lúc đó là gì?"* nhằm làm rõ creepy factor từ phía người dạy.

---

## 5. AI Support Log

| Việc | AI hỗ trợ gì? | Nhóm phải tự kiểm / chỉnh gì? |
| :--- | :--- | :--- |
| **Chuyển Evidence Map thành Big 3** | Gợi ý 3 learning goals cốt lõi từ Chặng 1, trong đó xác định đúng "Scary Assumption" về sự an toàn tâm lý của học viên khi bị giám sát. | Nhóm đã kiểm tra và xác nhận Big 3 này phản ánh đúng các rủi ro lớn nhất trong change chain. |
| **Viết Conversation Guide** | Soạn thảo các câu hỏi Story Opener và Main Questions theo chuẩn Mom Test (neo vào quá khứ, loại bỏ solution/opinion). | Nhóm đã chỉnh sửa câu hỏi Learner Q3 sau khi nhận thấy nó bị cụt trong lúc phỏng vấn giả định. |
| **Kiểm tra leading / hypothetical questions** | Quét và lọc bỏ các câu hỏi dạng *"Thầy/cô có muốn..."* hoặc *"Em có thích..."* sang dạng hành vi thực tế. | Nhóm đã tự sửa lại kịch bản phỏng vấn thực tế để tránh lỗi solution leakage của Minh và opinion trap của Bách. |
| **Red Team Review & Mom Test** | Đóng vai trò UX Lead phản biện sắc bén các rủi ro thiên kiến (bias) trong nghiên cứu và đánh giá chất lượng câu hỏi. | Nhóm đã tự rút ra bài học thực tế thông qua buổi luyện tập phỏng vấn giả định để bổ sung phần Practice Reflection trung thực. |
