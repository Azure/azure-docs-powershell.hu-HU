---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 825090358ea94223d483fe418d06896f1f741045
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172892"
---
# <span data-ttu-id="88e0d-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="88e0d-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="88e0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="88e0d-103">Eltávolít egy VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="88e0d-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="88e0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88e0d-104">SYNTAX</span></span>

### <span data-ttu-id="88e0d-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88e0d-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88e0d-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="88e0d-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88e0d-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="88e0d-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88e0d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="88e0d-108">DESCRIPTION</span></span>
<span data-ttu-id="88e0d-109">Eltávolít egy VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="88e0d-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="88e0d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="88e0d-110">EXAMPLES</span></span>

### <span data-ttu-id="88e0d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="88e0d-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="88e0d-112">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="88e0d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="88e0d-113">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="88e0d-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="88e0d-114">Miután létrehozta az átjárót, az a New-AzVpnConnection parancs segítségével csatlakozik a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="88e0d-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="88e0d-115">Ezután eltávolítja a kapcsolatot a kapcsolat nevével.</span><span class="sxs-lookup"><span data-stu-id="88e0d-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="88e0d-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="88e0d-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="88e0d-117">Ugyanaz, mint a példa 1, de most már eltávolítja a kapcsolatot a Get-AzVpnConnection-től a vezetékes objektummal.</span><span class="sxs-lookup"><span data-stu-id="88e0d-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="88e0d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88e0d-118">PARAMETERS</span></span>

### <span data-ttu-id="88e0d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e0d-119">-DefaultProfile</span></span>
<span data-ttu-id="88e0d-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88e0d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e0d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="88e0d-121">-Force</span></span>
<span data-ttu-id="88e0d-122">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88e0d-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="88e0d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88e0d-123">-InputObject</span></span>
<span data-ttu-id="88e0d-124">A frissítendő VpnConnection objektum.</span><span class="sxs-lookup"><span data-stu-id="88e0d-124">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88e0d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88e0d-125">-Name</span></span>
<span data-ttu-id="88e0d-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="88e0d-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e0d-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="88e0d-127">-ParentResourceName</span></span>
<span data-ttu-id="88e0d-128">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="88e0d-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e0d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88e0d-129">-PassThru</span></span>
<span data-ttu-id="88e0d-130">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="88e0d-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="88e0d-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="88e0d-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="88e0d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e0d-132">-ResourceGroupName</span></span>
<span data-ttu-id="88e0d-133">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="88e0d-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e0d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88e0d-134">-ResourceId</span></span>
<span data-ttu-id="88e0d-135">A törlendő VpnConnection-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="88e0d-135">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88e0d-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88e0d-136">-Confirm</span></span>
<span data-ttu-id="88e0d-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88e0d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88e0d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88e0d-138">-WhatIf</span></span>
<span data-ttu-id="88e0d-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88e0d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88e0d-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88e0d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88e0d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e0d-141">CommonParameters</span></span>
<span data-ttu-id="88e0d-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88e0d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e0d-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88e0d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e0d-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88e0d-144">INPUTS</span></span>

### <span data-ttu-id="88e0d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="88e0d-145">System.String</span></span>

### <span data-ttu-id="88e0d-146">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="88e0d-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="88e0d-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88e0d-147">OUTPUTS</span></span>

### <span data-ttu-id="88e0d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88e0d-148">System.Boolean</span></span>

## <span data-ttu-id="88e0d-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88e0d-149">NOTES</span></span>

## <span data-ttu-id="88e0d-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88e0d-150">RELATED LINKS</span></span>

[<span data-ttu-id="88e0d-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="88e0d-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="88e0d-152">Új – AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="88e0d-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="88e0d-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="88e0d-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
