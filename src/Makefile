MCS  = mcs
MONO = mono

CCCOLOR   = "\033[33m"
EXECCOLOR = "\033[34;1m"
SRCCOLOR  = "\033[31m"
RMCOLOR   = "\033[1;31m"
BINCOLOR  = "\033[37;1m"
MAKECOLOR = "\033[32;1m"
ENDCOLOR  = "\033[0m"

QUIET_RM  = @printf '%b %b\n' $(RMCOLOR)REMOVE$(ENDCOLOR) $(BINCOLOR)$@$(ENDCOLOR) 1>&2;
QUIET_MCS = @printf '%b %b\n' $(CCCOLOR)MCS$(ENDCOLOR) $(SRCCOLOR)$@$(ENDCOLOR) 1>&2;
QUIET_EXE = @printf '%b %b\n' $(EXECCOLOR)MONO$(ENDCOLOR) $(BINCOLOR)$@$(ENDCOLOR) 1>&2;

QUIET_PROC=$(QUIET_MCS)$(MCS)
QUIET_EXEC=$(QUIET_EXE)$(MONO)
QUIET_REMOVE=$(QUIET_RM)rm -f

src  = c-sharp.cs

obj  = csharp

all:$(obj)

csharp:$(src)
	$(QUIET_PROC) $(src) -out:$(obj)

run:$(obj)
	$(QUIET_EXEC) $(obj)

.PHONY:clean
clean:
	$(QUIET_REMOVE) -f $(obj)
