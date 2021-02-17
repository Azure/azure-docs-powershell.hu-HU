---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 1e13cad885d18d8c15a033ae85b340041107cdc0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158914"
---
# <span data-ttu-id="eb864-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="eb864-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="eb864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb864-102">SYNOPSIS</span></span>
<span data-ttu-id="eb864-103">A Remove-AzVpnGateway parancsmag eltávolítja az Azure VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="eb864-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="eb864-104">Ez egy olyan átjáró, amely az Azure Virtual WAN szoftverrel definiált kapcsolatát használja.</span><span class="sxs-lookup"><span data-stu-id="eb864-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="eb864-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eb864-105">SYNTAX</span></span>

### <span data-ttu-id="eb864-106">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb864-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb864-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="eb864-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb864-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="eb864-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb864-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eb864-109">DESCRIPTION</span></span>
<span data-ttu-id="eb864-110">A Remove-AzVpnGateway parancsmag eltávolítja az Azure VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="eb864-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="eb864-111">Ez egy azure virtual WAN szoftverrel definiált kapcsolatra jellemző átjáró.</span><span class="sxs-lookup"><span data-stu-id="eb864-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="eb864-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eb864-112">EXAMPLES</span></span>

### <span data-ttu-id="eb864-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="eb864-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="eb864-114">Ebben a példában létrehoz egy Erőforrás csoportot (Virtual WAN, Virtual Hub, scalable VPN gateway in Central US, and immediately deletes it).</span><span class="sxs-lookup"><span data-stu-id="eb864-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="eb864-115">A virtuális átjáró törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="eb864-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="eb864-116">Ezzel törli a VpnGatewayt és a hozzá csatolt Összes VpnConnectiont.</span><span class="sxs-lookup"><span data-stu-id="eb864-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="eb864-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="eb864-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="eb864-118">Ebben a példában létrehoz egy Erőforrás csoportot (Virtual WAN, Virtual Hub, scalable VPN gateway in Central US, and immediately deletes it).</span><span class="sxs-lookup"><span data-stu-id="eb864-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="eb864-119">Ez a törlés powershell-pipázás használatával történik, amely a windowsos parancs által visszaadott VpnGateway Get-AzVpnGateway használ.</span><span class="sxs-lookup"><span data-stu-id="eb864-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="eb864-120">A virtuális átjáró törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="eb864-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="eb864-121">Ezzel törli a VpnGatewayt és a hozzá csatolt Összes VpnConnectiont.</span><span class="sxs-lookup"><span data-stu-id="eb864-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="eb864-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb864-122">PARAMETERS</span></span>

### <span data-ttu-id="eb864-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb864-123">-DefaultProfile</span></span>
<span data-ttu-id="eb864-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb864-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb864-125">-Force</span><span class="sxs-lookup"><span data-stu-id="eb864-125">-Force</span></span>
<span data-ttu-id="eb864-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb864-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eb864-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb864-127">-InputObject</span></span>
<span data-ttu-id="eb864-128">A vpnGateway-objektum, amit törölni kell.</span><span class="sxs-lookup"><span data-stu-id="eb864-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="eb864-129">-Name</span><span class="sxs-lookup"><span data-stu-id="eb864-129">-Name</span></span>
<span data-ttu-id="eb864-130">A vpnGateway neve.</span><span class="sxs-lookup"><span data-stu-id="eb864-130">The vpnGateway name.</span></span>

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

### <span data-ttu-id="eb864-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb864-131">-PassThru</span></span>
<span data-ttu-id="eb864-132">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="eb864-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eb864-133">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="eb864-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb864-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb864-134">-ResourceGroupName</span></span>
<span data-ttu-id="eb864-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eb864-135">The resource group name.</span></span>

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

### <span data-ttu-id="eb864-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb864-136">-ResourceId</span></span>
<span data-ttu-id="eb864-137">A vpnGateway törölt Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="eb864-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="eb864-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb864-138">-Confirm</span></span>
<span data-ttu-id="eb864-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eb864-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb864-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb864-140">-WhatIf</span></span>
<span data-ttu-id="eb864-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eb864-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb864-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb864-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb864-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb864-143">CommonParameters</span></span>
<span data-ttu-id="eb864-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb864-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb864-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb864-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb864-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb864-146">INPUTS</span></span>

### <span data-ttu-id="eb864-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="eb864-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="eb864-148">System.String</span><span class="sxs-lookup"><span data-stu-id="eb864-148">System.String</span></span>

## <span data-ttu-id="eb864-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb864-149">OUTPUTS</span></span>

### <span data-ttu-id="eb864-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eb864-150">System.Boolean</span></span>

## <span data-ttu-id="eb864-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eb864-151">NOTES</span></span>

## <span data-ttu-id="eb864-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb864-152">RELATED LINKS</span></span>

[<span data-ttu-id="eb864-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="eb864-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="eb864-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="eb864-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="eb864-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="eb864-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
