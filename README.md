# UsingProtobuffWitchUnity3d
require Visual Studia 2010 or 2012

1. First Create your .proto file (using protobuf v2) 
2. Download https://storage.googleapis.com/google-code-archive-downloads/v2/code.google.com/protobuf-net/protobuf-net%20r668.zip 
    unzip Archwive
    
3. Compile Your .proto using dwonlad archiwe bash command:
   C:\protobuf-net\ProtoGen\protogen.exe -i: Person.proto -o:Person.cs
   
4. Create New Projekt in VS like Class Liblary import file your *.cs file generate from your .proto file. Impport refence C:\protobuf-net\Full\unity\protobuff-net.dll
5 Change version .net to 2.0 version and compile project

6. Now Create Serializer. Create New Project like Console Aplication using .net 2.0 import Your.dll and protobuff.dll and paste code
 using System;
using ProtoBuf.Meta;
using packet.protobuff;

namespace YourNameSpace
{
    class Program
    {
        static void Main(string[] args)
        {
            var model = TypeModel.Create();
            model.Add(typeof(YourMainClass in .proto), true);
            model.Add(typeof(YourMainClass in .proto), true);

            model.AllowParseableTypes = true;
            model.AutoAddMissingTypes = true;

            model.Compile("YourNameSpace", "NameYourDll.dll");
        }
    }
}
Compile

7. You have 3 .dll protobuff-net yourClass.dll and yourSerializer.dll copy to unity your project Assets/plugins
8. Enjoi
    
