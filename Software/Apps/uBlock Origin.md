# uBlock Origin

Information about [uBlock Origin](https://ublockorigin.com/), the free Ad Blocker for various browsers.

---

## Filters

### YouTube

```git
# Youtube:  
# ========  
  
# from [https://www.reddit.com/r/uBlockOrigin/comments/sgamhs/trying_to_block_youtube_shorts/](https://www.reddit.com/r/uBlockOrigin/comments/sgamhs/trying_to_block_youtube_shorts/)  
  
## Block shorts in grid view:  
[www.youtube.com##span.style-scope.ytd-thumbnail-overlay-time-status-renderer[aria-label=Shorts]:upward(ytd-grid-video-renderer.style-scope.ytd-grid-renderer)](http://www.youtube.com/##span.style-scope.ytd-thumbnail-overlay-time-status-renderer[aria-label=Shorts]:upward(ytd-grid-video-renderer.style-scope.ytd-grid-renderer))  
  
## Block shorts in list view: (Makes page white - do not use)  
# [www.youtube.com##span.style-scope.ytd-thumbnail-overlay-time-status-renderer[aria-label=Shorts]:upward(ytd-item-section-renderer.style-scope.ytd-section-list-renderer)](http://www.youtube.com/##span.style-scope.ytd-thumbnail-overlay-time-status-renderer[aria-label=Shorts]:upward(ytd-item-section-renderer.style-scope.ytd-section-list-renderer))  
  
## Block shorts menu item:  
[www.youtube.com##ytd-guide-entry-renderer.style-scope.ytd-guide-section-renderer](http://www.youtube.com/##ytd-guide-entry-renderer.style-scope.ytd-guide-section-renderer) > a > tp-yt-paper-item > yt-formatted-string:has-text(/Shorts/):upward(ytd-guide-entry-renderer)
```