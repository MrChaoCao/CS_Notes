# Building rails routes

## Root
Root is a special case

root paths must always follow this convention:
root 'home#index'

otherwise routes look like this:
get 'home/index' ( * see below )
get 'home/index' => 'home#index'
get 'home/index', to: 'home#index'

( * ) By convention rails will add in the right half and replace '/' with '#' 
