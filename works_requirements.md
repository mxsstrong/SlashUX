Deposit: archive in the system
Publish: make a deposited item publicly visible

**Items persist in three states:**
* In-progress / saved
  *No DOI
  *Everything can be changed
  *Item can be deleted completely
  
* Deposited but embargoed
  *DOI assigned (_problematic_)
  *Content is fixed
  *Metadata can be edited
  
* Published
  *DOI assigned
  *Content is fixed
  *Metadata can be edited
  
**Functional requirements**
1. In-progress
  1. resume work
    1. edit metadata
    2. upload or delete files
    3. set rights / embargo
    4. publish
  2. delete / abandon
2. Published
  1. edit metadata
  2. upload new version
3. Embargoed 
  1. publish now
  2. change embargo date
  3. edit metadata
  4. upload new version
  5. grant access to someone else (e.g., for peer review)
      this is a complicated: not addressed right now

**Implementation notes**
1. In-progress
  1. resume work: re-opens workflow
      at latest point where the user entered something, or
      let user pick where
  2. delete / abandon
      require the user to confirm
2. Published
  1. edit metadata
      return to workflow, or
      open overlay identical to metadata page
  2. upload new version: create a new item
      prepopulate metadata from the existing item
      prepopulate "related works" with "new version of" link back to existing
      on deposit, add "previous version of" link from existing to new item
1. Embargoed
  1. publish now
      require the user to confirm
  2. change embargo date
      link to review page, or
      open just the date picker panel.
  3. upload new version
    1. prepopulate embargo date from the existing item
    
      
      
      
      
