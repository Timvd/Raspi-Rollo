DESCRIPTION = "RCSwitch on Raspberry Pi"
LICENSE = "GPL"
VERSION = 1.0

CXXFLAGS += -lwiringPi

all: send sendv2

send: RCSwitch.o send.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $+ -o $@ -lwiringPi
sendv2: RCSwitch.o sendv2.o
	$(CXX) $+ -o $@ $(CXXFLAGS) $(LDFLAGS)
clean:
	$(RM) *.o send
