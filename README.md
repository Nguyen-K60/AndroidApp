==================
Build caffe trên Ubuntu theo hướng dẫn: 
https://github.com/BVLC/caffe/wiki/Ubuntu-16.04-or-15.10-Installation-Guide

==================
caffe-android-demo
==================

Sử dụng mô hình được training theo Caffe, Alexnet
Copy file mô hình và các file cấu hình mô hình vào điện thoại theo đường dẫn:
/sdcard/caffe_mobile/bvlc_reference_caffenet/plantvillage.caffemodel
/sdcard/caffe_mobile/bvlc_reference_caffenet/solver.prototxt
/sdcard/caffe_mobile/bvlc_reference_caffenet/deploy.prototxt

+) file assets/synset_words.txt chứa tên các bệnh
+) thư mục jniLibs chứa thư viện libcaffe.so và libcaffe_jni.so được build từ https://github.com/sh1r0/caffe-android-lib chứa các hàm, phương thức đọc và sử dụng file mô hình caffemodel.
+) NOTE: khi chạy ứng dụng, cần cấp quyền truy cập Bộ nhớ và Máy ảnh cho ứng dụng.


*) Gửi dữ liệu từ Android lên Thingsboard Server.
        Note: Muon MQTT chay duoc phai cap phep o file AndroidManifest.xml
        Thêm trước dòng </application>
        <service android:name="org.eclipse.paho.android.service.MqttService" />
    Hàm sử dụng: publishMessage()
*) Sau khi có kết quả phát hiện, kết quả ở hàm onTaskCompleted(), nếu lá bị bệnh sẽ gửi ảnh lên firebase uploadImage() và gửi bản tin lên Thingsboard Server.


