[15:29] Bansal, Akshay

awk '(NF==6)&&($1=="/dev/mapper/vgroot-tmp")&&($2=="/tmp")&&($3=="xfs")&&($4=="defaults,noatime,nodev,nosuid,noexec"){ print $1,$2,$3,"defaults,noatime,nodev,nosuid,exec",0,0; next } 1' /etc/fstab > /tmp/fstabtest
