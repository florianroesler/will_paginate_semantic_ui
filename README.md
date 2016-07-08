# Will Paginate for Semantic UI

[![Gem Version](https://badge.fury.io/rb/will_paginate_semantic_ui.svg)](http://badge.fury.io/rb/will_paginate_semantic_ui) [![Travis](https://api.travis-ci.org/rafaelbiriba/will_paginate_semantic_ui.svg?branch=master)](https://travis-ci.org/rafaelbiriba/will_paginate_semantic_ui) [![Coverage Status](https://coveralls.io/repos/rafaelbiriba/will_paginate_semantic_ui/badge.svg?branch=master)](https://coveralls.io/r/rafaelbiriba/will_paginate_semantic_ui?branch=master)

#### If you are using [Will Paginate gem](https://github.com/mislav/will_paginate) and [Semantic UI framework](http://semantic-ui.com/), this gem is WHAT YOU NEED!

The html snippet for pagination that the `will_paginate` creates is incompatible with the semantic ui component.

This gem solves this problem with a custom render that creates the correct pagination html for the component.

![Example](https://raw.githubusercontent.com/rafaelbiriba/will_paginate_semantic_ui/master/docs/example1.png)
![Example](https://raw.githubusercontent.com/rafaelbiriba/will_paginate_semantic_ui/master/docs/example2.png)

## Requirements

Semantic UI `> 2.0` and will_paginate `> 3.0`

## Installation

As easy as `gem install will_paginate_semantic_ui` or add `gem "will_paginate_semantic_ui"` to your Gemfile

## How to use

### Rails

You need to use another render in the will paginate command:

`<%= will_paginate @collection, renderer: WillPaginateSemanticUi::Renderer %>`

## Tuning

You can also use some will_pagination options to customize your component:

`<%= will_paginate @archived_medias, renderer: WillPaginateSemanticUi::Renderer, class: "right floated", inner_window: 3 %>
`

The command above create this

![Example](https://raw.githubusercontent.com/rafaelbiriba/will_paginate_semantic_ui/master/docs/example1.png)

`inner_window: 3` as you see above, 3 pages to the left and to the right from the selected page. (This creates a component with 700px max width in the worst case)

![Example](https://raw.githubusercontent.com/rafaelbiriba/will_paginate_semantic_ui/master/docs/example3.png)

`class: "right floated"` useful if you are using inside a table. Floats the pagination to the right.
