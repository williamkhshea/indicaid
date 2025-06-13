# Extend Shopify Product Page Settings
Add new settings $ARGUMENTS to the $ARGUMENTS to extend the configurations. Think harder step by step.

## Instructions
1. Use grep `grep -r "schema"` to locate the schema block and add the new setting to the schema at the bottom of page. 
2. When you are creating name or label, add a new entry that is linking to the locales file, for example: `t:sections.main-product.blocks.inventory.settings.text_style.options__1.label`.
3. Add an English translation for the name or label settings in the `en.default.schema.json` file. The file is large so use `grep -r` to search for the section name.