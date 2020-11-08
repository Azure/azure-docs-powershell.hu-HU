---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013095"
---
# <span data-ttu-id="7be8e-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7be8e-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="7be8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7be8e-102">SYNOPSIS</span></span>
<span data-ttu-id="7be8e-103">Privát végpont-kapcsolati állapotot frissít a privát hivatkozás szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="7be8e-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="7be8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7be8e-104">SYNTAX</span></span>

### <span data-ttu-id="7be8e-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7be8e-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be8e-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="7be8e-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7be8e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7be8e-107">DESCRIPTION</span></span>
<span data-ttu-id="7be8e-108">A **set-AzPrivateEndpointConnection** parancsmag privát végpont-kapcsolati állapotot frissít egy privát hivatkozás szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="7be8e-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="7be8e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7be8e-109">EXAMPLES</span></span>

### <span data-ttu-id="7be8e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7be8e-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="7be8e-111">Ez a példa egy privát végpontos kapcsolati állapotot frissít a jóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="7be8e-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="7be8e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7be8e-112">PARAMETERS</span></span>

### <span data-ttu-id="7be8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be8e-113">-DefaultProfile</span></span>
<span data-ttu-id="7be8e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7be8e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7be8e-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7be8e-115">-Description</span></span>
<span data-ttu-id="7be8e-116">A tevékenység oka.</span><span class="sxs-lookup"><span data-stu-id="7be8e-116">The reason of action.</span></span>

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

### <span data-ttu-id="7be8e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7be8e-117">-Name</span></span>
<span data-ttu-id="7be8e-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7be8e-118">The resource name.</span></span>

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

### <span data-ttu-id="7be8e-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="7be8e-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="7be8e-120">A magánjellegű kapcsolat erőforrástípus.</span><span class="sxs-lookup"><span data-stu-id="7be8e-120">The private link resource type.</span></span>

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

### <span data-ttu-id="7be8e-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="7be8e-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="7be8e-122">Jóváhagyta vagy visszautasította az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="7be8e-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="7be8e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be8e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7be8e-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7be8e-124">The resource group name.</span></span>

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

### <span data-ttu-id="7be8e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7be8e-125">-ResourceId</span></span>
<span data-ttu-id="7be8e-126">A privát végpont-kapcsolat Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="7be8e-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="7be8e-127">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="7be8e-127">-ServiceName</span></span>
<span data-ttu-id="7be8e-128">A privát hivatkozás szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="7be8e-128">The private link service name.</span></span>

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

### <span data-ttu-id="7be8e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be8e-129">CommonParameters</span></span>
<span data-ttu-id="7be8e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7be8e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be8e-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7be8e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be8e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7be8e-132">INPUTS</span></span>

### <span data-ttu-id="7be8e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7be8e-133">System.String</span></span>

## <span data-ttu-id="7be8e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7be8e-134">OUTPUTS</span></span>

### <span data-ttu-id="7be8e-135">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7be8e-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="7be8e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7be8e-136">NOTES</span></span>

## <span data-ttu-id="7be8e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7be8e-137">RELATED LINKS</span></span>

[<span data-ttu-id="7be8e-138">Jóváhagyás – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7be8e-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7be8e-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7be8e-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7be8e-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7be8e-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7be8e-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7be8e-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)