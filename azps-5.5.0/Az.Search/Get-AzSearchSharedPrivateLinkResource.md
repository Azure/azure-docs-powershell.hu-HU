---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a49d73ea564cab6f01b9482a7c110aeaa7fc307
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159939"
---
# <span data-ttu-id="438a4-101">Get-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="438a4-101">Get-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="438a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="438a4-102">SYNOPSIS</span></span>
<span data-ttu-id="438a4-103">Az Azure Cognitive Search szolgáltatás megosztott privát hivatkozásforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="438a4-103">Gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="438a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="438a4-104">SYNTAX</span></span>

### <span data-ttu-id="438a4-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="438a4-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="438a4-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="438a4-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="438a4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="438a4-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="438a4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="438a4-108">DESCRIPTION</span></span>
<span data-ttu-id="438a4-109">A **Get-AzSearchSharedPrivateLinkResource** parancsmag az Azure Cognitive Search szolgáltatás megosztott hivatkozásforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="438a4-109">The **Get-AzSearchSharedPrivateLinkResource** cmdlet gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="438a4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="438a4-110">EXAMPLES</span></span>

### <span data-ttu-id="438a4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="438a4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/cosmos-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : cosmos-pe
GroupId               : Sql
PrivateLinkResourceId : /subscriptions/dc95d1b6-71a8-4dff-bcc9-a1c282bdbd8b/resourceGroups/arjagann/providers/Microsoft.DocumentDb/databaseAccounts/arjagann-sql
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe2
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe2
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting2
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="438a4-112">Ebben a példában az Azure Cognitive Search szolgáltatás összes megosztott privát hivatkozási erőforrása látható.</span><span class="sxs-lookup"><span data-stu-id="438a4-112">This example lists all the shared private link resources of the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="438a4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="438a4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name table-pe

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="438a4-114">Ebben a példában egy adott megosztott privát hivatkozáserőforrást sorolunk fel az Azure Kognitív keresési szolgáltatás neve alapján.</span><span class="sxs-lookup"><span data-stu-id="438a4-114">This example lists a specific shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="438a4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="438a4-115">PARAMETERS</span></span>

### <span data-ttu-id="438a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438a4-116">-DefaultProfile</span></span>
<span data-ttu-id="438a4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="438a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="438a4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="438a4-118">-Name</span></span>
<span data-ttu-id="438a4-119">Azure Cognitive Search Megosztott privát hivatkozás típusú erőforrás</span><span class="sxs-lookup"><span data-stu-id="438a4-119">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="438a4-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="438a4-120">-ParentObject</span></span>
<span data-ttu-id="438a4-121">Azure Kognitív keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="438a4-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="438a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="438a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="438a4-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="438a4-123">Resource Group name.</span></span>

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

### <span data-ttu-id="438a4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="438a4-124">-ResourceId</span></span>
<span data-ttu-id="438a4-125">Megosztott privát hivatkozás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="438a4-125">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="438a4-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="438a4-126">-ServiceName</span></span>
<span data-ttu-id="438a4-127">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="438a4-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="438a4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="438a4-128">-Confirm</span></span>
<span data-ttu-id="438a4-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="438a4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="438a4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="438a4-130">-WhatIf</span></span>
<span data-ttu-id="438a4-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="438a4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="438a4-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="438a4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="438a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438a4-133">CommonParameters</span></span>
<span data-ttu-id="438a4-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="438a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438a4-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="438a4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438a4-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="438a4-136">INPUTS</span></span>

### <span data-ttu-id="438a4-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="438a4-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="438a4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="438a4-138">System.String</span></span>

## <span data-ttu-id="438a4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="438a4-139">OUTPUTS</span></span>

### <span data-ttu-id="438a4-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="438a4-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="438a4-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="438a4-141">NOTES</span></span>

## <span data-ttu-id="438a4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="438a4-142">RELATED LINKS</span></span>

[<span data-ttu-id="438a4-143">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="438a4-143">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="438a4-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="438a4-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="438a4-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="438a4-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
