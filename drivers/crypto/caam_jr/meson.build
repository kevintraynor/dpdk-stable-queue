# SPDX-License-Identifier: BSD-3-Clause
# Copyright 2018 NXP

if host_machine.system() != 'linux'
        build = false
endif

deps += ['bus_vdev', 'bus_dpaa', 'security']
sources = files('caam_jr_capabilities.c',
		'caam_jr_hw.c',
		'caam_jr_uio.c',
		'caam_jr.c')

# FIXME: temporary solution for Bugzilla 469
if (toolchain == 'gcc' and cc.version().version_compare('>=10.0.0'))
	cflags += '-fcommon'
endif

allow_experimental_apis = true

includes += include_directories('../dpaa2_sec/')
includes += include_directories('../../bus/dpaa/include/')
