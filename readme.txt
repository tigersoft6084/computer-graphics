the xremesh.lib in the attached is our target. Edit the paths in /quad_remesher_1_2/QuadRemesherEngine_1.2/retopoSetting/RetopoSettings.txt so that they point to your machine directory. Then open xremesh.exe in x64dbg or IDA Pro, and execute the program with something like "C:\Users\user\Desktop\quad_remesher_1_2\QuadRemesherEngine_1.2\xremesh.exe" -s C:/Users/user/Desktop/quad_remesher_1_2/QuadRemesherEngine_1.2/retopoSetting/RetopoSettings.txt
you should see a retopo.fbx file created in your /retopoSetting folder.


The test subject is sub_180359E30, this function extracts feature curves from the input mesh, it's called from @1804BA04A. The goal is figure out if the curves populated by this function are used/accessed outside of sub_1804B9F50.

It took our engineer 20min to find where the curves are stored, no need to work out the functionality. That's what debuggers are for.
