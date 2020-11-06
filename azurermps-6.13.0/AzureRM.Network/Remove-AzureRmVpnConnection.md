---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
ms.openlocfilehash: da023b7c0b060e9e263b6b0677065746568524b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494998"
---
# <span data-ttu-id="13a65-101">Remove-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="13a65-101">Remove-AzureRmVpnConnection</span></span>

## <span data-ttu-id="13a65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13a65-102">SYNOPSIS</span></span>
<span data-ttu-id="13a65-103">Eltávolít egy VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="13a65-103">Removes a VpnConnection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13a65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13a65-104">SYNTAX</span></span>

### <span data-ttu-id="13a65-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13a65-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13a65-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="13a65-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzureRmVpnConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13a65-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="13a65-107">ByVpnConnectionObject</span></span>
```
Remove-AzureRmVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13a65-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="13a65-108">DESCRIPTION</span></span>
<span data-ttu-id="13a65-109">Eltávolít egy VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="13a65-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="13a65-110">Példák</span><span class="sxs-lookup"><span data-stu-id="13a65-110">EXAMPLES</span></span>

### <span data-ttu-id="13a65-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13a65-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="13a65-112">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="13a65-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="13a65-113">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="13a65-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="13a65-114">Miután létrehozta az átjárót, az a New-AzureRmVpnConnection parancs segítségével csatlakozik a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="13a65-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="13a65-115">Ezután eltávolítja a kapcsolatot a kapcsolat nevével.</span><span class="sxs-lookup"><span data-stu-id="13a65-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="13a65-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="13a65-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzureRmVpnConnection
```

<span data-ttu-id="13a65-117">Ugyanaz, mint a példa 1, de most már eltávolítja a kapcsolatot a Get-AzureRmVpnConnection-től a vezetékes objektummal.</span><span class="sxs-lookup"><span data-stu-id="13a65-117">Same as example 1, but it now removes the connection using the piped object from Get-AzureRmVpnConnection.</span></span>

## <span data-ttu-id="13a65-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13a65-118">PARAMETERS</span></span>

### <span data-ttu-id="13a65-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a65-119">-DefaultProfile</span></span>
<span data-ttu-id="13a65-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13a65-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13a65-121">-Force</span><span class="sxs-lookup"><span data-stu-id="13a65-121">-Force</span></span>
<span data-ttu-id="13a65-122">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="13a65-122">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="13a65-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13a65-123">-InputObject</span></span>
<span data-ttu-id="13a65-124">A frissítendő VpnConenction objektum.</span><span class="sxs-lookup"><span data-stu-id="13a65-124">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="13a65-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13a65-125">-Name</span></span>
<span data-ttu-id="13a65-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="13a65-126">The resource name.</span></span>

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

### <span data-ttu-id="13a65-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="13a65-127">-ParentResourceName</span></span>
<span data-ttu-id="13a65-128">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="13a65-128">The parent resource name.</span></span>

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

### <span data-ttu-id="13a65-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13a65-129">-PassThru</span></span>
<span data-ttu-id="13a65-130">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="13a65-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="13a65-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="13a65-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="13a65-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a65-132">-ResourceGroupName</span></span>
<span data-ttu-id="13a65-133">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="13a65-133">The resource group name.</span></span>

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

### <span data-ttu-id="13a65-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13a65-134">-ResourceId</span></span>
<span data-ttu-id="13a65-135">A törlendő VpnConenction-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="13a65-135">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="13a65-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13a65-136">-Confirm</span></span>
<span data-ttu-id="13a65-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13a65-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13a65-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13a65-138">-WhatIf</span></span>
<span data-ttu-id="13a65-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13a65-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13a65-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13a65-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13a65-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a65-141">CommonParameters</span></span>
<span data-ttu-id="13a65-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13a65-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a65-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a65-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a65-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13a65-144">INPUTS</span></span>

### <span data-ttu-id="13a65-145">System. String</span><span class="sxs-lookup"><span data-stu-id="13a65-145">System.String</span></span>

### <span data-ttu-id="13a65-146">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="13a65-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="13a65-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13a65-147">OUTPUTS</span></span>

### <span data-ttu-id="13a65-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13a65-148">System.Boolean</span></span>

## <span data-ttu-id="13a65-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13a65-149">NOTES</span></span>

## <span data-ttu-id="13a65-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13a65-150">RELATED LINKS</span></span>
