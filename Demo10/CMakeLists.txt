cmake_minimum_required(VERSION 3.0)
project(Demo10)

message("start")
option(x86_64_enable "Enable x86_64" ON)
if(x86_64_enable)
    message("x86_64 enable!!!")
elseif()
    message("aarch64 enable!!!")
endif()
message("end")

# 实际使用时可以作为开关使用
#[[
option(<variable> "<help_text>" [value])
variable 是变量名
help_text 是描述信息
value 是变量初始值，只能是 ON 或 OFF
]]