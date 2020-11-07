---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 338e65e4795f3b676a1f88e8a8281a41aee5a0c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836605"
---
# <span data-ttu-id="71529-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="71529-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="71529-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71529-102">SYNOPSIS</span></span>
<span data-ttu-id="71529-103">Fényképgyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="71529-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="71529-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71529-104">SYNTAX</span></span>

### <span data-ttu-id="71529-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71529-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71529-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="71529-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71529-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="71529-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71529-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="71529-108">DESCRIPTION</span></span>
<span data-ttu-id="71529-109">Fényképgyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="71529-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="71529-110">Példák</span><span class="sxs-lookup"><span data-stu-id="71529-110">EXAMPLES</span></span>

### <span data-ttu-id="71529-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="71529-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="71529-112">Fényképgyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="71529-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="71529-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71529-113">PARAMETERS</span></span>

### <span data-ttu-id="71529-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71529-114">-AsJob</span></span>
<span data-ttu-id="71529-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="71529-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71529-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71529-116">-DefaultProfile</span></span>
<span data-ttu-id="71529-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71529-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71529-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="71529-118">-Description</span></span>
<span data-ttu-id="71529-119">A Galéria képdefiníciós erőforrásának leírása.</span><span class="sxs-lookup"><span data-stu-id="71529-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="71529-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="71529-120">-DisallowedDiskType</span></span>
<span data-ttu-id="71529-121">A nem engedélyezett lemez típusa.</span><span class="sxs-lookup"><span data-stu-id="71529-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="71529-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="71529-122">-EndOfLifeDate</span></span>
<span data-ttu-id="71529-123">A gyűjtemény képdefiníciójának utolsó dátuma</span><span class="sxs-lookup"><span data-stu-id="71529-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="71529-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="71529-124">-Eula</span></span>
<span data-ttu-id="71529-125">A Galéria képdefiníciós licencszerződése</span><span class="sxs-lookup"><span data-stu-id="71529-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="71529-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="71529-126">-GalleryName</span></span>
<span data-ttu-id="71529-127">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="71529-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="71529-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71529-128">-InputObject</span></span>
<span data-ttu-id="71529-129">A PS-gyűjtemény képdefiníciós objektuma.</span><span class="sxs-lookup"><span data-stu-id="71529-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="71529-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="71529-130">-MaximumMemory</span></span>
<span data-ttu-id="71529-131">Az ajánlott memória maximális száma</span><span class="sxs-lookup"><span data-stu-id="71529-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="71529-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="71529-132">-MaximumVCPU</span></span>
<span data-ttu-id="71529-133">Az ajánlott CPU-mag maximális száma</span><span class="sxs-lookup"><span data-stu-id="71529-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="71529-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="71529-134">-MinimumMemory</span></span>
<span data-ttu-id="71529-135">Az ajánlott memória minimális száma</span><span class="sxs-lookup"><span data-stu-id="71529-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="71529-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="71529-136">-MinimumVCPU</span></span>
<span data-ttu-id="71529-137">Az ajánlott CPU-mag minimális száma</span><span class="sxs-lookup"><span data-stu-id="71529-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="71529-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71529-138">-Name</span></span>
<span data-ttu-id="71529-139">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="71529-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="71529-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="71529-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="71529-141">Az adatvédelmi nyilatkozat URI-ja.</span><span class="sxs-lookup"><span data-stu-id="71529-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="71529-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="71529-142">-PurchasePlanName</span></span>
<span data-ttu-id="71529-143">A beszerzési csomag azonosítója.</span><span class="sxs-lookup"><span data-stu-id="71529-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="71529-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="71529-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="71529-145">A beszerzési csomag termékazonosítója.</span><span class="sxs-lookup"><span data-stu-id="71529-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="71529-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="71529-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="71529-147">A beszerzési csomag közzétevő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="71529-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="71529-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="71529-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="71529-149">A kibocsátási Megjegyzés URI-ja.</span><span class="sxs-lookup"><span data-stu-id="71529-149">The release note uri.</span></span>

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

### <span data-ttu-id="71529-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71529-150">-ResourceGroupName</span></span>
<span data-ttu-id="71529-151">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71529-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="71529-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71529-152">-ResourceId</span></span>
<span data-ttu-id="71529-153">A kép definíciójának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="71529-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="71529-154">-Címke</span><span class="sxs-lookup"><span data-stu-id="71529-154">-Tag</span></span>
<span data-ttu-id="71529-155">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="71529-155">Resource tags</span></span>

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

### <span data-ttu-id="71529-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71529-156">-Confirm</span></span>
<span data-ttu-id="71529-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71529-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71529-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71529-158">-WhatIf</span></span>
<span data-ttu-id="71529-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71529-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71529-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71529-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71529-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71529-161">CommonParameters</span></span>
<span data-ttu-id="71529-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71529-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71529-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71529-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71529-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71529-164">INPUTS</span></span>

### <span data-ttu-id="71529-165">System. String</span><span class="sxs-lookup"><span data-stu-id="71529-165">System.String</span></span>

### <span data-ttu-id="71529-166">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="71529-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="71529-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="71529-167">System.DateTime</span></span>

### <span data-ttu-id="71529-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="71529-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="71529-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="71529-169">System.Int32</span></span>

### <span data-ttu-id="71529-170">System. string []</span><span class="sxs-lookup"><span data-stu-id="71529-170">System.String[]</span></span>

## <span data-ttu-id="71529-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71529-171">OUTPUTS</span></span>

### <span data-ttu-id="71529-172">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="71529-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="71529-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71529-173">NOTES</span></span>

## <span data-ttu-id="71529-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71529-174">RELATED LINKS</span></span>
