# DESIGN.md — Landing page xưởng nhạc cụ thủ công Tiếng Tơ

> Tài liệu thiết kế chốt cho sprint TEC-408 (task Thiết kế TEC-409). Dev (task Dev của sprint) dựng đúng tài liệu này, không tự thêm màu, font hay khối ngoài danh sách. QA đối chiếu bản dựng với tài liệu này, kèm kiểm tra đa dạng theo OPERATIONS.md mục 16.5.

## 0. Khác biệt so với các project gần nhất (bắt buộc theo mục 16.5 — đã đọc thật ngày 2026-10-26)

Thứ tự project mới nhất lấy từ https://msoft.genalpha.dev/api/office; DESIGN.md đọc trực tiếp qua raw.githubusercontent.com ngày 2026-10-26 (repo tarotlight-app là app mobile private, không có archetype web nên không tính):

| Project (mới → cũ) | Archetype | Cặp font | Nhiệt màu |
|---|---|---|---|
| Da Mộc (m-software-da-moc, TEC-398) | A1 Editorial dọc (bản dựng thật, PR #1, 10.222 byte) VÀ A3 Lệch tâm (bản trên main hiện tại, 8.264 byte, do Executor cũ ghi đè sau khi sprint đóng) — coi như đã dùng cả A1 lẫn A3 | Playfair Display + Be Vietnam Pro | Tối-ấm (nền `#1F1A15`) |
| Đắng Ngọt (m-software-dang-ngot, TEC-384) | A5 Theo chương | Fraunces + Be Vietnam Pro | Sáng-ấm (nền `#F3E9D7`) |
| Kim Ngọc (m-software-kim-ngoc, TEC-371) | A2 Split | Noto Serif Display + Manrope | Tối-ấm (nền `#141210`) |

Đối chiếu trực tiếp và lựa chọn cho Tiếng Tơ:

- **Archetype: A7 Typography-first** — KHÔNG phải A1 hay A3 của Da Mộc (project liền trước, tính cả hai bản), KHÔNG phải A5 của Đắng Ngọt (project liền trước nữa), và cũng khác A2 của Kim Ngọc. Cách A7 thể hiện ở: chữ làm chủ đạo — tên xưởng "Tiếng Tơ" ở hero và tiêu đề mỗi khối dùng cỡ chữ khổng lồ, ảnh đóng vai trò nền / minh họa phía sau hoặc bên dưới chữ, không phải xếp dọc từng khối ảnh lớn (A1), không phải lệch trục chồng lấn mép ảnh (A3), không phải chia chương đánh số (A5), không phải chia đôi đều hai bên (A2). Xem mục "Bố cục".
- **Cặp font: Fraunces + Be Vietnam Pro — GIỮ NGUYÊN công thức gợi ý, có cân nhắc và ghi rõ lý do:** cặp này KHÁC nguyên cặp của project liền trước Da Mộc (Playfair Display + Be Vietnam Pro) vì font tiêu đề đã đổi từ Playfair Display sang Fraunces — đúng tiền lệ Đắng Ngọt (đổi font tiêu đề là đủ đổi cặp). Cặp này trùng với Đắng Ngọt, nhưng Đắng Ngọt chỉ là project thứ 2 gần nhất, còn luật §16.5 chỉ cấm lặp nguyên cặp của project liền trước, nên không vi phạm. Giữ cặp này vì đúng tinh thần công thức gợi ý: Fraunces là serif cổ điển, nét đậm, hợp atelier chế tác đàn châu Âu cổ điển, ấm và trầm; Be Vietnam Pro đọc rõ tiếng Việt cho nội dung dài. Nếu đổi sang một cặp khác chỉ để tránh trùng với project thứ 2 gần nhất thì sẽ xa tinh thần gợi ý mà luật không bắt buộc.
- **Nhiệt màu: TỐI-ẤM — KHÔNG CẦN ĐỔI:** giữ nguyên công thức gợi ý (nền tối `#1C1A17`, chữ kem `#F3EDE2`, nhấn hổ phách `#D9A441`). Chuỗi nhiệt sau khi chọn: Tiếng Tơ (tối-ấm) → Da Mộc (tối-ấm) → Đắng Ngọt (sáng-ấm): chỉ 2 project tối-ấm liên tiếp, KHÔNG tạo thành 3 project liên tiếp cùng nhiệt màu. Không khí xưởng đàn buổi tối, ánh đèn vàng, gỗ tối – hổ phách được giữ nguyên.
- **Điểm nhấn đặc sắc riêng: "khuông nhạc + lỗ thoát âm"** (xem mục riêng bên dưới) — khác "đường chỉ khâu + lỗ đục da" của Da Mộc, "vạch chia thanh socola tan chảy + nhãn nốt vị" của Đắng Ngọt, "vạch cắt giác + sao 4 cánh" của Kim Ngọc.

## Tổng quan

- Sản phẩm: landing page 1 trang, visual-first, cho xưởng nhạc cụ thủ công Tiếng Tơ — làm tay guitar acoustic, ukulele, đàn tranh; nhận đặt làm riêng và tham quan xưởng.
- Archetype: **A7 Typography-first** — chữ khổng lồ làm chủ đạo, nhạc cụ và âm thanh được kể bằng chữ trước, ảnh sau.
- Phong cách tham chiếu: **atelier chế tác đàn châu Âu cổ điển, ấm và trầm** — xưởng gỗ tối, ánh đèn vàng hổ phách, thợ bào gỗ bằng tay, dây đàn căng, giấy vẽ phác dáng đàn; không dùng ảnh studio trắng, không dùng tông lạnh neon.
- Ngôn ngữ: tiếng Việt, hỗ trợ dấu đầy đủ (cả Fraunces và Be Vietnam Pro đều hỗ trợ tiếng Việt).

## Bảng màu (mã hex + vai trò)

| Mã hex | Vai trò |
|---|---|
| `#1C1A17` | Nền chính toàn trang — nâu gỗ tối, tối-ấm |
| `#292219` | Nền khối phụ xen kẽ (thẻ bộ sưu tập, khối quy trình) — nâu gỗ nhạt hơn nền chính một nấc |
| `#F3EDE2` | Chữ chính + tiêu đề — kem giấy vẽ phác, tương phản cao trên nền tối |
| `#A89A86` | Chữ phụ (mô tả ngắn, chú thích ảnh, ghi chú giá mẫu) — be xám ấm |
| `#D9A441` | Nhấn chính — vàng hổ phách: nút bấm, giá mẫu, khuông nhạc, lỗ thoát âm, số bước |
| `#7C5A2E` | Nhấn phụ — nâu gỗ đậm: viền thẻ, viền ảnh, chân trang; không làm nền khối lớn |

Quy tắc dùng màu: nền luôn là tối (`#1C1A17` hoặc `#292219` xen kẽ theo khối); không dùng khối nền sáng toàn trang; màu nhấn `#D9A441` chỉ dùng cho nút, giá, điểm nhấn — không tô nền lớn bằng màu nhấn; tối đa 2 màu nền trong một khối.

## Typography

- Font tiêu đề: **Fraunces** (serif cổ điển, nét đậm, hỗ trợ tiếng Việt) — tên xưởng ở hero 96px desktop / 56px mobile (đây là cỡ chữ chủ đạo của A7, lớn hơn hẳn tiêu đề khối), tiêu đề khối 56px desktop / 36px mobile, tên nhạc cụ 28px.
- Font nội dung: **Be Vietnam Pro** (hỗ trợ tiếng Việt) — nội dung 17px, dòng cao 1.7; chú thích 14px; nút bấm 16px đậm; nhãn khối 13px đậm, chữ hoa, giãn cách chữ 0,08em.
- Quy tắc A7: mỗi khối mở đầu bằng một từ khóa khổng lồ một dòng (ví dụ "GỖ", "DÂY", "ÂM") bằng Fraunces 96px desktop / 56px mobile, màu `#D9A441` ở độ mờ 15% làm nền chữ phía sau tiêu đề khối, không làm chữ chính khó đọc; tiêu đề khối chính đặt đè lên trên từ khóa đó.
- Không dùng thêm font thứ ba.

## Bố cục (A7 Typography-first)

- Desktop (rộng ≥ 1024px): nội dung chính rộng tối đa 1080px, căn giữa; khoảng cách giữa các khối 96px; padding section 96px.
- Hero (xem mục "Khối nội dung"): ảnh toàn màn hình thợ bào gỗ thân đàn làm nền, phủ tối 55% để chữ đọc được; tên xưởng "Tiếng Tơ" 96px Fraunces đặt giữa màn hình, kèm một câu định vị và 2 nút; không chia đôi, không thanh bên.
- Các khối sau hero: tiêu đề khối luôn đi kèm từ khóa khổng lồ mờ phía sau (quy tắc A7 ở trên); nội dung mỗi khối xếp dọc một cột, chữ chiếm tối đa 60% chiều rộng khối; ảnh đặt dưới chữ, rộng toàn khối, không xếp lưới nhiều cột kiểu tạp chí, không chia chương đánh số.
- Mobile (< 768px): một cột duy nhất; hero cắt 4:5 (giữ thợ ở giữa khung); từ khóa khổng lồ 56px; khoảng cách khối 64px.
- Không có cuộn ngang ở bất kỳ breakpoint nào.

## Khối nội dung (theo thứ tự, không đổi thứ tự, không thêm khối ngoài danh sách)

1. **Hero** — ảnh lớn toàn màn hình: thợ đang bào gỗ thân đàn (thấy rõ tay thợ, bào gỗ, vân gỗ); tiêu đề "Tiếng Tơ" + câu định vị một dòng "Đàn làm bằng tay, âm thanh làm bằng gỗ thật"; 2 nút "Xem bộ sưu tập" và "Đặt lịch tham quan".
2. **Giới thiệu xưởng + Quy trình 4 bước** — đoạn giới thiệu ngắn về xưởng (làm tay từ chọn gỗ tới căn chỉnh âm thanh, không làm dây chuyền); sau đó đúng 4 bước, xếp dọc từng bước (không xếp ngang 4 ô, không chia chương): (01) Chọn gỗ — (02) Tạo dáng — (03) Lắp dây — (04) Căn chỉnh âm thanh; mỗi bước gồm số bước lớn bằng Fraunces màu `#D9A441`, tên bước, mô tả 1–2 câu, 1 ảnh thợ đang làm bước đó.
3. **Bộ sưu tập** — đúng 3 nhóm, xếp dọc từng thẻ (mỗi thẻ: ảnh lớn, tên, mô tả 1–2 câu, giá mẫu): guitar acoustic, ukulele, đàn tranh; mỗi giá ghi rõ "(giá mẫu)" ngay cạnh giá.
4. **Câu chuyện người thợ + ảnh xưởng** — ảnh xưởng (bàn làm đàn, dụng cụ, đàn đang làm dở) + đoạn văn ngắn về người thợ chính (không bịa tên thật, dùng cách gọi chung "người thợ chính" hoặc placeholder); 2–3 cảm nhận khách mẫu, tên người cảm nhận để placeholder, ghi rõ là mẫu.
5. **Form liên hệ / đặt lịch tham quan — CHỈ giao diện** — các trường: họ tên, số điện thoại, loại yêu cầu (mua sẵn / đặt làm riêng / tham quan xưởng), ngày muốn tham quan, ghi chú; nút "Gửi yêu cầu" chỉ hiển thị, không gửi thật (xem mục "Quy tắc dữ liệu thật / mẫu").
6. **Chân trang** — tên xưởng, câu slogan một dòng, ghi chú "Trang demo — giá và form chỉ là mẫu", và các mục [CẦN BỔ SUNG] (xem dưới).

## Điểm nhấn đặc sắc: "khuông nhạc + lỗ thoát âm"

Nhìn thấy được, lặp lại xuyên suốt trang, không project gần đây nào có:

- **Vạch chia "khuông nhạc":** vạch chia giữa các khối KHÔNG phải đường kẻ liền trơn — là 5 đường ngang mảnh 1px màu `#D9A441`, cách nhau 6px, dài toàn bộ chiều rộng nội dung, ở chính giữa có một nốt nhạc đen ♩ cỡ 20px màu `#D9A441` đặt trên khuông. Vạch này xuất hiện ở đầu mỗi khối sau hero, không dùng ở nơi khác.
- **Dấu "lỗ thoát âm":** mỗi tiêu đề khối đi kèm một vòng tròn 28px viền đôi màu `#D9A441` (viền ngoài 2px, viền trong 1px, cách nhau 4px), bên trong vòng tròn có 6 đường dọc mảnh 1px màu `#D9A441` mô phỏng 6 dây đàn chạy qua lỗ thoát âm của guitar; vòng tròn đặt ngay trước tiêu đề khối. Mỗi thẻ bộ sưu tập cũng có một vòng tròn lỗ thoát âm nhỏ 16px ở góc trên bên phải ảnh.
- Không dùng đường kẻ liền trơn làm vạch chia chính ở bất cứ đâu trên trang.

## Quy tắc hình ảnh (§16.3)

- Tông ảnh: đồng tông gỗ tối – hổ phách — ảnh thợ làm đàn dưới ánh đèn vàng ấm, gỗ tối, vân gỗ rõ; tuyệt đối không dùng ảnh ánh sáng trắng lạnh, không dùng ảnh nền trắng studio.
- Tỉ lệ khung: hero toàn màn hình 16:9 trên desktop, cắt giữa thành 4:5 trên mobile (giữ thợ ở giữa khung); ảnh quy trình 3:2 ngang cho cả 4 bước; ảnh bộ sưu tập 4:5 dọc (ảnh lớn, chiếm gần hết chiều rộng thẻ); ảnh xưởng 16:9 ngang.
- Nội dung ảnh: hero bắt buộc là thợ đang bào gỗ thân đàn (thấy rõ bào gỗ và thân đàn đang thành hình); ảnh quy trình theo đúng bước (gỗ thô → dáng đàn → lắp dây → thợ gảy thử / căn chỉnh); ảnh bộ sưu tập là cận cảnh từng nhạc cụ hoàn thiện, thấy rõ thân đàn và dây.
- Ảnh mẫu: dùng ảnh mẫu chất lượng cao, đồng tông theo quy tắc trên ngay từ bản đầu tiên; ghi rõ là ảnh mẫu trong kết quả của Dev.

## Quy tắc dữ liệu thật / mẫu (bắt buộc cho Dev)

- Giá trên trang **luôn là giá mẫu**: mỗi giá phải kèm chữ "Giá mẫu" ngay cạnh, footer ghi rõ "Tất cả giá trên trang là giá mẫu".
- Địa chỉ, điện thoại, giờ mở cửa, người phụ trách và tên người cảm nhận để placeholder **`[CẦN BỔ SUNG]`**, tuyệt đối không bịa số liệu thật.
- Form liên hệ/đặt lịch tham quan **CHỈ giao diện**: submit dùng preventDefault và hiện thông báo mẫu ("Đây là bản giao diện mẫu — yêu cầu chưa được gửi đi thật"); không có thuộc tính action, không fetch, không mailto:, không tel:.
- Toàn bộ ảnh là ảnh mẫu, footer ghi rõ điều này.

## Ghi chú cho Dev / QA

- Dev dựng đúng tài liệu này, không tự thêm màu, font hay khối ngoài danh sách; ảnh dùng ảnh mẫu đồng tông gỗ tối – hổ phách, đúng tỉ lệ khung.
- QA đối chiếu bản dựng với tài liệu này ở mức code + thị giác theo §16.4, kèm kiểm tra đa dạng §16.5: archetype A7 phải khác A1/A3 (Da Mộc) và A5 (Đắng Ngọt); cặp font Fraunces + Be Vietnam Pro phải khác nguyên cặp Playfair Display + Be Vietnam Pro của Da Mộc; nhiệt màu tối-ấm không tạo thành 3 project liên tiếp cùng nhiệt (chuỗi: Tiếng Tơ tối-ấm → Da Mộc tối-ấm → Đắng Ngọt sáng-ấm).
