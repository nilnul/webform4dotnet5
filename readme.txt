web form for server generated UI, and for UI only. Web form mimics the front-end separation of UI(html) and Behavior(Js) by keeping the html tags in asp.net syntax as much as possible, not reinventing the wheels.

The UI then communicates with server using Js or webAssembly to fetch(or via ajax communications) for data (including reading/writing) in the format of JSON or XML, etc. For the API development, don't use webform, but WebAPi (which shall already be ported into dotnet5)
So when porting web form, the asp.net postback(clientside event such as click is sent back to server for re-rendering) will not be ported.


So the philosophy for porting webForm is:
1) webform is good in rendering UI. It's stable, endured/evolved time; the root stikes deep, with many thin tips tightly/softly clung to the occasion where it is useful.
2) it's not good in WebApi.
3) don't let #2 to deny the good in #1.
4) we port #1, not #2.

For example, when we write a long article (such as a treatise/report/solution), we mainly need UI and rarely need WebApi. It's perfect use case for webForm, and no need to introduce the complexity of, say, MVC/Razor, etc.
