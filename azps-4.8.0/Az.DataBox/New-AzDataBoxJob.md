---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184595"
---
# <span data-ttu-id="a46ae-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="a46ae-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="a46ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a46ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a46ae-103">Új databox-feladat létrehozása a megadott paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="a46ae-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="a46ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a46ae-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a46ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a46ae-105">DESCRIPTION</span></span>
<span data-ttu-id="a46ae-106">A **New-AzDataBoxJob** parancsmag segítségével új databox-feladatot hozhat létre a feladat létrehozásához szükséges adatok megadásával.</span><span class="sxs-lookup"><span data-stu-id="a46ae-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="a46ae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a46ae-107">EXAMPLES</span></span>

### <span data-ttu-id="a46ae-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a46ae-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="a46ae-109">A parancsmag az összes szükséges paramétert és néhány választható paramétert elvégzi a databox-feladat létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="a46ae-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="a46ae-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a46ae-110">PARAMETERS</span></span>

### <span data-ttu-id="a46ae-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="a46ae-111">-AddressType</span></span>
<span data-ttu-id="a46ae-112">A cím típusa.</span><span class="sxs-lookup"><span data-stu-id="a46ae-112">Type of Address.</span></span> <span data-ttu-id="a46ae-113">Elérhető értékek: AddressType. nincs (alapértelmezett), AddressType. lakó, AddressType. Commercial</span><span class="sxs-lookup"><span data-stu-id="a46ae-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="a46ae-114">-Város</span><span class="sxs-lookup"><span data-stu-id="a46ae-114">-City</span></span>
<span data-ttu-id="a46ae-115">A város neve</span><span class="sxs-lookup"><span data-stu-id="a46ae-115">Name of the City.</span></span> <span data-ttu-id="a46ae-116">Ex: San Francisco</span><span class="sxs-lookup"><span data-stu-id="a46ae-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="a46ae-117">-Vállalatnév</span><span class="sxs-lookup"><span data-stu-id="a46ae-117">-CompanyName</span></span>
<span data-ttu-id="a46ae-118">A cég neve</span><span class="sxs-lookup"><span data-stu-id="a46ae-118">Name of the company</span></span>

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

### <span data-ttu-id="a46ae-119">-KapcsolattartóNeve</span><span class="sxs-lookup"><span data-stu-id="a46ae-119">-ContactName</span></span>
<span data-ttu-id="a46ae-120">A partnerek neve</span><span class="sxs-lookup"><span data-stu-id="a46ae-120">Contact Name</span></span>

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

### <span data-ttu-id="a46ae-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="a46ae-121">-CountryCode</span></span>
<span data-ttu-id="a46ae-122">Ország kódja.</span><span class="sxs-lookup"><span data-stu-id="a46ae-122">Country Code.</span></span> <span data-ttu-id="a46ae-123">Ex: US</span><span class="sxs-lookup"><span data-stu-id="a46ae-123">Ex: US</span></span>

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

### <span data-ttu-id="a46ae-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="a46ae-124">-DataBoxType</span></span>
<span data-ttu-id="a46ae-125">A Databox SKU típusa.</span><span class="sxs-lookup"><span data-stu-id="a46ae-125">Sku type of Databox.</span></span>  <span data-ttu-id="a46ae-126">Elérhető értékek: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="a46ae-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="a46ae-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a46ae-127">-DefaultProfile</span></span>
<span data-ttu-id="a46ae-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a46ae-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a46ae-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="a46ae-129">-EmailId</span></span>
<span data-ttu-id="a46ae-130">Megadhatja a EmailIds.</span><span class="sxs-lookup"><span data-stu-id="a46ae-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="a46ae-131">A atleast egy kötelező</span><span class="sxs-lookup"><span data-stu-id="a46ae-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="a46ae-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="a46ae-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="a46ae-133">A DataBoxDisk megadásához a várható adatértékek terabájtban való megadása kötelező.</span><span class="sxs-lookup"><span data-stu-id="a46ae-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="a46ae-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="a46ae-134">-Location</span></span>
<span data-ttu-id="a46ae-135">Az előfizetés helye</span><span class="sxs-lookup"><span data-stu-id="a46ae-135">Location of the subscription</span></span>

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

### <span data-ttu-id="a46ae-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a46ae-136">-Name</span></span>
<span data-ttu-id="a46ae-137">Létrehozandó databox-feladat neve</span><span class="sxs-lookup"><span data-stu-id="a46ae-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="a46ae-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="a46ae-138">-PhoneNumber</span></span>
<span data-ttu-id="a46ae-139">Telefonszám</span><span class="sxs-lookup"><span data-stu-id="a46ae-139">Contact Number</span></span> 

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

### <span data-ttu-id="a46ae-140">-Irányítószám</span><span class="sxs-lookup"><span data-stu-id="a46ae-140">-PostalCode</span></span>
<span data-ttu-id="a46ae-141">Postai irányítószám</span><span class="sxs-lookup"><span data-stu-id="a46ae-141">Postal Code</span></span>

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

### <span data-ttu-id="a46ae-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a46ae-142">-ResourceGroupName</span></span>
<span data-ttu-id="a46ae-143">Az erőforráscsoport neve, amelynek a databox-feladatot létre kell tennie.</span><span class="sxs-lookup"><span data-stu-id="a46ae-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="a46ae-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="a46ae-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="a46ae-145">Adja meg az állam-vagy tartományi kódot.</span><span class="sxs-lookup"><span data-stu-id="a46ae-145">Input the state or province code.</span></span> <span data-ttu-id="a46ae-146">Like CA-California; FL-Florida; New York</span><span class="sxs-lookup"><span data-stu-id="a46ae-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="a46ae-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a46ae-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="a46ae-148">A raktározási fiókok erőforrás-azonosítóinak listája.</span><span class="sxs-lookup"><span data-stu-id="a46ae-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="a46ae-149">A atleast egy kötelező.</span><span class="sxs-lookup"><span data-stu-id="a46ae-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="a46ae-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="a46ae-150">-StreetAddress1</span></span>
<span data-ttu-id="a46ae-151">Utca címe</span><span class="sxs-lookup"><span data-stu-id="a46ae-151">Street Address</span></span>

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

### <span data-ttu-id="a46ae-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="a46ae-152">-StreetAddress2</span></span>
<span data-ttu-id="a46ae-153">További utcai cím</span><span class="sxs-lookup"><span data-stu-id="a46ae-153">Additional Street Address</span></span>

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

### <span data-ttu-id="a46ae-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="a46ae-154">-StreetAddress3</span></span>
<span data-ttu-id="a46ae-155">További utcai cím</span><span class="sxs-lookup"><span data-stu-id="a46ae-155">Additional Street Address</span></span>

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

### <span data-ttu-id="a46ae-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a46ae-156">-Confirm</span></span>
<span data-ttu-id="a46ae-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a46ae-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a46ae-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a46ae-158">-WhatIf</span></span>
<span data-ttu-id="a46ae-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a46ae-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a46ae-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a46ae-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a46ae-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46ae-161">CommonParameters</span></span>
<span data-ttu-id="a46ae-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a46ae-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46ae-163">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a46ae-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46ae-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a46ae-164">INPUTS</span></span>

### <span data-ttu-id="a46ae-165">System. string []</span><span class="sxs-lookup"><span data-stu-id="a46ae-165">System.String[]</span></span>

## <span data-ttu-id="a46ae-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a46ae-166">OUTPUTS</span></span>

### <span data-ttu-id="a46ae-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="a46ae-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="a46ae-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a46ae-168">NOTES</span></span>

## <span data-ttu-id="a46ae-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a46ae-169">RELATED LINKS</span></span>
