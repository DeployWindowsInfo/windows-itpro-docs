---
title: Planning for Migrating from a Previous Version of App-V (Windows 10)
description: Planning for Migrating from a Previous Version of App-V
author: MaggiePucciEvans
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
---


# Planning for Migrating from a Previous Version of App-V


Use the following information to plan how to migrate to Microsoft Application Virtualization (App-V) from previous versions of App-V.

## Migration requirements


Before you start any upgrades, review the following requirements:

-   If you are upgrading from a version earlier than 4.6 SP2, upgrade to version 4.6 SP2 or version 4.6 SP3 first before upgrading to App-V or later. In this scenario, upgrade the App-V clients first, and then upgrade the server components.

-   App-V supports only packages that are created using App-V 5.0 or App-V, or packages that have been converted to the **.appv** format.

-   If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V](appv-about-appv.md#bkmk-migrate-to-51) for instructions.

## Running the App-V client concurrently with App-V 4.6 SP2 or later


You can run the App-V client concurrently on the same computer with the App-V 4.6 SP2 client or App-V 4.6 SP3 client.

When you run coexisting App-V clients, you can:

-   Convert an App-V 4.6 SP2 or 4.6 SP3 package to the App-V format and publish both packages, when you have both clients running.

-   Define the migration policy for the converted package, which allows the converted App-V package to assume the file type associations and shortcuts from the App-V 4.6 SP2 package.

### Supported coexistence scenarios

The following table shows the supported App-V coexistence scenarios. We recommend that you install the latest available updates of a given release when you are running coexisting clients.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V 4.6.x client type</th>
<th align="left">App-V client type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4.6 SP2</p></td>
<td align="left"><p>App-V</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4.6 SP2 RDS</p></td>
<td align="left"><p>App-V RDS</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p>App-V</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4.6 SP3 RDS</p></td>
<td align="left"><p>App-V RDS</p></td>
</tr>
</tbody>
</table>

 

### Requirements for running coexisting clients

To run coexisting clients, you must:

-   Install the App-V 4.6 SP2 or App-V 4.6 SP3 client before you install the App-V client.

-   Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node. To deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](http://technet.microsoft.com/library/dn659707.aspx).

**Note**  
App-V packages can run side by side with App-V 4.X packages if you have coexisting installations of App-V and 4.X. However, App-V packages cannot interact with App-V 4.X packages in the same virtual environment.

 

### Client downloads and documentation

The following table provides links to the App-V 4.6.x client downloads and to the TechNet documentation about the releases. The downloads include the App-V “regular” and RDS clients. The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V version</th>
<th align="left">Link to download the client</th>
<th align="left">Link to TechNet documentation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4.6 SP2</p></td>
<td align="left"><p>[Microsoft Application Virtualization 4.6 Service Pack 2](http://www.microsoft.com/download/details.aspx?id=35513)</p></td>
<td align="left"><p>[About Microsoft Application Virtualization 4.6 SP2](http://technet.microsoft.com/library/jj680847.aspx)</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p>[Microsoft Application Virtualization 4.6 Service Pack 3](http://www.microsoft.com/download/details.aspx?id=41187)</p></td>
<td align="left"><p>[About Microsoft Application Virtualization 4.6 SP3](http://technet.microsoft.com/library/dn511019.aspx)</p></td>
</tr>
</tbody>
</table>

 

For more information about how to configure App-V client coexistence, see:

-   [App-V 5.0 Coexistence and Migration](http://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a>Converting “previous-version” packages using the package converter


Before migrating a package, created using App- 4.6 SP2 or earlier, to App-V, review the following requirements:

-   You must convert the package to the **.appv** file format.

-   The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later. To use the package converter on a package that was created using a previous version, you must use an App-V 4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.

For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](appv-convert-a-package-created-in-a-previous-version-of-appv.md). After you convert the file, you can deploy it to target computers that run the App-V client.

## Have a suggestion for App-V?


Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). For App-V issues, use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/en-US/home?forum=mdopappv).

## Related topics


[Planning to Deploy App-V](appv-planning-to-deploy-appv.md)

 

 





