all: bin/benchmarker

bin/benchmarker: *.go checker/*.go
	go build -o bin/benchmarker

exec:
	./bin/benchmarker -u ./userdata -t http://localhost/

