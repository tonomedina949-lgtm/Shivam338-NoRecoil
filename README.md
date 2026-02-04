A_DPIAdjusted := 5
A_DPIOriginal := 0
<^<+Numpad1::{
if A_DPIOriginal := 0{
; This line should retrieve the original mouse speed for later use
DllCall("SystemParametersInfo", "UInt", "SPI_GETMOUSESPEED", "UInt", 0, "UIntP", A_DPIOriginal, "UInt", 0)
}
; This line is supposed to adjust the current mouse speed
DllCall("SystemParametersInfo", "UInt", "SPI_SETMOUSESPEED", "UInt", 0, "UInt", A_DPIAdjusted, "UInt", 0)
}# Shivam338-NoRecoil