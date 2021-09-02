# nfs-dataset
setup MIND/fastswap/GAM servers on Cloudlab.

# usage
## *The following commands will copy VM images and traces so it will take some time (up to a few hours)*

for CN:
```
cd /local/repository/ && echo Y | ./init_env.sh && ./localize_data.sh CN $CN_first $CN_last && ./setup_CN.sh $sys $CN_first $CN_last
```
For example create CN 5 for mind, use:
```
cd /local/repository/ && echo Y | ./init_env.sh && ./localize_data.sh CN 5 5 && ./setup_CN.sh mind 5 5
```

For MN:
```
cd /local/repository/ && echo Y | ./init_env.sh && ./localize_data.sh MN && ./setup_MN.sh $sys
```
For example create MN for gam, use:
```
cd /local/repository/ && echo Y | ./init_env.sh && ./localize_data.sh MN && ./setup_MN.sh gam
```

I change the memory for mind MN to be 40GB because the old memory is too large to be allocated on current hardware.
Only mind VM has static IP now.
