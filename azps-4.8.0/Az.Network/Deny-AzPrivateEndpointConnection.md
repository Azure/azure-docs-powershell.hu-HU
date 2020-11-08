---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025230"
---
# <span data-ttu-id="48d31-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48d31-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="48d31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48d31-102">SYNOPSIS</span></span>
<span data-ttu-id="48d31-103">privát végpont-kapcsolat megtagadását.</span><span class="sxs-lookup"><span data-stu-id="48d31-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="48d31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48d31-104">SYNTAX</span></span>

### <span data-ttu-id="48d31-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48d31-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d31-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="48d31-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48d31-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="48d31-107">DESCRIPTION</span></span>
<span data-ttu-id="48d31-108">A **deny-AzPrivateEndpointConnection** parancsmag megtagadja a privát végpontos kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="48d31-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="48d31-109">Példák</span><span class="sxs-lookup"><span data-stu-id="48d31-109">EXAMPLES</span></span>

### <span data-ttu-id="48d31-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="48d31-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="48d31-111">Ez a példa a privát végpontok közötti kapcsolatot tagadja meg.</span><span class="sxs-lookup"><span data-stu-id="48d31-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="48d31-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48d31-112">PARAMETERS</span></span>

### <span data-ttu-id="48d31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d31-113">-DefaultProfile</span></span>
<span data-ttu-id="48d31-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48d31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d31-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="48d31-115">-Description</span></span>
<span data-ttu-id="48d31-116">A tevékenység oka.</span><span class="sxs-lookup"><span data-stu-id="48d31-116">The reason of action.</span></span>

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

### <span data-ttu-id="48d31-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48d31-117">-Name</span></span>
<span data-ttu-id="48d31-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="48d31-118">The resource name.</span></span>

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

### <span data-ttu-id="48d31-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="48d31-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="48d31-120">A magánjellegű kapcsolat erőforrástípus.</span><span class="sxs-lookup"><span data-stu-id="48d31-120">The private link resource type.</span></span>

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

### <span data-ttu-id="48d31-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d31-121">-ResourceGroupName</span></span>
<span data-ttu-id="48d31-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="48d31-122">The resource group name.</span></span>

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

### <span data-ttu-id="48d31-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48d31-123">-ResourceId</span></span>
<span data-ttu-id="48d31-124">A privát végpont-kapcsolat Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="48d31-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="48d31-125">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="48d31-125">-ServiceName</span></span>
<span data-ttu-id="48d31-126">Annak a szolgáltatásnak a neve, amelyhez a privát végpont-kapcsolat tartozik.</span><span class="sxs-lookup"><span data-stu-id="48d31-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="48d31-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d31-127">CommonParameters</span></span>
<span data-ttu-id="48d31-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48d31-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d31-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="48d31-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d31-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48d31-130">INPUTS</span></span>

### <span data-ttu-id="48d31-131">System. String</span><span class="sxs-lookup"><span data-stu-id="48d31-131">System.String</span></span>

## <span data-ttu-id="48d31-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48d31-132">OUTPUTS</span></span>

### <span data-ttu-id="48d31-133">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="48d31-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="48d31-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48d31-134">NOTES</span></span>

## <span data-ttu-id="48d31-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48d31-135">RELATED LINKS</span></span>

[<span data-ttu-id="48d31-136">Jóváhagyás – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48d31-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="48d31-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48d31-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="48d31-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48d31-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="48d31-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48d31-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)