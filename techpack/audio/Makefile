# auto-detect subdirs
ifeq ($(CONFIG_ARCH_SDM845), y)
include $(srctree)/techpack/audio/config/sdm845auto.conf
export $(shell sed 's/=.*//' $(srctree)/techpack/audio/config/sdm845auto.conf)
endif
ifeq ($(CONFIG_ARCH_SDM660), y)
include $(srctree)/techpack/audio/config/sdm660auto_static.conf
export $(shell sed 's/=.*//' $(srctree)/techpack/audio/config/sdm660auto_static.conf)
endif
ifeq ($(CONFIG_ARCH_SDM670), y)
include $(srctree)/techpack/audio/config/sdm670auto_static.conf
export $(shell sed 's/=.*//' $(srctree)/techpack/audio/config/sdm670auto_static.conf)
endif
ifeq ($(CONFIG_ARCH_SDXPOORWILLS), y)
include $(srctree)/techpack/audio/config/sdxpoorwillsauto.conf
export $(shell sed 's/=.*//' $(srctree)/techpack/audio/config/sdxpoorwillsauto.conf)
endif
ifeq ($(CONFIG_ARCH_SM6150), y)
include $(srctree)/techpack/audio/config/sm6150auto.conf
export $(shell sed 's/=.*//' $(srctree)/techpack/audio/config/sm6150auto.conf)
endif
ifeq ($(CONFIG_ARCH_SDMMAGPIE), y)
include $(srctree)/techpack/audio/config/sm6150auto.conf
export $(shell sed 's/=.*//' $(srctree)/techpack/audio/config/sm6150auto.conf)
endif
ifeq ($(CONFIG_ARCH_SM8150), y)
include $(srctree)/techpack/audio/config/sm8150auto.conf
export $(shell sed 's/=.*//' $(srctree)/techpack/audio/config/sm8150auto.conf)
endif
ifeq ($(CONFIG_ARCH_SDMSHRIKE), y)
include $(srctree)/techpack/audio/config/sm8150auto.conf
export $(shell sed 's/=.*//' $(srctree)/techpack/audio/config/sm8150auto.conf)
endif

ifeq ($(CONFIG_ARCH_ATOLL), y)
# Use USERINCLUDE when you must reference the UAPI directories only.
USERINCLUDE     += \
                -I$(srctree)/techpack/audio/4.0/include/uapi \

# Use LINUXINCLUDE when you must reference the include/ directory.
# Needed to be compatible with the O= option
LINUXINCLUDE    += \
                -I$(srctree)/techpack/audio/4.0/include/uapi \
                -I$(srctree)/techpack/audio/4.0/include
else
# Use USERINCLUDE when you must reference the UAPI directories only.
USERINCLUDE     += \
                -I$(srctree)/techpack/audio/include/uapi \

# Use LINUXINCLUDE when you must reference the include/ directory.
# Needed to be compatible with the O= option
LINUXINCLUDE    += \
                -I$(srctree)/techpack/audio/include/uapi \
                -I$(srctree)/techpack/audio/include
endif

ifeq ($(CONFIG_ARCH_SDM845), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sdm845autoconf.h
endif
ifeq ($(CONFIG_ARCH_SDM660), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sdm660autoconf.h
endif
ifeq ($(CONFIG_ARCH_SDM670), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sdm670autoconf.h
endif
ifeq ($(CONFIG_ARCH_SDXPOORWILLS), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sdxpoorwillsautoconf.h
endif
ifeq ($(CONFIG_ARCH_SM6150), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm6150autoconf.h
endif
ifeq ($(CONFIG_ARCH_SDMMAGPIE), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm6150autoconf.h
endif
ifeq ($(CONFIG_ARCH_SM8150), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm8150autoconf.h
endif
ifeq ($(CONFIG_ARCH_SDMSHRIKE), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm8150autoconf.h
endif
ifeq ($(CONFIG_ARCH_ATOLL), y)
ifeq ($(PROJECT_NAME),$(filter $(PROJECT_NAME),a52q))
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/4.0/config/sm7125_a52.h
else ifeq ($(PROJECT_NAME),$(filter $(PROJECT_NAME),m42q))
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/4.0/config/sm7125_m42.h
else ifeq ($(PROJECT_NAME),$(filter $(PROJECT_NAME),a72q))
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/4.0/config/sm7125_a72.h
else
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/4.0/config/atollautoconf.h
endif
endif
ifeq ($(CONFIG_ARCH_SM6150), y)
ifeq ($(filter y,$(CONFIG_SEC_A70Q_PROJECT)),y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm6150_a70q.h
else ifeq ($(filter y,$(CONFIG_SEC_A70S_PROJECT)),y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm6150_a70s.h
else ifeq ($(filter y,$(CONFIG_SEC_A71_PROJECT)),y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm7150_a71.h
else ifeq ($(PROJECT_NAME),$(filter $(PROJECT_NAME),a90q r1q))
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm7150_a90q.h
else ifeq ($(filter y,$(CONFIG_SEC_A70SQ_PROJECT)),y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm7150_a70sq.h
else ifeq ($(filter y,$(CONFIG_SEC_M41_PROJECT)),y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm7150_m41.h
else ifeq ($(filter y,$(CONFIG_SEC_M51_PROJECT)),y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm7150_m51.h
else ifeq ($(filter y,$(CONFIG_SEC_A60Q_PROJECT)),y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm6150_a60q.h
else ifeq ($(filter y,$(CONFIG_SEC_M40_PROJECT)),y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm6150_m40.h
else
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/sm6150autoconf.h
endif
endif

ifeq ($(CONFIG_ARCH_ATOLL), y)
obj-y += 4.0/soc/
obj-y += 4.0/dsp/
obj-y += 4.0/ipc/
obj-y += 4.0/asoc/
else
obj-y += soc/
obj-y += dsp/
obj-y += ipc/
obj-y += asoc/
endif
