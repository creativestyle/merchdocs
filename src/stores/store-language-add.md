---
title: Adding a Language
---

Most of the text that appears to be hard-coded on pages throughout your store can be instantly changed to a different language by changing the locale of the view. Changing the locale does not actually translate the text word-for-word, but simply references a different translation table that provides the interface text that is used throughout the store. The text that can be changed includes navigational titles, labels, buttons, and links such as “My Cart” and “My Account.” You can also use the [Inline Translation]({% link configuration/advanced/developer.md %}) tool to touch up text in the interface.

Language packs can be found under [Translations &amp; Localization][1] on Magento Marketplace. New extensions are continually added to Marketplace, so check back often!

## Step 1: Install a Language Pack

Follow the standard instructions to install the language pack extension from [Component Manager]({% link system/web-setup-extension-manager.md %}).

## Step 2: Create a Store View for the Language

1.  On the _Admin_ sidebar, click **Stores**.

1.  Under _Settings_, choose **All Stores**.

1.  Click **Create Store View**. Then, do the following:

    -  **Store**—Choose the store that is the parent of the view.

    -  **Name**—Enter a name for the store view. For example: Portuguese.

       In the header of the store, the name appears in the “language chooser.”

    -  **Code**—Enter a **Code** in lowercase characters to identify the view. For example: `portuguese`.

    -  **Status**—To activate the view, set to `Enabled`.

    -  **Sort Order**—(Optional) Enter a number to determine the sequence in which this view is listed with other views.

1.  When complete, click **Save Store View**.

## Step 3: Change the Locale of the Store View

1.  On the _Admin_ sidebar, click **Stores**.

1.  Under _Settings_, choose **Configuration**.

1.  In the upper-left corner, set **Store View** to the specific view where the configuration is to apply. When prompted to confirm scope switching, click **OK**.

1.  Expand ![]({% link images/images/btn-expand.png %}){: .Inline} the **Locale Options** section.

1.  Clear the **Use Website** checkbox after the Locale field. Then, set **Locale** to the language that you want to assign to the view.

    If there are several variations of the language available, make sure to choose the one for the specific region or dialect.

1.  When complete, click **Save Config**.

    After you change the language of the locale, the remaining content that you have created, including [product]({% link catalog/product-translate.md %}) names and descriptions, categories, [CMS]({% link cms/page-translate.md %}) pages, and blocks must be translated separately for each store view.

[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
