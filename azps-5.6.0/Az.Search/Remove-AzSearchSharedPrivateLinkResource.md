---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: ed5c5bf502e1d19b0ba095e5db68f1f116a71137
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920442"
---
# <span data-ttu-id="6b40e-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6b40e-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="6b40e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b40e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b40e-103">Távolítsa el a megosztott privát hivatkozásforrást az Azure Kognitív keresés szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="6b40e-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6b40e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b40e-104">SYNTAX</span></span>

### <span data-ttu-id="6b40e-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b40e-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b40e-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b40e-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b40e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b40e-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b40e-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b40e-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b40e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b40e-109">DESCRIPTION</span></span>
<span data-ttu-id="6b40e-110">A **Remove-AzSearchSharedPrivateLinkResource** parancsmag eltávolítja a megosztott privát hivatkozásforrást az Azure Kognitív keresés szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="6b40e-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6b40e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b40e-111">EXAMPLES</span></span>

### <span data-ttu-id="6b40e-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="6b40e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="6b40e-113">Ebben a példában töröl egy megosztott privát hivatkozás típusú erőforrást az Azure Kognitív keresési szolgáltatás neve alapján.</span><span class="sxs-lookup"><span data-stu-id="6b40e-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6b40e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b40e-114">PARAMETERS</span></span>

### <span data-ttu-id="6b40e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b40e-115">-AsJob</span></span>
<span data-ttu-id="6b40e-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6b40e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b40e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b40e-117">-DefaultProfile</span></span>
<span data-ttu-id="6b40e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b40e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b40e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6b40e-119">-Force</span></span>
<span data-ttu-id="6b40e-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b40e-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6b40e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b40e-121">-InputObject</span></span>
<span data-ttu-id="6b40e-122">Megosztott privát hivatkozás erőforrás-bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="6b40e-122">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b40e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6b40e-123">-Name</span></span>
<span data-ttu-id="6b40e-124">Azure Cognitive Search Megosztott privát hivatkozás típusú erőforrás</span><span class="sxs-lookup"><span data-stu-id="6b40e-124">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b40e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6b40e-125">-ParentObject</span></span>
<span data-ttu-id="6b40e-126">Azure Kognitív keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="6b40e-126">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b40e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b40e-127">-PassThru</span></span>
<span data-ttu-id="6b40e-128">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="6b40e-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6b40e-129">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="6b40e-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6b40e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b40e-130">-ResourceGroupName</span></span>
<span data-ttu-id="6b40e-131">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6b40e-131">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b40e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b40e-132">-ResourceId</span></span>
<span data-ttu-id="6b40e-133">Megosztott privát hivatkozás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6b40e-133">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b40e-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6b40e-134">-ServiceName</span></span>
<span data-ttu-id="6b40e-135">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="6b40e-135">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b40e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b40e-136">-Confirm</span></span>
<span data-ttu-id="6b40e-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b40e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b40e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b40e-138">-WhatIf</span></span>
<span data-ttu-id="6b40e-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b40e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b40e-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b40e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b40e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b40e-141">CommonParameters</span></span>
<span data-ttu-id="6b40e-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b40e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b40e-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b40e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b40e-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b40e-144">INPUTS</span></span>

### <span data-ttu-id="6b40e-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="6b40e-145">None</span></span>

## <span data-ttu-id="6b40e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b40e-146">OUTPUTS</span></span>

### <span data-ttu-id="6b40e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b40e-147">System.Boolean</span></span>

## <span data-ttu-id="6b40e-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b40e-148">NOTES</span></span>

## <span data-ttu-id="6b40e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b40e-149">RELATED LINKS</span></span>

[<span data-ttu-id="6b40e-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="6b40e-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="6b40e-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="6b40e-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="6b40e-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="6b40e-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)