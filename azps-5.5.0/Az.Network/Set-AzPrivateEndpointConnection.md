---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160587"
---
# <span data-ttu-id="364fe-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="364fe-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="364fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="364fe-102">SYNOPSIS</span></span>
<span data-ttu-id="364fe-103">Egy privát végpont kapcsolati állapotát frissíti a privát hivatkozásszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="364fe-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="364fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="364fe-104">SYNTAX</span></span>

### <span data-ttu-id="364fe-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="364fe-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="364fe-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="364fe-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="364fe-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="364fe-107">DESCRIPTION</span></span>
<span data-ttu-id="364fe-108">A **Set-AzPrivateEndpointConnection** parancsmag frissíti a magánjellegű végpontkapcsolat állapotát egy privát hivatkozásszolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="364fe-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="364fe-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="364fe-109">EXAMPLES</span></span>

### <span data-ttu-id="364fe-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="364fe-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="364fe-111">Ebben a példában egy privát végpont kapcsolati állapotát Jóváhagyva állapotra frissíti.</span><span class="sxs-lookup"><span data-stu-id="364fe-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="364fe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="364fe-112">PARAMETERS</span></span>

### <span data-ttu-id="364fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364fe-113">-DefaultProfile</span></span>
<span data-ttu-id="364fe-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="364fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="364fe-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="364fe-115">-Description</span></span>
<span data-ttu-id="364fe-116">A művelet oka.</span><span class="sxs-lookup"><span data-stu-id="364fe-116">The reason of action.</span></span>

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

### <span data-ttu-id="364fe-117">-Name</span><span class="sxs-lookup"><span data-stu-id="364fe-117">-Name</span></span>
<span data-ttu-id="364fe-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="364fe-118">The resource name.</span></span>

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

### <span data-ttu-id="364fe-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="364fe-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="364fe-120">A privát csatolás erőforrástípusa.</span><span class="sxs-lookup"><span data-stu-id="364fe-120">The private link resource type.</span></span>

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

### <span data-ttu-id="364fe-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="364fe-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="364fe-122">Jóváhagyta vagy elutasította az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="364fe-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="364fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="364fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="364fe-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="364fe-124">The resource group name.</span></span>

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

### <span data-ttu-id="364fe-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="364fe-125">-ResourceId</span></span>
<span data-ttu-id="364fe-126">A privát végpontkapcsolat Azure-erőforrás-kezelői azonosítója.</span><span class="sxs-lookup"><span data-stu-id="364fe-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="364fe-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="364fe-127">-ServiceName</span></span>
<span data-ttu-id="364fe-128">A magánjellegű hivatkozásszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="364fe-128">The private link service name.</span></span>

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

### <span data-ttu-id="364fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364fe-129">CommonParameters</span></span>
<span data-ttu-id="364fe-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="364fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364fe-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="364fe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364fe-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="364fe-132">INPUTS</span></span>

### <span data-ttu-id="364fe-133">System.String</span><span class="sxs-lookup"><span data-stu-id="364fe-133">System.String</span></span>

## <span data-ttu-id="364fe-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="364fe-134">OUTPUTS</span></span>

### <span data-ttu-id="364fe-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="364fe-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="364fe-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="364fe-136">NOTES</span></span>

## <span data-ttu-id="364fe-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="364fe-137">RELATED LINKS</span></span>

[<span data-ttu-id="364fe-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="364fe-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="364fe-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="364fe-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="364fe-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="364fe-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="364fe-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="364fe-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)