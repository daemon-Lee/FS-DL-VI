# Lifecycle

* Phase 1 is Project Planning and Project Setup: At this phase, we want to decide the problem to work on, determine the requirements and goals, as well as figure out how to allocate resources properly.
* Phase 2 is Data Collection and Data Labeling: At this phase, we want to collect training data (images, text, tabular, etc.) and potentially annotate them with ground truth, depending on the specific sources where they come from.
* Phase 3 is Model Training and Model Debugging: At this phase, we want to implement baseline models quickly, find and reproduce state-of-the-art methods for the problem domain, debug our implementation, and improve the model performance for specific tasks.
* Phase 4 is Model Deployment and Model Testing: At this phase, we want to pilot the model in a constrained environment, write tests to prevent regressions, and roll the model into production.


Vòng đời của của các dự án ML như nào, tất cả các hoạt động đi vào xây dựng một mô hình hình máy học

Vòng đời của 1 dự án ml khá giống với việc phát triển 1 sản phẩm phần mềm

Đặt ra bài toán → thu thập dữ liệu liên quan → lọc dữ liệu có ích → thử nghiệm mở hình → đánh giá → devops và sản phẩm

Nhìn quy trình đơn giản nhưng việc thực hiện sẽ chia thành nhiều cycle nhỏ phải thực nghiệm nhiều lần, tuy nhiên dần chúng ta đã có các phương pháp đánh giá để việc hiệu chỉnh đi đúng hướng. Hạn chế việc lãng phí tài nguyên và chi phí maintenance.

## Per-project activities

Phase 1 is Project Planning and Project setup:

- Decide to work on pose estimation
- Determine requirements and goals
- Allocate rescoures

Phase 2 is Data Collection and Data Labeling: 

- Collect training objects
- Setup sensors (e.g., cameras)
- Capture image of objects
- Annotate with ground truth (how?)

Phase 1 + 2:

- Too hard to get data
- Easier to label a different task (e.g., hard to annotate pose, easier to annotate per-pixel segmentation)

 Phase 3 is Model Training and Model Debugging

- Implement baseline models quickly
- Find and reproduce state-of-the-art methods for problem domain
- Debug our implementation
- Improve model performance for specific tasks.

Phase 3 look back 2:

- Collect more data (overfit or model can't learning)
- Realize data labeling is unreliable

Phase 3 look back 1:

- Realize task is too hard
- Requirements trade off with each other - revisit which are most important

Phase 4 is Deploying and testing

- Pilot in grasping system in the lab
- Write test to prevent regressions
- Roll out in production

Phase 4 look back 3:

- Doesn't work in the lab - keep improving accuracy of model

Phase 4 look back 2:

- Fix data mismatch between training data and seen in deployment
- Collect more data
- Mine hard cases

Phase 4 look back 1:

- The metric you picked doesn't actually drive downstream user behavior. Revisit the metric.
- Performance in the real world isn't great - revisit requirements (e.g., do we need to be faster or more accurate?)

## Cross-project infrastructure

Team and hiring

Infra and tooling

## Others

- Understand state of the art in your domain
    - Understand what's possible
    - Know what to try next
- We will introduce most promising research areas