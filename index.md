---
layout: default
---

Although [hypothes.is](http://hypothes.is) is primarily used for post-publication review and annotation with [Michigan Publishing's](http://www.publishing.umich.edu) [journals](http://www.journalofelectronicpublishing.org) and [monographs](http://dx.doi.org/10.3998/dh.12869322.0001.001), we envision a future where hypothes.is can be incorporated into many phases of the publishing workflow. For example, what if it were used by copy editors to mark edits and communicate changes to authors or production staff? Or used by peer-reviewers to annotate and make decisions on the publication status of a paper for editors of a scholarly journal? 

Accordingly this document outlines features, questions, and requirements organized around phases of a typical scholarly publishing workflow.

## Integration with AUTH and CMS

* Single sign on/Integration with university login/credentials
	* Comment BY 'Jake Hartnell' ON '2014-09-23T22:54:10' 
		* 'Annotate.' 
* GitHub integration
	* Comment BY 'Dan Whaley' ON '2014-09-03T16:06:56'
		* Can you clarify what you mean by integration?'
			* Comment BY 'Rebecca Welzenbach' ON '2014-09-03T16:06:56'
				* 'We were just thinking here of possible web-based, version-controlled authoring platforms that already exist; environments where cycles of review and editing might take place. So in this case, we imagined annotations being integrated back into a text, forming a new version of that file.'
* WordPress integration
	* Comment BY 'Dan Whaley' ON '2014-09-03T16:10:34'  
		* 'Do you mean in terms of having H. work on WP period, or in terms of having edit suggestions be able to be written back to WP and update the original source?'  
		* Comment BY 'Randall Leeds' ON '2014-08-13T23:24:06'  
			* 'Or totally alternative things this could mean: annotations self-hosted in wordpress. Annotations appearing in place of wordpress comments. Wordpress comments appearing as page comments in the sidebar. Etc, etc, etc. Interested to hear.'
		* Comment BY 'Rebecca Welzenbach' ON '2014-09-03T16:10:34'  
			* 'These are all great suggestions! I like the idea of annotations being used instead of comments on wordpress; I assume that on a published wordpress page/post displayed in a web browser, this would already work anyway as part of basic h functionality. For this particular document, I believe we had in mind incorporating annotations into the process of authoring, editing, and versioning Wordpress drafts.'

## Big questions in the whole editorial workflow

* How far can hypothes.is go (or how far does it want to go) in terms of cycling through versions and development of a manuscript? For example, in the editing process when the purpose of an annotation is to change the document, which then changes the annotations, and on and on.
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:12:04'
		* 'I think a combination of fuzzy anchoring, versioning and resolution can be effective here. So, one a suggestion is made to a manuscript that is accepted, the suggestion should be "resolved", which removes it from default view (though should still be discoverable later).'
			* Comment BY 'Benjamin Young' ON '2014-08-13T20:12:04'
				* 'RFC5829 <http://tools.ietf.org/html/rfc5829> provides the ability for one URL to state that it's a version of another URL.'  
				* 'Open Annotation provides "motivation" concepts--one of which is "editing"--which could be used in combination to provide a "resolved" state: first annotation is motivated by "editing" the second annotation is motivated by "moderation" (or perhaps a new type) and likely links to the URL of the version things were "resolved" in.'
* We feel this is a deeper and more complex issue than the question of fuzzy anchoring as a technical solution for annotating a portion of text that might change. To support annotation in the manuscript development/editorial process, the expectation and goal is for the entire document to evolve, perhaps radically. For the annotations to remain useful, Hypothes.is will need to entirely integrate with–or become!–some kind of version controlled authoring platform.
	* Comment BY 'Dan Whaley' ON '2014-09-03T17:29:21'
		* 'I think the handling of versions should be done by the underlying CMS, whether that's WP, github, gdocs, or whatever. We exist as a layer above that, but can interact with it if integrated. Not all CMSs handle versioning, and so therefore, an integrated experience may differ considerably based on the CMS or document store being used. We have notions eventually to support memento style queries for time stamped versions of a document-- and being able to go back to the version of a page at the point that an an annotation is created. I think the notion of "resolving" is potentially the right way to think about things. All annotations are always preserved (in the same way that all track changes in word are). There may be a few kinds of affordances that track changes gives you that a CMS+annotation approach do not, but this combination may allow a fair amount of functionality. Experiment and iterate.'
* We can think about this directionally: It seems that the function of hypothes.is to build an increasingly dense and robust web of annotation and commentary \*out\* from a core text? But in the context of authoring/editing, the relationship seems much more contained and internally focused: a layer of annotation reflected back at the text, and vice versa. What are the implications of re-purposing hypothes.is in this way? 
	* Comment BY 'Dan Whaley' ON '2014-08-13T23:29:06'
		* 'I don't see this as a repurposing so much as a use case of a combined set of capabilities that are core to our mission.'
  		* Comment BY 'Randall Leeds' ON '2014-08-13T23:29:06'
			* 'Same. I see this as two steps. The first is to have Hypothes.is expose the annotations in a way that's very accessible to developers working at various levels. The next is to develop the integrations that produce the flows needed. For instance, if we keep "Hypothesis" separate and aside for a moment, a WordPress plugin might modify the editor to show suggested edits by querying the annotations and finding ones which are suggested edits. The actual integration then isn't "Hypothesis" so much as it is a separate thing which leverages Hypothesis.'

## Authoring

*In this context, authoring is considered writing and developing a manuscript in MS Word or a web-based CMS like WordPress, Google Docs, or a collaborative environment like GitHub. In this use case the users would be the author(s), acquiring editor, and maybe selected colleagues or contributors to an edited volume.*

*	Ability to incorporate an annotation that is a suggested change into the text (effectively, a track changes function). Suggested anchoring to previous version.
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:19:46'  
		* 'This would require CMS integration-- and is a question of whether the platform enables it.'
		* Comment BY 'Benjamin Young' ON '2014-08-13T20:19:46'  
			* 'If the annotation were stated to be an actually revision of the selected content, then we could provide a standard diff format as a representation of the annotation. CMS vendors (or extenders) would have to care / implement the in-between bits, however.'
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:18:26'
		* 'RE: anchoring to previous version : Again, a question of whether the platform supports versioning, and provides an API into that version history.'
		* Comment BY 'Benjamin Young' ON '2014-08-13T20:18:26'  
			* NOTE: 'RFC5829 <http://tools.ietf.org/html/rfc5829> would give us "knowledge" that the page is a version of another resource. We could provide UI affordances once we have that knowledge.'
*	Closed/private group functionality
	* Comment BY 'Dan Whaley' ON '2014-08-13T19:01:26'
		* 'On the roadmap: <https://github.com/hypothesis/vision/issues/52>
*	Easy integration of bibliographic sources into annotations. 
	* Drag/drop bibliographic sources from a citation management system such as Zotero or EndNote.
	* Autocomplete sources you've already used?
	* Quick view of all annotations referring to/citing a single source
		* Comment BY 'Dan Whaley' ON '2014-08-13T19:19:23'
			* 'RE: integrating bib sources: not presently contemplated: EXPLORE'
* Use for composing endnotes/footnotes: write your notes as annotations, then have a way to convert all annotations (or selected/tagged ones) into endnotes/footnotes that are written into the document.
	* Comment BY 'Dan Whaley' ON '2014-08-13T19:19:14'
		* 'Not presently contemplated: EXPLORE.' 

## Peer Review

### Reviewers/Editors

* Anonymity/aliasing for reviewers (so John Smith can be represented as Reviewer A, Sue Jones as Reviewer B, etc.). The ability to differentiate between reviewers, and to find all annotations by a single reviewer, is important, so we don't want annotations to be completely anonymized.
	* Optional: only certain people (with admin privs, like an editor) can toggle the alias or anonymity for users.
		* Comment BY 'Dan Whaley' ON '2014-08-13T19:03:58'
			* 'This functionality is presently contemplated under work we are doing under the Sloan grant with eLife and AGU.'
* Ability to display a specific user's annotations/comments (show only Reviewer A's comments, hide Reviewer B's comments)
	* Comment BY 'Dan Whaley' ON '2014-08-13T21:14:10'
		* 'Yes, under Sloan work.'
* Ability to easily link to other annotations within an annotation (without having to manually embed a link).
	* Optional: Auto-complete self-referencing (keyboard shortcut? some textual cue like--_sub., sup., Cf., see also_, etc.--that you want to refer to an earlier annotation? Then either you select from previous annotations which one you're referring to, or start typing what you wrote in the other annotation, and hypothes.is it finds it for you)
		* Comment BY 'Dan Whaley' ON '2014-08-13T19:19:01'
			* 'EXPLORE'
* Reviewers cannot be able to see each other's comments
	* Comment BY 'Dan Whaley' ON '2014-08-13T19:19:43'
		* 'Yes, under Sloan work'
* Ability to export annotations to a report document that can be presented to an executive committee, author, or approval board.
	* The ability to self-select which annotations are exported.
		* Comment BY 'Dan Whaley' ON '2014-08-13T20:15:21'
			* 'Yes, under Sloan work'
* Ability to label or categorize type of comment, and filter for those
	* especially to indicate a final decision such as : "accept, reject, or accept with revisions." 
		* Comment BY 'Dan Whaley' ON '2014-08-13T20:15:38'
			* 'Functional now.'

### Author

*Author gets the document back with reviewer comments and makes revision. The functions suggested here mostly reflect our broader questions and concerns about the relationship between hypothes.is and any work in progress--see the comments at the top of this document.*

* Is the revised text a brand new document? 
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:19:07'  
		* 'It depends first of all whether it \*is\* a new document. For instance, if a Wordpress page is simply updated, then it's not a different document. However, different documents (at distinct URLs) can be "related" to each other. This can happen a variety of ways. Most easily through the use of rel=canonical or rel=alternate microformats in the HTML. If the revised document is related to the original, then pre-existing annotations will attempt to reanchor themselves to the original. Differences in the selections of those annotations will "show differences".'
* Alternatively, can the author go through the editor/reviewer comments and "resolve" each? 
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:20:23'  
		* 'This will be one of the very first features of a set of copy-editing features. <https://github.com/hypothesis/vision/issues/50>'
	* Do resolved annotations go away? Or are they preserved--in the hypothes.is stream?
		* Comment BY 'Dan Whaley' ON '2014-08-13T20:22:16'  
			* 'We imagine that they will \*not\* go away, but instead will be hidden from display by default. They will be discoverable on the document or in the stream if "show resolved" is toggled on (conceptually). Some of this is covered in design notes on a currently ongoing redesign here: <https://docs.google.com/a/hypothes.is/document/d/14OzyeX6-5K3uuYvoWMhABr7JOYiBXlC0RTLKyr-Wj2E/edit>
* Author needs to be able to respond to annotations and perhaps export those to a document/report
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:23:10'  
		* 'Yes, export of a variety of selections of annotations is a core anticipated feature. This will covered under the Sloan work above.'
* Support for layering annotations to versions of a document 
	* For example, if a document has been through multiple versions and those are somehow preserved, the ability to look at the history
		* Comment BY 'Dan Whaley' ON '2014-08-13T20:24:49'
			* 'The question is, where is the version history of the document, and how is it accessed. This is clearly an important capability, and one we've thought of often. So much depends on how the different pieces integrate-- which depends on those pieces.'

## Copy editing

*Usually a single copy editor working alone and then sharing changes, questions, and suggestions with the author via annotations and comments.*

* Integrate copy editing review/mark and vocabulary standards (Chicago, MLA) and allow for shortcuts.
	* Comment BY 'Dan Whaley'
		* We would love to have a call about these-- perhaps a larger call w/ other partners, review these and see how they can be effectively integrated into an annotation tool like H. Is there a link to these?
			* Comment BY 'Rebecca Welzenbach'
				* agree that this will require input from a different set of experts/stakeholders. We are none of us trained copyeditors or especially familiar with these marks ourselves. However, we have a number of such people in our office (and of course other partners probably do as well). We could do some groundwork to get recommendations about which standards are most desirable, and where to find a summary/listing of them. I found this, but do not know if it is the complete/only/best list: <http://www.chicagomanualofstyle.org/tools_proof.html>
					* Comment BY 'Dan Whaley'
						* Thank you, great start! Curious to find more resources like this!
* All version control/track changes functionality listed above would be crucial to this phase.
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:27:01'  
		* NOTE: 'Yep.'

## Publication

*Annotation and commenting in the traditional sense, post-publication.*

### Publisher/Editor/Manager
* e-mail notifications
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:32:55'  
		* 'We have reply email notifications on the short track for launch, code is already merged. Here: <https://github.com/hypothesis/h/pull/1378>  In terms of overall notifications (for instance, notify me of any annotation on a page), that is anticipated. Vision issue for tracking is here: <https://github.com/hypothesis/vision/issues/44>'
* spam protection/blocking
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:33:30'
		* 'Anticipated: <https://github.com/hypothesis/h/issues/825>'		
* moderation/deletion of annotations or comments
	* BY 'Dan Whaley' ON '2014-08-13T21:16:20'
		* 'We've discussed. EXPLORE'
* If a comment is flagged by another user, report to manager
	* BY 'Dan Whaley' ON '2014-08-13T21:16:29'  
		* 'EXPLORE'
* higher-level view (ability to view all annotations) for a publication
	* IE: could "watch" a specific article, but the ability to see annotations made across all articles.
		* Comment BY 'Dan Whaley' ON '2014-08-13T20:37:32'
		* 'This is a current feature of our stream view.'
* metrics on annotations/comments
	* who has annotated? how many times?
	* when are annotations made?
	* what type of content is being annotated?
	* number of annotations
	* what is most commented/annotated article?
	* would a separate dashboard/interface be required to display this data?
  	* Comment BY 'Dan Whaley' ON '2014-08-13T20:53:34'
  		* 'Anticipated: <https://github.com/hypothesis/vision/issues/75>'
* pingbacks/trackbacks
	* someone refers to an article from your journal in an annotation via DOI –notify me when this happens
	* Comment BY 'Dan Whaley' ON '2014-08-13T20:53:51'  
		* 'Interesting: EXPLORE'
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
  
  



