# vulkan-virtio-venus-termux
It basically compiles everything automatically for you.

# How to use
0. Start Termux-X11:
   - run -> `termux-x11`
1. Start VirGL:
   - run -> `LD_PRELOAD=/system/lib(64)/libvulkan.so virgl_test_server --no-virgl --venus`
2. Enjoy!
   - run -> `VN_DEBUG=vtest appname`
  
> If on Adreno append (or set) `ADRENO_GPU=1` before `LD_PRELOAD` before starting VirGL

# Credits
- [`@xMem`](https://github.com/xMeM)
- [AOSP](https://source.android.com/)
- [`@ThatMG393`](https://github.com/ThatMG393) _(me)_

## Patches:
### - Mesa -
- WSI:
  - [wsi1.patch](https://github.com/xMeM/termux-packages/blob/23cf5ca365a1c3feb9960ae6490165dabcc9112b/packages/mesa-vulkan-icd-freedreno-dri3/wsi-no-pthread_cancel.patch)
  - [wsi2.patch](https://github.com/xMeM/termux-packages/blob/23cf5ca365a1c3feb9960ae6490165dabcc9112b/packages/mesa-vulkan-icd-freedreno-dri3/wsi-termux-x11.patch)
- VirGL Socket: [virgl-socket.patch](https://github.com/xMeM/termux-packages/blob/23cf5ca365a1c3feb9960ae6490165dabcc9112b/packages/mesa-vulkan-icd-freedreno-dri3/virgl-socket-path.patch)
### - VirGL -
- VirGL Socket: [virgl-socket.patch](https://github.com/xMeM/termux-packages/blob/37100273db2f57f2c63eac8571c3bba3d8dff855/x11-packages/virglrenderer/vtest-vtest_protocol.h.patch)
- Venus: [venus.patch](https://github.com/xMeM/termux-packages/blob/37100273db2f57f2c63eac8571c3bba3d8dff855/x11-packages/virglrenderer/virglrenderer-venus-android.patch)




