---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 1e13cad885d18d8c15a033ae85b340041107cdc0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301787"
---
# <span data-ttu-id="6f9f3-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6f9f3-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="6f9f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9f3-103">Az Remove-AzVpnGateway parancsmag eltávolítja az Azure VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="6f9f3-104">Ez egy átjáró, amely az Azure Virtual WAN szoftver által definiált kapcsolatára vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="6f9f3-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f9f3-105">SYNTAX</span></span>

### <span data-ttu-id="6f9f3-106">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f9f3-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9f3-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6f9f3-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9f3-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6f9f3-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f9f3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f9f3-109">DESCRIPTION</span></span>
<span data-ttu-id="6f9f3-110">Az Remove-AzVpnGateway parancsmag eltávolítja az Azure VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="6f9f3-111">Ez egy átjáró, amely az Azure Virtual WAN szoftver által definiált kapcsolatára vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="6f9f3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="6f9f3-112">EXAMPLES</span></span>

### <span data-ttu-id="6f9f3-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6f9f3-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="6f9f3-114">Ez a példa létrehoz egy erőforráscsoport, virtuális WAN, virtuális hub, skálázható VPN-átjáró Közép-amerikai, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="6f9f3-115">Ha szeretné, hogy a virtuális átjáró törlésekor a kérdés ne legyen letiltva, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="6f9f3-116">Ezzel törli a VpnGateway és a hozzá társított összes VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="6f9f3-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="6f9f3-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="6f9f3-118">Ez a példa létrehoz egy erőforráscsoport, virtuális WAN, virtuális hub, skálázható VPN-átjáró Közép-amerikai, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="6f9f3-119">Ez a törlés a PowerShell-csővezetékek használatával történik, amely a Get-AzVpnGateway parancs által visszaadott VpnGateway objektumot használja.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="6f9f3-120">Ha szeretné, hogy a virtuális átjáró törlésekor a kérdés ne legyen letiltva, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="6f9f3-121">Ezzel törli a VpnGateway és a hozzá társított összes VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="6f9f3-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f9f3-122">PARAMETERS</span></span>

### <span data-ttu-id="6f9f3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9f3-123">-DefaultProfile</span></span>
<span data-ttu-id="6f9f3-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f9f3-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6f9f3-125">-Force</span></span>
<span data-ttu-id="6f9f3-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6f9f3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f9f3-127">-InputObject</span></span>
<span data-ttu-id="6f9f3-128">A törlendő vpnGateway objektum.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f3-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f9f3-129">-Name</span></span>
<span data-ttu-id="6f9f3-130">A vpnGateway neve.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f9f3-131">-PassThru</span></span>
<span data-ttu-id="6f9f3-132">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6f9f3-133">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6f9f3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9f3-134">-ResourceGroupName</span></span>
<span data-ttu-id="6f9f3-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f3-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f9f3-136">-ResourceId</span></span>
<span data-ttu-id="6f9f3-137">A törlendő vpnGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f3-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6f9f3-138">-Confirm</span></span>
<span data-ttu-id="6f9f3-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f9f3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f9f3-140">-WhatIf</span></span>
<span data-ttu-id="6f9f3-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f9f3-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6f9f3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f9f3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9f3-143">CommonParameters</span></span>
<span data-ttu-id="6f9f3-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f9f3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9f3-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f9f3-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9f3-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f9f3-146">INPUTS</span></span>

### <span data-ttu-id="6f9f3-147">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6f9f3-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="6f9f3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6f9f3-148">System.String</span></span>

## <span data-ttu-id="6f9f3-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f9f3-149">OUTPUTS</span></span>

### <span data-ttu-id="6f9f3-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f9f3-150">System.Boolean</span></span>

## <span data-ttu-id="6f9f3-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f9f3-151">NOTES</span></span>

## <span data-ttu-id="6f9f3-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f9f3-152">RELATED LINKS</span></span>

[<span data-ttu-id="6f9f3-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6f9f3-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="6f9f3-154">Új – AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6f9f3-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="6f9f3-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6f9f3-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
