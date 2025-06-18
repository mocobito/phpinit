Chạy lệnh sau để tạo service:
	sudo nano /etc/systemd/system/ae.service
Kích hoạt dịch vụ
	sudo systemctl daemon-reload
	sudo systemctl enable ae.service
	sudo systemctl start ae.service
Kiểm tra trạng thái
	sudo systemctl status ae.service || ps aux | grep java 
Xem log trực tiếp
	tail -f /var/log/ae.log
Hoặc nếu bạn muốn xem lỗi (nếu có):
	tail -f /var/log/ae-error.log
Xem nhật ký systemd:
	journalctl -u ae.service -f

Dừng và khởi động lại
	sudo systemctl stop ae.service
	sudo systemctl restart ae.service
	
	
Ctrl + O -> lưu file
Ctrl + X -> Thoát
