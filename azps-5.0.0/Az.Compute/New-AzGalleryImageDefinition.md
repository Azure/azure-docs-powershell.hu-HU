---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303191"
---
# <span data-ttu-id="562f3-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="562f3-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="562f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="562f3-102">SYNOPSIS</span></span>
<span data-ttu-id="562f3-103">Gyűjtemény képének definíciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="562f3-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="562f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="562f3-104">SYNTAX</span></span>

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

## <span data-ttu-id="562f3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="562f3-105">DESCRIPTION</span></span>
<span data-ttu-id="562f3-106">Gyűjtemény képének definíciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="562f3-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="562f3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="562f3-107">EXAMPLES</span></span>

### <span data-ttu-id="562f3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="562f3-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="562f3-109">Gyűjtemény képének definíciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="562f3-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="562f3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="562f3-110">PARAMETERS</span></span>

### <span data-ttu-id="562f3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="562f3-111">-AsJob</span></span>
<span data-ttu-id="562f3-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="562f3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="562f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="562f3-113">-DefaultProfile</span></span>
<span data-ttu-id="562f3-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="562f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="562f3-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="562f3-115">-Description</span></span>
<span data-ttu-id="562f3-116">A Galéria képdefiníciós erőforrásának leírása.</span><span class="sxs-lookup"><span data-stu-id="562f3-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="562f3-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="562f3-117">-DisallowedDiskType</span></span>
<span data-ttu-id="562f3-118">A nem engedélyezett lemez típusa.</span><span class="sxs-lookup"><span data-stu-id="562f3-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="562f3-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="562f3-119">-EndOfLifeDate</span></span>
<span data-ttu-id="562f3-120">A gyűjtemény képdefiníciójának utolsó dátuma</span><span class="sxs-lookup"><span data-stu-id="562f3-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="562f3-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="562f3-121">-Eula</span></span>
<span data-ttu-id="562f3-122">A Galéria képdefiníciós licencszerződése</span><span class="sxs-lookup"><span data-stu-id="562f3-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="562f3-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="562f3-123">-GalleryName</span></span>
<span data-ttu-id="562f3-124">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="562f3-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="562f3-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="562f3-125">-HyperVGeneration</span></span>
<span data-ttu-id="562f3-126">A virtuális gép hypervisor-generációja.</span><span class="sxs-lookup"><span data-stu-id="562f3-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="562f3-127">Csak az operációsrendszer-lemezekre érvényes.</span><span class="sxs-lookup"><span data-stu-id="562f3-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="562f3-128">A megengedett értékek a v1 és a v2.</span><span class="sxs-lookup"><span data-stu-id="562f3-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="562f3-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="562f3-129">-Location</span></span>
<span data-ttu-id="562f3-130">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="562f3-130">Resource location</span></span>

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

### <span data-ttu-id="562f3-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="562f3-131">-MaximumMemory</span></span>
<span data-ttu-id="562f3-132">Az ajánlott memória maximális száma</span><span class="sxs-lookup"><span data-stu-id="562f3-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="562f3-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="562f3-133">-MaximumVCPU</span></span>
<span data-ttu-id="562f3-134">Az ajánlott CPU-mag maximális száma</span><span class="sxs-lookup"><span data-stu-id="562f3-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="562f3-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="562f3-135">-MinimumMemory</span></span>
<span data-ttu-id="562f3-136">Az ajánlott memória minimális száma</span><span class="sxs-lookup"><span data-stu-id="562f3-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="562f3-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="562f3-137">-MinimumVCPU</span></span>
<span data-ttu-id="562f3-138">Az ajánlott CPU-mag minimális száma</span><span class="sxs-lookup"><span data-stu-id="562f3-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="562f3-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="562f3-139">-Name</span></span>
<span data-ttu-id="562f3-140">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="562f3-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="562f3-141">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="562f3-141">-Offer</span></span>
<span data-ttu-id="562f3-142">A Képtár képdefiníciós ajánlatának neve.</span><span class="sxs-lookup"><span data-stu-id="562f3-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="562f3-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="562f3-143">-OsState</span></span>
<span data-ttu-id="562f3-144">Az operációs rendszer állapota</span><span class="sxs-lookup"><span data-stu-id="562f3-144">The state of OS</span></span>

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

### <span data-ttu-id="562f3-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="562f3-145">-OsType</span></span>
<span data-ttu-id="562f3-146">Az operációs rendszer típusa</span><span class="sxs-lookup"><span data-stu-id="562f3-146">The type of OS</span></span>

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

### <span data-ttu-id="562f3-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="562f3-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="562f3-148">Az adatvédelmi nyilatkozat URI-ja.</span><span class="sxs-lookup"><span data-stu-id="562f3-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="562f3-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="562f3-149">-Publisher</span></span>
<span data-ttu-id="562f3-150">A Képtár képdefiníciójának közzétevője.</span><span class="sxs-lookup"><span data-stu-id="562f3-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="562f3-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="562f3-151">-PurchasePlanName</span></span>
<span data-ttu-id="562f3-152">A beszerzési csomag azonosítója.</span><span class="sxs-lookup"><span data-stu-id="562f3-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="562f3-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="562f3-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="562f3-154">A beszerzési csomag termékazonosítója.</span><span class="sxs-lookup"><span data-stu-id="562f3-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="562f3-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="562f3-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="562f3-156">A beszerzési csomag közzétevő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="562f3-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="562f3-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="562f3-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="562f3-158">A kibocsátási Megjegyzés URI-ja.</span><span class="sxs-lookup"><span data-stu-id="562f3-158">The release note uri.</span></span>

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

### <span data-ttu-id="562f3-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="562f3-159">-ResourceGroupName</span></span>
<span data-ttu-id="562f3-160">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="562f3-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="562f3-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="562f3-161">-Sku</span></span>
<span data-ttu-id="562f3-162">A gyűjtemény képdefiníciós SKU neve.</span><span class="sxs-lookup"><span data-stu-id="562f3-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="562f3-163">-Címke</span><span class="sxs-lookup"><span data-stu-id="562f3-163">-Tag</span></span>
<span data-ttu-id="562f3-164">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="562f3-164">Resource tags</span></span>

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

### <span data-ttu-id="562f3-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="562f3-165">-Confirm</span></span>
<span data-ttu-id="562f3-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="562f3-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="562f3-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="562f3-167">-WhatIf</span></span>
<span data-ttu-id="562f3-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="562f3-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="562f3-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="562f3-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="562f3-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="562f3-170">CommonParameters</span></span>
<span data-ttu-id="562f3-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="562f3-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="562f3-172">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="562f3-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="562f3-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="562f3-173">INPUTS</span></span>

### <span data-ttu-id="562f3-174">System. String</span><span class="sxs-lookup"><span data-stu-id="562f3-174">System.String</span></span>

### <span data-ttu-id="562f3-175">Microsoft. Azure. Management. kiszámítás. models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="562f3-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="562f3-176">Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="562f3-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="562f3-177">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="562f3-177">System.DateTime</span></span>

### <span data-ttu-id="562f3-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="562f3-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="562f3-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="562f3-179">System.Int32</span></span>

### <span data-ttu-id="562f3-180">System. string []</span><span class="sxs-lookup"><span data-stu-id="562f3-180">System.String[]</span></span>

## <span data-ttu-id="562f3-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="562f3-181">OUTPUTS</span></span>

### <span data-ttu-id="562f3-182">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="562f3-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="562f3-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="562f3-183">NOTES</span></span>

## <span data-ttu-id="562f3-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="562f3-184">RELATED LINKS</span></span>
