
PORT = 8001
SERVER_FILES = server.c user_online.c  
CLIENT_FILES = client.c client_fsm.c fsm.c client_view.c
#CFLAGS = -Wall
#CFLAGS = -UDEBUG
CFLAGS = -DDEBUG

SERVER = Server
CLIENT = Client

all:
	gcc $(CFLAGS) $(SERVER_FILES) -o $(SERVER)
	gcc $(CFLAGS) $(CLIENT_FILES) -o $(CLIENT) 
	#gcc -c $(CLIENT_FILES) 
	gcc $(CFLAGS) client_fsm.c -E -o test.i
	gcc $(CFLAGS) client.c -E -o test.i
#	gcc $(CFLAGS) user_online.c -E -o test.i
#	gcc $(CFLAGS) user_online.c -o test
#	gcc $(CFLAGS) client_fsm.c -o test

clean:
	rm $(SERVER) $(CLIENT)

s:
	./$(SERVER) $(PORT)

c:
	./$(CLIENT) 192.168.211.2 $(PORT)

