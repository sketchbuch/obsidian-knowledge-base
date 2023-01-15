# Impact Assessment

Information about measuring the results of the a11y changes you are making.

---

Can I tell if a user is using...

## A Screen Reader?

There is no way to tell if someone is using a Screen Reader, this information would need to be communicated via A11y APIs to supporting applications like Browsers and then they would need to expose this information in an API for developers to use.

## Keyboard only?

There are no real reliable ways of detecting this. You could listen for mouse movements or specific keyboard control use on components. Probably the best way at the moment is to use [Media Queries](https://stackoverflow.com/questions/7838680/detecting-that-the-browser-has-no-mouse-and-is-touch-only#answer-52854585), but these are not supported by all browsers yet.