# Secura Home enquiry form review

A small, self-initiated learning project: record a form-label finding and prepare a local HTML example of a proposed change.

## The finding

The recorded [contact page](https://www.securahome.co.uk/contact/) had nine form controls without associated labels or recorded alternative names. For the first-name field, the visible **First Name** caption was plain `div` text. Clicking it did not focus the input in the recorded check.

## The evidence

[contact-form-evidence.json](contact-form-evidence.json) retains the captured field information, first-name markup and focus result unchanged.

Recorded steps:

1. Focus the Business Name input.
2. Click the First Name caption.
3. Check the focused element and the first-name label lookup.

The first-name input remained unfocused; the label lookup returned zero matches. Recorded on **21 October 2026**, using desktop Chrome in a cloud session. Exact viewport and browser version were not retained.

## The proposed change

Give the input an ID and connect a real label to it:

```html
<label for="first-name">First Name*</label>
<input id="first-name" name="first_name" type="text">
```

This follows [W3C guidance on form labels](https://www.w3.org/WAI/tutorials/forms/labels/). The example preserves the field's name and type.

Download [form-label-example.html](form-label-example.html), open it in a browser and try clicking **First Name** above each box. GitHub's file view shows the source code.

## Scope

The proposed HTML label structure has been checked. Local browser interaction, mobile layout and screen-reader behaviour have not yet been tested. No enquiry was submitted and the live website was not changed. No effect on leads, sales or internal CRM systems has been established.

This is an ongoing learning project.
