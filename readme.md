# lamark
next generation markup language.


## about:
lamark is for humans, not machines.

technically,  
it is something between YAML and Markdown.

it is extension-free, tool-free, renderer-free  
and even device-free – you are free to use it on paper.


## first steps:
create _.txt_ file,  
open it in any text/code editor,  
start to structure your text lean on lamark spec sheet.

use monospaced fonts. Author like  
[JetBrains Mono NL](https://www.jetbrains.com/lp/mono/) (NL is No Ligatures).

you are also free to use it directly in Markdown,  
using [code formatting feature](https://www.markdownguide.org/extended-syntax/#fenced-code-blocks),  
in Slack or Telegram for example,  
it may seem handy for you.


## spec sheet / usage scenarios:
for ease of perception:  
- all items in lamark begin with lowercase letters.  
- sentences are broken up into new lines  
  according to their meaning.


### single-level list:
```
.. groceries:
   .. bananas
   .. lemonade
   .. rice brown
   .. bread
```


### multi-level list:
```
.. groceries:
   .. bananas
      .. mini
      .. classic
   .. lemonade
   .. rice brown
   .. bread
```
any depth is acceptable.


### multi-line item:
```
.. groceries:
   .. bananas
   .. lemonade
   .. rice brown
   .. bread
      gluten free
      sugar free
   .. cookies
      gluten free, sugar free
```
good for detailing.


### items in one-line, using multi-line:
```
.. groceries:
   bananas, lemonade, rice brown, bread
```
good for short items.


### when need to relate items, but header is not needed:
```
.. groceries:
   .. :
      .. bananas mini
      .. watermelon
      .. lemon
   .. :
      .. protein bars
      .. cookies
         gluten free
         sugar free
```


### remark / mini-comment / not list item:
```
.. groceries:
   .. rice brown
   .. bread
      ,. gluten free, sugar free
      .. brown
      .. wheat
```


### item needs is questionable / we have doubts / there is some uncertainty:
```
.. groceries:
   .. rice brown
   .. bread
      ,. gluten free, sugar free
      .. brown
      .. wheat
      .? loaf
```
notice dot position.


### item needed, but will be added later:
```
.. groceries:
   .. rice brown
   .. bread
      ,. gluten free, sugar free
      .. brown
      .. wheat
      .? loaf
      .. ...
```


### task management:
#### prioritization:
##### last-priority / probably not needed / difficulty in deciding to delete / preparing to be soon deleted:
```
.. groceries:
   9. bananas
   .. lemonade
   .. rice brown
   .. bread
   .. water
```


##### first-priority / asap / important / burning:
```
.. groceries:
   .. bananas
   1. lemonade
   .. rice brown
   .. bread
   1. water
```


##### second-priority / also important, but not for first:
```
.. groceries:
   2. bananas
   1. lemonade
   .. rice brown
   .. bread
   1. water
```

three numbers are supposed to be used:  
***1***, ***2*** and ***9***.  

at the same time,  
these numbers can be used many times.


#### done:
most convenient solution at the moment  
is next:

save an original list  
and work with a new copy  
by deleting done items in-place.


### combinations / using together:
mini-comment with doubts:
```
.. groceries:
   .. rice brown
   .. bread
      ,. gluten free, sugar free
      ,? hypoallergenic
      .. brown
      .. wheat
```

setting ***probably not needed*** for related items without header:
```
.. groceries:
   .. :
      .. bananas mini
      .. watermelon
      .. lemon
      .. ...
   9. :
      .. protein bars
      .. cookies
         gluten free
         sugar free
```


## versioning and release strategy:

```
branches and versions:

.. master-branch name:
   master
   ,. default branch.
   ,. branch is read-only.
   ,. branch for stable versions.
   ,. stable versions called like v2.3.[1-99].
   ,. each commit in this branch
      is a new release,
      so commit message should be called like
      "release v2.3.1".

.. development-branch name:
   v2.3.draft
   ,. branch for development new stable version.
   ,. branch open for contributions
      via pull requests.

,. information about switching to v2.4.*
   will be available later.

,. all in this project,
   including spec sheet and project description, 
   are one document (current) with
   one actual release-version,
   so any changes, 
   even changes in description,
   need to have new release.

,. first two numbers in the version (v*.*)  
   correspond to the year.
```


## contributing:
```
contributing:

,. branch v2.3.draft is open
   for contributions via pull requests.

,. please do not forget squash your commits
   before submitting pull request.

,. please do not send pull requests
   to the master-branch.
```
