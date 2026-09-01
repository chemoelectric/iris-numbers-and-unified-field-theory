.DELETE_ON_ERROR:
.DEFAULT_GOAL := default

WGET := wget

IRIS_NUMBERS =
IRIS_NUMBERS += $(notdir $(IRIS_NUMBERS_ACL2))
IRIS_NUMBERS += $(notdir $(IRIS_NUMBERS_01))
IRIS_NUMBERS += $(notdir $(IRIS_NUMBERS_02))
IRIS_NUMBERS += $(notdir $(IRIS_NUMBERS_03))
IRIS_NUMBERS += $(notdir $(IRIS_NUMBERS_04))
IRIS_NUMBERS += $(notdir $(IRIS_NUMBERS_05))

IRIS_NUMBERS_ACL2 = https://archive.org/download/iris-number-system-01-volume-i-fundamentals/iris_number_system.lisp
IRIS_NUMBERS_01 = https://archive.org/download/iris-number-system-01-volume-i-fundamentals/Iris_Number_System-01-Volume_I_Fundamentals.pdf
IRIS_NUMBERS_02 = https://archive.org/download/iris-number-system-02-volume-ii-number-theory-etc/Iris_Number_System-02-Volume_II_Number_Theory_etc.pdf
IRIS_NUMBERS_03 = https://archive.org/download/iris-number-system-03-volume-iii-geometry-algebra-etc/Iris_Number_System-03-Volume_III_Geometry_Algebra_etc.pdf
IRIS_NUMBERS_04 = https://archive.org/download/iris-number-system-04-volume-iv-physics-etc/Iris_Number_System-04-Volume_IV_Physics_etc.pdf
IRIS_NUMBERS_05 = https://archive.org/download/iris-number-system-05-volume-v-spectral-analysis-etc/Iris_Number_System-05-Volume_V_Spectral_Analysis_etc.pdf

download-iris-numbers = $(WGET) -N $(1)

.PHONY: get-iris-numbers
get-iris-numbers: \
	get-iris-numbers-acl2 \
	get-iris-numbers-01 \
	get-iris-numbers-02 \
	get-iris-numbers-03 \
	get-iris-numbers-04 \
	get-iris-numbers-05

.PHONY: get-iris-numbers-acl2
get-iris-numbers-acl2:
	(cd acl2-books && \
        $(call download-iris-numbers,$(IRIS_NUMBERS_ACL2)))

.PHONY: get-iris-numbers-01
get-iris-numbers-01:
	$(call download-iris-numbers,$(IRIS_NUMBERS_01))

.PHONY: get-iris-numbers-02
get-iris-numbers-02:
	$(call download-iris-numbers,$(IRIS_NUMBERS_02))

.PHONY: get-iris-numbers-03
get-iris-numbers-03:
	$(call download-iris-numbers,$(IRIS_NUMBERS_03))

.PHONY: get-iris-numbers-04
get-iris-numbers-04:
	$(call download-iris-numbers,$(IRIS_NUMBERS_04))

.PHONY: get-iris-numbers-05
get-iris-numbers-05:
	$(call download-iris-numbers,$(IRIS_NUMBERS_05))

.PHONY: default
	echo "Currently there is no default target."

# local variables:
# coding: utf-8
# end:
