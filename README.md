# mesa-configure-make-meson-example-tutorial
mesa , configure , make , meson , example , tutorial

meson example 1

cd build && meson --configure '-Ddri-drivers=nouveau, i915, i965, r200, r100,' -Ddri-drivers-path=/usr/lib/x86_64-linux-gnu/dri '-Ddri-search-path=/usr/lib/x86_64-linux-gnu/dri:\$${ORIGIN}/dri:/usr/lib/dri' '-Dvulkan-drivers=intel, amd,' -Dglvnd=true -Dshared-glapi=true -Dgallium-xvmc=false -Dgallium-omx=disabled -Db_ndebug=true -Dbuild-tests=true -Dglx-direct=true -Dgbm=true -Ddri3=true '-Dplatforms=x11,surfaceless ,wayland ,drm' -Dgallium-xa=true -Dllvm=true -Dgallium-opencl=icd -Dgallium-nine=true -Dgallium-extra-hud=true -Dgallium-vdpau=true -Dlmsensors=true -Dgallium-va=true '-Dgallium-drivers=nouveau, virgl, svga,zink, iris, r600, r300, radeonsi, swrast,' -Dgles1=false -Dgles2=true -Dosmesa=gallium -Dvulkan-overlay-layer=true -Dprefix=/usr -Dlibdir=lib/x86_64-linux-gnu -Dlocalstatedir=/var -Dsysconfdir=/etc -Dbuildtype=plain -Dwrap_mode=nodownload


 meson example 2 + libXvMCr600.so , libXvMCnouveau.so <- dependency libdrm2 gallium-xvmc=true , gles1=true
 
 mkdir build && cd build && meson --configure '-Ddri-drivers=nouveau, i915, i965, r200, r100,' -Ddri-drivers-path=/usr/lib/x86_64-linux-gnu/dri '-Ddri-search-path=/usr/lib/x86_64-linux-gnu/dri:\$${ORIGIN}/dri:/usr/lib/dri' '-Dvulkan-drivers=intel, amd,' -Dglvnd=true -Dshared-glapi=true -Dgallium-xvmc=true -Db_ndebug=true -Degl=true -Dshader-cache=auto -Dvalgrind=true -Dbuild-tests=true -Dglx-direct=true -Dgbm=true -Ddri3=true '-Dplatforms=x11,surfaceless ,wayland ,drm' -Dgallium-xa=true -Dllvm=true -Dgallium-opencl=icd -Dgallium-nine=true -Dgallium-extra-hud=true -Dgallium-vdpau=true -Dlmsensors=true -Dgallium-va=true '-Dgallium-drivers=nouveau, virgl, svga,zink, iris, r600, r300, radeonsi, swrast,' -Dgles1=true -Dgles2=true -Dosmesa=gallium -Dvulkan-overlay-layer=true -Dprefix=/usr -Dlibdir=lib/x86_64-linux-gnu -Dlocalstatedir=/var -Dsysconfdir=/etc -Dbuildtype=plain -Dwrap_mode=nodownload
 
 -------------------------------------------------------------------------------------------------------------------------------
 
 make example mesa version 11.2.0
 
 ./configure --prefix=/usr --libdir=/usr/lib/x86_64-linux-gnu --includedir=/usr/include --enable-osmesa --enable-ilo --with-dri-driverdir=/usr/lib/x86_64-linux-gnu/dri --with-gallium-drivers=r300,r600,radeonsi,svga,swrast,ilo --enable-autotools --with-gallium-drivers=r300,r600,ilo,svga,swrast --enable-gallium-llvm
 
 
 Данные варианты я оставляю для тех кто хочет собрать лучший видео драйвер если он модифицирован и имеет лучшее ускорение как это было ранее в моей убунту 16.04 и где рабочим сто процентов был директикс во всех программах.


