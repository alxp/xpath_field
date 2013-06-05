XPath Field module

This module extends the capabilities of the XML Field module. XML Field adds a field type for XML documents. XPath Field lets you add additional fields which can extract snippets from an XML Field instance and loads them as separate fields. 

The fields aren't persisted in storage, so modifying the contents of the XML will instantly be reflected in the derived XPath Fields. This is useful for connecting Drupal to an XML document store where you might otherwise add large numbers of fields which need updating whenever the source document changes.

INSTALLATION

This module depends on XML field, if that is installed then simply enable XPath Fragment the usual way.

Setting up fields

In Admin -> Content Types, create or edit a content type, and add an XML Field field. Save the new field, then add an XPath Fragment field. On the widget instance configuration page, you will see a select list showing the previously-created XML Field instance. If you added more than one XML field instance, you would be able to choose which field you want your XPath to reference.

Next enter in the XPath that this new field. XPaths which return multiple results will appear as multiple field values.

Now when you enter some XML into the XML Field, the XPath fragment will be extracted and behave just like any other field, and can be managed using Manage Display and themed just like any normal field.

For an introduction to XPath see https://developer.mozilla.org/en-US/docs/XPath

Author:
Alexander O'Neill
https://drupal.org/user/173521