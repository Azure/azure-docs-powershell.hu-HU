---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 7139831accd920858e7b97f775146d01b91cef3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928882"
---
# <span data-ttu-id="1ff83-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="1ff83-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="1ff83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ff83-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff83-103">Frissítse az Azure Cognitive Search szolgáltatás megosztott privát hivatkozásforrását.</span><span class="sxs-lookup"><span data-stu-id="1ff83-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1ff83-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ff83-104">SYNTAX</span></span>

### <span data-ttu-id="1ff83-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ff83-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ff83-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ff83-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ff83-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ff83-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ff83-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ff83-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ff83-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ff83-109">DESCRIPTION</span></span>
<span data-ttu-id="1ff83-110">Ez **a Set-AzSearchSharedPrivateLinkResource** frissíti az Azure Cognitive Search szolgáltatás megosztott privát hivatkozásforrását.</span><span class="sxs-lookup"><span data-stu-id="1ff83-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1ff83-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ff83-111">EXAMPLES</span></span>

### <span data-ttu-id="1ff83-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="1ff83-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -RequestMessage "Please kindly approve"


Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please kindly approve
ResourceRegion        :
```

<span data-ttu-id="1ff83-113">Ebben a példában az Azure Kognitív keresés szolgáltatás függőben lévő megosztott privát hivatkozásforrásának kérési üzenete frissül.</span><span class="sxs-lookup"><span data-stu-id="1ff83-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1ff83-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ff83-114">PARAMETERS</span></span>

### <span data-ttu-id="1ff83-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ff83-115">-AsJob</span></span>
<span data-ttu-id="1ff83-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1ff83-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ff83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff83-117">-DefaultProfile</span></span>
<span data-ttu-id="1ff83-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ff83-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ff83-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ff83-119">-InputObject</span></span>
<span data-ttu-id="1ff83-120">Megosztott privát hivatkozás erőforrás-bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="1ff83-120">Shared private link resource input object</span></span>

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

### <span data-ttu-id="1ff83-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1ff83-121">-Name</span></span>
<span data-ttu-id="1ff83-122">Azure Cognitive Search Megosztott privát hivatkozás típusú erőforrás</span><span class="sxs-lookup"><span data-stu-id="1ff83-122">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="1ff83-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1ff83-123">-ParentObject</span></span>
<span data-ttu-id="1ff83-124">Azure Kognitív keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="1ff83-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="1ff83-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="1ff83-125">-RequestMessage</span></span>
<span data-ttu-id="1ff83-126">Megosztott privát hivatkozás erőforrás-kérési üzenete</span><span class="sxs-lookup"><span data-stu-id="1ff83-126">Shared private link resource request message</span></span>

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

### <span data-ttu-id="1ff83-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff83-127">-ResourceGroupName</span></span>
<span data-ttu-id="1ff83-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1ff83-128">Resource Group name.</span></span>

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

### <span data-ttu-id="1ff83-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ff83-129">-ResourceId</span></span>
<span data-ttu-id="1ff83-130">Megosztott privát hivatkozás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1ff83-130">Shared private link resource id</span></span>

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

### <span data-ttu-id="1ff83-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1ff83-131">-ServiceName</span></span>
<span data-ttu-id="1ff83-132">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="1ff83-132">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="1ff83-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ff83-133">-Confirm</span></span>
<span data-ttu-id="1ff83-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1ff83-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ff83-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ff83-135">-WhatIf</span></span>
<span data-ttu-id="1ff83-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1ff83-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ff83-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ff83-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ff83-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff83-138">CommonParameters</span></span>
<span data-ttu-id="1ff83-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff83-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff83-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ff83-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff83-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ff83-141">INPUTS</span></span>

### <span data-ttu-id="1ff83-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="1ff83-142">None</span></span>

## <span data-ttu-id="1ff83-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ff83-143">OUTPUTS</span></span>

### <span data-ttu-id="1ff83-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="1ff83-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="1ff83-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ff83-145">NOTES</span></span>

## <span data-ttu-id="1ff83-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ff83-146">RELATED LINKS</span></span>

[<span data-ttu-id="1ff83-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="1ff83-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="1ff83-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="1ff83-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="1ff83-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="1ff83-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)