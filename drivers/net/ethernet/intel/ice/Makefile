# SPDX-License-Identifier: GPL-2.0
# Copyright (c) 2018, Intel Corporation.

#
# Makefile for the Intel(R) Ethernet Connection E800 Series Linux Driver
#

ccflags-y += -I$(src)
obj-$(CONFIG_ICE) += ice.o

ice-y := ice_main.o     \
         ice_controlq.o \
         ice_common.o   \
         ice_nvm.o      \
         ice_switch.o   \
         ice_sched.o    \
         ice_base.o     \
         ice_lib.o      \
         ice_txrx_lib.o \
         ice_txrx.o     \
         ice_fltr.o     \
         ice_irq.o      \
         ice_pf_vsi_vlan_ops.o \
         ice_vsi_vlan_ops.o \
         ice_vsi_vlan_lib.o \
         ice_gnss.o     \
         ice_tc_lib.o   \
         ice_fdir.o     \
         ice_ethtool_fdir.o     \
         ice_acl_main.o         \
         ice_acl.o              \
         ice_acl_ctrl.o         \
         ice_vlan_mode.o        \
         ice_ddp.o              \
         ice_flex_pipe.o        \
         ice_flow.o             \
         ice_lag.o              \
         ice_fwlog.o            \
         ice_ieps.o             \
         ice_ethtool.o
ice-$(CONFIG_NET_DEVLINK:m=y) += ice_devlink.o
ice-$(CONFIG_NET_DEVLINK:m=y) += ice_eswitch.o ice_repr.o
ice-y += ice_idc.o

ice-$(CONFIG_PCI_IOV) +=                \
        ice_dcf.o                       \
        ice_sriov.o                     \
        ice_vf_mbx.o                    \
        ice_vf_vsi_vlan_ops.o           \
        ice_virtchnl_allowlist.o        \
        ice_vf_adq.o                    \
        ice_virtchnl.o                  \
        ice_virtchnl_fdir.o             \
        ice_vf_lib.o

ice-$(CONFIG_RFS_ACCEL) += ice_arfs.o
ice-y += kcompat.o
# Use kcompat DIMLIB if kernel doesn't provide it
ifndef CONFIG_DIMLIB
ice-y += kcompat_dim.o kcompat_net_dim.o
endif
ice-y += auxiliary.o


