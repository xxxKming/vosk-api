CFLAGS=-I../src
LDFLAGS=-L../src -lvosk -ldl -lpthread -Wl,-rpath,../src

all: test_vosk test_vosk_speaker test_phone_results

test_vosk: test_vosk.o
	gcc $^ -o $@ $(LDFLAGS)

test_vosk_speaker: test_vosk_speaker.o
	gcc $^ -o $@ $(LDFLAGS)

test_phone_results: test_phone_results.o
	g++ $^ -o $@ $(LDFLAGS)
%.o: %.c
	gcc $(CFLAGS) -c -o $@ $<

clean:
	rm -f *.o *.a test_vosk test_vosk_speaker test_phone_results
