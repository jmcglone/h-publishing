---
layout: default
---

Although [hypothes.is](http://hypothes.is) is primarily used for post-publication review and annotation with [Michigan Publishing's](http://www.publishing.umich.edu) [journals](http://www.journalofelectronicpublishing.org) and [monographs](http://dx.doi.org/10.3998/dh.12869322.0001.001), we envision a future where hypothes.is can be incorporated into many phases of the publishing workflow. For example, what if it were used by copy editors to mark edits and communicate changes to authors or production staff? Or used by peer-reviewers to annotate and make decisions on the publication status of a paper for editors of a scholarly journal? 

Accordingly this document outlines features, questions, and requirements organized around phases of a typical scholarly publishing workflow.

## Integration with AUTH and CMS

* Single sign on/Integration with university login/credentials
* GitHub integration
* WordPress integration

## Big questions in the whole editorial workflow

* How far can hypothes.is go (or how far does it want to go) in terms of cycling through versions and development of a manuscript? For example, in the editing process when the purpose of an annotation is to change the document, which then changes the annotations, and on and on.
	
* We feel this is a deeper and more complex issue than the question of fuzzy anchoring as a technical solution for annotating a portion of text that might change. To support annotation in the manuscript development/editorial process, the expectation and goal is for the entire document to evolve, perhaps radically. For the annotations to remain useful, Hypothes.is will need to entirely integrate with–or become!–some kind of version controlled authoring platform.
	
* We can think about this directionally: It seems that the function of hypothes.is to build an increasingly dense and robust web of annotation and commentary \*out\* from a core text? But in the context of authoring/editing, the relationship seems much more contained and internally focused: a layer of annotation reflected back at the text, and vice versa. What are the implications of re-purposing hypothes.is in this way? 

## Authoring

*In this context, authoring is considered writing and developing a manuscript in MS Word or a web-based CMS like WordPress, Google Docs, or a collaborative environment like GitHub. In this use case the users would be the author(s), acquiring editor, and maybe selected colleagues or contributors to an edited volume.*

*	Ability to incorporate an annotation that is a suggested change into the text (effectively, a track changes function). Suggested anchoring to previous version.
*	Closed/private group functionality
*	Easy integration of bibliographic sources into annotations. 
	* Drag/drop bibliographic sources from a citation management system such as Zotero or EndNote.
	* Autocomplete sources you've already used?
	* Quick view of all annotations referring to/citing a single source
* Use for composing endnotes/footnotes: write your notes as annotations, then have a way to convert all annotations (or selected/tagged ones) into endnotes/footnotes that are written into the document.
	
## Peer Review

### Reviewers/Editors

* Anonymity/aliasing for reviewers (so John Smith can be represented as Reviewer A, Sue Jones as Reviewer B, etc.). The ability to differentiate between reviewers, and to find all annotations by a single reviewer, is important, so we don't want annotations to be completely anonymized.
	* Optional: only certain people (with admin privs, like an editor) can toggle the alias or anonymity for users.
* Ability to display a specific user's annotations/comments (show only Reviewer A's comments, hide Reviewer B's comments)
* Ability to easily link to other annotations within an annotation (without having to manually embed a link).
	* Optional: Auto-complete self-referencing (keyboard shortcut? some textual cue like--_sub., sup., Cf., see also_, etc.--that you want to refer to an earlier annotation? Then either you select from previous annotations which one you're referring to, or start typing what you wrote in the other annotation, and hypothes.is it finds it for you)
* Reviewers cannot be able to see each other's comments
* Ability to export annotations to a report document that can be presented to an executive committee, author, or approval board.
	* The ability to self-select which annotations are exported.
* Ability to label or categorize type of comment, and filter for those
	* especially to indicate a final decision such as : "accept, reject, or accept with revisions." 

### Author

*Author gets the document back with reviewer comments and makes revision. The functions suggested here mostly reflect our broader questions and concerns about the relationship between hypothes.is and any work in progress--see the comments at the top of this document.*

* Is the revised text a brand new document? 
* Alternatively, can the author go through the editor/reviewer comments and "resolve" each? 
	* Do resolved annotations go away? Or are they preserved--in the hypothes.is stream?
* Author needs to be able to respond to annotations and perhaps export those to a document/report
* Support for layering annotations to versions of a document 
	* For example, if a document has been through multiple versions and those are somehow preserved, the ability to look at the history

## Copy editing

*Usually a single copy editor working alone and then sharing changes, questions, and suggestions with the author via annotations and comments.*

* Integrate copy editing review/mark and vocabulary standards (Chicago, MLA) and allow for shortcuts.
* All version control/track changes functionality listed above would be crucial to this phase.

## Publication

*Annotation and commenting in the traditional sense, post-publication.*

### Publisher/Editor/Manager
* e-mail notifications
* spam protection/blocking
* moderation/deletion of annotations or comments
* If a comment is flagged by another user, report to manager
* higher-level view (ability to view all annotations) for a publication
	* IE: could "watch" a specific article, but the ability to see annotations made across all articles.
* metrics on annotations/comments
	* who has annotated? how many times?
	* when are annotations made?
	* what type of content is being annotated?
	* number of annotations
	* what is most commented/annotated article?
	* would a separate dashboard/interface be required to display this data?
* pingbacks/trackbacks
	* someone refers to an article from your journal in an annotation via DOI –notify me when this happens
* editor's picks
	* ability for the editor to go through and "promote" or highlight comments and annotations that are contribute to the conversation.

### Reader/User

*The everyday reader of a journal or monograph who would be using and or interacting with hypothes.is annotations and comments.*

* permanent URI for an annotation so it could be cited or pointed to.
 	* Comment BY 'Rebecca Welzenbach' ON '2014-08-13T20:30:06'  
		* 'This is an existing feature of hypothes.is, or at least is meant to be--with "how permanent is permanent" being an open question...'
		* Comment BY 'Dan Whaley' ON '2014-08-13T20:30:06'  
			* 'As permanent and reliable as the operator of your store of annotations. (Our code is open source, you can host it yourself.)'
* Notifications (when someone replies to your annotation)
	* BY 'Dan Whaley' ON '2014-08-13T20:39:51'  
		* '\*Email\* notifications are implemented and about to be deployed.'
* Ability to "watch" \*any\* annotation and be notified of \*any\* reply
	* Comment BY 'Dan Whaley' ON '2014-08-13T21:16:13'  
		* 'We've discussed. EXPLORE'
* Orcid ID integration
	* This could help ID certain annotators/commenters and also help establish authority.
		* Comment BY 'Dan Whaley' ON '2014-08-13T20:39:21'  
			* 'This is anticipated under several ongoing implementations (arXiv, eLife, AGU) and also other proposals in process.'
* Citation mgmt integration
	* drag and drop a citation from zotero or EndNote into an annotation you are making
	* Actually CITE an annotation as a resource in zotero or endnote!
		* Comment BY 'Dan Whaley' ON '2014-08-13T20:51:06'  
			* 'EXPLORE'
* Mute thread/annotation(s)
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:50:57'  
		* 'Anticipated with any advanced notification functionality: EXPLORE.']
* Complex filter on article pages
	* location
	* sort by discipline (based on orcid id)
	* time/when comment was made
	* username
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:40:35'  
		* 'We are in the process of redesigning the current View/sort controls. Design notes here: <https://docs.google.com/a/hypothes.is/document/d/14OzyeX6-5K3uuYvoWMhABr7JOYiBXlC0RTLKyr-Wj2E/edit>'
* Flag/report comment
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:41:32'  
		* 'Anticipated as a form of spam control above. Same functionality.'
* Profile pages?
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:45:01'  
		* 'Anticipated: <https://github.com/hypothesis/vision/issues/28>'
* Direct/private messaging between users 
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:50:32'  
		* 'This has been occasionally discussed. EXPLORE.'
* notifying/alerting other users in annotation (@username, +username)
	* BY 'Dan Whaley' ON '2014-08-13T20:47:53'
		* 'Anticipated: (Issue number pending)'

### Author (Post-production)

* get notifications for annotations on your published articles (even if you are not the publisher). 
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:49:08' 
		* 'Anticipated. (Discussed above): Issue: <https://github.com/hypothesis/vision/issues/44>'
* From a dashboard: ability to watch your work published all over/anywhere on the web
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:49:42'  
		* 'This should be part of stream functionality. We anticipate this. EXPLORE.']
	* add to my dashboard/add to my list of tracking articles type button
* integration with orcid profile/google scholar
* Annotations made by the author of a work are visibly different, so that readers may quickly recognize them (e.g. if the ORCID ID of the annotator matches that of the author, the annotation shows up in green)
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:50:12'
		* 'Anticipated: Need issue number.'
  
  



