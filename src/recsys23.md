---
layout: base.njk
title: (vi) Tóm tắt hội nghị RecSys-23
---

${toc}


## Tóm tắt
Dưới đây là toàn bộ điểm nhấn mà mình lĩnh hội được sau 5 ngày tham dự [RecSys 23](https://recsys.acm.org/recsys23/) diễn ra tại Singapore.
- Các ông lớn đang xây dựng hệ thống nền tảng cho hệ thống gợi ý: từ Google, Meta, Amazon đến Netflix.
- Mô hình ngôn ngữ lớn (LLM) đang dần dần xâm chiếm cộng đồng nghiên cứu hệ thống gợi ý.
- Đánh giá tính hiệu quả của hệ thống vẫn còn là vấn đề nan giải.
## Ngày 1

Mặc dù tiêu đề của buổi hội thảo đầu tiên nói về [học sâu cho dữ liệu thưa](https://dlp4rec.github.io/), nhưng các bài trình bày khá là thập cẩm với đủ chủ đề khác nhau. Có vẻ vì được tài trợ (và tổ chức) bởi Huawei nên hầu hết các bài đều đến từ tập đoàn này. Xu hướng chung của năm nay (hoặc chí ít từ Huawei) là kết hợp LLM vào hệ thống gợi ý. Một hướng nghiên cứu nữa cũng được quan tâm là kết hợp mô hình đa phương [^5] trong hệ thống gợi ý. Điều này cũng dễ hiểu vì hiện giờ người dùng cuối tương tác với hệ thống quảng cáo/gợi ý bằng đa phương tiện: văn bản, hình ảnh, video. Các bài thuyết trình diễn ra chóng vánh bởi sự cố kỹ thuật liên tục (dẫn đến không có thời gian cho Q&A) và quá giờ. Một phần có vẻ Huawei hơi tham lam, dồn nhiều nghiên cứu của mình vào trong buổi workshop này. Không một bài báo nào quá ấn tượng, duy chỉ có [bài khảo sát về LLM cho hệ thống gợi ý](https://github.com/CHIANGEL/Awesome-LLM-for-RecSys) là đáng chú ý.

Buổi chiều mình dự được 1 phần của [CARS](https://cars-workshops.com/), chủ yếu là keynote về LLM. Bài này không gì ấn tượng, và trùng nội dung kha khá với bài khảo sát lúc sáng. Nghiên cứu đề xuất cũng không quá nổi bật.

Lúc sau thì mình chạy sang phần tutorial chủ đề [Recommender in the wild](https://github.com/recs-in-the-wild/recsys23-tutorial) vì có Kim thuyết trình (Principal Data Scientist mới của Visenze). Lúc qua thì phần của Kim đã xong, nên mình xem phần tiếp sau, tập trung về Bayesian A/B Testing. Phần này theo mình bám sát thực tế, cũng như đi vào trọng tâm khi phát triển hệ thống gợi ý người dùng. Một điểm quan trọng được nhấn mạnh là sử dụng độ đo như thế nào để sát với mục đích đánh giá, thuyết phục các bên liên quan (stakeholders) về ý nghĩa của độ đo. Từ sáng giờ thì bài về Bayesian A/B Testing là thu hút mình nhất, slides sinh động và diễn giả lôi cuốn người nghe.

Tính tranh thủ xem [FashionXrecsys](https://fashionxrecsys.github.io/fashionxrecsys-2023/) nhưng không có thời gian.

[^5]: Multi-modality - mình không biết dịch sao luôn.
## Ngày 2
Hôm nay mình xem được vài keynotes tại 2 workshops: ORSUM2023, CONSEQUENCES và VideoRecSys.

[Bài keynote từ ORSUM](https://web-ainf.aau.at/pub/jannach/slides/ORSUM2023-Keynote.pdf) ấn tượng, giàu thông tin, cung cấp cho người xem khái quát về hệ thống gợi ý chuỗi [^6] và hệ thống gợi ý theo phiên [^7]. Bài nói cũng nêu lên những vấn đề trong việc đánh giá tính hiệu quả của hệ thống, việc các chỉ số không nói lên được sự hài lòng của người dùng và các vấn đề liên quan. Nhiều trích dẫn trong bài liên quan đến đánh giá mô hình theo mình khá hữu dụng.

> Sequential recommender: Ví dụ trong giỏ hàng bạn có bánh phở, thịt bò, xương ống thì hệ thống sẽ đoán là bạn đang chuẩn bị làm phở nên sẽ gợi ý bạn mua thêm hành, chanh, gừng hay các nguyên liệu khác để chế biến, cho dù bạn có chế biến với các nguyên liệu đó hay không là 1 chuyện khác 🤣

> Session-based recommender: thông tin cho huyến luyện và dự đoán là phiên người dùng ẩn danh, không có lịch sử truy cập của từng account.

Những phần thuyết trình còn lại lần lượt đến từ Youtube Research, Instagram và Netflix rải rác ở workshop [CONSEQUENCES](https://www.youtube.com/watch?v=WRRnsZfcQ9g&ab_channel=CONSEQUENCESRecSysWorkshop) và [VideoRecsys](https://videorecsys.com/). Theo mình thì ngoại trừ bài của Youtube ra thì cả Instagram và Netflix chất lượng không cao, không tập trung vào vấn đề nào cụ thể. Tuy nhiên vẫn có vài mẫu thông tin hữu ích:
- Youtube trước kia tập trung phát triển mô hình để thu hút người xem. Giờ đây trong mô hình của họ cũng tối ưu cho người kiến tạo nội dung. Mình nghĩ với sự cạnh tranh từ Tiktok, đây là điều không tránh khỏi. Youtube cần tối ưu hệ thống sao cho các Youtuber cảm thấy nội dung của họ thực sự được người xem quan tâm và hứng thú, đồng thời giữ chân các Youtuber ở lại nền tảng của mình.
- Cả Youtube lẫn [Netflix đều đưa yếu tố UI khi tối ưu mô hình gợi ý](https://videorecsys.com/slides/mark_talk3.pdf). Đối với [Youtube thì đó là danh sách Xem Tiếp](https://videorecsys.com/slides/lukasz_keynote.pdf)[^1], quảng cáo[^2]. Trong khi đó thì Netflix tối ưu thứ tự các mục trong UI của họ: không phải lúc nào phần "Tiếp tục xem" nằm ở phần trên cùng của danh sách. Netflix còn tối ưu thứ tự của từng phim trong mỗi mục, và lẫn kết quả trả về khi search. Netflix xài chung 1 mô hình cho tìm kiếm và lẫn gợi ý (trải nghiệm cá nhân là phần tìm kiếm của Netflix hơi ngu, nhiều khi gợi ý phim mà Netflix không có).
- Trang "Khám Phá" của [Youtube đã bắt đầu sử dụng LLM để cải thiện embedding](https://arxiv.org/pdf/2305.15498.pdf) của tập huấn luyện. Đồng thời chủ đề gợi ý cũng sử dụng LLM để làm giàu bộ corpus.
- Netflix phát triển riêng từng mô hình cho mỗi quốc gia. Điều này khá tốn kém. Theo quan sát của họ, những thị trường mới này dần dần sẽ có kết quả tương đồng với mô hình của thị trường cũ, nên để tiết kiệm chi phí duy trì và phát hành, họ sẽ gộp các mô hình lại.
- Instagram đang bắt đầu phát triển một kỹ thuật mới: [Semantic ID(s)](https://videorecsys.com/slides/thomas_talk1.pdf).
- Mặc dù là **video**recsys, cả 3 ông lớn (Microsoft, Netflix, Meta) không hề đề cập bất cứ kỹ thuật, vấn đề nào khi làm việc với dữ liệu ảnh hay video. Hơi thất vọng vì mình đã kì vọng nhiều hơn từ những bài đến từ các nhóm này.

[^1]: Phía bên phải màn hình.
[^2]: quảng cáo có thể ảnh hưởng tiêu cực đến trải nghiệm xem của người dùng, dẫn đến sự không hài lòng khi trải nghiệm hệ thống gợi ý
[^6]: Sequential Recomendation.
[^7]: Session-based Recommendation.
## Ngày 3
Keynote là một bài PR đến từ Microsoft Research. Không nhiều ấn tượng bởi chủ yếu vẫn xoay quanh những sản phẩm sắp ra lò (Bing AI) mà Microsoft đang tập trung phát triển. Hôm nay là phiên posters đầu tiên, không được nhiều bài quá thú vị (1 phần là do những bài này đã được trình bài trong workshop). Có 1 bài bên Shopee sử dụng graph-based recommender, [bên Amazon (JP) phát triển mô hình nền tảng (foundational model) cho hành vi người dùng](https://www.amazon.science/publications/mcm-a-multi-task-pre-trained-customer-model-for-personalization). Mình xem phiên báo cáo chủ để Click-Through Rate Predictions, 3 bài đến từ Huawei và 1 bài đến từ JD (nhưng JD không trình bày). Không có gì ấn tượng, hoặc là người thuyết trình không cho mình cảm giác là công trình họ có gì ấn tượng. Tương tự với Trustworthy in Recommendation. Phần Sequential Recomendation (SRS) có vài bài thú vị. Một bài sử dụng [thông tin sản phẩm](https://dl.acm.org/doi/10.1145/3604915.3610643)[^3] đề cải thiện độ chính xác của mô hình. Một bài khác tìm cách [giảm kích thước và thời gian truy vấn](https://dl.acm.org/doi/10.1145/3604915.3608779).
- ⭐ [STRec: Sparse Transformer for Sequential Recommendations](https://dl.acm.org/doi/10.1145/3604915.3608779)
- ⭐ [Distribution-based Learnable Filters with Side Information for Sequential Recommendation](https://dl.acm.org/doi/10.1145/3604915.3608782)
- [Personalized Category Frequency prediction for Buy It Again recommendations](https://dl.acm.org/doi/abs/10.1145/3604915.3608822)
- [Integrating Item Relevance in Training Loss for Sequential Recommender Systems](https://dl.acm.org/doi/10.1145/3604915.3610643)
- [Complementary Product Recommendation for Long-tail Products](https://dl.acm.org/doi/10.1145/3604915.3608864)
- [How Users Ride the Carousel: Exploring the Design of Multi-List Recommender Interfaces From a User Perspective](https://dl.acm.org/doi/10.1145/3604915.3610638)
- [Bootstrapped Personalized Popularity for Cold Start Recommender Systems](https://dl.acm.org/doi/10.1145/3604915.3608820)

[^3]: như là thuộc tính của sản phẩm, hay danh mục sản phẩm.
## Ngày 4
GS. Tat-Seng Chua [khảo sát những tiến bộ gần đây của LLM(s)](https://drive.google.com/file/d/1-CcNK_2UXNrJ_MGEBURBvLe7Alh-dcPD/view). So với phần của Microsoft hôm qua thì bài này thú vị hơn nhiều. Một số hướng nghiên cứu được đề cập bao gồm finetune LLM cho các ứng dụng khác nhau với domain knowledge. Để làm giàu thêm ứng dụng của LLM, GS đề xuất sử dụng RAG ([Retrieval-Augmented Generation](https://research.ibm.com/blog/retrieval-augmented-generation-RAG)) nhằm cung cấp, bổ sung thông tin hệ thống LLM, đồng thời sử dụng công cụ ngoài luồng (external tools) cho xác thực nội dung. Một hướng đi cũng thú vị đó là Proactive Dialogs: ChatGPT chủ động đặt câu hỏi lại cho người dùng nhằm cải thiện chất lượng/độ chính xác của thông tin. Vì là hội nghị về mô hình gợi ý, GS cũng giới thiệu những công trình gần đây tận dụng LLM trong hệ thống gợi ý với 2 hướng nghiên cứu chính:
- Sử dụng embedding cho khởi tạo mô hình
- Trực tiếp huấn luyện LLM như một mô hình ứng dụng.

Mình dự phiên trình bày [Knowledge & Context](https://recsys.acm.org/recsys23/session-8/). Cả 4 bài được trình bày đều có ý tưởng thú vị (hoặc là do bản thân mình chưa tìm hiểu nhiều về Graph-based Neural Network nên thấy cái nào cũng mới lạ). Buồi chiều mình dự phiên [Reinforcement Learning](https://recsys.acm.org/recsys23/session-10/) và [Evaluation](https://recsys.acm.org/recsys23/session-12/). Phần Reinforcement Learning khiến mình buồn ngủ (một phần mình không hiểu vấn đề mà các tác giả muốn giải quyết). Trong khi đó phần Evaluation thì cực hay và lôi cuốn, cả 4 bài trình bày ở phiên này đều chứa thông tin hữu ích và thấu suốt về việc đánh giá các mô hình gợi ý.
- [Knowledge-based Multiple Adaptive Spaces Fusion for Recommendation](https://dl.acm.org/doi/10.1145/3604915.3608787)
- [KGTORe: Tailored Recommendations through Knowledge-aware GNN Models](https://dl.acm.org/doi/10.1145/3604915.3608804)
- [Pairwise Intent Graph Embedding Learning for Context-Aware Recommendation](https://dl.acm.org/doi/10.1145/3604915.3608815)
- [Heterogeneous Knowledge Fusion: A Novel Approach for Personalized Recommendation via LLM](https://dl.acm.org/doi/10.1145/3604915.3608874)
- [How Should We Measure Filter Bubbles? A Regression Model and Evidence for Online News](https://dl.acm.org/doi/10.1145/3604915.3608805)
- [Everyone’s a Winner! On Hyperparameter Tuning of Recommendation Models](https://dl.acm.org/doi/10.1145/3604915.3609488)
- [What We Evaluate When We Evaluate Recommender Systems: Understanding Recommender Systems’ Performance using Item Response Theory](https://dl.acm.org/doi/10.1145/3604915.3608809)
- [Identifying Controversial Pairs in Item-to-Item Recommendations](https://dl.acm.org/doi/10.1145/3604915.3608871)
## Ngày 5
Bài keynote đến từ Amazon đầy ấn tượng bởi sự chuyên sâu và đánh vào trọng tâm. Mình khá bất ngờ bởi tính hàm lượng kỹ thuật trong bài nói của [phó chủ tịch của amazon](https://en.wikipedia.org/wiki/Rajeev_Rastogi). Bài nói xoay quanh một số vấn đề trọng tâm nhưng gợi ý nốt trong đồ thị có hướng (Node recommendations in directed graphs), phản hồi trì hoãn (Delayed feedback), và tính bất định trong mô hình dự đoán (Uncertainty in model predictions). Có lẽ mình sẽ viết một bài riêng mà mình quan tâm trong hội nghị này. Nhiều phiên trình bày của hôm nay thú vị và cung cấp thông tin quan trọng để đánh giá một hệ thống. Một số bài hay ho bao gồm:
- [STAN: Stage-Adaptive Network for Multi-Task Recommendation by Learning User Lifecycle-Based Representation](https://dl.acm.org/doi/10.1145/3604915.3608796)
- [MCM: A Multi-task Pre-trained Customer Model for Personalization](https://dl.acm.org/doi/10.1145/3604915.3608868)
- [Understanding and Modeling Passive-Negative Feedback for Short-video Sequential Recommendation](https://dl.acm.org/doi/10.1145/3604915.3608814)
- [Personalised Recommendations for the BBC iPlayer: Initial approach and current challenges](https://dl.acm.org/doi/10.1145/3604915.3608867)
- [Reproducibility Analysis of Recommender Systems relying on Visual Features: traps, pitfalls, and countermeasures](https://dl.acm.org/doi/pdf/10.1145/3604915.3609492)
- Toàn bộ [Session 18: Women in RecSys](https://recsys.acm.org/recsys23/session-18/)