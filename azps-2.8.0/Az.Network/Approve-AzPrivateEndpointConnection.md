---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9b47fb1954b13e28268f6b7aad66fa8190e20584
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837397"
---
# <span data-ttu-id="793aa-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="793aa-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="793aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="793aa-102">SYNOPSIS</span></span>
<span data-ttu-id="793aa-103">Privát végpont-kapcsolatot hagy jóvá.</span><span class="sxs-lookup"><span data-stu-id="793aa-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="793aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="793aa-104">SYNTAX</span></span>

### <span data-ttu-id="793aa-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="793aa-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="793aa-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="793aa-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="793aa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="793aa-107">DESCRIPTION</span></span>
<span data-ttu-id="793aa-108">A **jóváhagyás – AzPrivateEndpointConnection** parancsmag jóváhagyja a privát végpontos kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="793aa-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="793aa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="793aa-109">EXAMPLES</span></span>

### <span data-ttu-id="793aa-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="793aa-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="793aa-111">Ez a példa egy privát végpont-kapcsolatot hagy jóvá.</span><span class="sxs-lookup"><span data-stu-id="793aa-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="793aa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="793aa-112">PARAMETERS</span></span>

### <span data-ttu-id="793aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793aa-113">-DefaultProfile</span></span>
<span data-ttu-id="793aa-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="793aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="793aa-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="793aa-115">-Description</span></span>
<span data-ttu-id="793aa-116">A tevékenység oka.</span><span class="sxs-lookup"><span data-stu-id="793aa-116">The reason of action.</span></span>

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

### <span data-ttu-id="793aa-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="793aa-117">-Name</span></span>
<span data-ttu-id="793aa-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="793aa-118">The resource name.</span></span>

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

### <span data-ttu-id="793aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="793aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="793aa-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="793aa-120">The resource group name.</span></span>

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

### <span data-ttu-id="793aa-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="793aa-121">-ResourceId</span></span>
<span data-ttu-id="793aa-122">A privát végpont-kapcsolat Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="793aa-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="793aa-123">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="793aa-123">-ServiceName</span></span>
<span data-ttu-id="793aa-124">A privát hivatkozás szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="793aa-124">The private link service name.</span></span>

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

### <span data-ttu-id="793aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793aa-125">CommonParameters</span></span>
<span data-ttu-id="793aa-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="793aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793aa-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="793aa-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793aa-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="793aa-128">INPUTS</span></span>

### <span data-ttu-id="793aa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="793aa-129">System.String</span></span>

## <span data-ttu-id="793aa-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="793aa-130">OUTPUTS</span></span>

### <span data-ttu-id="793aa-131">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="793aa-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="793aa-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="793aa-132">NOTES</span></span>

## <span data-ttu-id="793aa-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="793aa-133">RELATED LINKS</span></span>

[<span data-ttu-id="793aa-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="793aa-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="793aa-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="793aa-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="793aa-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="793aa-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)