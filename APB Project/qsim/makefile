VLOG=C:\questasim64_10.6c\win64\vlog
VSIM=C:\questasim64_10.6c\win64\vsim
VCOVER=C:\questasim64_10.6c\win64\vcover
VOPT=C:\questasim64_10.6c\win64\vopt

TEST = test  
   
QUESTA_SIM_PATH =  C:\questasim64_10.6c\win64

compile:
	$(VLOG) C:\questasim64_10.6c\apb_project\ut\uvm_tb\src\testbench.sv -l compile.log
  
RUN: compile
	$(VSIM) test "+UVM_TESTNAME=apb_base_test" +UVM_VERBOSITY=UVM_HIGH -wlf waveform.wlf -do "log -r /*" -do "run -all" -c

RUN_WAVE: RUN
	$(VSIM) wave_apb.wlf
