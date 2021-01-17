---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339749"
---
# <span data-ttu-id="b011e-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="b011e-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="b011e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b011e-102">SYNOPSIS</span></span>
<span data-ttu-id="b011e-103">Gyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b011e-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="b011e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b011e-104">SYNTAX</span></span>

### <span data-ttu-id="b011e-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b011e-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b011e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b011e-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b011e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b011e-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b011e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b011e-108">DESCRIPTION</span></span>
<span data-ttu-id="b011e-109">Gyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b011e-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="b011e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b011e-110">EXAMPLES</span></span>

### <span data-ttu-id="b011e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b011e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="b011e-112">Gyűjtemény képdefiníciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b011e-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="b011e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b011e-113">PARAMETERS</span></span>

### <span data-ttu-id="b011e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b011e-114">-AsJob</span></span>
<span data-ttu-id="b011e-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b011e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b011e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b011e-116">-DefaultProfile</span></span>
<span data-ttu-id="b011e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b011e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b011e-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b011e-118">-Description</span></span>
<span data-ttu-id="b011e-119">A gyűjtemény képdefiníciós erőforrásának leírása.</span><span class="sxs-lookup"><span data-stu-id="b011e-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="b011e-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="b011e-120">-DisallowedDiskType</span></span>
<span data-ttu-id="b011e-121">A nem engedélyezett lemeztípusok.</span><span class="sxs-lookup"><span data-stu-id="b011e-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="b011e-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="b011e-122">-EndOfLifeDate</span></span>
<span data-ttu-id="b011e-123">A gyűjtemény Képdefiníció életciklusának vége</span><span class="sxs-lookup"><span data-stu-id="b011e-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="b011e-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="b011e-124">-Eula</span></span>
<span data-ttu-id="b011e-125">A képdefiníció gyűjteményre vonatkozó Eula-szerződés.</span><span class="sxs-lookup"><span data-stu-id="b011e-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="b011e-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="b011e-126">-GalleryName</span></span>
<span data-ttu-id="b011e-127">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="b011e-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="b011e-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b011e-128">-InputObject</span></span>
<span data-ttu-id="b011e-129">A PS-gyűjtemény képdefiníciós objektuma.</span><span class="sxs-lookup"><span data-stu-id="b011e-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="b011e-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="b011e-130">-MaximumMemory</span></span>
<span data-ttu-id="b011e-131">Az ajánlott memória maximális mérete</span><span class="sxs-lookup"><span data-stu-id="b011e-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="b011e-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="b011e-132">-MaximumVCPU</span></span>
<span data-ttu-id="b011e-133">Az ajánlott processzormag maximális mérete</span><span class="sxs-lookup"><span data-stu-id="b011e-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="b011e-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="b011e-134">-MinimumMemory</span></span>
<span data-ttu-id="b011e-135">Az ajánlott memória minimális</span><span class="sxs-lookup"><span data-stu-id="b011e-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="b011e-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="b011e-136">-MinimumVCPU</span></span>
<span data-ttu-id="b011e-137">Az ajánlott processzormag minimuma</span><span class="sxs-lookup"><span data-stu-id="b011e-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="b011e-138">-Name</span><span class="sxs-lookup"><span data-stu-id="b011e-138">-Name</span></span>
<span data-ttu-id="b011e-139">A gyűjtemény képdefiníciójának neve.</span><span class="sxs-lookup"><span data-stu-id="b011e-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="b011e-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="b011e-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="b011e-141">Az adatvédelmi nyilatkozat uri.</span><span class="sxs-lookup"><span data-stu-id="b011e-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="b011e-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="b011e-142">-PurchasePlanName</span></span>
<span data-ttu-id="b011e-143">A vásárlási csomag azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b011e-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="b011e-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="b011e-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="b011e-145">A vásárlási csomag termékazonosítója.</span><span class="sxs-lookup"><span data-stu-id="b011e-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="b011e-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b011e-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="b011e-147">A vásárlási csomag kiadóazonosítója.</span><span class="sxs-lookup"><span data-stu-id="b011e-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="b011e-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="b011e-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="b011e-149">A kibocsátási megjegyzés uri.</span><span class="sxs-lookup"><span data-stu-id="b011e-149">The release note uri.</span></span>

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

### <span data-ttu-id="b011e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b011e-150">-ResourceGroupName</span></span>
<span data-ttu-id="b011e-151">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b011e-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="b011e-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b011e-152">-ResourceId</span></span>
<span data-ttu-id="b011e-153">A képdefiníció erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b011e-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="b011e-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="b011e-154">-Tag</span></span>
<span data-ttu-id="b011e-155">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="b011e-155">Resource tags</span></span>

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

### <span data-ttu-id="b011e-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b011e-156">-Confirm</span></span>
<span data-ttu-id="b011e-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b011e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b011e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b011e-158">-WhatIf</span></span>
<span data-ttu-id="b011e-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b011e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b011e-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b011e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b011e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b011e-161">CommonParameters</span></span>
<span data-ttu-id="b011e-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b011e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b011e-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b011e-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b011e-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b011e-164">INPUTS</span></span>

### <span data-ttu-id="b011e-165">System.String</span><span class="sxs-lookup"><span data-stu-id="b011e-165">System.String</span></span>

### <span data-ttu-id="b011e-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="b011e-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="b011e-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="b011e-167">System.DateTime</span></span>

### <span data-ttu-id="b011e-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b011e-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b011e-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b011e-169">System.Int32</span></span>

### <span data-ttu-id="b011e-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b011e-170">System.String[]</span></span>

## <span data-ttu-id="b011e-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b011e-171">OUTPUTS</span></span>

### <span data-ttu-id="b011e-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="b011e-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="b011e-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b011e-173">NOTES</span></span>

## <span data-ttu-id="b011e-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b011e-174">RELATED LINKS</span></span>
