---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: c3d311cc091026bcd08225e5a11a8232102a03a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670017"
---
# <span data-ttu-id="4e68b-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="4e68b-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="4e68b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e68b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e68b-103">Méretezhető ExpressRoute-átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="4e68b-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="4e68b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e68b-104">SYNTAX</span></span>

### <span data-ttu-id="4e68b-105">ByExpressRouteGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e68b-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 -MaxScaleUnits <UInt32> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e68b-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4e68b-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e68b-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4e68b-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e68b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e68b-108">DESCRIPTION</span></span>

<span data-ttu-id="4e68b-109">Set-AzExpressRouteGateway frissíti a ExpressRouteGateway tartozó méretarányos mértékegységeket.</span><span class="sxs-lookup"><span data-stu-id="4e68b-109">Set-AzExpressRouteGateway updates the scale units for the ExpressRouteGateway</span></span>

## <span data-ttu-id="4e68b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4e68b-110">EXAMPLES</span></span>

### <span data-ttu-id="4e68b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4e68b-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="4e68b-112">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="4e68b-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4e68b-113">Ezt követően létrejön egy ExpressRoute-átjáró a virtuális központban, 2 léptékű egységgel, amelyet ezután 3 léptékű egységre kell módosítani.</span><span class="sxs-lookup"><span data-stu-id="4e68b-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="4e68b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e68b-114">PARAMETERS</span></span>

### <span data-ttu-id="4e68b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e68b-115">-AsJob</span></span>
<span data-ttu-id="4e68b-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4e68b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e68b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e68b-117">-DefaultProfile</span></span>
<span data-ttu-id="4e68b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e68b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e68b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e68b-119">-InputObject</span></span>
<span data-ttu-id="4e68b-120">A ExpressRouteGateway frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="4e68b-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68b-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="4e68b-121">-MaxScaleUnits</span></span>
<span data-ttu-id="4e68b-122">A ExpressRouteGateway léptékének maximális száma.</span><span class="sxs-lookup"><span data-stu-id="4e68b-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="4e68b-123">Érvényes tartományok > 2</span><span class="sxs-lookup"><span data-stu-id="4e68b-123">Valid range > 2</span></span>

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

### <span data-ttu-id="4e68b-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="4e68b-124">-MinScaleUnits</span></span>
<span data-ttu-id="4e68b-125">Az adott ExpressRouteGateway tartozó méretarányok minimális száma.</span><span class="sxs-lookup"><span data-stu-id="4e68b-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="4e68b-126">Érvényes tartományok > 2</span><span class="sxs-lookup"><span data-stu-id="4e68b-126">Valid range > 2</span></span>

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

### <span data-ttu-id="4e68b-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e68b-127">-Name</span></span>
<span data-ttu-id="4e68b-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4e68b-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e68b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e68b-129">-ResourceGroupName</span></span>
<span data-ttu-id="4e68b-130">A frissítendő ExpressRouteGateway erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4e68b-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e68b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e68b-131">-ResourceId</span></span>
<span data-ttu-id="4e68b-132">Annak a ExpressRouteGateway a azonosítója, amelyet frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="4e68b-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68b-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="4e68b-133">-Tag</span></span>
<span data-ttu-id="4e68b-134">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4e68b-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4e68b-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e68b-135">-Confirm</span></span>
<span data-ttu-id="4e68b-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e68b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e68b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e68b-137">-WhatIf</span></span>
<span data-ttu-id="4e68b-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e68b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e68b-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e68b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e68b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e68b-140">CommonParameters</span></span>
<span data-ttu-id="4e68b-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e68b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e68b-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e68b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e68b-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e68b-143">INPUTS</span></span>

### <span data-ttu-id="4e68b-144">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4e68b-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="4e68b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4e68b-145">System.String</span></span>

## <span data-ttu-id="4e68b-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e68b-146">OUTPUTS</span></span>

### <span data-ttu-id="4e68b-147">Microsoft. Azure. commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="4e68b-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="4e68b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e68b-148">NOTES</span></span>

## <span data-ttu-id="4e68b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e68b-149">RELATED LINKS</span></span>
