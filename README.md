<!--h-->
# Enso Vue Components

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/c0ebffca7afd42beaf0e48b3113096df)](https://www.codacy.com/app/laravel-enso/VueComponents?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=laravel-enso/VueComponents&amp;utm_campaign=Badge_Grade)
[![StyleCI](https://styleci.io/repos/99346868/shield?branch=master)](https://styleci.io/repos/99346868)
[![License](https://poser.pugx.org/laravel-enso/vuecomponents/license)](https://packagist.org/packages/laravel-enso/vuecomponents)
[![Total Downloads](https://poser.pugx.org/laravel-enso/vuecomponents/downloads)](https://packagist.org/packages/laravel-enso/vuecomponents)
[![Latest Stable Version](https://poser.pugx.org/laravel-enso/vuecomponents/version)](https://packagist.org/packages/laravel-enso/vuecomponents)
<!--/h-->

VueJS Components Collection for [Laravel Enso](https://github.com/laravel-enso/Enso).

### Features
- Bulma elements, suite of common, reusable components styled for Bulma
- Charts components, for the [Charts](https://github.com/laravel-enso/Charts) package
- Comments components, for the [CommentsManager](https://github.com/laravel-enso/CommentsManager) package
- Contacts components, for the [Contacts](https://github.com/laravel-enso/Contacts) package
- Datatable component, for the [Datatable](https://github.com/laravel-enso/Datatable) package
- Documents components, for the [DocumentsManager](https://github.com/laravel-enso/DocumentsManager) package
- FileUploader component, for handling the upload of files
- NProgress component, for showing load progress
- RoleManager components, for the [RoleManager](https://github.com/laravel-enso/RoleManager) package
- Select component, for the [Select](https://github.com/laravel-enso/Select) package

#### Bulma
- `BooleanFilter`, a single option filtering component with predefined options to filter boolean values (true, false, null), that can be used in conjunction with datatables or anywhere else you need it 
- `Card`, a multi purpose container
- `Dropdown`, a simple dropdown
- `Modal`, an ultra light and smart modal component
- `Overlay`, an overlay container
- `Paginate`, a simple to use and powerful pagination module
- `Popover`, a basic dual option popover useful for confirming actions
- `Tabs`, a tab manager component
- `Typeahead`, exactly what the name says
- `VueFilter`, a single option filtering component, that can be used in conjunction with datatables or anywhere else you need it 
- `VueSelectFilter`, a select option filtering component

#### BooleanFilter
Takes the following properties (in addition to the propertios of `VueFilter`:
- `yesLabel` - string, the label for filter = true | default `Yes` | (optional)
- `yesLabel` - string, the label for filter = false | default `No` | (optional)

To use it include it in the page:
```
<boolean-filter
        title="Active"
        v-model="filters.users.active">
</boolean-filter>
```

##### Card
Takes the following properties:
- `collapsed`, boolean, flag for the initial state of the card | default `false` | (optional)
- `icon`, object, an icon object for the card's icon | default `null` | (optional)
- `title`, string, the name that's displayed as title | default `null` | (optional)
- `search`, boolean, flag for showing the search box | default `false` | (optional)
- `badge`, number, value that's displayed | default `null` | (optional)
- `refresh`, boolean, flag for refresh control | default `false`| (optional)
- `fixed`, boolean, flag for making the card non collapsible | default `false` | (optional)
- `removable`, boolean, flag for showing the close button | default `false`| (optional)
- `controls`, number, option for generating the needed number of controls slots | default `0` | (optional)
- `overlay`, boolean, flag for rendering the overlay inner component | default `false`, | (optional)

#### DateIntervalFilter
Takes the following properties:
- `title`, string, the name that's displayed as title | default `null` | (optional)
- `min`, the starting date for lower limit date selector | required
- `max` - the starting date for higher limit date selector | required

#### Dropdown
Takes the following properties:
- `width`, number, the minimum width for the dropdown menu | default `64` | (required)
- `height` - number, the maximum height for the dropdown content | default `200` | (optional)

#### IntervalFilter
Takes the following properties:
- `title`, string, the name that's displayed as title | default `null` | (optional)
- `type`, string, the type of the two filter inputs | required
- `min`, the starting date for lower limit input | required
- `max` - the starting date for higher limit input | required

#### Modal
The Modal component renders itself as a `<body>` child, within a div, by default with the `modal-wrapper` wrapper class,
as it offers an elegant solution to various z-index related issues that might otherwise arise.

Irrespective of its content, the modal renders a subtle close button in the top right corner, 
and will also close when using the Esc key.
 
Takes the following properties:
- `show`, boolean, makes the modal visible | (required)
- `card`, boolean, if true, renders a card with header, body & footer slots, 
otherwise renders a simple div with an unnamed, default slot | defaults to `false` | (optional)
- `container`, string, the css class of the div container used to render the modal | default `modal-wrapper` | (optional)

#### Overlay
Takes the following properties:
- `size`, small/medium/large, size of the loader | default `small` | (optional)
- `transparent`, boolean, sets the transparency | default `false` | (optional)
- `color`, string, the color code for the overlay | default `#f44336` | (optional)

#### Paginate
Takes the following properties:
- `list`, array, the items that need to be paginated | (required)
- `length`, number, the starting number of items on one page | default `10` | (optional)
- `lengths`, array, an array of lengths to choose from | default `[10, 15, 20, 25, 30]` | (optional)
- `border`, boolean, a flag for showing a border around the component | default `false` | (optional)    

#### Popover
Takes the following properties:
- `placement`, string, the placement position (`top`, `top-start`, `top-end`, `right`, `right-start`, `right-end`, 
`bottom`, `bottom-start`, `bottom-end`, `left`, `left-start`, `left-end`) | default `bottom` | (required)
- `trigger`, string, the type of trigger to be used (`hover`, `click`, `focus`, `manual`) | default `click` | (optional)
- `open`, boolean, flag that make the component visible | default `false` | (optional)

#### Tabs
Takes the following properties:
- `alignment`, left/center/right, the alignment of the tabs | default `left` | (optional)
- `size`, small/normal,medium/large, the size of the element, as styled by bulma's is-* classes| default `normal` | (optional)
- `boxed`, boolean, flag that toggles the rendering of the tabs in a box | default `false` | (optional)
- `toggle`, boolean, flag that toggles the `is-toggle` bulma class, for mutually exclusive tabs | default `false` | (optional)
- `toggleRounded`, boolean, flag that toggles the `is-toggle-rounded` bulma class, where the first and last tabs are rounded | default `false` | (optional)
- `fullwidth`, boolean, flag that toggles the `is-fullwidth` bulma class, where the tabs take up the entire available width | default `false` | (optional)

#### Tab
Takes the following properties:
- `id`, string/object, a value used to identify the tab - gets passed to parent (Tabs) component | required 
- `default`, boolean, tab index value, sets the active tab | default `false` | (optional)

#### Typeahead
Takes the following properties:
- `disabled`, boolean, the title string | default `null` | (optional)
- `length`, number, the number of retrieved options | default `10` | (optional)
- `source`, string, the endpoing that gives back results | (required)
- `params`, object, properties object that gets sent with the request | default `null` | (optional)
- `label`, string, label | (required) 
- `placeholder`, string | default `What are you searching for today?` | (optional)
- `notResults`, string, a placeholder when not having results | default `No results found matching the criteria...` | (optional)
- `searching`, string, a placeholder while searching | default `Searching...` | (optional)
- `validator`, boolean, flag that enables the value validation using the regular expression | default `false` | (optional)
- `regExp`, RegExp, validation regular expression | default `/.*/` | (optional)
- `value`, String, starting value | default `` | (optional)

#### VueFilter
Takes the following properties:
- `title` - string, the title to display above the options | default `null` | (optional)
- `options` - object, the options the user can choose from when filtering | default `{}` | (required)
- `value` -  the selected value from the list of options | (required)
- `theme` - string, the theme to use for styling the box | default `primary` | (optional)
- `hideOff` - boolean, flag for showing an off switch | default `false` | (optional)

To use it include it in the page:
```
<vue-filter
        title="Taxes Paid"
        v-model="filters.orders.paid_taxes"
        :options="options">
</vue-filter>
```

where the `options` and `filters` may be something like:

```
options: [
    {value:true, label:"Yes"},
    {value:false, label:"No"}
],
filters: {
    orders: {                
        paid_taxes: '',                
    }
},
```

Next, when defining your DataTable, make sure you give it your filters:

```
<vue-table class="box"
    source="orders" 
    :extra-filters="filters" 
    id="index-orders-id">
</vue-table>
```

Note that you may use more than one such filter, just bind it inside the same encompassing `filters` object 
and it will get passed to the datatables BE logic.


#### FileUploader
Takes the following properties:

- `multiple` - boolean, flag that allows single/multiple selection | default false | (optional)
- `url` - string, the url to post to the selected files | (required)
- `fileSizeLimit` - number, the max file size for the upload | default `8388608` | (optional)
- `params` - object, params that get sent along with the files | default `null` | (optional)
- `fileKey` - string, request key for the file(s) sent when uploading, 
allowing for a more meaningful interpretation of the request in the backend | default `file` | (optional)

Also, fires the following self explanatory events:
- `upload-start`
- `upload-successful`
- `upload-error`


#### NProgress
On init, the component adds itself to the Axios `request` & `response` interceptors, as well as to the `beforeEach` & `afterEach` interceptors of VueRouter so it starts and stops without manual intervention.

The `NProgress.vue` listens to the following, self-descriptive, events:
- `nprogress-add-request`
- `nprogress-add-response`
- `nprogress-done`


### Publishes

- `php artisan vendor:publish --tag=vue-components` - the main VueJS components and their dependencies
- `php artisan vendor:publish --tag=enso-assets` - a common alias for when wanting to update the VueJS assets,
once a newer version is released, can be used with the `--force` flag


### Notes

The [Laravel Enso Core](https://github.com/laravel-enso/Core) package comes with this package included.


<!--h-->
### Contributions

are welcome. Pull requests are great, but issues are good too.

### License

This package is released under the MIT license.
<!--/h-->