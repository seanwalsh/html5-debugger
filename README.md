
# Debugging SCSS File Usage Guide

This SCSS file is designed to help you identify unsupported or partially supported HTML elements across various browsers. It highlights elements that are either obsolete, have limited support, or are unsupported in HTML5.

## How to Use

1. **Include the SCSS File in Your Project:** First, include the debug.scss file in your project. You can do this by importing it into your main SCSS file using the `@import` directive.

```scss
@import 'path/to/debug.scss';
```

2. **Enable or Disable Debugging:** By default, the debugging features are not active. To activate or deactivate the debugging features, you will need to set a `$debug` variable at the beginning of the `debug.scss` file.

To enable debugging, set `$debug` to `true`:

```scss
$debug: true;
```

To disable debugging, set `$debug` to `false`:

```scss
$debug: false;
```

3. **View the Debugging Indicators:** When `$debug` is set to `true`, the HTML elements that are not fully supported or are unsupported will be visually highlighted when you view your project in a browser. The specific styles applied to each category of elements are as follows:

- **Red Border:** Unsupported tags.
- **Orange Border:** Tags not supported by all browsers.
- **Black Dashed Bottom Border:** Unsupported attributes.
- **Yellow Background:** Other specific cases noted in the comments within the file.

## Customization

You can customize the debugging indicators by modifying the respective CSS properties within the `debug.scss` file.

## Integration

Remember to set `$debug` to `false` or remove the import statement from your production environment to ensure that the debugging styles do not interfere with your site's live presentation.

---