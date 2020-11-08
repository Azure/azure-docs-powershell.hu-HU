---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194540"
---
# <span data-ttu-id="4c91c-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c91c-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="4c91c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c91c-102">SYNOPSIS</span></span>
<span data-ttu-id="4c91c-103">Privát végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4c91c-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="4c91c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c91c-104">SYNTAX</span></span>

### <span data-ttu-id="4c91c-105">Minden</span><span class="sxs-lookup"><span data-stu-id="4c91c-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c91c-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c91c-106">DESCRIPTION</span></span>

<span data-ttu-id="4c91c-107">A **New-AzPrivateEndpoint** parancsmag létrehoz egy privát végpontot.</span><span class="sxs-lookup"><span data-stu-id="4c91c-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="4c91c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4c91c-108">EXAMPLES</span></span>

### <span data-ttu-id="4c91c-109">Példa 1: privát végpont létrehozása</span><span class="sxs-lookup"><span data-stu-id="4c91c-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="4c91c-110">A következő példa létrehoz egy privát végpontot egy adott privát hivatkozás-szolgáltatási AZONOSÍTÓval egy virtuális hálózat meghatározott alhálózatában.</span><span class="sxs-lookup"><span data-stu-id="4c91c-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="4c91c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c91c-111">PARAMETERS</span></span>

### <span data-ttu-id="4c91c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c91c-112">-AsJob</span></span>

<span data-ttu-id="4c91c-113">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="4c91c-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="4c91c-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="4c91c-114">-ByManualRequest</span></span>

<span data-ttu-id="4c91c-115">A kapcsolat létrehozásához kézi kérést kell használni.</span><span class="sxs-lookup"><span data-stu-id="4c91c-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="4c91c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c91c-116">-DefaultProfile</span></span>

<span data-ttu-id="4c91c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c91c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c91c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4c91c-118">-Force</span></span>

<span data-ttu-id="4c91c-119">Ne kérjen megerősítést az erőforrás felülírásához.</span><span class="sxs-lookup"><span data-stu-id="4c91c-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="4c91c-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="4c91c-120">-Location</span></span>

<span data-ttu-id="4c91c-121">A privát végpont helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c91c-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="4c91c-122">Használja a [Get-AzLocation](/powershell/module/az.resources/get-azlocation) a paraméter érvényes értékeinek meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="4c91c-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="4c91c-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c91c-123">-Name</span></span>

<span data-ttu-id="4c91c-124">A privát végpont neve</span><span class="sxs-lookup"><span data-stu-id="4c91c-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="4c91c-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="4c91c-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="4c91c-126">Az erőforrás azonosítója a privát végponthoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="4c91c-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="4c91c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c91c-127">-ResourceGroupName</span></span>

<span data-ttu-id="4c91c-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c91c-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4c91c-129">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="4c91c-129">-Subnet</span></span>

<span data-ttu-id="4c91c-130">A magánjellegű végpont alhálózata.</span><span class="sxs-lookup"><span data-stu-id="4c91c-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="4c91c-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="4c91c-131">-Tag</span></span>

<span data-ttu-id="4c91c-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="4c91c-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4c91c-133">Például: @ {key0 = ' value0 '; key1 = $null; azonosító2 = ' érték2 '}</span><span class="sxs-lookup"><span data-stu-id="4c91c-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="4c91c-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4c91c-134">-Confirm</span></span>

<span data-ttu-id="4c91c-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4c91c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c91c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c91c-136">-WhatIf</span></span>

<span data-ttu-id="4c91c-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4c91c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c91c-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c91c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c91c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c91c-139">CommonParameters</span></span>

<span data-ttu-id="4c91c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c91c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c91c-141">További információt a [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4c91c-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="4c91c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c91c-142">INPUTS</span></span>

### <span data-ttu-id="4c91c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4c91c-143">System.String</span></span>

### <span data-ttu-id="4c91c-144">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="4c91c-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="4c91c-145">Microsoft. Azure. commands. Network. models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="4c91c-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="4c91c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c91c-146">OUTPUTS</span></span>

### <span data-ttu-id="4c91c-147">Microsoft. Azure. commands. Network. models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c91c-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="4c91c-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c91c-148">NOTES</span></span>

## <span data-ttu-id="4c91c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c91c-149">RELATED LINKS</span></span>

[<span data-ttu-id="4c91c-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c91c-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="4c91c-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c91c-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="4c91c-152">Új – AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="4c91c-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)