BOARD ?= nrf52840dk

include ../Makefile.sys_common

USEMODULE += ztimer
USEMODULE += ztimer_usec

USEMODULE += psa_crypto

USEMODULE += psa_hash
USEMODULE += psa_hash_sha_256
USEMODULE += psa_secure_element
USEMODULE += psa_secure_element_ateccx08a
USEMODULE += psa_secure_element_ateccx08a_cipher_aes_128
USEMODULE += psa_secure_element_ateccx08a_hmac_sha256
USEMODULE += psa_secure_element_ateccx08a_ecc_p256

CFLAGS += -DCONFIG_PSA_PROTECTED_KEY_COUNT=4
CFLAGS += -DCONFIG_PSA_SINGLE_KEY_COUNT=1

CFLAGS += -DSECURE_ELEMENT
CFLAGS += -DCUSTOM_ATCA_PARAMS

INCLUDES += -I$(APPDIR) # Application specific (not needed by PSA)

include $(RIOTBASE)/Makefile.include
