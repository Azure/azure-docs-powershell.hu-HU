---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: c72af57f860dcc1c889ecf81111341fa7dbe21eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837927"
---
# <span data-ttu-id="0cb7c-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0cb7c-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="0cb7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0cb7c-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb7c-103">Privát végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="0cb7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0cb7c-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cb7c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0cb7c-105">DESCRIPTION</span></span>
<span data-ttu-id="0cb7c-106">A **New-AzPrivateEndpoint** parancsmag létrehoz egy privát végpontot.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="0cb7c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0cb7c-107">EXAMPLES</span></span>

### <span data-ttu-id="0cb7c-108">1: privát végpont létrehozása</span><span class="sxs-lookup"><span data-stu-id="0cb7c-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="0cb7c-109">Ez a példa olyan privát végpontot hoz létre, amelyben a virtuális hálózat meghatározott alhálózata egy adott alhálózatban van.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="0cb7c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0cb7c-110">PARAMETERS</span></span>

### <span data-ttu-id="0cb7c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cb7c-111">-AsJob</span></span>
<span data-ttu-id="0cb7c-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0cb7c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0cb7c-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="0cb7c-113">-ByManualRequest</span></span>
<span data-ttu-id="0cb7c-114">Kézi kérés használata.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-114">Using manual request.</span></span>

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

### <span data-ttu-id="0cb7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb7c-115">-DefaultProfile</span></span>
<span data-ttu-id="0cb7c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cb7c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0cb7c-117">-Force</span></span>
<span data-ttu-id="0cb7c-118">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0cb7c-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="0cb7c-119">-Location</span></span>
<span data-ttu-id="0cb7c-120">helyre.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-120">location.</span></span>

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

### <span data-ttu-id="0cb7c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0cb7c-121">-Name</span></span>
<span data-ttu-id="0cb7c-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cb7c-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0cb7c-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="0cb7c-124">A privát kapcsolat szolgáltatás kapcsolata.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-124">The private link service connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cb7c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cb7c-125">-ResourceGroupName</span></span>
<span data-ttu-id="0cb7c-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-126">The resource group name.</span></span>

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

### <span data-ttu-id="0cb7c-127">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="0cb7c-127">-Subnet</span></span>
<span data-ttu-id="0cb7c-128">A privát végpont alhálózata</span><span class="sxs-lookup"><span data-stu-id="0cb7c-128">The subnet of the private endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cb7c-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="0cb7c-129">-Tag</span></span>
<span data-ttu-id="0cb7c-130">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0cb7c-131">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="0cb7c-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cb7c-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0cb7c-132">-Confirm</span></span>
<span data-ttu-id="0cb7c-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cb7c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cb7c-134">-WhatIf</span></span>
<span data-ttu-id="0cb7c-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cb7c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cb7c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb7c-137">CommonParameters</span></span>
<span data-ttu-id="0cb7c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0cb7c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb7c-139">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb7c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cb7c-140">INPUTS</span></span>

### <span data-ttu-id="0cb7c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0cb7c-141">System.String</span></span>

### <span data-ttu-id="0cb7c-142">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="0cb7c-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="0cb7c-143">Microsoft. Azure. commands. Network. models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="0cb7c-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="0cb7c-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cb7c-144">OUTPUTS</span></span>

### <span data-ttu-id="0cb7c-145">Microsoft. Azure. commands. Network. models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0cb7c-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="0cb7c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0cb7c-146">NOTES</span></span>

## <span data-ttu-id="0cb7c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cb7c-147">RELATED LINKS</span></span>

[<span data-ttu-id="0cb7c-148">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0cb7c-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="0cb7c-149">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0cb7c-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="0cb7c-150">Új – AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0cb7c-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)