1.base image có gradle +jdk21 ,đặt tên AS build
2.copy buld.gradle, settings.gradle, src/ vào /app va chạy bootJar -x test
3.base image jre21
4.chỉ copy app.jar (từ stage --build ) qua user thường
5.Arg APP_VERSION truyền vào lúc build image gán vao ENV APP_VERSION,expose port 8080,entryoint dạng exec
6.app truyền từ app gốc của repo .truyền build-arg APP_VERSION
7.tên image <APP_NAME>:<APP_TAG> mặc định là devops-final-app:latest
8.db_name, db_user, db_password lấy  mýqp trong student.env
9.nginx public cổng cá nhan APP_PORT ra cỏng 80
10.muốn read-only : nginx/default.conf -> etc/nginx/conf.d/default.conf

