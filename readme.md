# Nav Accordion Plugin

This project is a jQuery plugin can be used to easily add accordion expand/collapse functionality to a navigation area. It is most useful for a navigation drawer or left navigation. It works best when the navigation pattern is similar to `ul > li > a`. 

## Features to note

> This plugin has self contained styling for positioning the expand and collapse icons, so there is no css that needs to be added to your template for this to work correctly, although you will probably still want to do some styling to the accordion expand/collapse buttons such as applying a background color. Use the class `.accordion-btn` for stying the buttons.

> By default, the plugin will leave parent page links intact, so clicking the accordion button will expand the child navigation but clicking on the parent link text will go to the page. However, if a page is set to be a header only (no link on the `<a>` tag), the whole link will act as the expand/collapse button.

> It will automatically expand the sub navigation for the currently selected channel (the `<li>` that has the class "selected") when the page first loads.

## How to use

To use this plugin, you must first have load the jQuery library on the page. You can next include the `navAccordion.min.js` script. The plugin should be called on the element that immediately wraps the first ul of the navigation. The following function contains the most basic options for calling the plugin, and this is what you will probably use the majority of the time.

```javascript
	//Basic function for calling nav accordion plugin
	jQuery('.m-pikabu-sidebar .mainNav').navAccordion({
		//Text inside of expand and collapse buttons
		// This can be HTML, such as a Font Awesome Icon, for example
		expandButtonText: '<i class="fa fa-plus"></i>',  
		collapseButtonText: '<i class="fa fa-minus"></i>'
	});
```

## Plugin Options

- `expandButtonText` - `+` is default - text inside of expand button - this can be HTML

- `collapseButtonText` - `-` is default - text inside of collapse button - this can be HTML

- `buttonWidth` - `20%` is default - width of accordion expand/collapse button as a percentage or pixels

- `buttonPosition` - `right` is default - position of button - you can also choose `left`

- `multipleLevels` - true is default - setting to false will add the accordion functionality only to the top level links

- `selectedClass` -`selected` is default - class name that will be used to detect the currently selected channel - this will check the "parentElement" for this class (the parent <li> by default)

- `selectedExpand` - `true` is default - boolean to expand the selected channel or not

- `headersOnly` - false is default - setting to true will make any link with sub-nav behave as if it were set to a header only (no href), making the link inaccessible - this option is useful if you are using the plugin for a non-navigation area

- `headersOnlyCheck` - false is default - set to true to apply the accordion only to links that are set as "header only" (have no href)