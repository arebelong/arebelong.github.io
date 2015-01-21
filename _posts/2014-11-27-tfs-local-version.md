How to find what the latest change set you are working on locally. 

First install Microsoft Visual Studio Team Foundation Server 2013 Power Tools
https://visualstudiogallery.msdn.microsoft.com/f017b10c-02b4-4d6d-9845-58a06545627

open a command prompt

set path=%path%;"C:\Program Files (x86)\Microsoft Visual Studio 12.0\Common7\IDE";

Change to the folder containing the project eg. Marketing or Shared

tf history . /r /noprompt /stopafter:1 /version:W

I found the information on this blog
http://blogs.msdn.com/b/buckh/archive/2009/01/26/how-to-determine-the-latest-changeset-in-your-workspace.aspx
