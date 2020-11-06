---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
ms.openlocfilehash: 34e143b3ca6114fd90d52a5ad6ee8c022fda5688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503491"
---
# <span data-ttu-id="ea815-101">Remove-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ea815-101">Remove-AzureRmVpnGateway</span></span>

## <span data-ttu-id="ea815-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea815-102">SYNOPSIS</span></span>
<span data-ttu-id="ea815-103">Az Remove-AzureRmVpnGateway parancsmag eltávolítja az Azure VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="ea815-103">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="ea815-104">Ez egy átjáró, amely az Azure Virtual WAN szoftver által definiált kapcsolatára vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="ea815-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea815-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea815-105">SYNTAX</span></span>

### <span data-ttu-id="ea815-106">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea815-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea815-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ea815-107">ByVpnGatewayObject</span></span>
```
Remove-AzureRmVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea815-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ea815-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzureRmVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea815-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea815-109">DESCRIPTION</span></span>
<span data-ttu-id="ea815-110">Az Remove-AzureRmVpnGateway parancsmag eltávolítja az Azure VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="ea815-110">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="ea815-111">Ez egy átjáró, amely az Azure Virtual WAN szoftver által definiált kapcsolatára vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="ea815-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="ea815-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ea815-112">EXAMPLES</span></span>

### <span data-ttu-id="ea815-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ea815-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="ea815-114">Ez a példa létrehoz egy erőforráscsoport, virtuális WAN, virtuális hub, skálázható VPN-átjáró Közép-amerikai, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="ea815-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="ea815-115">Ha szeretné, hogy a virtuális átjáró törlésekor a kérdés ne legyen letiltva, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="ea815-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="ea815-116">Ezzel törli a VpnGateway és a hozzá társított összes VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="ea815-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="ea815-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="ea815-117">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzureRmVpnGateway-Passthru
```

<span data-ttu-id="ea815-118">Ez a példa létrehoz egy erőforráscsoport, virtuális WAN, virtuális hub, skálázható VPN-átjáró Közép-amerikai, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="ea815-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="ea815-119">Ez a törlés a PowerShell-csővezetékek használatával történik, amely a Get-AzureRmVpnGateway parancs által visszaadott VpnGateway objektumot használja.</span><span class="sxs-lookup"><span data-stu-id="ea815-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzureRmVpnGateway command.</span></span>
<span data-ttu-id="ea815-120">Ha szeretné, hogy a virtuális átjáró törlésekor a kérdés ne legyen letiltva, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="ea815-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="ea815-121">Ezzel törli a VpnGateway és a hozzá társított összes VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="ea815-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="ea815-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea815-122">PARAMETERS</span></span>

### <span data-ttu-id="ea815-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea815-123">-DefaultProfile</span></span>
<span data-ttu-id="ea815-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea815-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea815-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ea815-125">-Force</span></span>
<span data-ttu-id="ea815-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea815-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ea815-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea815-127">-InputObject</span></span>
<span data-ttu-id="ea815-128">A törlendő vpnGateway objektum.</span><span class="sxs-lookup"><span data-stu-id="ea815-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="ea815-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea815-129">-Name</span></span>
<span data-ttu-id="ea815-130">A vpnGateway neve.</span><span class="sxs-lookup"><span data-stu-id="ea815-130">The vpnGateway name.</span></span>

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

### <span data-ttu-id="ea815-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea815-131">-PassThru</span></span>
<span data-ttu-id="ea815-132">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ea815-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ea815-133">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ea815-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea815-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea815-134">-ResourceGroupName</span></span>
<span data-ttu-id="ea815-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ea815-135">The resource group name.</span></span>

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

### <span data-ttu-id="ea815-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea815-136">-ResourceId</span></span>
<span data-ttu-id="ea815-137">A törlendő vpnGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="ea815-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="ea815-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea815-138">-Confirm</span></span>
<span data-ttu-id="ea815-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea815-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea815-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea815-140">-WhatIf</span></span>
<span data-ttu-id="ea815-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ea815-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea815-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea815-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea815-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea815-143">CommonParameters</span></span>
<span data-ttu-id="ea815-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea815-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea815-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea815-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea815-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea815-146">INPUTS</span></span>

### <span data-ttu-id="ea815-147">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ea815-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="ea815-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ea815-148">System.String</span></span>

## <span data-ttu-id="ea815-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea815-149">OUTPUTS</span></span>

### <span data-ttu-id="ea815-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea815-150">System.Boolean</span></span>

## <span data-ttu-id="ea815-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea815-151">NOTES</span></span>

## <span data-ttu-id="ea815-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea815-152">RELATED LINKS</span></span>
