
# Calling LabVIEW dll in MATLAB and exploring dll based on .NET

[toc]

### Introduction

I was trying to control a remote instrument ([Quantum Design DynaCool](http://www.qdusa.com/products/ppms.html)). The instrument is connected to a remote computer. Only LabVIEW controlling programs are provided. But I love MATLAB and most other instruments are controlled via MATLAB visa. The LabVIEW programs provided are based on a dll file called QDInstrument.dll.

I first tried packing LabVIEW vi to dll files and then use them in MATLAB. The final solution is directly using the QDInstrument.dll

This article will describe problems I met and solutions.

### Create dll from LabVIEW vi

LabVIEW provides this functionality. See [How Do I Create a DLL from a LabVIEW Project?](http://digital.ni.com/public.nsf/allkb/A3804F88FCDB1E6286257CE00043C1A7)

vi's are converted to functions in the dll. That's it.

### Load dll and call functions inside in MATLAB

Use `loadlibrary` in MATLAB to load dll library. But it's not that simple! I got different error message on different platform, e.g., `index out of range` on MATLAB R2014a, and something like `lack of compiler` on MATLAB R2016a, and it's the problem.

I tried installing mingw-w64, which is suggested by MATLAB. The problem is still there. I wasted some time on it and the final solution I found is installing Visual Studio, Visual Studio 2012 in my case. It must have a bunch of compilers so that MATLAB is very happy.

But, after VS2012 installed, the error message changed to `not a valid win32` program, or `not a valid win64` perhaps. I should note down those error message next time. I found that now the problem is that my LabVIEW is 32-bit but MATLAB is 64-bit. A 32-bit MATLAB setup.exe should be found in `\bin\win32\setup.exe` in the virtual drive for MATLAB version later than...hmm...2014a? So I installed a 32-bit MATLAB R2014a and no error message!

Now I can control the instrument via dll generated from vi created by me, which I know the interface. I can see functions inside the dll using `libfunctions` and call functions via `calllib` in MATLAB. It's working fine. I started packaging them into a pretty MATLAB class. Then I found that they were not working so smooth. A client is created each function call and it's completely unnecessary.

Since I could see that a client object is created within LabVIEW, and then the creating process is packaged into functions inside LabVIEW dll. I have to understand and use QDInstrument.dll to avoid this.

### .NET in MATLAB

I don'know csharp but it's similar to c/c++. To use the QDInstrument.dll provided by the seller, I have to know the interface, or better read the code.

I use a brilliant tool called [ILSpy](http://ilspy.net/) and it provides plug-in for Visual Studio. Create an empty Visual C\# project and include the dll file, then you can right click on it and `open it in ILSpy`.

MATLAB also has plenty of documents about coding with .NET library and assembly. You can use `NET.addAssembly` to add the dll file. Then TAB should work for classes and functions in the dll. Use TAB to explore the dll file. I found the function I want to use in ILSpy and try to call it in MATLAB. The function take a enumeration as one of the input argument and getting that object in MATLAB took me some time. The enumeration is defined in an abstract class hence I got errors everytime I tried to directly call the enumeration via that abstract class. Finally, other routine can be found to get that object, but it always returns the first item in the enumeration. After trying random stuff, I found that simply use TAB one more time on the enumeration, all items are provided. I really felt fooled after finding that.

Hence the point is, you might need objects defined within the dll for calling functions from the dll, and you can get those objects by exploring options MATLAB provide via TAB.

Another possible issue might be calling function with ref Keyword. See [Call .NET Methods With ref Keyword](https://cn.mathworks.com/help/matlab/matlab_external/call-net-methods-with-ref-keyword.html)

The problem I still have: When I restart MATLAB and add the assembly for the first time, MATLAB seems not knowing the whole content of that dll. I have to load multiple times and try random stuff (like class and enumerations in the dll) to make TAB work in MATLAB, i.e., showing candidate object in that dll for my partial input.

> Written with [StackEdit](https://stackedit.io/).