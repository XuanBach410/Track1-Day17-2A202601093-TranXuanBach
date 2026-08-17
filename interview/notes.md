# Interview Notes — Case C

## Interviewee Info
- **Code/ID**: LC1 (LabCoach 1 - Quang Anh)
- **Role**: LabCoach / Assistant (Sinh viên khóa 2)
- **Date & Time**: Chưa xác định từ dữ liệu hiện có.
- **Interviewer**: Nguyễn Quốc Thịnh
- **Recruitment Check**: PASS (Interviewee trực tiếp làm LabCoach hướng dẫn thực hành và sửa lỗi kỹ thuật trực tiếp cho học viên trong lớp học "AI Thực Chiến", đã và đang trực tiếp trải qua các tình huống phát hiện học viên bế tắc).
- **Recording Link**: [Google Drive Folder](https://drive.google.com/drive/folders/17ukLaYeC2AkHzRGFSofs_9RR1bju806A?usp=sharing)

## Recent Event
- **Situation**: Các buổi thực hành lab code trực tiếp của khóa học "AI Thực Chiến" với quy mô lớp đông học viên.
- **Trigger**: LabCoach nhận biết học viên gặp khó khăn qua việc học viên chủ động giơ tay lên gọi hoặc LabCoach chủ động đi tuần tra vòng quanh lớp từ phía sau và phát hiện học viên bị kẹt (dừng lâu, loay hoay tại một chỗ) trên màn hình laptop.
- **Goal**: Hỗ trợ học viên giải quyết các lỗi kỹ thuật cài đặt môi trường lab, lỗi đăng ký tài khoản hoặc debug lỗi code thực hành.
- **What happened**: Học viên gặp lỗi kỹ thuật hoặc bug code -> Họ loay hoay tự giải quyết hoặc giơ tay gọi -> LabCoach đi xuống xem màn hình (hoặc phát hiện học viên bị kẹt khi quan sát từ phía sau) -> LabCoach chủ động hỏi han và giải quyết lỗi -> Học viên vượt qua lỗi và tiếp tục bài thực hành.

## Observed Past Behavior
- LabCoach đi vòng vòng đằng sau các học viên để quan sát màn hình laptop của họ trong buổi thực hành.
- Theo dõi xem học viên có bị kẹt (dừng lâu một lúc tại một thao tác) để chủ động can thiệp hỏi thăm hỗ trợ.
- Sửa lỗi đăng ký tài khoản, lỗi cài đặt môi trường lab, và debug bug code thực hành cho học viên.
- Chỉ hỗ trợ được 1 học viên tại một thời điểm (không thể hỗ trợ đồng thời nhiều người).
- Sử dụng hệ thống VILAB: Theo dõi danh sách ticket được học viên gửi lên bảng điều khiển trực tuyến và đi xuống hỗ trợ đúng vị trí.

## Workarounds
- **Đi vòng quanh lớp quan sát màn hình từ phía sau**: Nhằm phát hiện chủ động học viên bị kẹt, giải quyết việc nhiều học viên gặp lỗi nhưng có xu hướng ngại hỏi trực tiếp.
- **Sử dụng hệ thống VILAB để raise ticket**: Cho phép học viên gửi thắc mắc hoặc yêu cầu trợ giúp gián tiếp qua hệ thống thay vì phải giơ tay phát biểu trực tiếp.

## Effort / Cost
- **Time Cost**: Thời gian hỗ trợ xử lý lỗi đăng ký tài khoản hoặc debug bug code tốn nhiều thời gian nhất ("support nó hơi lâu").
- **Capacity Limit**: LabCoach bị giới hạn năng lực hỗ trợ (chỉ có thể giải quyết 1-1 tại một thời điểm, dễ gây nghẽn hàng đợi hỗ trợ nếu nhiều học viên gặp lỗi cùng lúc).
- **Deploy issues**: Chưa xác định từ dữ liệu hiện có (LabCoach xác nhận chưa gặp trường hợp học viên bị lỗi deploy trong các buổi thực hành gần đây).

## Consequences
- Học viên gặp lỗi kỹ thuật hoặc bug code sẽ bị bế tắc, không thể tiếp tục thực hiện bài lab tiếp theo nếu không được can thiệp kịp thời.
- Sự e ngại của học viên ("ngại hỏi", "gặp vấn đề nhưng lại ngại hỏi người khác") khiến họ im lặng chịu đựng lỗi, làm lãng phí thời gian học tập trong buổi lab.

## Frequency / Recurrence
- Tình trạng học viên ngại hỏi diễn ra thường xuyên và là xu hướng chung của học viên ("học viên vẫn đang có xu hướng là ngại hỏi... đôi lúc họ gặp vấn đề nhưng họ lại ngại hỏi người khác").

## Key Quotes
- *"Hiện tại mình là có hai hình thức, là một là học viên sẽ gọi mình, giơ tay lên và gọi... Hoặc là mình sẽ đi vòng vòng vòng đằng sau các bạn ấy và mình nhìn vào màn hình laptop các bạn ấy xem các bạn ấy đang làm gì. Nếu mà khó khăn mình thấy các bạn ấy kẹt ở đấy một lúc rồi mà vẫn không qua được thì mình sẽ chủ động hỏi thăm để support."*
- *"Theo mình thấy tốn công là... đôi lúc các bạn ấy gặp vấn đề về đăng ký tài khoản, hoặc là vấn đề về gặp một số bug lỗi gì đấy ở đâu đấy, thì mình support nó hơi lâu."*
- *"Mình thấy là các bạn học viên vẫn đang có xu hướng là ngại hỏi... đôi lúc họ gặp vấn đề nhưng họ lại ngại hỏi người khác."*
- *"Mới đây thì có cái VILAB, thì ở trong phòng lab nếu mà có sinh viên nào ngại hỏi thì họ có thể lên đấy để họ gõ tay vào... họ raise ticket lên đấy, bọn mình sẽ xem được ở trên kia và mình xuống tận nơi."*

## Evidence FOR Hypothesis
- **Evidence**: LabCoach xác nhận học viên gặp khó khăn thường có xu hướng im lặng và ngại chủ động hỏi người khác ("vẫn đang có xu hướng là ngại hỏi... đôi lúc họ gặp vấn đề nhưng họ lại ngại hỏi người khác").
  - *Nó củng cố phần nào của hypothesis*: Củng cố rào cản thông tin ở Chặng 1, chứng minh rằng học viên struggle thực tế sẽ chọn im lặng thay vì chủ động tìm kiếm sự giúp đỡ từ giảng viên/trợ giảng.
- **Evidence**: LabCoach phải dùng các chỉ số hành vi thực tế như việc học viên "kẹt ở đấy một lúc rồi mà vẫn không qua được" (quan sát thủ công qua màn hình) làm tín hiệu can thiệp.
  - *Nó củng cố phần nào của hypothesis*: Củng cố giả thuyết rằng "thời gian kẹt/dừng lâu trên slide hoặc bài tập" là tín hiệu chẩn đoán sớm có giá trị thực tế để nhận biết trạng thái struggle.

## Evidence AGAINST Hypothesis
- **Evidence**: Phòng thực hành hiện tại đã trang bị hệ thống VILAB cho phép học viên raise ticket trợ giúp gián tiếp lên hệ thống và LabCoach sẽ dựa vào đó để xuống tận nơi hỗ trợ.
  - *Nó làm yếu assumption nào*: Làm yếu giả định cho rằng giảng viên/trợ giảng hoàn toàn "mù thông tin" về tiến trình học và không có công cụ hỗ trợ nào khác ngoài việc chờ học viên giơ tay trực tiếp. Hệ thống ticket VILAB đã đóng vai trò là một Support Queue thủ công/bán tự động khá hiệu quả.
  - *Mức ảnh hưởng*: Medium.

## Surprises & New Insights
- **Observation**: Học viên ngại giao tiếp mặt đối mặt trước lớp (giơ tay) nhưng sẵn sàng gõ yêu cầu hoặc raise ticket thông qua hệ thống VILAB.
  - *Why surprising*: Cho thấy rào cản của học viên chủ yếu là tâm lý e ngại gây chú ý hoặc sợ bị đánh giá năng lực, chứ không phải họ từ chối sự hỗ trợ.
  - *Possible implication*: Một cơ chế gửi tín hiệu hỗ trợ gián tiếp (raise ticket) tích hợp tinh tế ngay trên Vlearn có thể giải quyết tốt nỗi đau của học viên mà không cần hệ thống AI tự động theo dõi hành vi phức tạp (tránh creepy factor).

## Follow-up Actions
- **Evidence gap**: Chưa phỏng vấn được Giảng viên chính (Instructor) để kiểm chứng rào cản về mặt thời gian và mức độ sẵn sàng duyệt Support Queue trực tuyến ngoài giờ dạy.
- **Next interview target**: Cần phỏng vấn ít nhất 1 Giảng viên chính (Instructor) quản lý lớp học online/blended quy mô lớn.
- **Question cần đào sâu**: Giảng viên chính có sẵn lòng dành thời gian duyệt queue hỗ trợ học viên ngoài giờ dạy hay không, hay họ sẽ ủy quyền toàn bộ cho LabCoach/TA vận hành? Quy trình bàn giao và phối hợp giữa Instructor và LabCoach hiện tại ra sao?
