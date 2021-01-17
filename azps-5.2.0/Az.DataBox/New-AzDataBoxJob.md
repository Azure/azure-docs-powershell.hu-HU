---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352890"
---
# <span data-ttu-id="55620-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="55620-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="55620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55620-102">SYNOPSIS</span></span>
<span data-ttu-id="55620-103">Új adatdoboz-feladatot hoz létre a megadott paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="55620-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="55620-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55620-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55620-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55620-105">DESCRIPTION</span></span>
<span data-ttu-id="55620-106">A **New-AzDataBox Job** parancsmag egy új adatdoboz-feladat létrehozásához használható a feladat létrehozásához szükséges részletek megadásával.</span><span class="sxs-lookup"><span data-stu-id="55620-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="55620-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55620-107">EXAMPLES</span></span>

### <span data-ttu-id="55620-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="55620-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="55620-109">A parancsmag az adatdoboz-feladat létrehozásához az összes szükséges és néhány választható paramétert beveszi.</span><span class="sxs-lookup"><span data-stu-id="55620-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="55620-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55620-110">PARAMETERS</span></span>

### <span data-ttu-id="55620-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="55620-111">-AddressType</span></span>
<span data-ttu-id="55620-112">A cím típusa.</span><span class="sxs-lookup"><span data-stu-id="55620-112">Type of Address.</span></span> <span data-ttu-id="55620-113">Rendelkezésre álló értékek: AddressType.None (alapértelmezett), AddressType.Címjegyzék, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="55620-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="55620-114">-City</span><span class="sxs-lookup"><span data-stu-id="55620-114">-City</span></span>
<span data-ttu-id="55620-115">A város neve.</span><span class="sxs-lookup"><span data-stu-id="55620-115">Name of the City.</span></span> <span data-ttu-id="55620-116">Pl. San Francisco</span><span class="sxs-lookup"><span data-stu-id="55620-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="55620-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="55620-117">-CompanyName</span></span>
<span data-ttu-id="55620-118">A vállalat neve</span><span class="sxs-lookup"><span data-stu-id="55620-118">Name of the company</span></span>

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

### <span data-ttu-id="55620-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="55620-119">-ContactName</span></span>
<span data-ttu-id="55620-120">Partner neve</span><span class="sxs-lookup"><span data-stu-id="55620-120">Contact Name</span></span>

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

### <span data-ttu-id="55620-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="55620-121">-CountryCode</span></span>
<span data-ttu-id="55620-122">Országkód.</span><span class="sxs-lookup"><span data-stu-id="55620-122">Country Code.</span></span> <span data-ttu-id="55620-123">Pl. US</span><span class="sxs-lookup"><span data-stu-id="55620-123">Ex: US</span></span>

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

### <span data-ttu-id="55620-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="55620-124">-DataBoxType</span></span>
<span data-ttu-id="55620-125">Az adatkészlet termékváltozattípusa.</span><span class="sxs-lookup"><span data-stu-id="55620-125">Sku type of Databox.</span></span>  <span data-ttu-id="55620-126">Rendelkezésre álló értékek: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="55620-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="55620-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55620-127">-DefaultProfile</span></span>
<span data-ttu-id="55620-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55620-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55620-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="55620-129">-EmailId</span></span>
<span data-ttu-id="55620-130">Meg lehet adni az e-mail-adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="55620-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="55620-131">Legalább egy kötelező</span><span class="sxs-lookup"><span data-stu-id="55620-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="55620-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="55620-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="55620-133">A DataBoxDisk sorrendben kötelező megadni a várt adatokat terabájtban.</span><span class="sxs-lookup"><span data-stu-id="55620-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="55620-134">-Location</span><span class="sxs-lookup"><span data-stu-id="55620-134">-Location</span></span>
<span data-ttu-id="55620-135">Az előfizetés helye</span><span class="sxs-lookup"><span data-stu-id="55620-135">Location of the subscription</span></span>

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

### <span data-ttu-id="55620-136">-Name</span><span class="sxs-lookup"><span data-stu-id="55620-136">-Name</span></span>
<span data-ttu-id="55620-137">A létrehozható adatdoboz-feladat neve</span><span class="sxs-lookup"><span data-stu-id="55620-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="55620-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="55620-138">-PhoneNumber</span></span>
<span data-ttu-id="55620-139">Kapcsolatfelvételi szám</span><span class="sxs-lookup"><span data-stu-id="55620-139">Contact Number</span></span> 

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

### <span data-ttu-id="55620-140">-Irányítószám</span><span class="sxs-lookup"><span data-stu-id="55620-140">-PostalCode</span></span>
<span data-ttu-id="55620-141">Irányítószám</span><span class="sxs-lookup"><span data-stu-id="55620-141">Postal Code</span></span>

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

### <span data-ttu-id="55620-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55620-142">-ResourceGroupName</span></span>
<span data-ttu-id="55620-143">Erőforráscsoport neve, amely alatt létre kell hozatni az adatdoboz-feladatot.</span><span class="sxs-lookup"><span data-stu-id="55620-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="55620-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="55620-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="55620-145">Adja meg az állam vagy tartomány kódját.</span><span class="sxs-lookup"><span data-stu-id="55620-145">Input the state or province code.</span></span> <span data-ttu-id="55620-146">Like CA - California; FL - Florida; NY – New York</span><span class="sxs-lookup"><span data-stu-id="55620-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="55620-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="55620-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="55620-148">Tárfiókok erőforrás-azonosítóinak listája.</span><span class="sxs-lookup"><span data-stu-id="55620-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="55620-149">Legalább egy kötelező.</span><span class="sxs-lookup"><span data-stu-id="55620-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="55620-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="55620-150">-StreetAddress1</span></span>
<span data-ttu-id="55620-151">Utcacím</span><span class="sxs-lookup"><span data-stu-id="55620-151">Street Address</span></span>

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

### <span data-ttu-id="55620-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="55620-152">-StreetAddress2</span></span>
<span data-ttu-id="55620-153">További utcacím</span><span class="sxs-lookup"><span data-stu-id="55620-153">Additional Street Address</span></span>

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

### <span data-ttu-id="55620-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="55620-154">-StreetAddress3</span></span>
<span data-ttu-id="55620-155">További utcacím</span><span class="sxs-lookup"><span data-stu-id="55620-155">Additional Street Address</span></span>

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

### <span data-ttu-id="55620-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55620-156">-Confirm</span></span>
<span data-ttu-id="55620-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="55620-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55620-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55620-158">-WhatIf</span></span>
<span data-ttu-id="55620-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="55620-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55620-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55620-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55620-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55620-161">CommonParameters</span></span>
<span data-ttu-id="55620-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55620-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55620-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55620-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55620-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55620-164">INPUTS</span></span>

### <span data-ttu-id="55620-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="55620-165">System.String[]</span></span>

## <span data-ttu-id="55620-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55620-166">OUTPUTS</span></span>

### <span data-ttu-id="55620-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="55620-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="55620-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55620-168">NOTES</span></span>

## <span data-ttu-id="55620-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55620-169">RELATED LINKS</span></span>
