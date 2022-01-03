[Best Practices for Writing Code
Comments](https://stackoverflow.blog/2021/12/23/best-practices-for-writing-code-comments/)

# Rules of thumb for better comments in code

## Comments should not duplicate code

Recently, I was told by a senior engineer that we don't ever need comments.
Everything we need is in the code. That statement has some truth to it, even tho
I don't agree with it 100%. Assuming people who read your code know about the
programming language and its syntax, there is no need to explain what the code
does on every line. We don't need to point out "oh this is a for loop" or "this
is an integer". Syntactical definitions like those are clearly presented in the
code, so we don't need to explain them with comments.

## Comments should not excuse bad code

One example that comes to mind is the variable naming convention. Each variable
should have a descriptive name. If we need to write comment to explain what the
variable is, we should rename that variable. Bad naming conventions (like a
single-letter variables) introduce unclear code, which can be improved by better
naming conventions.

## If you can't explain your code in the comment, rewrite your code

We should always try to understand what we're coding. The why is important, but
the what is crucial. If we can't explain what the code is doing, we don't
understand it well enough, so how do we expect readers of our code to understand
it. This also presents a problem when we need to debug the code. The Kernighan's
law goes like this:

```Debugging is twice as hard as writing the code in the first place. Therefore,
if you write the code as cleverly as possible, you are, by definition, not smart
enough to debug it.```

## Explain unidiomatic code in the comments

For pieces of code that are called, if they behave in an unexpected way, we
should note that in the comment. A good example is null checking a boolean when
needed. If an API call can return some unexpected/standard result, it's a good
idea to put them in the comments as well to save the readers some time.

## Provide link to the code/references we find useful online

There is no secret we all copy code from stackoverflow from time to time.
Putting the url of the post in the comments can help readers quickly go get more
information if need to. It's also important to understand the code before we
copy paste as it can contain malicious code.

Reading documentation is a skill every program should master. Links to these
documentations can prove to be very helpful when provided. If we think the
readers can benefit from the extra information found in the documentations, we
should definitely provide the links in comments.

## Use comments for bug fix to provide quick context

Explain why the code changes were needed. A ticket number would also be useful
here.

## Use comments to mark for incomplete implementation

If we check in incomplete code, which is code with limitation or technical debt,
note that in the comments so we can be reminded next time. It's also a good idea
to explain the reason why something isn't done/completed.
