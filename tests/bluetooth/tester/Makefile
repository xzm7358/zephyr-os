# Makefile - Bluetooth tester Makefile for microkernel

#
# Copyright (c) 2015-2016 Intel Corporation
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

# DESCRIPTION
# Makefile for the Bluetooth tester application
# default for qemu_cortex_m3 as only this currently supports enought UARTs
BOARD ?= qemu_cortex_m3

MDEF_FILE = prj.mdef
KERNEL_TYPE = micro
CONF_FILE ?= prj.conf

# UART for Bluetooth
QEMU_EXTRA_FLAGS = -serial unix:/tmp/bt-server-bredr

# UART for Tester
QEMU_EXTRA_FLAGS += -serial pipe:/tmp/bt-stack-tester

PRJ_INCPATH += ${ZEPHYR_BASE}/include/drivers

include $(ZEPHYR_BASE)/Makefile.inc
