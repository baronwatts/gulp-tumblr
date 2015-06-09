## Gulp-Tumblr

###Goals:
Provide accurate (i.e. congruent with Tumblr output) mocks for each template tag:

Want to help?  Grab a tag, implement a mock, and make a pull request.

####Basic Variables
* {Title} The HTML-safe title of your blog.
* {Description} The description of your blog. (may include HTML)
* {MetaDescription} The HTML-safe description of your blog.  e.g., <meta name="description" content="{MetaDescription}" />
* {BlogURL} Main URL for your blog.
* {RSS} RSS feed URL for your blog.
* {Favicon} Favicon URL for your blog.
* {CustomCSS} Any custom CSS code added on your Customize page.
* {block:PermalinkPage} {/block:PermalinkPage}  Rendered on post permalink pages. Useful for embedding comment widgets
* {block:IndexPage} {/block:IndexPage}  Rendered on index (post) pages.
* {block:PostTitle} {PostTitle} {/block:PostTitle}  Rendered on permalink pages. (Useful for displaying the current post title in the page title) Example: <title>{Title}{block:PostTitle} - {PostTitle}{/block:PostTitle}</title>
* {block:PostSummary} {PostSummary} {/block:PostSummary}  Identical to {PostTitle}, but will automatically generate a summary if a title does not exist.
* {PortraitURL-16}  Portrait photo URL for your blog. 16-pixels by 16-pixels.
* {PortraitURL-24}  Portrait photo URL for your blog. 24-pixels by 24-pixels.
* {PortraitURL-30}  Portrait photo URL for your blog. 30-pixels by 30-pixels.
* {PortraitURL-40}  Portrait photo URL for your blog. 40-pixels by 40-pixels.
* {PortraitURL-48}  Portrait photo URL for your blog. 48-pixels by 48-pixels.
* {PortraitURL-64}  Portrait photo URL for your blog. 64-pixels by 64-pixels.
* {PortraitURL-96}  Portrait photo URL for your blog. 96-pixels by 96-pixels.
* {PortraitURL-128} Portrait photo URL for your blog. 128-pixels by 128-pixels.
* {CopyrightYears}  Displays the span of years your blog has existed.

####Global Appearance
These template tags define custom colors, fonts, and other options that apply to your appearance on mobile devices and the default theme.
* {TitleFont} The font used for your blog title.
* {TitleFontWeight} The weight of your title font ("normal" or "bold").
* {BackgroundColor} The background color of your blog.
* {TitleColor}  The title color of your blog.
* {AccentColor} The accent color of your blog.
* {HeaderImage} URL of your header image in all its glory. This will always have a value, even if it is a default header image.
* {AvatarShape} The display shape of your avatar ("circle" or "square").
* {block:ShowTitle} {/block:ShowTitle}  Rendered if you have "Show title" enabled.
* {block:HideTitle} {/block:HideTitle}  Rendered if you have "Show title" disabled.
* {block:ShowDescription} {/block:ShowDescription}  Rendered if you have "Show description" enabled.
* {block:HideDescription} {/block:HideDescription}  Rendered if you have "Show description" disabled.
* {block:ShowAvatar} {/block:ShowAvatar}  Rendered if you have "Show avatar" enabled.
* {block:HideAvatar} {/block:HideAvatar}  Rendered if you have "Show avatar" disabled.
* {block:ShowHeaderImage} {/block:ShowHeaderImage}  Rendered if you have "Show header image" enabled.
* {block:HideHeaderImage} {/block:HideHeaderImage}  Rendered if you have "Show header image" disabled.

####Navigation
* {block:Pagination} {/block:Pagination} Rendered if there is a "previous" or "next" page.
* {block:PreviousPage} {/block:PreviousPage} Rendered if there is a "previous" page (newer posts) to navigate to.
* {block:NextPage} {/block:NextPage} Rendered if there is a "next" page (older posts) to navigate to.
* {PreviousPage}  URL for the "previous" page (newer posts).
* {NextPage}  URL for the "next" page (older posts).
* {CurrentPage} Current page number.
* {TotalPages}  Total page count.
* {block:SubmissionsEnabled} {/block:SubmissionsEnabled}  Rendered if Submissions are enabled.
* {SubmitLabel} The customizable label for the Submit link.
* {block:AskEnabled} {/block:AskEnabled} Rendered if asking questions is enabled.
* {AskLabel}  The customizable label for the Ask link.

####Jump Pagination
* {block:JumpPagination length="5"} {/block:JumpPagination} Rendered for each page greater than the current page minus one-half length up to current page plus one-half length.
* {block:CurrentPage} {/block:CurrentPage}  Rendered when jump page is the current page.
* {block:JumpPage} {/block:JumpPage}  Rendered when jump page is not the current page.
* {PageNumber}  Page number for jump page.
* {URL} URL for jump page.

####Pages
* {block:HasPages} {/block:HasPages}  Rendered if you have defined any custom pages.
* {block:Pages} {/block:Pages}  Rendered for each custom page.
* {URL} The URL for this page.
* {Label} The label for this page.

####Permalink Navigation
* {block:PermalinkPagination} Rendered if there is a "previous" or "next" post.
* {block:PreviousPost} {/block:PreviousPost}  Rendered if there is a "previous" post to navigate to.
* {block:NextPost} {/block:NextPost}  Rendered if there is a "next" post to navigate to.
* {PreviousPost}  URL for the "previous" (newer) post.
* {NextPost}  URL for the "next" (older) post.

####Posts
* {block:Posts} {/block:Posts}  This block gets rendered for each post in reverse chronological order. The number of posts that appear per-page can be configured in the Customize area for the blog on the Advanced tab.
* {block:Posts inlineMediaWidth="500"} {/block:Posts} Width for inline media in the post body.  Minimum: 250px
* {block:Posts inlineNestedMediaWidth="250"} {/block:Posts} Width for inline media in the reblog chain.  Minimum: 250px (must be smaller than or same as inlineMediaWidth)
* {block:Text} {/block:Text}  Rendered for Text posts.
* {block:Photo} {/block:Photo}  Rendered for Photo posts.
* {block:Panorama} {/block:Panorama}  Rendered for Panorama posts.
* {block:Photoset} {/block:Photoset}  Rendered for Photoset posts.
* {block:Quote} {/block:Quote}  Rendered for Quote posts.
* {block:Link} {/block:Link}  Rendered for Link posts.
* {block:Chat} {/block:Chat}  Rendered for Conversation posts.
* {block:Audio} {/block:Audio}  Rendered for Audio posts.
* {block:Video} {/block:Video}  Rendered for Video posts.
* {block:Answer} {/block:Answer}  Rendered for Answer posts.
* {PostType}  The name of the current post type.
* {Permalink} The permalink for a post.
* {ShortURL}  A shorter URL that redirects to this post.
* {PostID}  The numeric ID for a post.
* {TagsAsClasses} An HTML class-attribute friendly list of the posts tags.
* {block:Post[1-15]} {/block:Post[1-15]}  Rendered for the post at the specified offset. This makes it possible to insert an advertisement or design element in the middle of your posts.
* {block:Odd} {/block:Odd}  Rendered for every one of the current pages odd-numbered posts.
* {block:Even} {/block:Even}  Rendered for every one of the current pages even-numbered posts.
* {block:More} {/block:More}  Rendered on index pages for posts with Read More breaks.
* {PostNotesURL}  URL to an HTML partial of this posts Notes. Useful for loading Notes via AJAX.

####Reblogs
* {block:RebloggedFrom} {/block:RebloggedFrom}  Rendered if a post was reblogged from another post.
* {ReblogParentName}  The username of the blog this post was reblogged from.
* {ReblogParentTitle} The title of the blog this post was reblogged from.
* {ReblogParentURL} The URL for the blog this post was reblogged from.
* {ReblogParentPortraitURL-16}  Portrait photo URL for the blog this post was reblogged from. 16-pixels by 16-pixels.
* {ReblogParentPortraitURL-24}  Portrait photo URL for the blog this post was reblogged from. 24-pixels by 24-pixels.
* {ReblogParentPortraitURL-30}  Portrait photo URL for the blog this post was reblogged from. 30-pixels by 30-pixels.
* {ReblogParentPortraitURL-40}  Portrait photo URL for the blog this post was reblogged from. 40-pixels by 40-pixels.
* {ReblogParentPortraitURL-48}  Portrait photo URL for the blog this post was reblogged from. 48-pixels by 48-pixels.
* {ReblogParentPortraitURL-64}  Portrait photo URL for the blog this post was reblogged from. 64-pixels by 64-pixels.
* {ReblogParentPortraitURL-96}  Portrait photo URL for the blog this post was reblogged from. 96-pixels by 96-pixels.
* {ReblogParentPortraitURL-128} Portrait photo URL for the blog this post was reblogged from. 128-pixels by 128-pixels.
* {ReblogRootName}  The username of the blog this post was created by.
* {ReblogRootTitle} The title of the blog this post was created by.
* {ReblogRootURL} The URL for the blog this post was created by.
* {ReblogRootPortraitURL-16}  Portrait photo URL for the blog this post was created by. 16-pixels by 16-pixels.
* {ReblogRootPortraitURL-24}  Portrait photo URL for the blog this post was created by. 24-pixels by 24-pixels.
* {ReblogRootPortraitURL-30}  Portrait photo URL for the blog this post was created by. 30-pixels by 30-pixels.
* {ReblogRootPortraitURL-40}  Portrait photo URL for the blog this post was created by. 40-pixels by 40-pixels.
* {ReblogRootPortraitURL-48}  Portrait photo URL for the blog this post was created by. 48-pixels by 48-pixels.
* {ReblogRootPortraitURL-64}  Portrait photo URL for the blog this post was created by. 64-pixels by 64-pixels.
* {ReblogRootPortraitURL-96}  Portrait photo URL for the blog this post was created by. 96-pixels by 96-pixels.
* {ReblogRootPortraitURL-128} Portrait photo URL for the blog this post was created by. 128-pixels by 128-pixels.
* {block:NotReblog} {/block:NotReblog}  Rendered if a post was not reblogged from another post.

####Text Posts
* {block:Title} {/block:Title}  Rendered if there is a title for this post.
* {Title} The title of this post.
* {Body}  The content of this post.

####Photo Posts
* {PhotoAlt}  The HTML-safe version of the caption (if one exists) of this post.
* {block:Caption} {/block:Caption}  Rendered if there is a caption for this post.
* {Caption} The caption for this post.
* {block:LinkURL} Rendered if this photo has a click-through set.
* {LinkURL} A click-through URL for this photo.
* {LinkOpenTag} An HTML open anchor-tag including the click-through URL if set.
* {LinkCloseTag}  A closing anchor-tag output only if a click-through URL is set.
* {PhotoURL-500}  URL for the photo of this post. No wider than 500-pixels.
* {PhotoWidth-500}  Width for the 500px size photo.
* {PhotoHeight-500} Height for the 500px size photo.
* {PhotoURL-400}  URL for the photo of this post. No wider than 400-pixels.
* {PhotoWidth-400}  Width for the 400px size photo.
* {PhotoHeight-400} Height for the 400px size photo.
* {PhotoURL-250}  URL for the photo of this post. No wider than 250-pixels.
* {PhotoWidth-250}  Width for the 250px size photo.
* {PhotoHeight-250} Height for the 250px size photo.
* {PhotoURL-100}  URL for the photo of this post. No wider than 100-pixels.
* {PhotoWidth-100}  Width for the 100px size photo.
* {PhotoHeight-100} Height for the 100px size photo.
* {PhotoURL-75sq} URL for a square version of the photo of this post. 75-pixels by 75-pixels.
* {block:HighRes} {/block:HighRes}  Rendered if there is a high-res or panorama photo for a post.
* {PhotoURL-HighRes}  URL for the high-res or panorama sized photo of this post. No wider than 1280px or 2560px respectively.
* {PhotoURL-1280}, {PhotoWidth-1280}, and {PhotoHeight-1280} access the 1280 media directly.
* {PhotoWidth-HighRes}  Width for the high-res size photo.
* {PhotoHeight-HighRes} Height for the high-res size photo.
* {block:Exif} {/block:Exif}  Rendered if this photo has Exif data.
* {block:Camera} {Camera} {/block:Camera} Rendered if this photos Exif data contains camera info.
* {block:Aperture} {Aperture} {/block:Aperture} Rendered if this photos Exif data contains aperture info.
* {block:Exposure} {Exposure} {/block:Exposure} Rendered if this photos Exif data contains exposure info.
* {block:FocalLength} {FocalLength} {/block:FocalLength}  Rendered if this photos Exif data contains focal length.

####Panorama Posts
The template tags defined for {block:Photo} are also available to {block:Panorama}, with the following additions:
* {LinkOpenTag} An HTML open anchor-tag with Javascript to activate the Panorama lightbox.
* {LinkCloseTag}  A closing anchor-tag.
* {PhotoURL-Panorama} URL for the panorama photo of this post.  These images can be very big. (2560+ pixels wide)
* {PhotoWidth-Panorama} Width for the panorama size photo.
* {PhotoHeight-Panorama}  Height for the panorama size photo.

####Photoset Posts
* {block:Caption} {/block:Caption}  Rendered if there is a caption for this post.
* {Caption} The caption for this post.
* {Photoset}  Embed code for a responsive Photoset that shrinks to fit the container (max. 700-pixels wide).
* {Photoset-700}  Embed code for a 700-pixel wide photoset.
* {Photoset-500}  Embed code for a 500-pixel wide photoset.
* {Photoset-400}  Embed code for a 400-pixel wide photoset.
* {Photoset-250}  Embed code for a 250-pixel wide photoset.
* {PhotoCount}  The number of photos in the Photoset.
* {PhotosetLayout}  An integer representation of the Photoset layout.
* {JSPhotosetLayout}  JavaScript array of the Photoset column counts.
* {block:Photos} {/block:Photos}  Rendered for each of the Photoset photos. Each contains the same variables as {block:Photo}

####Quote Posts
* {Quote} The content of this post.
* {block:Source} {/block:Source}  Rendered if there is a source for this post.
* {Source}  The source for this post.  May contain HTML
* {Length}  "short", "medium", or "long", depending on the length of the quote.

####Link Posts
* {URL} The URL of this post.
* {Name}  The name of this post. Defaults to the URL if no name is entered.
* {Target}  Should be included inside the A-tags of Link posts.Output target="_blank" if youve enabled "Open links in new window".
* {block:Host} {/block:Host}  Rendered if there is a host for this post (if both URL and name exists).
* {Host}  The host name of the URL, sans 'www'. For example tumblr.com
* {block:Thumbnail} {/block:Thumbnail}  Rendered if there is an image thumbnail for the post.
* {Thumbnail} Link thumbnail URL.
* {Thumbnail-HighRes} Link high-res thumbnail URL.
* {block:Description} {/block:Description}  Rendered if there is a description for this post.
* {Description} The description for this post.
* {block:Author} {/block:Author}  Rendered if the post includes an author.
* {Author}  The linked authors name.
* {block:Excerpt} {/block:Excerpt}  Rendered if the post includes an excerpt.
* {Excerpt} The excerpt for this post.

####Chat Posts
* {block:Title} {/block:Title}  Rendered if there is a title for this post.
* {Title} The title of this post.
* {block:Lines} {/block:Lines}  Rendered for each line of this post.
* {block:Label} {/block:Label}  Rendered if a label was extracted for the current line of this post.
* {Label} The label (if one was extracted) for the current line of this post.
* {Name}  The username (if one was extracted) for the current line of this post.
* {Line}  The current line of this post.
* {UserNumber}  A unique identifying integer representing the user of the current line of this post.
* {Alt} "odd" or "even" for each line of this post.

####Audio Posts
* {block:Caption} {/block:Caption}  Rendered if there is a caption for this post.
* {Caption} The caption for this post.
* {block:AudioEmbed} {/block:AudioEmbed}  Rendered if an embedded audio player is available.
* {AudioEmbed}  Embed-code for the content of this post. Defaults to 500-pixels wide.
* {AudioEmbed-250}  Embed-code for the content of this post. 250-pixels wide.
* {AudioEmbed-400}  Embed-code for the content of this post. 400-pixels wide.
* {AudioEmbed-500}  Embed-code for the content of this post. 500-pixels wide.
* {AudioEmbed-640}  Embed-code for the content of this post. 640-pixels wide.
* {block:AudioPlayer} {/block:AudioPlayer}  Rendered if a native audio player is available
* {AudioPlayer} Default audio player.
* {RawAudioURL} URL for this posts audio file.  iPhone Themes only.
* {block:PlayCount} {/block:PlayCount}  Rendered if there is a play count for the audio.
* {PlayCount} The number of times this post has been played.
* {FormattedPlayCount}  The number of times this post has been played, formatted with commas.  e.g., "12,309"
* {PlayCountWithLabel}  The number of times this post has been played, formatted with commas and pluralized label e.g., "12,309 plays"
* {block:ExternalAudio} {/block:ExternalAudio}  Rendered if this post uses an externally hosted MP3.  Useful for adding a "Download" link
* {ExternalAudioURL}  The external MP3 URL, if this post uses an externally hosted MP3.
* {block:AlbumArt} {AlbumArtURL} {/block:AlbumArt} Rendered if this audio files ID3 info contains album art.
* {block:Artist} {Artist} {/block:Artist} Rendered if this audio files ID3 info contains the artist name.
* {block:Album} {Album} {/block:Album}  Rendered if this audio files ID3 info contains the album title.
* {block:TrackName} {TrackName} {/block:TrackName}  Rendered if this audio files ID3 info contains the track name.

####Video Posts
* {block:Caption} {/block:Caption}  Rendered if there is a caption for this post.
* {Caption} The caption for this post.
* {Video-700} Embed-code for the content of this post. 700-pixels wide.
* {Video-500} Embed-code for the content of this post. 500-pixels wide.
* {Video-400} Embed-code for the content of this post. 400-pixels wide.
* {Video-250} Embed-code for the content of this post. 250-pixels wide.
* {VideoEmbed-700}  Same as {Video-700}, but removes the lightbox effect from directly uploaded video. 700-pixels wide.
* {VideoEmbed-500}  Same as {Video-500}, but removes the lightbox effect from directly uploaded video. 500-pixels wide.
* {VideoEmbed-400}  Same as {Video-400}, but removes the lightbox effect from directly uploaded video. 400-pixels wide.
* {VideoEmbed-250}  Same as {Video-250}, but removes the lightbox effect from directly uploaded video. 250-pixels wide.
* {PlayCount} The number of times this post has been played.
* {FormattedPlayCount}  The number of times this post has been played, formatted with commas.  e.g., "12,309"
* {PlayCountWithLabel}  The number of times this post has been played, formatted with commas and pluralized label e.g., "12,309 plays"
* {block:VideoThumbnail} {VideoThumbnailURL} {/block:VideoThumbnail} Rendered if there is a video thumbnail available.
* {block:VideoThumbnails} {VideoThumbnailURL} {/block:VideoThumbnails}  Rendered for each video thumbnail when there are multiple.

####Answer Posts
* {Question}  The question for this post.  May contain heavily filtered HTML
* {Answer}  The answer for this post.  May contain HTML
* {Asker} Simple HTML text link with the askers username and URL, or the plain text string "Anonymous".
* {AskerPortraitURL-16} Portrait photo URL for the asker. 16-pixels by 16-pixels.
* {AskerPortraitURL-24} Portrait photo URL for the asker. 24-pixels by 24-pixels.
* {AskerPortraitURL-30} Portrait photo URL for the asker. 30-pixels by 30-pixels.
* {AskerPortraitURL-40} Portrait photo URL for the asker. 40-pixels by 40-pixels.
* {AskerPortraitURL-48} Portrait photo URL for the asker. 48-pixels by 48-pixels.
* {AskerPortraitURL-64} Portrait photo URL for the asker. 64-pixels by 64-pixels.
* {AskerPortraitURL-96} Portrait photo URL for the asker. 96-pixels by 96-pixels.
* {AskerPortraitURL-128}  Portrait photo URL for the asker. 128-pixels by 128-pixels.
* {block:Answerer}{/block:Answerer} Rendered if post contains a reblogged answer.
* {Answerer}  Simple HTML text link with the reblogged answerers username and URL.  Only exists within {block:Answerer}{/block:Answerer} and if post has been reblogged.
* {AnswererPortraitURL-16}  Portrait photo URL for the reblogged answerer. 16-pixels by 16-pixels.  Only exists within {block:Answerer}{/block:Answerer} and if post has been reblogged.
* {AnswererPortraitURL-24}  Portrait photo URL for the reblogged answerer. 24-pixels by 24-pixels.  Only exists within {block:Answerer}{/block:Answerer} and if post has been reblogged.
* {AnswererPortraitURL-30}  Portrait photo URL for the reblogged answerer. 30-pixels by 30-pixels.  Only exists within {block:Answerer}{/block:Answerer} and if post has been reblogged.
* {AnswererPortraitURL-40}  Portrait photo URL for the reblogged answerer. 40-pixels by 40-pixels.  Only exists within {block:Answerer}{/block:Answerer} and if post has been reblogged.
* {AnswererPortraitURL-48}  Portrait photo URL for the reblogged answerer. 48-pixels by 48-pixels.  Only exists within {block:Answerer}{/block:Answerer} and if post has been reblogged.
* {AnswererPortraitURL-64}  Portrait photo URL for the reblogged answerer. 64-pixels by 64-pixels.  Only exists within {block:Answerer}{/block:Answerer} and if post has been reblogged.
* {AnswererPortraitURL-96}  Portrait photo URL for the reblogged answerer. 96-pixels by 96-pixels.  Only exists within {block:Answerer}{/block:Answerer} and if post has been reblogged.
* {AnswererPortraitURL-128} Portrait photo URL for the reblogged answerer. 128-pixels by 128-pixels.  Only exists within {block:Answerer}{/block:Answerer} and if post has been reblogged.
* {Replies} Reblog chain. If not a reblog {Replies} is an alias for {Answer}

####Dates
* {block:Date} {/block:Date}  Rendered for all posts.  Always wrap dates in this block so they will be properly hidden on non-post pages.
* {block:NewDayDate} {/block:NewDayDate}  Rendered for posts that are the first to be listed for a given day.
* {block:SameDayDate} {/block:SameDayDate}  Rendered for subsequent posts listed for a given day.
* {DayOfMonth}  "1" to "31"
* {DayOfMonthWithZero}  "01" to "31"
* {DayOfWeek} "Monday" through "Sunday"
* {ShortDayOfWeek}  "Mon" through "Sun"
* {DayOfWeekNumber} "1" through "7"
* {DayOfMonthSuffix}  "st", "nd", "rd", "th"
* {DayOfYear} "1" through "365"
* {WeekOfYear}  "1" through "52"
* {Month} "January" through "December"
* {ShortMonth}  "Jan" through "Dec"
* {MonthNumber} "1" through "12"
* {MonthNumberWithZero} "01" through "12"
* {Year}  "2007"
* {ShortYear} "07"
* {AmPm}  "am" or "pm"
* {CapitalAmPm} "AM" or "PM"
* {12Hour}  "1" through "12"
* {24Hour}  "0" through "23"
* {12HourWithZero}  "01" through "12"
* {24HourWithZero}  "00" through "23"
* {Minutes} "0" through "59"
* {Seconds} "0" through "59"
* {Beats} "0" through "999"
* {Timestamp} "1172705619"
* {TimeAgo} A contextual time.  e.g., "1 minute ago", "2 hours ago", "3 weeks ago", etc.

####Notes
* {block:PostNotes} {/block:PostNotes}  Rendered on permalink pages if this post has notes.
* {PostNotes} Standard HTML output of this posts notes. Only rendered on permalink pages.
* {PostNotes-16}  Standard HTML output of this posts notes with 16x16 sized avatars. Only rendered on permalink pages.
* {PostNotes-64}  Standard HTML output of this posts notes with 64x64 sized avatars. Only rendered on permalink pages.
* {block:NoteCount} {/block:NoteCount}  Rendered if this post has notes.  Always wrap note counts in this block so they will be properly hidden on non-post pages.
* {NoteCount} The number of this posts notes.
* {NoteCountWithLabel}  The number of this posts notes with pluralized label.  e.g., "24 notes"

######Notes are paginated with AJAX. If your theme needs to manipulate the Notes markup or DOM nodes, you can add a Javascript callback that fires when a new page of Notes is loaded or inserted:
* tumblrNotesLoaded(notes_html) If this Javascript function is defined, it will be triggered when a new page of Notes is loaded and ready to be inserted. If this function returns false, it will block the Notes from being inserted.
* tumblrNotesInserted() If this Javascript function is defined, it will be triggered after a new page of Notes has been inserted into the DOM.

####Tags
* {block:HasTags} {/block:HasTags}  Rendered inside {block:Posts} if post has tags.
* {block:Tags} {/block:Tags}  Rendered for each of a posts tags.
* {Tag} The name of this tag.
* {URLSafeTag}  A URL safe version of this tag.
* {TagURL}  The tag page URL with other posts that share this tag.
* {TagURLChrono}  The tag page URL with other posts that share this tag in chronological order.

####Content Sources
* {block:ContentSource} {/block:ContentSource}  Rendered if a source is specified for a posts content.
* {SourceURL} URL of the attributed source.
* {block:SourceLogo} {/block:SourceLogo}  Rendered if a logo exists for the content source.
* {BlackLogoURL}  URL of the sources logo.
* {LogoWidth} Width of the sources logo.
* {LogoHeight}  Height of the sources logo.
* {SourceTitle} Title of the content source.
* {block:NoSourceLogo} {/block:NoSourceLogo}  Rendered if no source logo exists.

####Submissions
* {block:Submission} {/block:Submission}  Rendered if a post is a submission.
* {Submitter} The name of the submitting blog.
* {SubmitterURL}  URL to submitters blog.
* {SubmitterPortraitURL-16} Portrait photo URL for the submitter. 16-pixels by 16-pixels.
* {SubmitterPortraitURL-24} Portrait photo URL for the submitter. 24-pixels by 24-pixels.
* {SubmitterPortraitURL-30} Portrait photo URL for the submitter. 30-pixels by 30-pixels.
* {SubmitterPortraitURL-40} Portrait photo URL for the submitter. 40-pixels by 40-pixels.
* {SubmitterPortraitURL-48} Portrait photo URL for the submitter. 48-pixels by 48-pixels.
* {SubmitterPortraitURL-64} Portrait photo URL for the submitter. 64-pixels by 64-pixels.
* {SubmitterPortraitURL-96} Portrait photo URL for the submitter. 96-pixels by 96-pixels.
* {SubmitterPortraitURL-128}  Portrait photo URL for the submitter. 128-pixels by 128-pixels.

####Group Blogs & Members
* {block:GroupMembers} {/block:GroupMembers}  Rendered on additional public group blogs.
* {block:GroupMember} {/block:GroupMember}  Rendered for each additional public group blog member.
* {GroupMemberName} The username of the members blog.
* {GroupMemberTitle}  The title of the members blog.
* {GroupMemberURL}  The URL for the members blog.
* {GroupMemberPortraitURL-16} Portrait photo URL for the member. 16-pixels by 16-pixels.
* {GroupMemberPortraitURL-24} Portrait photo URL for the member. 24-pixels by 24-pixels.
* {GroupMemberPortraitURL-30} Portrait photo URL for the member. 30-pixels by 30-pixels.
* {GroupMemberPortraitURL-40} Portrait photo URL for the member. 40-pixels by 40-pixels.
* {GroupMemberPortraitURL-48} Portrait photo URL for the member. 48-pixels by 48-pixels.
* {GroupMemberPortraitURL-64} Portrait photo URL for the member. 64-pixels by 64-pixels.
* {GroupMemberPortraitURL-96} Portrait photo URL for the member. 96-pixels by 96-pixels.
* {GroupMemberPortraitURL-128}  Portrait photo URL for the member. 128-pixels by 128-pixels.

####Post Authors
* {PostAuthorName}  The username of the author of a post to an additional group blog.
* {PostAuthorTitle} The title of the authors blog for a post to an additional group blog.
* {PostAuthorURL} The blog URL for the author of a post to an additional group blog.
* {PostAuthorPortraitURL-16}  The portrait photo URL for the author of a post to an additional group blog. 16-pixels by 16-pixels.
* {PostAuthorPortraitURL-24}  The portrait photo URL for the author of a post to an additional group blog. 24-pixels by 24-pixels.
* {PostAuthorPortraitURL-30}  The portrait photo URL for the author of a post to an additional group blog. 30-pixels by 30-pixels.
* {PostAuthorPortraitURL-40}  The portrait photo URL for the author of a post to an additional group blog. 40-pixels by 40-pixels.
* {PostAuthorPortraitURL-48}  The portrait photo URL for the author of a post to an additional group blog. 48-pixels by 48-pixels.
* {PostAuthorPortraitURL-64}  The portrait photo URL for the author of a post to an additional group blog. 64-pixels by 64-pixels.
* {PostAuthorPortraitURL-96}  The portrait photo URL for the author of a post to an additional group blog. 96-pixels by 96-pixels.
* {PostAuthorPortraitURL-128} The portrait photo URL for the author of a post to an additional group blog. 128-pixels by 128-pixels.

####Day Pages
Tumblr blogs can display posts from a given day using a URL like http://david.tumblr.com/day/2007/04/29/ . By including the following markup, these pages can include pagination for the previous and next days with posts.
* {block:DayPage} {/block:DayPage}  Rendered on day pages.
* {block:DayPagination} {/block:DayPagination}  Rendered if there is a "previous" or "next" day page.
* {block:PreviousDayPage} {/block:PreviousDayPage}  Rendered if there is a "previous" day page to navigate to.
* {block:NextDayPage} {/block:NextDayPage}  Rendered if there is a "next" day page to navigate to.
* {PreviousDayPage} URL for the "previous" day page.
* {NextDayPage} URL for the "next" day page.

####Tag Pages
* {block:TagPage} {/block:TagPage}  Rendered on tag pages.
* {Tag} The name of this tag.
* {URLSafeTag}  A URL safe version of this tag.
* {TagURL}  The tag page URL with other posts that share this tag.
* {TagURLChrono}  The tag page URL with other posts that share this tag in chronological order.

####Search
* {SearchQuery} The current search query.
* {URLSafeSearchQuery}  A URL-safe version of the current search query for use in links and Javascript.
* {block:SearchPage}  Rendered on search pages.
* {SearchResultCount} The number of results returned for the current search query.
* {block:NoSearchResults} Rendered if no search results were returned for the current search query.

####Following
* {block:Following} {/block:Following}  Rendered if youre following other blogs.
* {block:Followed} {/block:Followed}  Rendered for each blog youre following.
* {FollowedName}  The username of the blog youre following.
* {FollowedTitle} The title of the blog youre following.
* {FollowedURL} The URL for the blog youre following.
* {FollowedPortraitURL-16}  Portrait photo URL for the blog youre following. 16-pixels by 16-pixels.
* {FollowedPortraitURL-24}  Portrait photo URL for the blog youre following. 24-pixels by 24-pixels.
* {FollowedPortraitURL-30}  Portrait photo URL for the blog youre following. 30-pixels by 30-pixels.
* {FollowedPortraitURL-40}  Portrait photo URL for the blog youre following. 40-pixels by 40-pixels.
* {FollowedPortraitURL-48}  Portrait photo URL for the blog youre following. 48-pixels by 48-pixels.
* {FollowedPortraitURL-64}  Portrait photo URL for the blog youre following. 64-pixels by 64-pixels.
* {FollowedPortraitURL-96}  Portrait photo URL for the blog youre following. 96-pixels by 96-pixels.
* {FollowedPortraitURL-128} Portrait photo URL for the blog youre following. 128-pixels by 128-pixels.

####Likes
* {block:Likes} {/block:Likes}  Rendered if you are sharing your likes.
* {Likes} Standard HTML output of your likes.
* {Likes limit="5"} Standard HTML output of your last 5 likes.  Maximum: 10
* {Likes width="200"} Standard HTML output of your likes with Audio and Video players scaled to 200-pixels wide.  Scale images with CSS max-width or similar.
* {Likes summarize="100"} Standard HTML output of your likes with text summarized to 100-characters.  Maximum: 250

####Like and Reblog buttons
######Like Button
* {LikeButton}  Default Like button.
* {LikeButton color="grey"} Like button color.  Grey, White, or Black. Like button will always be red if visitor has liked the post.
* {LikeButton size="20"}  Like button size.  Maximum: 100

If your theme uses infinite scrolling or some other form of AJAX pagination, you must request the like status of the new posts once the page is loaded or inserted:
* Tumblr.LikeButton.get_status_by_page(n) Call this function after requesting a new page of Posts. Takes the page number that was just loaded as an integer.
* Tumblr.LikeButton.get_status_by_post_ids([n,n,n]) Request Like status for individual posts. Takes an array of post IDs.

######Reblog Button
* {ReblogButton}  Default Reblog button.
* {ReblogButton color="grey"} Reblog button color.  Grey, White, or Black.
* {ReblogButton size="20"}  Reblog button size.  Maximum: 100


#### Theme Options
{BackgroundColor}
{TitleColor}
{AccentColor}

#### Enabling Custom Fonts
By including special meta-font tags in your theme, users can easily change those fonts using the Customize page.

You can also specify {TitleFont} as the default to inherit the value from the "Title font" global appearance parameter unless the user chooses a different font manually.

Example
<html>
    <head>
        <!-- DEFAULT FONTS -->
        <meta name="font:Title" content="Helvetica Neue"/>
        <meta name="font:Body" content="Arial, Helvetica, sans-serif"/>

        <style type="text/css">
            h1 {
                font: 30px {font:Title};
            }

            #content {
                font: 12px {font:Body};
            }
        </style>
    </head>
    ...
</html>
Enabling Booleans
By including special meta-if tags in your theme, users can easily toggle options you define. This is useful for showing or hiding different widgets or design elements.

Example
<html>
    <head>
        <!-- DEFAULTS -->
        <meta name="if:Show people I follow" content="1"/>
        <meta name="if:Reverse pagination" content="0"/>
    </head>
    <body>
        {block:IfNotReversePagination}
            <a href="...">Previous</a> <a href="...">Next</a>
        {/block:IfNotReversePagination}{block:IfReversePagination}
            <a href="...">Next</a> <a href="...">Previous</a>
        {/block:IfReversePagination}{block:IfShowPeopleIFollow}
            <div id="following">...</div>
        {/block:IfShowPeopleIFollow}
    </body>
</html>
Enabling drop-down lists
By including special meta-select tags in your theme, you can give users several options for a particular design element.

Example
<html>
    <head>
        <!-- DEFAULTS -->
        <meta name="select:Layout" content="regular" title="Regular">
        <meta name="select:Layout" content="narrow" title="Narrow">
        <meta name="select:Layout" content="grid" title="Grid">
    </head>
    <body>
        <div class="content {select:Layout}">
            ...
        </div>
    </body>
</html>
Enabling Custom Text
By including special meta-text tags in your theme, users can easily configure text variables you define. This is useful for adjusting text or configuring widgets that require information from the user.

Example
<html>
    <head>
        <!-- DEFAULT TEXT -->
        <meta name="text:Flickr Username" content=""/>
    </head>
    <body>
        {block:IfFlickrUsername}
            <div id="flickr_widget">
                <script type="text/javascript"
                src="http://flickr.com/widget?user={text:Flickr Username}">
                </script>
            </div>
        {/block:IfFlickrUsername}
    </body>
</html>
Enabling Custom Images
By including special meta-image tags in your theme, users can easily use custom images without editing your theme. Image variables (e.g., {image:Logo} ) will return a 1-pixel transparent square if no image is set.

You can also specify {HeaderImage} as the default to inherit the value from the "Header image" global appearance parameter until the user uploads a different image.

Example
<html>
    <head>
        <!-- DEFAULT IMAGE -->
        <meta name="image:Background" content="http://static.tumblr.com/..."/>
        <meta name="image:Header" content="{HeaderImage}"/>

        <style type="text/css">
            body {
                background: #2D567C url('{image:Background}');
            }
        </style>
    </head>
    <body>
        {block:IfHeaderImage}<img src="{image:Header}"/>{/block:IfHeaderImage}
        {block:IfNotHeaderImage}<h1>{Title}</h1>{/block:IfNotHeaderImage}
    </body>
</html>
Enabling Custom CSS
By including the {CustomCSS} tag at the bottom of your theme's CSS style block, users you share your theme with will be able to tweak the appearance of your theme without editing its markup.

Example
<html>
    <head>
        <style type="text/css">
            #content {
                background-color: #fff;
                color: #000;
            }

            {CustomCSS}
        </style>
    </head>
    <body>
        <div id="content">
            ...
        </div>
    </body>
</html>
Twitter
If you've enabled Twitter integration in your Tumblr preferences, you can include the /tweets.js Javascript file on your primary blog to display your recent tweets. This file runs the callback function recent_tweets(), sending the Twitter API JSON data as its only parameter.

Variable  Description
{block:Twitter} {/block:Twitter}  Rendered if you have Twitter integration enabled.
{TwitterUsername} Your Twitter username.
Example
{block:Twitter}
    <div id="twitter" style="display:none;">
        <h3><a href="http://twitter.com/{TwitterUsername}">Latest Tweets</a></h3>

        <div id="tweets"></div>
    </div>

    <script type="text/javascript">
        function recent_tweets(data) {
            for (i=0; i<data.length; i++) {
                document.getElementById("tweets").innerHTML =
                    document.getElementById("tweets").innerHTML +
                    '<a href="http://twitter.com/{TwitterUsername}/status/' +
                    (data[i].id_str ? data[i].id_str : data[i].id) +
                    '"><div class="content">' + data[i].text +
                    '</div></a>';
            }
            document.getElementById("twitter").style.display = 'block';
        }
    </script>
{/block:Twitter}

<!-- Put this at the bottom of the page -->
{block:Twitter}
    <script type="text/javascript" src="/tweets.js"></script>
{/block:Twitter}
iPhone Themes
Tumblr blogs automatically use optimized layouts when browsing on mobile devices. The iPhone layout can be overridden by adding a Custom Layout Page (via Customize) to your blog with the URL /iphone-theme.

Variable Transformations
By prefixing variables with special transformation keywords, Tumblr will output variables in specialized formats — useful when passing data to Javascript, etc. Tumblr currently supports five transformations:

Plaintext Prefix any theme variable with Plaintext to output the string with HTML-tags stripped and appropriate characters converted to HTML-entities so they’re safe to include in HTML attributes, etc.
Javascript  Prefix any theme variable with JS to output a Javascript string (wrapped in quotes).
Javascript Plaintext  Prefix any theme variable with JSPlaintext to output a Javascript string (wrapped in quotes) with HTML-tags stripped and appropriate characters converted to HTML-entities.
URLEncoded  Prefix any theme variable with URLEncoded to output a URL encoded string.
RGB Prefix a color variable with RGB to convert the hex output to RGB.
Example
<a href="{URL}" title="{PlaintextName}">{Name}</a>

<script type="text/javascript">
    var description      = {JSDescription};
    var description_text = {JSPlaintextDescription};
</script>

<a href="http://digg.com/submit?url={URLEncodedPermalink}">Digg this</a>

Todo:
Define mocks for:
Generate Regex for
