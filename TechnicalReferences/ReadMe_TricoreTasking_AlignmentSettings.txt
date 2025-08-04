Tricore / Tasking Alignment Settings
-----------------------------------------------------------------------------------------


!!!CAUTION!!!
-----------------------------------------------------------------------------------------
Please use the Tasking compiler options with care as there are many possibilities
to change the alignment of the compiler.
Always check the alignment of the Post-Build XML Generator against the alignment of the
Tasking compiler and ensure that it fits with the chosen settings. 
-----------------------------------------------------------------------------------------


If the Tricore / Tasking platform is used, the PostBuildXmlGen.exe has to be invoked
with the following additional cmd line parameters: 

Cmd line parameter                       |Description
-----------------------------------------------------------------------------------------
    --align-enum="Align16Bit"            |Change natural alignment of type enum to 16Bit.
                                         |Only required if parameter "SizeOfEnum"
                                         |in EcuC module is configured to Size32Bit.
-----------------------------------------------------------------------------------------
    --align-int="Align16Bit"             |Change natural alignment of type int.
-----------------------------------------------------------------------------------------
    --align-long="Align16Bit"            |Change natural alignment of type long.
-----------------------------------------------------------------------------------------
    --align-float="Align16Bit"           |Change natural alignment of type float.
-----------------------------------------------------------------------------------------
    --align-double="Align16Bit"          |Change natural alignment of type double.
-----------------------------------------------------------------------------------------
    --align-struct-ge16="Align16Bit"     |16Bit alignment of unions/structures
                                         |that are >= 16Bit.
-----------------------------------------------------------------------------------------
    --align-struct-ge64="Align32Bit"     |32Bit alignment of unions/structures
                                         |that are >= 64Bit.
-----------------------------------------------------------------------------------------

Additional information about the usage of the Post-Build XML Generator interface is
provided in "TechnicalReference_PostBuildXmlGenerator.pdf".