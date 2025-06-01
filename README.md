mountvol

D:

dir/w

cd sources

diskpart

lis dis

sel dis 0/1(depends on the number by which your partition is denoted)

lis par

conv gpt (if using Legacy, use MBR)

cre par efi size=512

form fs=fat32 quick

ass letter w

lis par

cre par pri

form quick

ass letter z

exit

dism /apply-image /imagefile:install.wim /index:4 /applydir:Z:\

bcdboot Z:\Windows /s W:

wpeutil reboot

DISCLAIMER: This will install Windows 11 Education. The Command Prompt can be triggered by pressing Shift + F10.
