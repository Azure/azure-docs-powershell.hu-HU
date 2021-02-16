---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162210"
---
# <span data-ttu-id="e6890-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="e6890-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="e6890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6890-102">SYNOPSIS</span></span>
<span data-ttu-id="e6890-103">Gyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="e6890-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="e6890-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6890-104">SYNTAX</span></span>

### <span data-ttu-id="e6890-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6890-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6890-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e6890-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6890-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e6890-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6890-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6890-108">DESCRIPTION</span></span>
<span data-ttu-id="e6890-109">Gyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="e6890-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="e6890-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6890-110">EXAMPLES</span></span>

### <span data-ttu-id="e6890-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e6890-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="e6890-112">Gyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="e6890-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="e6890-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6890-113">PARAMETERS</span></span>

### <span data-ttu-id="e6890-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6890-114">-AsJob</span></span>
<span data-ttu-id="e6890-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e6890-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6890-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6890-116">-DefaultProfile</span></span>
<span data-ttu-id="e6890-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6890-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6890-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e6890-118">-Description</span></span>
<span data-ttu-id="e6890-119">A gyűjtemény képdefiníciós erőforrásának leírása.</span><span class="sxs-lookup"><span data-stu-id="e6890-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="e6890-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="e6890-120">-DisallowedDiskType</span></span>
<span data-ttu-id="e6890-121">A nem engedélyezett lemeztípusok.</span><span class="sxs-lookup"><span data-stu-id="e6890-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="e6890-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="e6890-122">-EndOfLifeDate</span></span>
<span data-ttu-id="e6890-123">A gyűjtemény Képdefiníció életciklusának vége</span><span class="sxs-lookup"><span data-stu-id="e6890-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="e6890-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="e6890-124">-Eula</span></span>
<span data-ttu-id="e6890-125">A képdefiníció gyűjteményre vonatkozó Eula-szerződés.</span><span class="sxs-lookup"><span data-stu-id="e6890-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="e6890-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="e6890-126">-GalleryName</span></span>
<span data-ttu-id="e6890-127">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="e6890-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="e6890-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6890-128">-InputObject</span></span>
<span data-ttu-id="e6890-129">A PS-gyűjtemény képdefiníciós objektuma.</span><span class="sxs-lookup"><span data-stu-id="e6890-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="e6890-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="e6890-130">-MaximumMemory</span></span>
<span data-ttu-id="e6890-131">Az ajánlott memória maximális mérete</span><span class="sxs-lookup"><span data-stu-id="e6890-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="e6890-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="e6890-132">-MaximumVCPU</span></span>
<span data-ttu-id="e6890-133">Az ajánlott processzormag maximális mérete</span><span class="sxs-lookup"><span data-stu-id="e6890-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="e6890-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="e6890-134">-MinimumMemory</span></span>
<span data-ttu-id="e6890-135">Az ajánlott memória minimális</span><span class="sxs-lookup"><span data-stu-id="e6890-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="e6890-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="e6890-136">-MinimumVCPU</span></span>
<span data-ttu-id="e6890-137">Az ajánlott processzormag minimuma</span><span class="sxs-lookup"><span data-stu-id="e6890-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="e6890-138">-Name</span><span class="sxs-lookup"><span data-stu-id="e6890-138">-Name</span></span>
<span data-ttu-id="e6890-139">A gyűjtemény képdefiníciójának neve.</span><span class="sxs-lookup"><span data-stu-id="e6890-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="e6890-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="e6890-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="e6890-141">Az adatvédelmi nyilatkozat uri.</span><span class="sxs-lookup"><span data-stu-id="e6890-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="e6890-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="e6890-142">-PurchasePlanName</span></span>
<span data-ttu-id="e6890-143">A vásárlási csomag azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e6890-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="e6890-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="e6890-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="e6890-145">A vásárlási csomag termékazonosítója.</span><span class="sxs-lookup"><span data-stu-id="e6890-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="e6890-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="e6890-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="e6890-147">A vásárlási csomag kiadóazonosítója.</span><span class="sxs-lookup"><span data-stu-id="e6890-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="e6890-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="e6890-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="e6890-149">A kibocsátási megjegyzés uri.</span><span class="sxs-lookup"><span data-stu-id="e6890-149">The release note uri.</span></span>

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

### <span data-ttu-id="e6890-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6890-150">-ResourceGroupName</span></span>
<span data-ttu-id="e6890-151">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6890-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6890-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6890-152">-ResourceId</span></span>
<span data-ttu-id="e6890-153">A képdefiníció erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e6890-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="e6890-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6890-154">-Tag</span></span>
<span data-ttu-id="e6890-155">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="e6890-155">Resource tags</span></span>

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

### <span data-ttu-id="e6890-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6890-156">-Confirm</span></span>
<span data-ttu-id="e6890-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e6890-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6890-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6890-158">-WhatIf</span></span>
<span data-ttu-id="e6890-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e6890-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6890-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6890-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6890-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6890-161">CommonParameters</span></span>
<span data-ttu-id="e6890-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6890-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6890-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6890-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6890-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6890-164">INPUTS</span></span>

### <span data-ttu-id="e6890-165">System.String</span><span class="sxs-lookup"><span data-stu-id="e6890-165">System.String</span></span>

### <span data-ttu-id="e6890-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="e6890-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="e6890-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="e6890-167">System.DateTime</span></span>

### <span data-ttu-id="e6890-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6890-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e6890-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e6890-169">System.Int32</span></span>

### <span data-ttu-id="e6890-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e6890-170">System.String[]</span></span>

## <span data-ttu-id="e6890-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6890-171">OUTPUTS</span></span>

### <span data-ttu-id="e6890-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="e6890-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="e6890-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6890-173">NOTES</span></span>

## <span data-ttu-id="e6890-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6890-174">RELATED LINKS</span></span>
