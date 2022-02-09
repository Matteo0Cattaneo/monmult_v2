<<<<<<< HEAD
# Monmult module
=======

##Disclaimer
this is my copy for the monmult project
link to the original repository https://github.com/putoale/monmult_v2
>>>>>>> 81b66ee30d138eacd842d146f0a692a07573013d

## **Description:**

<<<<<<< HEAD
=======
# Monmult module

## **Description:**

>>>>>>> 81b66ee30d138eacd842d146f0a692a07573013d
VHDL implementation of Coarsely Integrated Operand Scanning (CIOS) algorithm for Montgomery multiplication. 

## **Vivado Version:**
The vhdl project has been created and edited with `Vivado 2021.1`.

## **Top Modules:**
There are two implementations of the block:
* `monmult_module.vhd`
* `monmult_module_v2.vhd`

The first one has been completely tested with test vectors having different number of bits, fed into the block with different number bits per word and different number of words per operand. All the used test vectors passed, as it's possible to notice from the csv files inside the folder:

    ./Sources/Python/tb_vec_gen/txt/

The second one also includes word converters. They make possible to use different length for input data to the block and data fed into computational units. However it hasn't been correctly tested yet, so we will refer to the monmult_module.vhd in our presentation.


## **Hierarchy overview:**

* monmult_module.vhd
    * cios_top_1w.vhd
        * FSM_add.vhd
            * simple_1w_adder.vhd
        * FSM_mac_ab.vhd
            * simple_1w_mac.vhd
            * sr.vhd
        * FSM_mac_mn.vhd
            * simple_1w_mac.vhd
        * FSM_mult.vhd
            * simple_1w_mult.vhd
        * FSM_sub_v2.vhd
            * simple_1w_sub.vhd
    * input_mem_abn.vhd
    * start_regulator.vhd

The following modules are instead used (only) in the monmult_module_v2.vhd:

* input_memory_v2.vhd
* in_mem_controller.vhd
* out_memory_controller.vhd

## **Python:**
In order to generate test vectors, write them into file, and compare the result generated by the monmult block, we created some python scripts:

### **tb_vec_gen.py**:
Python module collecting all the functions used inside the scripts.

### **tv_gen_script.py**:
This script is used to generate casual test vectors, and to export them to file, together with the test vectors taken from reference paper.

### **tv_res_comp_script.py:**
<<<<<<< HEAD
This script compares the result of the monmult module with the golden result for all the used test vectors.
=======
This script compares the result of the monmult module with the golden result for all the used test vectors.
>>>>>>> 81b66ee30d138eacd842d146f0a692a07573013d
