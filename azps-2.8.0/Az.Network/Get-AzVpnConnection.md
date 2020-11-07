---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: 85b6472cd6dd99210e188f6fc9b66ba4b00e3198
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837255"
---
# <span data-ttu-id="b9244-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b9244-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="b9244-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9244-102">SYNOPSIS</span></span>
<span data-ttu-id="b9244-103">Virtuális magánhálózati kapcsolatot kap, vagy felsorolja a VpnGateway csatlakoztatott összes VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="b9244-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="b9244-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9244-104">SYNTAX</span></span>

### <span data-ttu-id="b9244-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9244-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9244-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b9244-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9244-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b9244-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9244-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9244-108">DESCRIPTION</span></span>
<span data-ttu-id="b9244-109">Virtuális magánhálózati kapcsolatot kap, vagy felsorolja a VpnGateway csatlakoztatott összes VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="b9244-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="b9244-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b9244-110">EXAMPLES</span></span>

### <span data-ttu-id="b9244-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b9244-111">Example 1</span></span>

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
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="b9244-112">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b9244-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b9244-113">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="b9244-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b9244-114">Miután létrehozta az átjárót, az a New-AzVpnConnection parancs segítségével csatlakozik a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b9244-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="b9244-115">Ezután a kapcsolat neve alapján kapja meg a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="b9244-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="b9244-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="b9244-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
```

<span data-ttu-id="b9244-117">Ez a parancsmag a "teszt" kezdetű összes kapcsolatot megkapja.</span><span class="sxs-lookup"><span data-stu-id="b9244-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="b9244-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9244-118">PARAMETERS</span></span>

### <span data-ttu-id="b9244-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9244-119">-DefaultProfile</span></span>
<span data-ttu-id="b9244-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9244-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9244-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9244-121">-Name</span></span>
<span data-ttu-id="b9244-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b9244-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9244-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b9244-123">-ParentObject</span></span>
<span data-ttu-id="b9244-124">A kapcsolat fölérendelt VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="b9244-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9244-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b9244-125">-ParentResourceId</span></span>
<span data-ttu-id="b9244-126">A kapcsolat fölérendelt VpnGateway tartozó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b9244-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9244-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b9244-127">-ParentResourceName</span></span>
<span data-ttu-id="b9244-128">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b9244-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9244-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9244-129">-ResourceGroupName</span></span>
<span data-ttu-id="b9244-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9244-130">The resource group name.</span></span>

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

### <span data-ttu-id="b9244-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9244-131">CommonParameters</span></span>
<span data-ttu-id="b9244-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9244-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9244-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b9244-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9244-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9244-134">INPUTS</span></span>

### <span data-ttu-id="b9244-135">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b9244-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="b9244-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b9244-136">System.String</span></span>

## <span data-ttu-id="b9244-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9244-137">OUTPUTS</span></span>

### <span data-ttu-id="b9244-138">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b9244-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="b9244-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9244-139">NOTES</span></span>

## <span data-ttu-id="b9244-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9244-140">RELATED LINKS</span></span>

[<span data-ttu-id="b9244-141">Új – AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b9244-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="b9244-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b9244-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="b9244-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b9244-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
