web form for server generated UI, and for UI only.

The UI then communicates with server using Js or webAssembly to fetch(or via ajax communications) for data (including reading/writing) in the format of JSON or XML, etc. For the API development, don't use webform, but WebAPi (which shall already be ported into dotnet5)
So when porting web form, the asp.net postback(clientside event such as click is sent back to server for re-rendering) will not be ported.
