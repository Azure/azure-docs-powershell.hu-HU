---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195372"
---
# <span data-ttu-id="d6e12-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d6e12-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="d6e12-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6e12-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e12-103">Méretezhető ExpressRoute-átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d6e12-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="d6e12-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6e12-104">SYNTAX</span></span>

### <span data-ttu-id="d6e12-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6e12-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e12-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="d6e12-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e12-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d6e12-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6e12-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6e12-108">DESCRIPTION</span></span>

<span data-ttu-id="d6e12-109">A New-AzExpressRouteGateway méretezhető ExpressRoute-átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d6e12-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="d6e12-110">Ez a szoftver által definiált kapcsolat a helyszíni Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d6e12-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="d6e12-111">Ezt az átjárót az itt vagy az Set-AzExpressRouteGateway parancsmagban megadott méretarány alapján lehet átméretezni.</span><span class="sxs-lookup"><span data-stu-id="d6e12-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="d6e12-112">Egy kapcsolat egy helyszíni ExpressRoute-áramkörről a skálázható átjáróra van állítva.</span><span class="sxs-lookup"><span data-stu-id="d6e12-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="d6e12-113">A ExpressRouteGateway ugyanabba a helyre kerül, mint a hivatkozott VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d6e12-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="d6e12-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d6e12-114">EXAMPLES</span></span>

### <span data-ttu-id="d6e12-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d6e12-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="d6e12-116">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d6e12-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d6e12-117">Ezt követően létrejön egy ExpressRoute-átjáró, amely a virtuális központban 2 léptékű egységgel jön létre.</span><span class="sxs-lookup"><span data-stu-id="d6e12-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="d6e12-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6e12-118">PARAMETERS</span></span>

### <span data-ttu-id="d6e12-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6e12-119">-AsJob</span></span>
<span data-ttu-id="d6e12-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d6e12-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6e12-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e12-121">-DefaultProfile</span></span>
<span data-ttu-id="d6e12-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6e12-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6e12-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="d6e12-123">-MaxScaleUnits</span></span>
<span data-ttu-id="d6e12-124">A ExpressRouteGateway léptékének maximális száma.</span><span class="sxs-lookup"><span data-stu-id="d6e12-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="d6e12-125">Érvényes tartományok > 2</span><span class="sxs-lookup"><span data-stu-id="d6e12-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e12-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="d6e12-126">-MinScaleUnits</span></span>
<span data-ttu-id="d6e12-127">Az adott ExpressRouteGateway tartozó méretarányok minimális száma.</span><span class="sxs-lookup"><span data-stu-id="d6e12-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="d6e12-128">Érvényes tartományok > 2</span><span class="sxs-lookup"><span data-stu-id="d6e12-128">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e12-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6e12-129">-Name</span></span>
<span data-ttu-id="d6e12-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6e12-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e12-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e12-131">-ResourceGroupName</span></span>
<span data-ttu-id="d6e12-132">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6e12-132">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e12-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="d6e12-133">-Tag</span></span>
<span data-ttu-id="d6e12-134">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d6e12-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e12-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="d6e12-135">-VirtualHub</span></span>
<span data-ttu-id="d6e12-136">A VirtualHub ehhez a VpnGateway társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d6e12-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e12-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="d6e12-137">-VirtualHubId</span></span>
<span data-ttu-id="d6e12-138">Annak a VirtualHub az azonosítóját, amelyre ezt a VpnGateway társítani kell.</span><span class="sxs-lookup"><span data-stu-id="d6e12-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e12-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="d6e12-139">-VirtualHubName</span></span>
<span data-ttu-id="d6e12-140">Annak a VirtualHub az azonosítóját, amelyre ezt a VpnGateway társítani kell.</span><span class="sxs-lookup"><span data-stu-id="d6e12-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e12-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6e12-141">-Confirm</span></span>
<span data-ttu-id="d6e12-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6e12-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6e12-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6e12-143">-WhatIf</span></span>
<span data-ttu-id="d6e12-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6e12-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6e12-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6e12-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6e12-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e12-146">CommonParameters</span></span>
<span data-ttu-id="d6e12-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6e12-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e12-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6e12-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e12-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6e12-149">INPUTS</span></span>

### <span data-ttu-id="d6e12-150">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d6e12-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d6e12-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d6e12-151">System.String</span></span>

## <span data-ttu-id="d6e12-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6e12-152">OUTPUTS</span></span>

### <span data-ttu-id="d6e12-153">Microsoft. Azure. commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d6e12-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="d6e12-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6e12-154">NOTES</span></span>

## <span data-ttu-id="d6e12-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6e12-155">RELATED LINKS</span></span>