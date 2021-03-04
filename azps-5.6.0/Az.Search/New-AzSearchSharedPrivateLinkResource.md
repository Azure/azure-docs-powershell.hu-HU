---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 683a6105273bcd2ff2f254352cf6e991491c035d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930817"
---
# <span data-ttu-id="fffd8-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="fffd8-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="fffd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fffd8-102">SYNOPSIS</span></span>
<span data-ttu-id="fffd8-103">Létrehoz egy megosztott privát hivatkozásforrást az Azure Kognitív keresés szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="fffd8-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fffd8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fffd8-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fffd8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fffd8-105">DESCRIPTION</span></span>
<span data-ttu-id="fffd8-106">A **New-AzSearchSharedPrivateLinkResource létrehoz** egy megosztott privát hivatkozásforrást az Azure Cognitive Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="fffd8-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fffd8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fffd8-107">EXAMPLES</span></span>

### <span data-ttu-id="fffd8-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fffd8-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -PrivateLinkResourceId /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting -GroupId blob -RequestMessage "Please approve" 

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please approve
ResourceRegion        :
```

<span data-ttu-id="fffd8-109">Ebben a példában megosztott privát hivatkozáserőforrást hoz létre az Azure Kognitív keresés szolgáltatás tárfiókja blobszolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="fffd8-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fffd8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fffd8-110">PARAMETERS</span></span>

### <span data-ttu-id="fffd8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fffd8-111">-AsJob</span></span>
<span data-ttu-id="fffd8-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fffd8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fffd8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fffd8-113">-DefaultProfile</span></span>
<span data-ttu-id="fffd8-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fffd8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fffd8-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="fffd8-115">-GroupId</span></span>
<span data-ttu-id="fffd8-116">Megosztott privát hivatkozás erőforráscsoport-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fffd8-116">Shared private link resource group id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fffd8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fffd8-117">-Name</span></span>
<span data-ttu-id="fffd8-118">Azure Cognitive Search Megosztott privát hivatkozás típusú erőforrás</span><span class="sxs-lookup"><span data-stu-id="fffd8-118">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fffd8-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="fffd8-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="fffd8-120">Megosztott privát hivatkozás célerőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fffd8-120">Shared private link target resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fffd8-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="fffd8-121">-RequestMessage</span></span>
<span data-ttu-id="fffd8-122">Megosztott privát hivatkozás erőforrás-kérési üzenete</span><span class="sxs-lookup"><span data-stu-id="fffd8-122">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fffd8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fffd8-123">-ResourceGroupName</span></span>
<span data-ttu-id="fffd8-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fffd8-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fffd8-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="fffd8-125">-ResourceRegion</span></span>
<span data-ttu-id="fffd8-126">(Nem kötelező) Megosztott privát hivatkozás erőforrásterülete</span><span class="sxs-lookup"><span data-stu-id="fffd8-126">(Optional) Shared private link resource region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fffd8-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fffd8-127">-ServiceName</span></span>
<span data-ttu-id="fffd8-128">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="fffd8-128">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fffd8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fffd8-129">-Confirm</span></span>
<span data-ttu-id="fffd8-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fffd8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fffd8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fffd8-131">-WhatIf</span></span>
<span data-ttu-id="fffd8-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fffd8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fffd8-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fffd8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fffd8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fffd8-134">CommonParameters</span></span>
<span data-ttu-id="fffd8-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fffd8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fffd8-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fffd8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fffd8-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fffd8-137">INPUTS</span></span>

### <span data-ttu-id="fffd8-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="fffd8-138">None</span></span>

## <span data-ttu-id="fffd8-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fffd8-139">OUTPUTS</span></span>

### <span data-ttu-id="fffd8-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="fffd8-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="fffd8-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fffd8-141">NOTES</span></span>

## <span data-ttu-id="fffd8-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fffd8-142">RELATED LINKS</span></span>

[<span data-ttu-id="fffd8-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="fffd8-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="fffd8-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="fffd8-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="fffd8-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="fffd8-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
