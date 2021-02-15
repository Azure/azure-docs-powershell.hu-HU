---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-AzSearchPrivateLinkResource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
ms.openlocfilehash: 24941a301d0ffcc4e7219dc923fefcf1e007de99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143571"
---
# <span data-ttu-id="ef082-101">Get-AzSearchPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="ef082-101">Get-AzSearchPrivateLinkResource</span></span>

## <span data-ttu-id="ef082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef082-102">SYNOPSIS</span></span>
<span data-ttu-id="ef082-103">Személyes hivatkozáserőforrás-adatokat kap az Azure Kognitív keresés szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="ef082-103">Gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ef082-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef082-104">SYNTAX</span></span>

### <span data-ttu-id="ef082-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef082-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef082-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef082-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef082-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef082-107">InputObjectParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-InputObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef082-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef082-108">DESCRIPTION</span></span>
<span data-ttu-id="ef082-109">A **Get-AzSearchPrivateLinkResource** parancsmag személyes hivatkozáserőforrás-adatokat kap az Azure Cognitive Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="ef082-109">The **Get-AzSearchPrivateLinkResource** cmdlet gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ef082-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef082-110">EXAMPLES</span></span>

### <span data-ttu-id="ef082-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ef082-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateLinkResource -ResourceGroupName arjagann -Name arjagann-test-cuseuap | ConvertTo-Json

  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateLinkResources/searchService",
  "Type": "Microsoft.Search/searchServices/privateLinkResources",
  "GroupId": "searchService",
  "RequiredMembers": [
    "searchService"
  ],
  "RequiredZoneNames": [
    "privatelink.search-dogfood.windows-int.net"
  ],
  "ShareablePrivateLinkResourceTypes": [
    {
      "Name": "blob",
      "Description": "Azure Cognitive Search indexers can connect to blobs in Azure Storage for reading data (data source), for writing intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "blob"
    },
    {
      "Name": "table",
      "Description": "Azure Cognitive Search indexers can connect to tables in Azure Storage for reading data (data source), for writing book-keeping information about intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "table"
    },
    {
      "Name": "Sql",
      "Description": "Azure Cognitive Search indexers can connect to CosmosDB using the SQL head for reading data (data source).",
      "Type": "Microsoft.DocumentDB/databaseAccounts",
      "GroupId": "Sql"
    },
    {
      "Name": "plr",
      "Description": "Azure Cognitive Search indexers can connect to AzureSQL databases in a SQL server for reading data (data source).",
      "Type": "Microsoft.Sql/servers",
      "GroupId": "sqlServer"
    },
    {
      "Name": "vault",
      "Description": "Azure Cognitive Search can access keys in Azure Key Vault to encrypt search index and synonym map data",
      "Type": "Microsoft.KeyVault/vaults",
      "GroupId": "vault"
    }
  ]
}
```

<span data-ttu-id="ef082-112">A példa bemutatja, hogy miként olvashatja be a privát hivatkozás típusú erőforrások adatait (az egyszerűség kedvéért JSON-formában) az Azure Kognitív keresés szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="ef082-112">The example shows how to get the private link resource details (in JSON form for convenience) for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ef082-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef082-113">PARAMETERS</span></span>

### <span data-ttu-id="ef082-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef082-114">-DefaultProfile</span></span>
<span data-ttu-id="ef082-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef082-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef082-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef082-116">-InputObject</span></span>
<span data-ttu-id="ef082-117">Azure Kognitív keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="ef082-117">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef082-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ef082-118">-Name</span></span>
<span data-ttu-id="ef082-119">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="ef082-119">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="ef082-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef082-120">-ResourceGroupName</span></span>
<span data-ttu-id="ef082-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef082-121">Resource Group name.</span></span>

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

### <span data-ttu-id="ef082-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef082-122">-ResourceId</span></span>
<span data-ttu-id="ef082-123">Azure Kognitív keresési szolgáltatás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef082-123">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="ef082-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef082-124">-Confirm</span></span>
<span data-ttu-id="ef082-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef082-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef082-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef082-126">-WhatIf</span></span>
<span data-ttu-id="ef082-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef082-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef082-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef082-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef082-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef082-129">CommonParameters</span></span>
<span data-ttu-id="ef082-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef082-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef082-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef082-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef082-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef082-132">INPUTS</span></span>

### <span data-ttu-id="ef082-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="ef082-133">None</span></span>

## <span data-ttu-id="ef082-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef082-134">OUTPUTS</span></span>

### <span data-ttu-id="ef082-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="ef082-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="ef082-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef082-136">NOTES</span></span>

## <span data-ttu-id="ef082-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef082-137">RELATED LINKS</span></span>

[<span data-ttu-id="ef082-138">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="ef082-138">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="ef082-139">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="ef082-139">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="ef082-140">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="ef082-140">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="ef082-141">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="ef082-141">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)