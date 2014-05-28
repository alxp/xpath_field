XPath Field module

XPath Field lets you add additional fields which can extract snippets from another field of the same node which contains XML text and loads them as separate fields.

The fields aren't persisted in storage, so modifying the contents of the XML will instantly be reflected in the derived XPath Fields. This is useful for connecting Drupal to an XML document store where you might otherwise add large numbers of fields which need updating whenever the source document changes.

REQUIREMENTS

Drupal core version >= 7.22 - This module calls field_info_field_map, introduced in Drupal 7.22.

INSTALLATION

Setting up fields

In Admin -> Content Types, create or edit a content type, and add an either a XML Field field or a standard long text field. The advantage of an XML field is that it enforces correctness of the XML data entered into it, but this isn’t required.

Alternatively, you can choose a field which contains a path to XML data stored on another web server. When you select the field on the node that will contain the XML file path, you will be asked to specify the prefix (server address and optionally a path prefix) that the path field will be appended to.

For example, the prefix might be: http://myxmlstore.mycomain.com/xml/ and the field may contain a value like “/article/1/1/metadata.xml”. Putting these two paths together should resolve to an XML document.

Save the new field, then add an XPath Fragment field. On the widget instance configuration page, you will see a select list showing the previously-created field instance. If you added more than one field instance, you would be able to choose which field you want your XPath to reference.

Next enter in the XPath that this new field will use to extract its value. XPaths which return multiple results will appear as multiple field values.

Now when you enter some XML into the XML Field, the XPath fragment will be extracted and behave just like any other field, and can be managed using Manage Display and themed just like any normal field.

For an introduction to XPath see https://developer.mozilla.org/en-US/docs/XPath

Author:
Alexander O'Neill
https://drupal.org/user/173521
