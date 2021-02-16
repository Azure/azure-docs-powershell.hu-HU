---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163866"
---
# <span data-ttu-id="ecccd-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="ecccd-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="ecccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecccd-102">SYNOPSIS</span></span>
<span data-ttu-id="ecccd-103">Új adatdoboz-feladatot hoz létre a megadott paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="ecccd-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="ecccd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ecccd-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecccd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ecccd-105">DESCRIPTION</span></span>
<span data-ttu-id="ecccd-106">A **New-AzDataBox Job** parancsmag egy új adatdoboz-feladat létrehozásához használható a feladat létrehozásához szükséges részletek megadásával.</span><span class="sxs-lookup"><span data-stu-id="ecccd-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="ecccd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ecccd-107">EXAMPLES</span></span>

### <span data-ttu-id="ecccd-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ecccd-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="ecccd-109">A parancsmag az adatdoboz-feladat létrehozásához az összes szükséges paramétert és néhány opcionális paramétert beveszi.</span><span class="sxs-lookup"><span data-stu-id="ecccd-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="ecccd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecccd-110">PARAMETERS</span></span>

### <span data-ttu-id="ecccd-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="ecccd-111">-AddressType</span></span>
<span data-ttu-id="ecccd-112">A cím típusa.</span><span class="sxs-lookup"><span data-stu-id="ecccd-112">Type of Address.</span></span> <span data-ttu-id="ecccd-113">Rendelkezésre álló értékek: AddressType.None (alapértelmezett), AddressType.Lakás, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="ecccd-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="ecccd-114">-City</span><span class="sxs-lookup"><span data-stu-id="ecccd-114">-City</span></span>
<span data-ttu-id="ecccd-115">A város neve.</span><span class="sxs-lookup"><span data-stu-id="ecccd-115">Name of the City.</span></span> <span data-ttu-id="ecccd-116">Pl. San Francisco</span><span class="sxs-lookup"><span data-stu-id="ecccd-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="ecccd-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="ecccd-117">-CompanyName</span></span>
<span data-ttu-id="ecccd-118">A vállalat neve</span><span class="sxs-lookup"><span data-stu-id="ecccd-118">Name of the company</span></span>

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

### <span data-ttu-id="ecccd-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="ecccd-119">-ContactName</span></span>
<span data-ttu-id="ecccd-120">Partner neve</span><span class="sxs-lookup"><span data-stu-id="ecccd-120">Contact Name</span></span>

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

### <span data-ttu-id="ecccd-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="ecccd-121">-CountryCode</span></span>
<span data-ttu-id="ecccd-122">Országkód.</span><span class="sxs-lookup"><span data-stu-id="ecccd-122">Country Code.</span></span> <span data-ttu-id="ecccd-123">Pl. US</span><span class="sxs-lookup"><span data-stu-id="ecccd-123">Ex: US</span></span>

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

### <span data-ttu-id="ecccd-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="ecccd-124">-DataBoxType</span></span>
<span data-ttu-id="ecccd-125">Az adatkészlet termékváltozattípusa.</span><span class="sxs-lookup"><span data-stu-id="ecccd-125">Sku type of Databox.</span></span>  <span data-ttu-id="ecccd-126">Rendelkezésre álló értékek: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="ecccd-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="ecccd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecccd-127">-DefaultProfile</span></span>
<span data-ttu-id="ecccd-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecccd-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecccd-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="ecccd-129">-EmailId</span></span>
<span data-ttu-id="ecccd-130">Meg lehet adni az e-mail-adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="ecccd-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="ecccd-131">Legalább egy kötelező</span><span class="sxs-lookup"><span data-stu-id="ecccd-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="ecccd-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="ecccd-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="ecccd-133">A DataBoxDisk sorrendben kötelező megadni a várt adatokat terabájtban.</span><span class="sxs-lookup"><span data-stu-id="ecccd-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="ecccd-134">-Location</span><span class="sxs-lookup"><span data-stu-id="ecccd-134">-Location</span></span>
<span data-ttu-id="ecccd-135">Az előfizetés helye</span><span class="sxs-lookup"><span data-stu-id="ecccd-135">Location of the subscription</span></span>

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

### <span data-ttu-id="ecccd-136">-Name</span><span class="sxs-lookup"><span data-stu-id="ecccd-136">-Name</span></span>
<span data-ttu-id="ecccd-137">A létrehozni szükséges adatdoboz-feladat neve</span><span class="sxs-lookup"><span data-stu-id="ecccd-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="ecccd-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="ecccd-138">-PhoneNumber</span></span>
<span data-ttu-id="ecccd-139">Kapcsolatfelvételi szám</span><span class="sxs-lookup"><span data-stu-id="ecccd-139">Contact Number</span></span> 

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

### <span data-ttu-id="ecccd-140">-Irányítószám</span><span class="sxs-lookup"><span data-stu-id="ecccd-140">-PostalCode</span></span>
<span data-ttu-id="ecccd-141">Irányítószám</span><span class="sxs-lookup"><span data-stu-id="ecccd-141">Postal Code</span></span>

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

### <span data-ttu-id="ecccd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecccd-142">-ResourceGroupName</span></span>
<span data-ttu-id="ecccd-143">Erőforráscsoport neve, amely alatt létre kell hozatni az adatdoboz-feladatot.</span><span class="sxs-lookup"><span data-stu-id="ecccd-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="ecccd-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="ecccd-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="ecccd-145">Adja meg az állam vagy tartomány kódját.</span><span class="sxs-lookup"><span data-stu-id="ecccd-145">Input the state or province code.</span></span> <span data-ttu-id="ecccd-146">Like CA - California; FL - Florida; NY – New York</span><span class="sxs-lookup"><span data-stu-id="ecccd-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="ecccd-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ecccd-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="ecccd-148">Tárfiókok erőforrás-azonosítóinak listája.</span><span class="sxs-lookup"><span data-stu-id="ecccd-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="ecccd-149">Legalább egy kötelező.</span><span class="sxs-lookup"><span data-stu-id="ecccd-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="ecccd-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="ecccd-150">-StreetAddress1</span></span>
<span data-ttu-id="ecccd-151">Utcacím</span><span class="sxs-lookup"><span data-stu-id="ecccd-151">Street Address</span></span>

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

### <span data-ttu-id="ecccd-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="ecccd-152">-StreetAddress2</span></span>
<span data-ttu-id="ecccd-153">További utcacím</span><span class="sxs-lookup"><span data-stu-id="ecccd-153">Additional Street Address</span></span>

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

### <span data-ttu-id="ecccd-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="ecccd-154">-StreetAddress3</span></span>
<span data-ttu-id="ecccd-155">További utcacím</span><span class="sxs-lookup"><span data-stu-id="ecccd-155">Additional Street Address</span></span>

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

### <span data-ttu-id="ecccd-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecccd-156">-Confirm</span></span>
<span data-ttu-id="ecccd-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ecccd-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecccd-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecccd-158">-WhatIf</span></span>
<span data-ttu-id="ecccd-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ecccd-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecccd-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ecccd-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecccd-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecccd-161">CommonParameters</span></span>
<span data-ttu-id="ecccd-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecccd-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecccd-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecccd-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecccd-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecccd-164">INPUTS</span></span>

### <span data-ttu-id="ecccd-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ecccd-165">System.String[]</span></span>

## <span data-ttu-id="ecccd-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecccd-166">OUTPUTS</span></span>

### <span data-ttu-id="ecccd-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="ecccd-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="ecccd-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ecccd-168">NOTES</span></span>

## <span data-ttu-id="ecccd-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecccd-169">RELATED LINKS</span></span>
