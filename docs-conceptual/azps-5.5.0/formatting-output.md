---
title: Azure PowerShell-parancsmag kimenetének formázása
description: Az Azure PowerShell-parancsmagok kimenetének formázása.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 44016cc9546869b05693276293119c21ca02e4b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012690"
---
# <a name="format-azure-powershell-cmdlet-output"></a><span data-ttu-id="8e38b-103">Azure PowerShell-parancsmag kimenetének formázása</span><span class="sxs-lookup"><span data-stu-id="8e38b-103">Format Azure PowerShell cmdlet output</span></span>

<span data-ttu-id="8e38b-104">Alapértelmezés szerint minden Azure PowerShell-parancsmag könnyen olvasható formátumúra alakítja át a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8e38b-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="8e38b-105">A PowerShell segítségével a parancsmagok kimenete konvertálható vagy formázható az alábbi parancsmagok egyikére történő átirányítással:</span><span class="sxs-lookup"><span data-stu-id="8e38b-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="8e38b-106">Formátum</span><span class="sxs-lookup"><span data-stu-id="8e38b-106">Formatting</span></span>      | <span data-ttu-id="8e38b-107">Átalakítás</span><span class="sxs-lookup"><span data-stu-id="8e38b-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="8e38b-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="8e38b-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="8e38b-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="8e38b-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="8e38b-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="8e38b-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="8e38b-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="8e38b-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="8e38b-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="8e38b-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="8e38b-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="8e38b-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="8e38b-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="8e38b-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="8e38b-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="8e38b-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="8e38b-116">Formázás esetén a kimenet megjeleníthető egy PowerShell-terminálon, konvertálással pedig más szkriptek vagy programok által használható adatok állíthatók elő.</span><span class="sxs-lookup"><span data-stu-id="8e38b-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="8e38b-117">Tábla kimeneti formátum</span><span class="sxs-lookup"><span data-stu-id="8e38b-117">Table output format</span></span>

<span data-ttu-id="8e38b-118">Az Azure PowerShell-parancsmagok kimenete alapértelmezés szerint táblázatos formátumú.</span><span class="sxs-lookup"><span data-stu-id="8e38b-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="8e38b-119">Ez a formátum nem jeleníti meg a kért erőforrás összes adatát:</span><span class="sxs-lookup"><span data-stu-id="8e38b-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="8e38b-120">A `Format-Table` által megjelenített adatok mennyiségét a PowerShell-munkamenet ablakának szélessége is korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="8e38b-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="8e38b-121">Ha a kimenetben csak adott tulajdonságokat szerepeltetne, és ezeket rendezni is szeretné, tulajdonságnevek is megadhatók a `Format-Table` argumentumaiként:</span><span class="sxs-lookup"><span data-stu-id="8e38b-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="8e38b-122">Lista kimeneti formátum</span><span class="sxs-lookup"><span data-stu-id="8e38b-122">List output format</span></span>

<span data-ttu-id="8e38b-123">A Lista kimeneti formátum két oszlopot tartalmaz: az első oszlopban a tulajdonságnév, a másodikban annak értéke szerepel.</span><span class="sxs-lookup"><span data-stu-id="8e38b-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="8e38b-124">Összetett objektumok esetében ezek helyett az objektumtípus látható.</span><span class="sxs-lookup"><span data-stu-id="8e38b-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="8e38b-125">Az alábbi kimenetből néhány mező el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8e38b-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="8e38b-126">A `Format-Table` formátumhoz hasonlóan a kimenet tulajdonságnevek megadásával is rendezhető és szűkíthető:</span><span class="sxs-lookup"><span data-stu-id="8e38b-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="8e38b-127">Széles kimeneti formátum</span><span class="sxs-lookup"><span data-stu-id="8e38b-127">Wide output format</span></span>

<span data-ttu-id="8e38b-128">A Széles kimeneti formátum lekérdezésenként egyetlen tulajdonságnevet jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="8e38b-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="8e38b-129">Az, hogy ez melyik tulajdonság legyen, az adott tulajdonság argumentumként való megadásával állítható be.</span><span class="sxs-lookup"><span data-stu-id="8e38b-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="8e38b-130">Egyéni kimeneti formátum</span><span class="sxs-lookup"><span data-stu-id="8e38b-130">Custom output format</span></span>

<span data-ttu-id="8e38b-131">A `Custom-Format` kimenettípus egyéni objektumok formázására szolgál.</span><span class="sxs-lookup"><span data-stu-id="8e38b-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="8e38b-132">Argumentum nélkül ugyanúgy viselkedik, mint a `Format-List`, de egyéni osztályok tulajdonságneveit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="8e38b-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="8e38b-133">Az alábbi kimenetből néhány mező el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8e38b-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="8e38b-134">Argumentumokként tulajdonságneveket megadva a `Custom-Format` egyéni objektumok tulajdonság/érték párjait jeleníti meg értékként:</span><span class="sxs-lookup"><span data-stu-id="8e38b-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="8e38b-135">Az alábbi kimenetből néhány mező el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8e38b-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="8e38b-136">Átalakítás egyéb adatformátumokká</span><span class="sxs-lookup"><span data-stu-id="8e38b-136">Conversion to other data formats</span></span>

<span data-ttu-id="8e38b-137">A `ConvertTo-*` parancsmagcsalád segítségével az Azure PowerShell-parancsmagok által visszaadott eredmények számítógép által olvasható formátumra konvertálhatók.</span><span class="sxs-lookup"><span data-stu-id="8e38b-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="8e38b-138">Ha az Azure PowerShell által visszaadott eredményekből csak egyes tulajdonságokat szeretne lekérni, még az átalakítás végrehajtása előtt használja a `Select-Object` parancsot az adott folyamatban.</span><span class="sxs-lookup"><span data-stu-id="8e38b-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="8e38b-139">Az alábbi példák az egyes átalakítások kimeneteinek különböző fajtáit mutatják be.</span><span class="sxs-lookup"><span data-stu-id="8e38b-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="8e38b-140">Átalakítás CSV formátumba</span><span class="sxs-lookup"><span data-stu-id="8e38b-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="8e38b-141">Átalakítás JSON formátumba</span><span class="sxs-lookup"><span data-stu-id="8e38b-141">Conversion to JSON</span></span>

<span data-ttu-id="8e38b-142">A JSON-kimenet alapértelmezés szerint nem bontja ki az összes tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="8e38b-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="8e38b-143">A tulajdonságok kibontási mélységének módosítása a `-Depth` argumentummal történik.</span><span class="sxs-lookup"><span data-stu-id="8e38b-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="8e38b-144">Az alapértelmezett kibontási mélység a `2`.</span><span class="sxs-lookup"><span data-stu-id="8e38b-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="8e38b-145">Az alábbi kimenetből néhány mező el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8e38b-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="8e38b-146">Átalakítás XML formátumba</span><span class="sxs-lookup"><span data-stu-id="8e38b-146">Conversion to XML</span></span>

<span data-ttu-id="8e38b-147">A `ConvertTo-XML` parancsmag az Azure PowerShell-válaszobjektumot tiszta XML-objektummá konvertálja, amely a többi XML-objektumhoz hasonlóan kezelhető a PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="8e38b-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="8e38b-148">Átalakítás HTML formátumba</span><span class="sxs-lookup"><span data-stu-id="8e38b-148">Conversion to HTML</span></span>

<span data-ttu-id="8e38b-149">Az objektumok HTML formátumba való konvertálásának kimenete HTML-táblázatként lesz megjelenítve.</span><span class="sxs-lookup"><span data-stu-id="8e38b-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="8e38b-150">A HTML formátumú kimenet renderelése attól függ, hogy a böngészője hogyan jeleníti meg a szélességadatokat nem tartalmazó táblázatokat.</span><span class="sxs-lookup"><span data-stu-id="8e38b-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="8e38b-151">Az egyéni osztály objektumok nincsenek kibontva.</span><span class="sxs-lookup"><span data-stu-id="8e38b-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```
