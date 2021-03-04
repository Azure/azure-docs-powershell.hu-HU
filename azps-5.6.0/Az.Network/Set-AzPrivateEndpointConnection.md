---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7684072abbef4af8344cc07aa4bef6cab88ad3ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932354"
---
# <span data-ttu-id="9b8c2-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9b8c2-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="9b8c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b8c2-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8c2-103">Egy privát végpont kapcsolati állapotát frissíti a privát hivatkozásszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="9b8c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b8c2-104">SYNTAX</span></span>

### <span data-ttu-id="9b8c2-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b8c2-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b8c2-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="9b8c2-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b8c2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b8c2-107">DESCRIPTION</span></span>
<span data-ttu-id="9b8c2-108">A **Set-AzPrivateEndpointConnection** parancsmag frissíti a magánjellegű végpontkapcsolat állapotát egy privát hivatkozásszolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="9b8c2-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="9b8c2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b8c2-109">EXAMPLES</span></span>

### <span data-ttu-id="9b8c2-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9b8c2-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="9b8c2-111">Ebben a példában egy privát végpont kapcsolati állapotát Jóváhagyva állapotra frissíti.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="9b8c2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b8c2-112">PARAMETERS</span></span>

### <span data-ttu-id="9b8c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b8c2-113">-DefaultProfile</span></span>
<span data-ttu-id="9b8c2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b8c2-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9b8c2-115">-Description</span></span>
<span data-ttu-id="9b8c2-116">A művelet oka.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-116">The reason of action.</span></span>

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

### <span data-ttu-id="9b8c2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9b8c2-117">-Name</span></span>
<span data-ttu-id="9b8c2-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-118">The resource name.</span></span>

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

### <span data-ttu-id="9b8c2-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="9b8c2-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="9b8c2-120">A privát csatolás erőforrástípusa.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-120">The private link resource type.</span></span>

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

### <span data-ttu-id="9b8c2-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="9b8c2-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="9b8c2-122">Jóváhagyta vagy elutasította az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="9b8c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b8c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b8c2-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-124">The resource group name.</span></span>

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

### <span data-ttu-id="9b8c2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b8c2-125">-ResourceId</span></span>
<span data-ttu-id="9b8c2-126">A privát végpontkapcsolat Azure-erőforrás-kezelői azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9b8c2-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9b8c2-127">-ServiceName</span></span>
<span data-ttu-id="9b8c2-128">A privát hivatkozásszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-128">The private link service name.</span></span>

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

### <span data-ttu-id="9b8c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8c2-129">CommonParameters</span></span>
<span data-ttu-id="9b8c2-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8c2-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b8c2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8c2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b8c2-132">INPUTS</span></span>

### <span data-ttu-id="9b8c2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9b8c2-133">System.String</span></span>

## <span data-ttu-id="9b8c2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b8c2-134">OUTPUTS</span></span>

### <span data-ttu-id="9b8c2-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9b8c2-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="9b8c2-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b8c2-136">NOTES</span></span>

## <span data-ttu-id="9b8c2-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b8c2-137">RELATED LINKS</span></span>

[<span data-ttu-id="9b8c2-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9b8c2-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9b8c2-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9b8c2-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9b8c2-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9b8c2-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9b8c2-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9b8c2-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)