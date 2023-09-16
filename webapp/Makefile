reset:
	docker compose down
	docker volume rm webapp_mysql
	sudo rm -r logs/mysql/mysql-slow.log
	sudo rm -r logs/nginx
up:
	docker compose up
