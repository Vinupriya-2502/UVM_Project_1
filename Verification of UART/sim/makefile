VLOG=/tool/mentor/questa-10.7c/questasim/bin/vlog
VSIM=/tool/mentor/questa-10.7c/questasim/bin/vsim
VCOVER=/tool/mentor/questa-10.7c/questasim/bin/vcover
VOPT=/tool/mentor/questa-10.7c/questasim/bin/vopt

TEST = test

QUESTA_SIM_PATH  = '/tool/mentor/questa-10.7c/questasim/bin'

compile:        
	$(VLOG) C:\questasim64_10.6c\uart_design_verification\rtl\uart_top.sv C:\questasim64_10.6c\uart_design_verification\ut\uvm_tb\src\tb.sv  -l compile.log

RUN: compile
	$(VSIM) tb "+UVM_TESTNAME=test" +UVM_VERBOSITY=UVM_HIGH -wlf waveform.wlf -do "log -r /*" -do "run -all" -c

RUN_WAVE: RUN
	$(VSIM) waveform.wlf
