---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 0ed07bed894d31be68b8fd4b71605e94b19171ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999782"
---
# <span data-ttu-id="9f95c-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9f95c-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="9f95c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f95c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f95c-103">Privát végpontkapcsolatot kap az Azure Kognitív keresés szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="9f95c-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9f95c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f95c-104">SYNTAX</span></span>

### <span data-ttu-id="9f95c-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f95c-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f95c-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f95c-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f95c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f95c-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f95c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f95c-108">DESCRIPTION</span></span>
<span data-ttu-id="9f95c-109">A **Get-AzSearchPrivateEndpointConnection** parancsmag megkapja a privát végpontkapcsolatokat az Azure Cognitive Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="9f95c-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9f95c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f95c-110">EXAMPLES</span></span>

### <span data-ttu-id="9f95c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9f95c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="9f95c-112">A példa beszerszi az Azure Cognitive Search szolgáltatással létesíthető összes privát végpontkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="9f95c-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="9f95c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="9f95c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266  | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 1,
    "Description": "Auto-approved",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="9f95c-114">A példa egy adott, név szerint (JSON-nak átalakítva a könnyebb olvasás érdekében) és az Azure Kognitív keresés szolgáltatásba beszerkesedő magánjellegű végpontkapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="9f95c-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9f95c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f95c-115">PARAMETERS</span></span>

### <span data-ttu-id="9f95c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f95c-116">-DefaultProfile</span></span>
<span data-ttu-id="9f95c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f95c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f95c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9f95c-118">-Name</span></span>
<span data-ttu-id="9f95c-119">Azure Kognitív keresési szolgáltatás – privát végpontkapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="9f95c-119">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="9f95c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9f95c-120">-ParentObject</span></span>
<span data-ttu-id="9f95c-121">Azure Kognitív keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="9f95c-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="9f95c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f95c-122">-ResourceGroupName</span></span>
<span data-ttu-id="9f95c-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9f95c-123">Resource Group name.</span></span>

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

### <span data-ttu-id="9f95c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f95c-124">-ResourceId</span></span>
<span data-ttu-id="9f95c-125">Private link service resource id</span><span class="sxs-lookup"><span data-stu-id="9f95c-125">Private link service resource id</span></span>

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

### <span data-ttu-id="9f95c-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9f95c-126">-ServiceName</span></span>
<span data-ttu-id="9f95c-127">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="9f95c-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="9f95c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f95c-128">-Confirm</span></span>
<span data-ttu-id="9f95c-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9f95c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f95c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f95c-130">-WhatIf</span></span>
<span data-ttu-id="9f95c-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9f95c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f95c-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f95c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f95c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f95c-133">CommonParameters</span></span>
<span data-ttu-id="9f95c-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f95c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f95c-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f95c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f95c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f95c-136">INPUTS</span></span>

### <span data-ttu-id="9f95c-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9f95c-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="9f95c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9f95c-138">System.String</span></span>

## <span data-ttu-id="9f95c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f95c-139">OUTPUTS</span></span>

### <span data-ttu-id="9f95c-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9f95c-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="9f95c-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f95c-141">NOTES</span></span>

## <span data-ttu-id="9f95c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f95c-142">RELATED LINKS</span></span>

[<span data-ttu-id="9f95c-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="9f95c-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="9f95c-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="9f95c-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
