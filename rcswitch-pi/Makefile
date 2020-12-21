all: send sendv2

send: RCSwitch.o send.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $+ -o $@ -lwiringPi -lrt -lcrypt -pthread  -lpthread
sendv2: RCSwitch.o sendv2.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $+ -o $@ -lwiringPi -lrt -lcrypt -pthread  -lpthread
clean:
	$(RM) *.o send