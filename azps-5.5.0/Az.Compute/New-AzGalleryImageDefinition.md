---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144938"
---
# <span data-ttu-id="f4589-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="f4589-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="f4589-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4589-102">SYNOPSIS</span></span>
<span data-ttu-id="f4589-103">Gyűjtemény képdefiníciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="f4589-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="f4589-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4589-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4589-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4589-105">DESCRIPTION</span></span>
<span data-ttu-id="f4589-106">Gyűjtemény képdefiníciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="f4589-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="f4589-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4589-107">EXAMPLES</span></span>

### <span data-ttu-id="f4589-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f4589-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="f4589-109">Gyűjtemény képdefiníciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="f4589-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="f4589-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4589-110">PARAMETERS</span></span>

### <span data-ttu-id="f4589-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4589-111">-AsJob</span></span>
<span data-ttu-id="f4589-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f4589-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4589-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4589-113">-DefaultProfile</span></span>
<span data-ttu-id="f4589-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4589-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4589-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f4589-115">-Description</span></span>
<span data-ttu-id="f4589-116">A gyűjtemény képdefiníciós erőforrásának leírása.</span><span class="sxs-lookup"><span data-stu-id="f4589-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="f4589-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="f4589-117">-DisallowedDiskType</span></span>
<span data-ttu-id="f4589-118">A nem engedélyezett lemeztípusok.</span><span class="sxs-lookup"><span data-stu-id="f4589-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="f4589-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="f4589-119">-EndOfLifeDate</span></span>
<span data-ttu-id="f4589-120">A gyűjtemény Képdefiníció életciklusának vége</span><span class="sxs-lookup"><span data-stu-id="f4589-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="f4589-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="f4589-121">-Eula</span></span>
<span data-ttu-id="f4589-122">A képdefiníció gyűjteményre vonatkozó Eula-szerződés.</span><span class="sxs-lookup"><span data-stu-id="f4589-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="f4589-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="f4589-123">-GalleryName</span></span>
<span data-ttu-id="f4589-124">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="f4589-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="f4589-125">-HyperVGeneráció</span><span class="sxs-lookup"><span data-stu-id="f4589-125">-HyperVGeneration</span></span>
<span data-ttu-id="f4589-126">A virtuális gép hipervizor-generálása.</span><span class="sxs-lookup"><span data-stu-id="f4589-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="f4589-127">Csak operációs rendszer lemezei esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="f4589-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="f4589-128">Az engedélyezett értékek a V1 és a V2.</span><span class="sxs-lookup"><span data-stu-id="f4589-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="f4589-129">-Location</span><span class="sxs-lookup"><span data-stu-id="f4589-129">-Location</span></span>
<span data-ttu-id="f4589-130">Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="f4589-130">Resource location</span></span>

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

### <span data-ttu-id="f4589-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="f4589-131">-MaximumMemory</span></span>
<span data-ttu-id="f4589-132">Az ajánlott memória maximális mérete</span><span class="sxs-lookup"><span data-stu-id="f4589-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="f4589-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="f4589-133">-MaximumVCPU</span></span>
<span data-ttu-id="f4589-134">Az ajánlott processzormag maximális mérete</span><span class="sxs-lookup"><span data-stu-id="f4589-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="f4589-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="f4589-135">-MinimumMemory</span></span>
<span data-ttu-id="f4589-136">Az ajánlott memória minimális</span><span class="sxs-lookup"><span data-stu-id="f4589-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="f4589-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="f4589-137">-MinimumVCPU</span></span>
<span data-ttu-id="f4589-138">Az ajánlott processzormag minimális</span><span class="sxs-lookup"><span data-stu-id="f4589-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="f4589-139">-Name</span><span class="sxs-lookup"><span data-stu-id="f4589-139">-Name</span></span>
<span data-ttu-id="f4589-140">A gyűjtemény képdefiníciójának neve.</span><span class="sxs-lookup"><span data-stu-id="f4589-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="f4589-141">-Offer</span><span class="sxs-lookup"><span data-stu-id="f4589-141">-Offer</span></span>
<span data-ttu-id="f4589-142">A képdefiníciós gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="f4589-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="f4589-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="f4589-143">-OsState</span></span>
<span data-ttu-id="f4589-144">Az operációs rendszer állapota</span><span class="sxs-lookup"><span data-stu-id="f4589-144">The state of OS</span></span>

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

### <span data-ttu-id="f4589-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="f4589-145">-OsType</span></span>
<span data-ttu-id="f4589-146">Az operációs rendszer típusa</span><span class="sxs-lookup"><span data-stu-id="f4589-146">The type of OS</span></span>

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

### <span data-ttu-id="f4589-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="f4589-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="f4589-148">Az adatvédelmi nyilatkozat uri.</span><span class="sxs-lookup"><span data-stu-id="f4589-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="f4589-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f4589-149">-Publisher</span></span>
<span data-ttu-id="f4589-150">A gyűjtemény Képdefiníciós kiadójának neve.</span><span class="sxs-lookup"><span data-stu-id="f4589-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="f4589-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="f4589-151">-PurchasePlanName</span></span>
<span data-ttu-id="f4589-152">A vásárlási csomag azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f4589-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="f4589-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="f4589-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="f4589-154">A vásárlási csomag termékazonosítója.</span><span class="sxs-lookup"><span data-stu-id="f4589-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="f4589-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="f4589-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="f4589-156">A vásárlási csomag kiadóazonosítója.</span><span class="sxs-lookup"><span data-stu-id="f4589-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="f4589-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="f4589-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="f4589-158">A kibocsátási megjegyzés uri.</span><span class="sxs-lookup"><span data-stu-id="f4589-158">The release note uri.</span></span>

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

### <span data-ttu-id="f4589-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4589-159">-ResourceGroupName</span></span>
<span data-ttu-id="f4589-160">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4589-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4589-161">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="f4589-161">-Sku</span></span>
<span data-ttu-id="f4589-162">A gyűjtemény képdefiníciós termékváltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="f4589-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="f4589-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4589-163">-Tag</span></span>
<span data-ttu-id="f4589-164">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="f4589-164">Resource tags</span></span>

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

### <span data-ttu-id="f4589-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4589-165">-Confirm</span></span>
<span data-ttu-id="f4589-166">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f4589-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4589-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4589-167">-WhatIf</span></span>
<span data-ttu-id="f4589-168">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f4589-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4589-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4589-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4589-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4589-170">CommonParameters</span></span>
<span data-ttu-id="f4589-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4589-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4589-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4589-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4589-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4589-173">INPUTS</span></span>

### <span data-ttu-id="f4589-174">System.String</span><span class="sxs-lookup"><span data-stu-id="f4589-174">System.String</span></span>

### <span data-ttu-id="f4589-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="f4589-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="f4589-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="f4589-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="f4589-177">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="f4589-177">System.DateTime</span></span>

### <span data-ttu-id="f4589-178">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4589-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f4589-179">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f4589-179">System.Int32</span></span>

### <span data-ttu-id="f4589-180">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f4589-180">System.String[]</span></span>

## <span data-ttu-id="f4589-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4589-181">OUTPUTS</span></span>

### <span data-ttu-id="f4589-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="f4589-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="f4589-183">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4589-183">NOTES</span></span>

## <span data-ttu-id="f4589-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4589-184">RELATED LINKS</span></span>
