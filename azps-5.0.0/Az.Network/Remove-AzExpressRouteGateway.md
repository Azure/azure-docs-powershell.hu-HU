---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185960"
---
# <span data-ttu-id="e6a83-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="e6a83-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="e6a83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6a83-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a83-103">Az Remove-AzExpressRouteGateway parancsmag eltávolítja az Azure ExpressRoute átjárót.</span><span class="sxs-lookup"><span data-stu-id="e6a83-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="e6a83-104">Ez egy átjáró, amely az Azure Virtual WAN szoftver által definiált kapcsolatára vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="e6a83-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="e6a83-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6a83-105">SYNTAX</span></span>

### <span data-ttu-id="e6a83-106">ByExpressRouteGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6a83-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a83-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e6a83-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a83-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e6a83-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a83-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6a83-109">DESCRIPTION</span></span>
<span data-ttu-id="e6a83-110">Az Remove-AzExpressRouteGateway parancsmag eltávolítja az Azure ExpressRoute átjárót.</span><span class="sxs-lookup"><span data-stu-id="e6a83-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="e6a83-111">Ez egy átjáró, amely az Azure Virtual WAN szoftver által definiált kapcsolatára vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="e6a83-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="e6a83-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e6a83-112">EXAMPLES</span></span>

### <span data-ttu-id="e6a83-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6a83-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="e6a83-114">Ez a példa létrehoz egy erőforráscsoportot, a virtuális WAN-ot, a virtuális hubot, a skálázható ExpressRoute-átjárót Közép-amerikai, majd azonnal törli.</span><span class="sxs-lookup"><span data-stu-id="e6a83-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="e6a83-115">Ha szeretné, hogy a virtuális átjáró törlésekor a kérdés ne legyen letiltva, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="e6a83-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="e6a83-116">Ezzel törli a ExpressRouteGateway és a hozzá társított összes ExpressRouteConnections.</span><span class="sxs-lookup"><span data-stu-id="e6a83-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="e6a83-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="e6a83-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="e6a83-118">Ez a példa létrehoz egy erőforráscsoportot, a virtuális WAN-ot, a virtuális hub-ot, a skálázható ExpressRoute-átjárót a Nyugat-középen, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="e6a83-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="e6a83-119">Ez a törlés a PowerShell-csővezetékek használatával történik, amely a Get-AzExpressRouteGateway parancs által visszaadott ExpressRouteGateway objektumot használja.</span><span class="sxs-lookup"><span data-stu-id="e6a83-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="e6a83-120">Ha szeretné, hogy a virtuális átjáró törlésekor a kérdés ne legyen letiltva, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="e6a83-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="e6a83-121">Ezzel törli a ExpressRouteGateway és a hozzá társított összes ExpressRouteConnections.</span><span class="sxs-lookup"><span data-stu-id="e6a83-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="e6a83-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6a83-122">PARAMETERS</span></span>

### <span data-ttu-id="e6a83-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a83-123">-DefaultProfile</span></span>
<span data-ttu-id="e6a83-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6a83-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6a83-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e6a83-125">-Force</span></span>
<span data-ttu-id="e6a83-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6a83-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e6a83-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6a83-127">-InputObject</span></span>
<span data-ttu-id="e6a83-128">A törlendő ExpressRouteGateway objektum.</span><span class="sxs-lookup"><span data-stu-id="e6a83-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="e6a83-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6a83-129">-Name</span></span>
<span data-ttu-id="e6a83-130">A ExpressRouteGateway neve.</span><span class="sxs-lookup"><span data-stu-id="e6a83-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a83-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6a83-131">-PassThru</span></span>
<span data-ttu-id="e6a83-132">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e6a83-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e6a83-133">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e6a83-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6a83-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a83-134">-ResourceGroupName</span></span>
<span data-ttu-id="e6a83-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6a83-135">The resource group name.</span></span>

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

### <span data-ttu-id="e6a83-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6a83-136">-ResourceId</span></span>
<span data-ttu-id="e6a83-137">A törlendő ExpressRouteGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="e6a83-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a83-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6a83-138">-Confirm</span></span>
<span data-ttu-id="e6a83-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6a83-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a83-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a83-140">-WhatIf</span></span>
<span data-ttu-id="e6a83-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6a83-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6a83-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6a83-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a83-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a83-143">CommonParameters</span></span>
<span data-ttu-id="e6a83-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6a83-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a83-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a83-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a83-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6a83-146">INPUTS</span></span>

### <span data-ttu-id="e6a83-147">Microsoft. Azure. commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="e6a83-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="e6a83-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e6a83-148">System.String</span></span>

## <span data-ttu-id="e6a83-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6a83-149">OUTPUTS</span></span>

### <span data-ttu-id="e6a83-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6a83-150">System.Boolean</span></span>

## <span data-ttu-id="e6a83-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6a83-151">NOTES</span></span>

## <span data-ttu-id="e6a83-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6a83-152">RELATED LINKS</span></span>