
all: onie-syseeprom

CC := gcc

%.o : %.c
	$(CC) -g -c $(CFLAGS) $(CPPFLAGS) $< -o $@

SRCS := onie_tlvinfo.c sys_eeprom.c
INCS := onie_tlvinfo.h sys_eeprom_platform.h
OBJS := onie_tlvinfo.o sys_eeprom.o

onie-syseeprom: $(OBJS)
	$(CC) -g -o $@ $(OBJS) -lz

clean:
	rm -f $(OBJS) onie-syseeprom
