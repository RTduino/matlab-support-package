from building import *
import os

cwd  = GetCurrentDir()
src = []
inc = []

# arduinotarget
arduinotarget_path = os.path.join(cwd,'arduinotarget')
src += \
[
    # arduinotarget_path + '/src/MW_ArduinoHWInit.cpp',
    # arduinotarget_path + '/src/rtiostream_serial.cpp',
    # arduinotarget_path + '/scheduler/src/RTduinoScheduler.cpp',
]
inc += [arduinotarget_path + '/include', arduinotarget_path + '/scheduler/include']

# ioserver
# see template\IO_Server_flags.mk
ioserver_path = os.path.join(cwd,'ioserver')
src += \
[
    # ioserver_path + '/ioserver/src/IO_utilities.c',
    # ioserver_path + '/ioserver/src/IO_packet.c',
    # ioserver_path + '/ioserver/src/IO_server.c',
    # ioserver_path + '/ioserver/src/IO_standardperipherals.c',
    # ioserver_path + '/ioserver/src/IO_wrapperDigitalIO.c',
    # ioserver_path + '/ioserver/src/IO_wrapperI2C.c',
    # ioserver_path + '/ioserver/src/IO_wrapperPWM.c',
    # ioserver_path + '/ioserver/src/IO_wrapperSPI.c',
    # ioserver_path + '/ioserver/src/PeripheralToHandle.c',
]
inc += [ioserver_path + '/ioserver/inc']

# ioserver/custom
ioserver_custom_path = os.path.join(ioserver_path, 'custom', 'peripherals')
inc += [ioserver_custom_path + '/inc']

#src += 

# svd
svd_path = os.path.join(cwd,'svd')
inc += [svd_path + '/include']

# arduinobase
arduinobase_path = os.path.join(cwd,'ioserver')
src += \
[
    # arduinobase_path + '/src/MW_SerialRead.cpp',
    # arduinobase_path + '/src/MW_SerialWrite.cpp',
    # arduinobase_path + '/src/io_wrappers.cpp',
]
inc += [arduinobase_path + '/include']

# generated
inc += [cwd + '/generated']

group = DefineGroup('RTduino-MATLAB', src, depend = ['PKG_USING_ARDUINO_MATLAB_SUPPORT'], CPPPATH = inc)

Return('group')
