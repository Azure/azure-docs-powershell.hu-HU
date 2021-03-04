---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 2c78f8b40621ba58b84169f2bd9022399fce80b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942977"
---
# <span data-ttu-id="932e6-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="932e6-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="932e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="932e6-102">SYNOPSIS</span></span>
<span data-ttu-id="932e6-103">Új adatdoboz-feladatot hoz létre a megadott paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="932e6-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="932e6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="932e6-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="932e6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="932e6-105">DESCRIPTION</span></span>
<span data-ttu-id="932e6-106">A **New-AzDataBox Job** parancsmag egy új adatdoboz-feladat létrehozásához használható a feladat létrehozásához szükséges részletek megadásával.</span><span class="sxs-lookup"><span data-stu-id="932e6-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="932e6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="932e6-107">EXAMPLES</span></span>

### <span data-ttu-id="932e6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="932e6-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="932e6-109">A parancsmag az adatdoboz-feladat létrehozásához az összes szükséges és néhány választható paramétert beveszi.</span><span class="sxs-lookup"><span data-stu-id="932e6-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="932e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="932e6-110">PARAMETERS</span></span>

### <span data-ttu-id="932e6-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="932e6-111">-AddressType</span></span>
<span data-ttu-id="932e6-112">A cím típusa.</span><span class="sxs-lookup"><span data-stu-id="932e6-112">Type of Address.</span></span> <span data-ttu-id="932e6-113">Rendelkezésre álló értékek: AddressType.None (alapértelmezett), AddressType.Címjegyzék, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="932e6-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-114">-City</span><span class="sxs-lookup"><span data-stu-id="932e6-114">-City</span></span>
<span data-ttu-id="932e6-115">A város neve.</span><span class="sxs-lookup"><span data-stu-id="932e6-115">Name of the City.</span></span> <span data-ttu-id="932e6-116">Pl. San Francisco</span><span class="sxs-lookup"><span data-stu-id="932e6-116">Ex : San Francisco</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="932e6-117">-CompanyName</span></span>
<span data-ttu-id="932e6-118">A vállalat neve</span><span class="sxs-lookup"><span data-stu-id="932e6-118">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="932e6-119">-ContactName</span></span>
<span data-ttu-id="932e6-120">Partner neve</span><span class="sxs-lookup"><span data-stu-id="932e6-120">Contact Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="932e6-121">-CountryCode</span></span>
<span data-ttu-id="932e6-122">Országkód.</span><span class="sxs-lookup"><span data-stu-id="932e6-122">Country Code.</span></span> <span data-ttu-id="932e6-123">Pl. US</span><span class="sxs-lookup"><span data-stu-id="932e6-123">Ex: US</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="932e6-124">-DataBoxType</span></span>
<span data-ttu-id="932e6-125">Az adatkészlet termékváltozattípusa.</span><span class="sxs-lookup"><span data-stu-id="932e6-125">Sku type of Databox.</span></span>  <span data-ttu-id="932e6-126">Rendelkezésre álló értékek: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="932e6-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="932e6-127">-DefaultProfile</span></span>
<span data-ttu-id="932e6-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="932e6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="932e6-129">-EmailId</span></span>
<span data-ttu-id="932e6-130">Meg lehet adni az e-mail-adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="932e6-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="932e6-131">Legalább egy kötelező</span><span class="sxs-lookup"><span data-stu-id="932e6-131">Atleast one is mandatory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="932e6-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="932e6-133">A DataBoxDisk sorrendben kötelező megadni a várt adatokat terabájtban.</span><span class="sxs-lookup"><span data-stu-id="932e6-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-134">-Location</span><span class="sxs-lookup"><span data-stu-id="932e6-134">-Location</span></span>
<span data-ttu-id="932e6-135">Az előfizetés helye</span><span class="sxs-lookup"><span data-stu-id="932e6-135">Location of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-136">-Name</span><span class="sxs-lookup"><span data-stu-id="932e6-136">-Name</span></span>
<span data-ttu-id="932e6-137">A létrehozható adatdoboz-feladat neve</span><span class="sxs-lookup"><span data-stu-id="932e6-137">Name of the databox job to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="932e6-138">-PhoneNumber</span></span>
<span data-ttu-id="932e6-139">Kapcsolatfelvételi szám</span><span class="sxs-lookup"><span data-stu-id="932e6-139">Contact Number</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-140">-Irányítószám</span><span class="sxs-lookup"><span data-stu-id="932e6-140">-PostalCode</span></span>
<span data-ttu-id="932e6-141">Irányítószám</span><span class="sxs-lookup"><span data-stu-id="932e6-141">Postal Code</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="932e6-142">-ResourceGroupName</span></span>
<span data-ttu-id="932e6-143">Erőforráscsoport neve, amely alatt létre kell hozatni az adatdoboz-feladatot.</span><span class="sxs-lookup"><span data-stu-id="932e6-143">Resource Group Name under which the databox job has to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="932e6-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="932e6-145">Adja meg az állam vagy tartomány kódját.</span><span class="sxs-lookup"><span data-stu-id="932e6-145">Input the state or province code.</span></span> <span data-ttu-id="932e6-146">Like CA - California; FL - Florida; NY – New York</span><span class="sxs-lookup"><span data-stu-id="932e6-146">Like CA - California; FL - Florida; NY - New York</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="932e6-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="932e6-148">Tárfiókok erőforrás-azonosítóinak listája.</span><span class="sxs-lookup"><span data-stu-id="932e6-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="932e6-149">Legalább egy kötelező.</span><span class="sxs-lookup"><span data-stu-id="932e6-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="932e6-150">-StreetAddress1</span></span>
<span data-ttu-id="932e6-151">Utcacím</span><span class="sxs-lookup"><span data-stu-id="932e6-151">Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="932e6-152">-StreetAddress2</span></span>
<span data-ttu-id="932e6-153">További utcacím</span><span class="sxs-lookup"><span data-stu-id="932e6-153">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="932e6-154">-StreetAddress3</span></span>
<span data-ttu-id="932e6-155">További utcacím</span><span class="sxs-lookup"><span data-stu-id="932e6-155">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="932e6-156">-Confirm</span></span>
<span data-ttu-id="932e6-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="932e6-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="932e6-158">-WhatIf</span></span>
<span data-ttu-id="932e6-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="932e6-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="932e6-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="932e6-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932e6-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="932e6-161">CommonParameters</span></span>
<span data-ttu-id="932e6-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="932e6-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="932e6-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="932e6-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="932e6-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="932e6-164">INPUTS</span></span>

### <span data-ttu-id="932e6-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="932e6-165">System.String[]</span></span>

## <span data-ttu-id="932e6-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="932e6-166">OUTPUTS</span></span>

### <span data-ttu-id="932e6-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="932e6-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="932e6-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="932e6-168">NOTES</span></span>

## <span data-ttu-id="932e6-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="932e6-169">RELATED LINKS</span></span>
