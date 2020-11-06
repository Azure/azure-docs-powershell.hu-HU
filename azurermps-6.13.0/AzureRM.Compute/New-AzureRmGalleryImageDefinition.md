---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 8dcfe4adedd7da375e888dade108125d7899d7d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504495"
---
# <span data-ttu-id="bf354-101">New-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="bf354-101">New-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="bf354-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf354-102">SYNOPSIS</span></span>
<span data-ttu-id="bf354-103">Gyűjtemény képének definíciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf354-103">Create a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf354-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf354-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Location] <String> -Publisher <String> -Offer <String> -Sku <String>
 -OsState <OperatingSystemStateTypes> -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf354-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf354-105">DESCRIPTION</span></span>
<span data-ttu-id="bf354-106">Gyűjtemény képének definíciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf354-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="bf354-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf354-107">EXAMPLES</span></span>

### <span data-ttu-id="bf354-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bf354-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="bf354-109">Gyűjtemény képének definíciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf354-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="bf354-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf354-110">PARAMETERS</span></span>

### <span data-ttu-id="bf354-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf354-111">-AsJob</span></span>
<span data-ttu-id="bf354-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bf354-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf354-113">-DefaultProfile</span></span>
<span data-ttu-id="bf354-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf354-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="bf354-115">-Description</span></span>
<span data-ttu-id="bf354-116">A Galéria képdefiníciós erőforrásának leírása.</span><span class="sxs-lookup"><span data-stu-id="bf354-116">The description of the gallery image Definition resource.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="bf354-117">-DisallowedDiskType</span></span>
<span data-ttu-id="bf354-118">A nem engedélyezett lemez típusa.</span><span class="sxs-lookup"><span data-stu-id="bf354-118">The disallowed disk types.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="bf354-119">-EndOfLifeDate</span></span>
<span data-ttu-id="bf354-120">A gyűjtemény képdefiníciójának utolsó dátuma</span><span class="sxs-lookup"><span data-stu-id="bf354-120">The end of life date of the gallery Image Definition</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="bf354-121">-Eula</span></span>
<span data-ttu-id="bf354-122">A Galéria képdefiníciós licencszerződése</span><span class="sxs-lookup"><span data-stu-id="bf354-122">The Eula agreement for the gallery Image Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="bf354-123">-GalleryName</span></span>
<span data-ttu-id="bf354-124">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="bf354-124">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="bf354-125">-Location</span></span>
<span data-ttu-id="bf354-126">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="bf354-126">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="bf354-127">-MaximumMemory</span></span>
<span data-ttu-id="bf354-128">Az ajánlott memória maximális száma</span><span class="sxs-lookup"><span data-stu-id="bf354-128">The maximum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="bf354-129">-MaximumVCPU</span></span>
<span data-ttu-id="bf354-130">Az ajánlott CPU-mag maximális száma</span><span class="sxs-lookup"><span data-stu-id="bf354-130">The maximum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="bf354-131">-MinimumMemory</span></span>
<span data-ttu-id="bf354-132">Az ajánlott memória minimális száma</span><span class="sxs-lookup"><span data-stu-id="bf354-132">The minimum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="bf354-133">-MinimumVCPU</span></span>
<span data-ttu-id="bf354-134">Az ajánlott CPU-mag minimális száma</span><span class="sxs-lookup"><span data-stu-id="bf354-134">The minimum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf354-135">-Name</span></span>
<span data-ttu-id="bf354-136">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="bf354-136">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-137">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="bf354-137">-Offer</span></span>
<span data-ttu-id="bf354-138">A Képtár képdefiníciós ajánlatának neve.</span><span class="sxs-lookup"><span data-stu-id="bf354-138">The name of the gallery Image Definition offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="bf354-139">-OsState</span></span>
<span data-ttu-id="bf354-140">Az operációs rendszer állapota</span><span class="sxs-lookup"><span data-stu-id="bf354-140">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="bf354-141">-OsType</span></span>
<span data-ttu-id="bf354-142">Az operációs rendszer típusa</span><span class="sxs-lookup"><span data-stu-id="bf354-142">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="bf354-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="bf354-144">Az adatvédelmi nyilatkozat URI-ja.</span><span class="sxs-lookup"><span data-stu-id="bf354-144">The privacy statement uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="bf354-145">-Publisher</span></span>
<span data-ttu-id="bf354-146">A Képtár képdefiníciójának közzétevője.</span><span class="sxs-lookup"><span data-stu-id="bf354-146">The name of the gallery Image Definition publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="bf354-147">-PurchasePlanName</span></span>
<span data-ttu-id="bf354-148">A beszerzési csomag azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bf354-148">The ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="bf354-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="bf354-150">A beszerzési csomag termékazonosítója.</span><span class="sxs-lookup"><span data-stu-id="bf354-150">The product ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="bf354-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="bf354-152">A beszerzési csomag közzétevő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bf354-152">The publisher ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="bf354-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="bf354-154">A kibocsátási Megjegyzés URI-ja.</span><span class="sxs-lookup"><span data-stu-id="bf354-154">The release note uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf354-155">-ResourceGroupName</span></span>
<span data-ttu-id="bf354-156">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bf354-156">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="bf354-157">-Sku</span></span>
<span data-ttu-id="bf354-158">A gyűjtemény képdefiníciós SKU neve.</span><span class="sxs-lookup"><span data-stu-id="bf354-158">The name of the gallery Image Definition SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-159">-Címke</span><span class="sxs-lookup"><span data-stu-id="bf354-159">-Tag</span></span>
<span data-ttu-id="bf354-160">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="bf354-160">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf354-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf354-161">-Confirm</span></span>
<span data-ttu-id="bf354-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf354-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf354-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf354-163">-WhatIf</span></span>
<span data-ttu-id="bf354-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf354-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf354-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf354-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf354-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf354-166">CommonParameters</span></span>
<span data-ttu-id="bf354-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf354-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf354-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf354-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf354-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf354-169">INPUTS</span></span>

### <span data-ttu-id="bf354-170">System. String</span><span class="sxs-lookup"><span data-stu-id="bf354-170">System.String</span></span>

### <span data-ttu-id="bf354-171">Microsoft. Azure. Management. kiszámítás. models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="bf354-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="bf354-172">Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="bf354-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="bf354-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bf354-173">System.DateTime</span></span>

### <span data-ttu-id="bf354-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bf354-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bf354-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bf354-175">System.Int32</span></span>

### <span data-ttu-id="bf354-176">System. string []</span><span class="sxs-lookup"><span data-stu-id="bf354-176">System.String[]</span></span>

## <span data-ttu-id="bf354-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf354-177">OUTPUTS</span></span>

### <span data-ttu-id="bf354-178">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="bf354-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="bf354-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf354-179">NOTES</span></span>

## <span data-ttu-id="bf354-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf354-180">RELATED LINKS</span></span>