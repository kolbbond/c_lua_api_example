BIN=engine

LIBS=-llua5.4 -l:liblua5.4.a -I/usr/include/lua5.4

test: test_api.cpp Makefile
	clear
	$(CC) test_api.cpp $(LIBS) -o $(BIN)
	
clean:
	rm -f $(BIN)
