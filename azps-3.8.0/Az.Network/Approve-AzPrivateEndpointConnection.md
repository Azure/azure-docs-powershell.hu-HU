---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012519"
---
# <span data-ttu-id="800f3-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="800f3-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="800f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="800f3-102">SYNOPSIS</span></span>
<span data-ttu-id="800f3-103">Privát végpont-kapcsolatot hagy jóvá.</span><span class="sxs-lookup"><span data-stu-id="800f3-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="800f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="800f3-104">SYNTAX</span></span>

### <span data-ttu-id="800f3-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="800f3-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="800f3-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="800f3-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="800f3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="800f3-107">DESCRIPTION</span></span>
<span data-ttu-id="800f3-108">A **jóváhagyás – AzPrivateEndpointConnection** parancsmag jóváhagyja a privát végpontos kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="800f3-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="800f3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="800f3-109">EXAMPLES</span></span>

### <span data-ttu-id="800f3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="800f3-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="800f3-111">Ez a példa egy privát végpont-kapcsolatot hagy jóvá.</span><span class="sxs-lookup"><span data-stu-id="800f3-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="800f3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="800f3-112">PARAMETERS</span></span>

### <span data-ttu-id="800f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800f3-113">-DefaultProfile</span></span>
<span data-ttu-id="800f3-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="800f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="800f3-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="800f3-115">-Description</span></span>
<span data-ttu-id="800f3-116">A tevékenység oka.</span><span class="sxs-lookup"><span data-stu-id="800f3-116">The reason of action.</span></span>

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

### <span data-ttu-id="800f3-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="800f3-117">-Name</span></span>
<span data-ttu-id="800f3-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="800f3-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800f3-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="800f3-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="800f3-120">A magánjellegű kapcsolat erőforrástípus.</span><span class="sxs-lookup"><span data-stu-id="800f3-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800f3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="800f3-121">-ResourceGroupName</span></span>
<span data-ttu-id="800f3-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="800f3-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800f3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="800f3-123">-ResourceId</span></span>
<span data-ttu-id="800f3-124">A privát végpont-kapcsolat Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="800f3-124">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800f3-125">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="800f3-125">-ServiceName</span></span>
<span data-ttu-id="800f3-126">A privát hivatkozás szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="800f3-126">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```


### <span data-ttu-id="800f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800f3-127">CommonParameters</span></span>
<span data-ttu-id="800f3-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="800f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800f3-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="800f3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800f3-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="800f3-130">INPUTS</span></span>

### <span data-ttu-id="800f3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="800f3-131">System.String</span></span>

## <span data-ttu-id="800f3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="800f3-132">OUTPUTS</span></span>

### <span data-ttu-id="800f3-133">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="800f3-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="800f3-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="800f3-134">NOTES</span></span>

## <span data-ttu-id="800f3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="800f3-135">RELATED LINKS</span></span>

[<span data-ttu-id="800f3-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="800f3-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="800f3-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="800f3-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="800f3-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="800f3-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="800f3-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="800f3-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)