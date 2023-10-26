# dataverse-docs
User Guides for LibraData UVa Dataverse Repository

**NOTE:** *These pages are no longer used as *guides*, but used to re-direct to the new Libguides for UVA Dataverse.*

Guide links are used in email notifications AND are seen in the application on various pages. 

To override the default "base" value “http://guides.dataverse.org” for the guides URL, UVA has the following setting:

**:GuidesBaseUrl** = http://uvalib.github.io/dataverse-docs

But this setting ONLY overrides the **base** URL, not the entire URL (path), which is hard-coded in the Bundle.properties file.

Here is full Dataverse guide path, using UVA's guide base for the Dataset Management guide:  `http://uvalib.github.io/dataverse-docs/en/current/user/dataset-management.html`

which is composed of **GuidesBaseURL** + en/current/user/**GUIDE_NAME**

The part `en/current/user/` is always added to the base guide URL (I assume because of what is in the Bundle.properties file).

## Re-directing UVA Dataverse Guides to another PATH
To make the guides link go to UVA-specific Dataverse guides, we did the following:

* Created a github repository [dataverse-docs](https://github.com/uvalib/dataverse-docs)
* Added re-direct (html) files in the PATH `en/current/user` for
  * dataset-management.html
  * index.html
  * dataverse-management.html  (UVA did not re-direct this path, since creating sub-collections is only done my Dataverse Admins)
  * account.html
  * find-use-data.html
* Set the **GuidesBaseURL** to the github "pages" site (`http://uvalib.github.io/dataverse-docs`, in UVA's case)

  The re-direct from the github pages to our libguides is done via html coding and not DNS, see the files in the github repo.
  There might be a better way, but this is working for now. Please let me know if there is a better way.

Problems with UVA's way:
* Some of the guide links in the UI point to anchor links, such as: `http://uvalib.github.io/dataverse-docs/en/current/user/dataset-management.html#widgets`
these do not redirect to the actual UVA guide for the specific "anchor".


