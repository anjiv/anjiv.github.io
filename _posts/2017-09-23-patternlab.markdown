---
layout: post
title:  "Patternlab"
date:   2017-09-23
categories: anjali update
---

Patternlab is used for creating atomic designs so that, the code can be reused wherever necessary.
Code once written in a file can be included in the other file wherever required.

Pattern as the name suggest contains a pattern which needs to be followed to create the pages.

As patternlab is used to create atomic design so, it follows the structure of an atom.

Atom is the smallest unit that has some property. Likewise, the smallest part while building a page are buttons, images, text, etc which acts like an atom.
These atoms are then grouped together to form a molecule which in terms of a webpage can be thought as blocks, forms and many more like this.
Now, a molecule is grouped together to form a organism which can be a list, section, etc.
Then, organisms are used to form templates so that they can be used to build pages. Templates can be dashboard, detail, form, homepage.
Finally, these templates are used to build different webpages which involves all of the above.

For eg
lets suppose there is a login form on a page
This form can be thought of as a block molecule. The molecule will contain three type of atoms (Input , Label n button).

` input-atom.twig`
``` twig
<div class="input-atom">
  <input class="sd" type="text"/>
</div>
```

` label-atom.twig`
``` twig
<div class="input-atom">
  <label> Label </label>
</div>
```

` button-atom.twig`
``` twig
<div class="input-atom">
  <button> Button </button>
</div>
```

` form-molecule.twig`
