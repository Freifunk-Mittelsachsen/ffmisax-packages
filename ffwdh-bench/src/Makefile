all: ffwdh-bench-server ffwdh-bench-client

CFLAGS += -Wall

ffwdh-bench-server:
		$(CC) $(CPPFLAGS) $(CFLAGS) $(LDFLAGS) -o $@ ffwdh-bench-server.c $(LDLIBS)

ffwdh-bench-client:
		$(CC) $(CPPFLAGS) $(CFLAGS) $(LDFLAGS) -o $@ ffwdh-bench-client.c $(LDLIBS)
