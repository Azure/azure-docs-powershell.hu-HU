---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194558"
---
# <span data-ttu-id="fdcb6-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fdcb6-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="fdcb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdcb6-102">SYNOPSIS</span></span>
<span data-ttu-id="fdcb6-103">Privát végpont-kapcsolatot hagy jóvá.</span><span class="sxs-lookup"><span data-stu-id="fdcb6-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="fdcb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdcb6-104">SYNTAX</span></span>

### <span data-ttu-id="fdcb6-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fdcb6-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdcb6-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="fdcb6-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdcb6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdcb6-107">DESCRIPTION</span></span>
<span data-ttu-id="fdcb6-108">A **jóváhagyás – AzPrivateEndpointConnection** parancsmag jóváhagyja a privát végpontos kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="fdcb6-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="fdcb6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fdcb6-109">EXAMPLES</span></span>

### <span data-ttu-id="fdcb6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fdcb6-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="fdcb6-111">Ez a példa egy privát végpont-kapcsolatot hagy jóvá.</span><span class="sxs-lookup"><span data-stu-id="fdcb6-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="fdcb6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdcb6-112">PARAMETERS</span></span>

### <span data-ttu-id="fdcb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdcb6-113">-DefaultProfile</span></span>
<span data-ttu-id="fdcb6-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdcb6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdcb6-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="fdcb6-115">-Description</span></span>
<span data-ttu-id="fdcb6-116">A tevékenység oka.</span><span class="sxs-lookup"><span data-stu-id="fdcb6-116">The reason of action.</span></span>

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

### <span data-ttu-id="fdcb6-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fdcb6-117">-Name</span></span>
<span data-ttu-id="fdcb6-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="fdcb6-118">The resource name.</span></span>

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

### <span data-ttu-id="fdcb6-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="fdcb6-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="fdcb6-120">A magánjellegű kapcsolat erőforrástípus.</span><span class="sxs-lookup"><span data-stu-id="fdcb6-120">The private link resource type.</span></span>

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

### <span data-ttu-id="fdcb6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdcb6-121">-ResourceGroupName</span></span>
<span data-ttu-id="fdcb6-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fdcb6-122">The resource group name.</span></span>

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

### <span data-ttu-id="fdcb6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdcb6-123">-ResourceId</span></span>
<span data-ttu-id="fdcb6-124">A privát végpont-kapcsolat Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="fdcb6-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="fdcb6-125">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="fdcb6-125">-ServiceName</span></span>
<span data-ttu-id="fdcb6-126">A privát hivatkozás szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="fdcb6-126">The private link service name.</span></span>

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


### <span data-ttu-id="fdcb6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdcb6-127">CommonParameters</span></span>
<span data-ttu-id="fdcb6-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdcb6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdcb6-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fdcb6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdcb6-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdcb6-130">INPUTS</span></span>

### <span data-ttu-id="fdcb6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fdcb6-131">System.String</span></span>

## <span data-ttu-id="fdcb6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdcb6-132">OUTPUTS</span></span>

### <span data-ttu-id="fdcb6-133">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fdcb6-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="fdcb6-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdcb6-134">NOTES</span></span>

## <span data-ttu-id="fdcb6-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdcb6-135">RELATED LINKS</span></span>

[<span data-ttu-id="fdcb6-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fdcb6-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="fdcb6-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fdcb6-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="fdcb6-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fdcb6-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="fdcb6-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fdcb6-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)