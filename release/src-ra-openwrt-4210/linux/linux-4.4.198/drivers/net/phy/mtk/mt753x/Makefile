#
# Makefile for MediaTek MT753x gigabit switch
#

obj-$(CONFIG_MT753X_GSW)	+= mt753x.o

mt753x-$(CONFIG_SWCONFIG)	+= mt753x_swconfig.o

mt753x-y			+= mt753x_mdio.o mt7530.o mt7531.o \
					mt753x_common.o mt753x_nl.o mt753x_phy.o \
					mt753x_extphy.o

ifeq ($(CONFIG_ASUS_EXT),y)
EXTRA_CFLAGS += -DASUS_EXT
ifeq ($(CONFIG_MODEL_RTAX54),y)
EXTRA_CFLAGS += -DCONFIG_MODEL_RTAX54
else ifeq ($(CONFIG_MODEL_RTAC85P),y)
EXTRA_CFLAGS += -DCONFIG_MODEL_RTAC85P
else ifeq ($(CONFIG_MODEL_RTMIR3P),y)
EXTRA_CFLAGS += -DCONFIG_MODEL_RTMIR3P
else ifeq ($(CONFIG_MODEL_R6800),y)
EXTRA_CFLAGS += -DCONFIG_MODEL_R6800
endif
endif
