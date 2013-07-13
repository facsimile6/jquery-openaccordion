# jQuery OpenAccordion

OpenAccordion is a jQuery plugin for accordion-style drop-downs which can use arbitrary tags or selectors as
section headings. Any content located between headings headings is collapsed into accordian sections.

Especially useful in CMS and WYSIWYG environments where it is difficult to be sure of the exact HTML structure to be
used.

## Installation

    <script type="text/javascript" src="//code.jquery.com/jquery-2.0.3.min.js"></script>
    <script type="text/javascript" src="path/to/jquery.openaccordion.min.js"></script>

## Usage

Initialize an accordion section with default options using jQuery selectors:

    $("#my-accordion").openaccordion();

Additionally you may pass an options object to the openaccordion method:

    $("#my-accordion").openaccordion({
        sectionHeading: 'h3',
        openedIndicator: "&#9660;",
        closedIndicator: "&#x25b6;",
        displayOpenIndicator: true,
        activeClasses: ['active'],
        breakOn: ['h1', 'h2'],
        hideInactive: true,
        contentWrapper: $('<div></div>'),
        contentWrapperClass: 'jquery-openaccordion-content'
    });

The above options are the defaults, but can be modified to suit your needs. The option values are explained below.

## Options

- __sectionHeading__: The tag or selector to be used to deliniate the heading and start of an accordion section. Defaults to ```h3```
- __openedIndicator__: A character, HTML entity, or element to be used as the indicator that a section is open/expanded. Defaults to the down pointing triangle HTML entity (&#9660;).
- __closedIndicator__: A character, HTML entity, or element to be used as the indicator that a section is closed/contracted. Defaults to the right pointing triangle HTML entity (&#x25b6;).
- __displayOpenIndicator__: Whether or not the open/closed indicators should be added. Defaults to ```true```
- __activeClasses__: An array of class names to add to the delimiter element to indicate that it is active. Defaults to ```['active']```
- __breakOn__: An array of tags or selectors to use to indicate elements which should break out of the accordion section. Defaults to ```['h1', 'h2']```
- __hideInactive__: Whether or not inactive accordions should be automatically hidden when another one is opened. Defaults to ```true```
- __contentWrapper__: A jQuery element to wrap each section's content with. Pass a falsy value if you don't want the content wrapped. Defaults to ```$('<div></div>')```
- __contentWrapperClass__: A class to add to the contentWrapper. Defaults to ```'jquery-openaccordion-content'```

Please note that I do not provide any stylesheet with this plugin, and the script itself only adds minimal required styling, so it's up to you to style your accordion and content appropriately using CSS.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request