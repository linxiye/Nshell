#===============================================================================
# @brief    Scons make file
# Copyright (c) 2018 HiSilicon Technologies Co., Ltd.
#===============================================================================

Import('env')
import os
from EnvironmentUtils import SocTargetConfig, BuildType
from ModuleUtils import Module

module = 'shell'

public_include_dirs = [os.path.join(Dir('inc/.').srcnode().abspath)]
source_files = []
source_files.extend( Glob(os.path.join('src/*.c')) )

env.Append(CPPPATH = public_include_dirs)
lib = env.Library(target = module, source = Flatten(source_files))

Return ('lib')