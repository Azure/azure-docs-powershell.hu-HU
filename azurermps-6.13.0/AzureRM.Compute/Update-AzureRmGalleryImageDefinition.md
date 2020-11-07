---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 445029c41e27cce14bff2ac14d826adf28f3c9ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671981"
---
# <span data-ttu-id="f7749-101">Update-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="f7749-101">Update-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="f7749-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7749-102">SYNOPSIS</span></span>
<span data-ttu-id="f7749-103">Fényképgyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="f7749-103">Update a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7749-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7749-104">SYNTAX</span></span>

### <span data-ttu-id="f7749-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7749-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7749-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f7749-106">ResourceIdParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7749-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f7749-107">ObjectParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7749-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7749-108">DESCRIPTION</span></span>
<span data-ttu-id="f7749-109">Fényképgyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="f7749-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="f7749-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f7749-110">EXAMPLES</span></span>

### <span data-ttu-id="f7749-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f7749-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="f7749-112">Fényképgyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="f7749-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="f7749-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7749-113">PARAMETERS</span></span>

### <span data-ttu-id="f7749-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7749-114">-AsJob</span></span>
<span data-ttu-id="f7749-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f7749-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7749-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7749-116">-DefaultProfile</span></span>
<span data-ttu-id="f7749-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7749-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7749-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f7749-118">-Description</span></span>
<span data-ttu-id="f7749-119">A Galéria képdefiníciós erőforrásának leírása.</span><span class="sxs-lookup"><span data-stu-id="f7749-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="f7749-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="f7749-120">-DisallowedDiskType</span></span>
<span data-ttu-id="f7749-121">A nem engedélyezett lemez típusa.</span><span class="sxs-lookup"><span data-stu-id="f7749-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="f7749-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="f7749-122">-EndOfLifeDate</span></span>
<span data-ttu-id="f7749-123">A gyűjtemény képdefiníciójának utolsó dátuma</span><span class="sxs-lookup"><span data-stu-id="f7749-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="f7749-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="f7749-124">-Eula</span></span>
<span data-ttu-id="f7749-125">A Galéria képdefiníciós licencszerződése</span><span class="sxs-lookup"><span data-stu-id="f7749-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="f7749-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="f7749-126">-GalleryName</span></span>
<span data-ttu-id="f7749-127">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="f7749-127">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7749-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7749-128">-InputObject</span></span>
<span data-ttu-id="f7749-129">A PS-gyűjtemény képdefiníciós objektuma.</span><span class="sxs-lookup"><span data-stu-id="f7749-129">The PS Gallery Image Definition Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7749-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="f7749-130">-MaximumMemory</span></span>
<span data-ttu-id="f7749-131">Az ajánlott memória maximális száma</span><span class="sxs-lookup"><span data-stu-id="f7749-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="f7749-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="f7749-132">-MaximumVCPU</span></span>
<span data-ttu-id="f7749-133">Az ajánlott CPU-mag maximális száma</span><span class="sxs-lookup"><span data-stu-id="f7749-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="f7749-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="f7749-134">-MinimumMemory</span></span>
<span data-ttu-id="f7749-135">Az ajánlott memória minimális száma</span><span class="sxs-lookup"><span data-stu-id="f7749-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="f7749-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="f7749-136">-MinimumVCPU</span></span>
<span data-ttu-id="f7749-137">Az ajánlott CPU-mag minimális száma</span><span class="sxs-lookup"><span data-stu-id="f7749-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="f7749-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7749-138">-Name</span></span>
<span data-ttu-id="f7749-139">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="f7749-139">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7749-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="f7749-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="f7749-141">Az adatvédelmi nyilatkozat URI-ja.</span><span class="sxs-lookup"><span data-stu-id="f7749-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="f7749-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="f7749-142">-PurchasePlanName</span></span>
<span data-ttu-id="f7749-143">A beszerzési csomag azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f7749-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="f7749-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="f7749-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="f7749-145">A beszerzési csomag termékazonosítója.</span><span class="sxs-lookup"><span data-stu-id="f7749-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="f7749-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="f7749-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="f7749-147">A beszerzési csomag közzétevő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f7749-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="f7749-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="f7749-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="f7749-149">A kibocsátási Megjegyzés URI-ja.</span><span class="sxs-lookup"><span data-stu-id="f7749-149">The release note uri.</span></span>

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

### <span data-ttu-id="f7749-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7749-150">-ResourceGroupName</span></span>
<span data-ttu-id="f7749-151">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7749-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7749-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7749-152">-ResourceId</span></span>
<span data-ttu-id="f7749-153">A kép definíciójának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f7749-153">The resource ID for the image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7749-154">-Címke</span><span class="sxs-lookup"><span data-stu-id="f7749-154">-Tag</span></span>
<span data-ttu-id="f7749-155">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="f7749-155">Resource tags</span></span>

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

### <span data-ttu-id="f7749-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7749-156">-Confirm</span></span>
<span data-ttu-id="f7749-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7749-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7749-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7749-158">-WhatIf</span></span>
<span data-ttu-id="f7749-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7749-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7749-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7749-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7749-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7749-161">CommonParameters</span></span>
<span data-ttu-id="f7749-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7749-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7749-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7749-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7749-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7749-164">INPUTS</span></span>

### <span data-ttu-id="f7749-165">System. String</span><span class="sxs-lookup"><span data-stu-id="f7749-165">System.String</span></span>

### <span data-ttu-id="f7749-166">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="f7749-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="f7749-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="f7749-167">System.DateTime</span></span>

### <span data-ttu-id="f7749-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f7749-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f7749-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f7749-169">System.Int32</span></span>

### <span data-ttu-id="f7749-170">System. string []</span><span class="sxs-lookup"><span data-stu-id="f7749-170">System.String[]</span></span>

## <span data-ttu-id="f7749-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7749-171">OUTPUTS</span></span>

### <span data-ttu-id="f7749-172">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="f7749-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="f7749-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7749-173">NOTES</span></span>

## <span data-ttu-id="f7749-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7749-174">RELATED LINKS</span></span>
