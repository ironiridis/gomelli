# gomelli
gomelli is a tool aimed at managing rapid, short-term project assignment.

The title of the project is a reference to [Gemelli][], a variety of pasta. Gemelli is a single piece of pasta that appears to be two pieces twisted together.

gomelli is targetted toward small development shops who may be currently sharing files and deploying via [Dropbox][], [Google Drive][], or some other file-sharing service. They may be using these services to sync a folder of project files, or to deliver files for deployment. Often environments that force proprietary GUI-based tooling foster this kind of colaboration. Two examples: [AMX][] and [Crestron][].

The developers on these platforms don't tend to have a workflow that involves working in a shell – indeed, many of these developers aren't comfortable working in a Windows Command Prompt. Asking developers to `cd` to their project directory, `git add -A *`, `git commit -m 'fix projector power time'`, `git push` for every compile/load/test/deploy cycle is a non-starter for many of them.

gomelli aims to work differently than that. It delivers a smaller set of functions, laser-focused on the needs of these kinds of companies.

 [Gemelli]: https://en.wikipedia.org/wiki/Gemelli_(pasta)
 [Dropbox]: https://www.dropbox.com
 [Google Drive]: https://drive.google.com
 [AMX]: http://www.amx.com/trade.asp
 [Crestron]: http://www.crestron.com

## Projects and systems
*todo*

## Collaboration
In a small shop with two or more developers, a single developer will take a project for a short period of time, possibly through the initial phase of deployment. In an ideal world, this developer will take the project through testing and troubleshooting until project sign off. But this often isn't the case when resource availability and schedules change.

gomelli allows a project to be assigned to one or many resources at any point during its lifecycle. Notes, history, and files attached to the project come along. Checking files in and out ensures safe collaboration when multiple people are working in it. Files can be located in per-resource "boxes", essentially delegating responsibility to resources where required.

Resources can be assigned permissions, creating a mechanism for safely involving 3rd party developers (or other staff).

## Checking in and checking out
Checking out files changes the state of the project so the box containing those files becomes locked to that resource. Boxes are unlocked when either the resource checks in new files, or the box is unlocked manually. This creates the intuitive notion that pulling files to work on them must be balanced with storing them back on the system. A resource can choose to keep a box locked during check-in if, for example, it was an incremental change and work will continue.

## Deployment to the field
A deployment box can be created which creates a read-only way for a resource to obtain files for deployment.

## Tags and content categorization
*todo*

## Browser based
Everything is done through a web browser, permitting non-technical resources to work with your system just as simply as they would with Dropbox. Drag-and-drop to upload, click to download. gomelli is completely dynamic – utilizing websockets where possible – so a user waiting for a deployed file sees their file as it is being uploaded, no refresh required.
