# How to Deploy PnP Modern Search Web Parts v4

If you use Microsoft 365 (Office 365), you probably have been using
[Microsoft Search](https://searchexplained.com/microsoft-search/), too.
But there might be use cases, when it\'s not enough - for example, when
you need a customized Search Application. If this is the case, your
number one option might be to deploy [PnP Modern Search Web
Parts](https://github.com/microsoft-search/pnp-modern-search). This is
an open source solution that helps you to build customized search
applications in SharePoint Online modern experience.
[However, this solution has to be deployed manually to your tenant.
Let\'s see how.]
## 1 - Download the PnP package


You can download the latest releases
[HERE](https://github.com/microsoft-search/pnp-modern-search/releases/).


You\'ll see there are two major versions: v3 and v4. Important notes:


-   **The v4 version uses a brand new code architecture and replaces the
    older v3 codebase**. There will be no new features added to v3.x
    anymore, but bug fixes will be provided as needed.
-   Because v4.x is not at feature parity yet with v3.x, you can still
    use the v3.x packages to meet your requirements.
-   Also, **there is not an auto-upgrade path from v3 to v4** due to the
    new architecture.
-   New search functionality backed by the Microsoft Graph Search API
    will be v4 only.

**If this is the first time you install PnP Modern Search, always go for
v4.**
On the Releases page, scroll down to Assets, and then click on the
.sppkg file:



**Note**: *If you've installed the 2021 Jan release of v4, you had to
deploy two packages, because the extensibility library was a separate
.sppkg file. With the 2021 March release, there's only one package, the
team has replaced the extensibility library dependency by an [npm
package](https://www.npmjs.com/package/@pnp/modern-search-extensibility).
Now you only need to deploy one SPFx solution in you app catalog.*
## 2 - Deploy the PnP Modern Search package to your tenant's App Catalog 

App Catalog is a special site collection in SharePoint, that stores the
apps for your organization' use. If you have an existing App Catalog,
you can [deploy the PnP Modern Search package
there](https://searchexplained.com/deploy-pnp-modern-search-web-parts-sharepoint-online/#deploy-pnp).
Otherwise, you have to create a new App Catalog.

### 2.1 - Create a new App Catalog 

You have to be a tenant administrator to create a new App Catalog.

Go to Microsoft 365 Admin / SharePoint Admin Center. On the left menu,
click on "More features", and the select "Apps":
![pnp-modern-search-sharepoint-app-catalog-01-1024x834](https://techcommunity.microsoft.com/t5/image/serverpage/image-id/298677iBE9DBBA877984A83/image-size/large?v=v2&px=999 "pnp-modern-search-sharepoint-app-catalog-01-1024x834")
Once here, click on New App Catalog, then fill in the form, so that the
new site collection will be created:
 

![pnp-modern-search-sharepoint-app-catalog-02-1024x535](https://techcommunity.microsoft.com/t5/image/serverpage/image-id/298678iB9FA7FB1790BB970/image-size/large?v=v2&px=999 "pnp-modern-search-sharepoint-app-catalog-02-1024x535")

### 2.2 - Deploy the PnP Modern Search Package 

Once your App Catalog is done, or you have one that has been created
earlier, open its URL and then click on "Apps for SharePoint":
![pnp-modern-search-sharepoint-app-catalog-03-1024x553](https://techcommunity.microsoft.com/t5/image/serverpage/image-id/298682iFE847005315A31AC/image-size/large?v=v2&px=999 "pnp-modern-search-sharepoint-app-catalog-03-1024x553")
On this screen, click on Upload, then choose the PnP Modern Search
package file which you downloaded above.

![pnp-modern-search-sharepoint-app-catalog-04-1024x652](https://techcommunity.microsoft.com/t5/image/serverpage/image-id/298683i9F61C7A55D8A9332/image-size/large?v=v2&px=999 "pnp-modern-search-sharepoint-app-catalog-04-1024x652")

When you're asked if you trust PnP Modern Search Web Parts, click the
checkbox if you want to deploy it to all site collections, otherwise
leave it unchecked if you need it on a few selected sites only. Then
click Deploy:
![pnp-modern-search-sharepoint-app-catalog-05](https://techcommunity.microsoft.com/t5/image/serverpage/image-id/298684i8925F9C0A92215B5/image-size/large?v=v2&px=999 "pnp-modern-search-sharepoint-app-catalog-05")
Once done, you should see the PnP Modern Search Web Parts in the App
Catalog:
![pnp-modern-search-sharepoint-app-catalog-06-1024x274](https://techcommunity.microsoft.com/t5/image/serverpage/image-id/298685iC7A61983F9CD5483/image-size/large?v=v2&px=999 "pnp-modern-search-sharepoint-app-catalog-06-1024x274")

## 3 - Enjoy! 

Now, go to any (modern) site on your tenant (in a site collection where
you've deployed PnP Modern Search above), and edit the page. In the web
parts list, search for "PnP", and you'll see the PnP Modern Search Web
Parts there:
![pnp-modern-search-v4-webparts](https://techcommunity.microsoft.com/t5/image/serverpage/image-id/298686iA4A17C62AEA28C58/image-size/large?v=v2&px=999 "pnp-modern-search-v4-webparts")


*This article was originally posted on [Search Explained
Blog](https://searchexplained.com/deploy-pnp-modern-search-web-parts-sharepoint-online/).*