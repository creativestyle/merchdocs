---
title: Custom Rewrites
---

A custom rewrite can be used to manage miscellaneous redirects, such as redirecting a page from your store to an external website. For example, you might have two Magento websites, each with their own domain. You can use a custom redirect to reroute requests for a product, category, or page to the other website. Unlike other redirect types, the target of a custom redirect is not chosen from a list of existing pages in your store.

Before you begin, make sure that you understand exactly what the redirect is to accomplish. Think in terms of "target" and "original request", or "redirect to" and "redirect from". Although people might still navigate to the former page from search engines or outdated links, the redirect causes your store to switch to the new target.

![]({% link images/images/url-rewrite-custom.png %}){: .zoom}
*Add URL Rewrite*

## Step 1. Plan the Rewrite

To avoid mistakes, write down the URL of the "redirect to" page, and the URL key of the "redirect from" page.

If you are not sure, open each page, and copy the URL from the address bar of your browser.

**Custom Path**

Redirect to:

    http://www.different-website.com/page.html

Redirect from:

    cms-page
    category.html
    category/subcategory.html
    product.html
    category/product.html

## Step 2. Create the Rewrite

1. On the Admin sidebar, tap **Marketing**. Then under **SEO &amp; Search**, choose **URL Rewrites**.

1. Before you proceed, do the following to verify that the "request path" is available:

    * In the search filter at the top of the **Request Path** column, enter the URL key of the page that is to be redirected. Then, tap <span class="btn">Search</span>.

    * If there are multiple redirect records for the page, find the one that matches the applicable store view. Then, open the redirect record in edit mode.

    * In the upper-right corner, tap <span class="btn">Delete</span>. When prompted, tap <span class="btn">OK</span> to confirm.

1. When you return to the URL Rewrites page, tap <span class="btn">Add URL Rewrite</span>.

1. Set **Create URL Rewrite** to “Custom”.

1. Under URL Rewrite Information, do the following:

    * If you have multiple store views, select the **Store** where the rewrite applies.

    * In the **Request Path** field, enter the URL key and path—if applicable—of the product, category, or CMS page that is to be redirected.

        {: .bs-callout .bs-callout-info}
        The Request Path must be unique for the specified store. If there is already a redirect that uses the same Request Path, you will receive an error when you try to save the redirect. The previous redirect must be deleted before you can create a new one.

    * In the **Target Path** field, enter the URL of the destination. If the target is located on another website, enter the fully qualified URL.

    * Set **Redirect** to one of the following:

        * Temporary (302)
        * Permanent (301)

    * For your reference, enter a brief description of the rewrite.

    ![]({% link images/images/url-rewrite-custom-add.png %}){: .zoom}
    *Custom URL Rewrite*

1. Before saving the redirect, review the following:

    * The Request Path contains the URL key or path of the original "redirect from" page.
    * The Target Path contains the URL of the "redirect to" page.

1. When complete, tap <span class="btn">Save</span>.

    The new rewrite appears in the grid at the top of the list.

    ![]({% link images/images/url-rewrite-cms-page-saved.png %}){: .zoom}
    *Saved URL Rewrite*

## Step 3. Test the Result

1. Go to the home page of your store.

1. Do one of the following:

    * Navigate to the original "redirect from" page.
    * In the address bar of the browser, enter the name of the original "redirect from" page immediately after the store URL. Then, press **Enter**.

    The new target page appears instead of the original page request.

## Field Descriptions

Create URL Rewrite
: Indicates the type of rewrite. The type cannot be changed after the rewrite is created. Options:CustomFor categoryFor productFor CMS page

Request Path
: The path to the product, category, or CMS page that is to be redirected. Depending on your configuration, the Request Path might include the .html or .htm suffix. The Request Path must be unique, and cannot be in use by another redirect. If you receive an error that the Request Path already exists, delete the existing redirect, and try again.

Target Path
: The path or URL that is the  destination of the redirect.

Redirect
: Determines the type of redirect. Options:
   * No - No redirect is specified.Many operations create redirect requests of this type. For example, every time you add products to a category, a redirect of the "No" type is created each store view.
   * Temporary (302) - Indicates to search engines that the rewrite is for a limited time. Search engines generally do not retain page rank information for temporary rewrites.
   * Permanent (301) - Indicates to search engines that the rewrite is permanent. Search engines generally retain page rank information for permanent rewrites.

Description
: Describes the purpose of the rewrite for internal reference.