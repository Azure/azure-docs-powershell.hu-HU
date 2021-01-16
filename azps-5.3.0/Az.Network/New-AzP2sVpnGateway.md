---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 516cd38257a8742f1bc23b3207b7e3c982d9eb36
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470189"
---
# <span data-ttu-id="99030-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="99030-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="99030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99030-102">SYNOPSIS</span></span>
<span data-ttu-id="99030-103">Hozzon létre egy új P2SVpnGatewayt a VirtualHub alatt, hogy a webhelyre mutasson a kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="99030-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="99030-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="99030-104">SYNTAX</span></span>

### <span data-ttu-id="99030-105">ByVirtualHubNameByVpnServerConfigurationObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99030-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99030-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="99030-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99030-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="99030-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99030-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="99030-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99030-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="99030-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99030-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="99030-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99030-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="99030-111">DESCRIPTION</span></span>
<span data-ttu-id="99030-112">A **New-AzP2sVpnGateway** parancsmag lehetővé teszi, hogy új P2SVpnGatewayt hozzon létre a VirtualHub alatt, hogy a Point to site connectivity-ból a site clients to Azure VirtualWan alkalmazásba tudjanak áttérni.</span><span class="sxs-lookup"><span data-stu-id="99030-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="99030-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="99030-113">EXAMPLES</span></span>

### <span data-ttu-id="99030-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="99030-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "EnableInternetSecurity": True,
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="99030-115">A **New-AzP2sVpnGateway** parancsmag lehetővé teszi, hogy új P2SVpnGatewayt hozzon létre a VirtualHub alatt a Point to site connectivity beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="99030-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="99030-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99030-116">PARAMETERS</span></span>

### <span data-ttu-id="99030-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99030-117">-AsJob</span></span>
<span data-ttu-id="99030-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="99030-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99030-119">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="99030-119">-CustomDnsServer</span></span>
<span data-ttu-id="99030-120">Az egyéni DNS-kiszolgálók listája.</span><span class="sxs-lookup"><span data-stu-id="99030-120">The list of Custom Dns Servers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99030-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99030-121">-DefaultProfile</span></span>
<span data-ttu-id="99030-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99030-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99030-123">-Name</span><span class="sxs-lookup"><span data-stu-id="99030-123">-Name</span></span>
<span data-ttu-id="99030-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="99030-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99030-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99030-125">-ResourceGroupName</span></span>
<span data-ttu-id="99030-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="99030-126">The resource name.</span></span>

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

### <span data-ttu-id="99030-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="99030-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="99030-128">Internetbiztonsági jelző engedélyezése ehhez a P2SVpnGateway-kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="99030-128">Enable internet security flag for this P2SVpnGateway connections</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99030-129">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="99030-129">-RoutingConfiguration</span></span>
<span data-ttu-id="99030-130">Útválasztási konfiguráció ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="99030-130">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99030-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="99030-131">-Tag</span></span>
<span data-ttu-id="99030-132">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="99030-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="99030-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="99030-133">-VirtualHub</span></span>
<span data-ttu-id="99030-134">A VirtualHub ezzel a P2SVpnGateway-sel kell társítva lennie.</span><span class="sxs-lookup"><span data-stu-id="99030-134">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99030-135">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="99030-135">-VirtualHubId</span></span>
<span data-ttu-id="99030-136">Annak a VirtualHubnak az azonosítója, amelyhez a P2SVpnGatewaynek társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="99030-136">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99030-137">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="99030-137">-VirtualHubName</span></span>
<span data-ttu-id="99030-138">Annak a VirtualHubnak az azonosítója, amelyhez a P2SVpnGatewaynek társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="99030-138">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99030-139">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="99030-139">-VpnClientAddressPool</span></span>
<span data-ttu-id="99030-140">P2S VpnClient AddressPool ehhez a P2SVpnGateway P2SConnectionConfigurationhoz.</span><span class="sxs-lookup"><span data-stu-id="99030-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99030-141">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="99030-141">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="99030-142">A P2SVpnGateway méretaránya.</span><span class="sxs-lookup"><span data-stu-id="99030-142">The scale unit for this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="99030-143">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="99030-143">-VpnServerConfiguration</span></span>
<span data-ttu-id="99030-144">A P2SVpnGatewayhez csatolható VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="99030-144">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99030-145">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="99030-145">-VpnServerConfigurationId</span></span>
<span data-ttu-id="99030-146">A vpn-kiszolgáló konfigurációs objektumának azonosítója, amelyhez a P2SVpnGateway csatolva lesz.</span><span class="sxs-lookup"><span data-stu-id="99030-146">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99030-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99030-147">-Confirm</span></span>
<span data-ttu-id="99030-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="99030-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99030-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99030-149">-WhatIf</span></span>
<span data-ttu-id="99030-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="99030-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99030-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99030-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99030-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99030-152">CommonParameters</span></span>
<span data-ttu-id="99030-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99030-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99030-154">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99030-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99030-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99030-155">INPUTS</span></span>

### <span data-ttu-id="99030-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="99030-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="99030-157">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="99030-157">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="99030-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99030-158">OUTPUTS</span></span>

### <span data-ttu-id="99030-159">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="99030-159">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="99030-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="99030-160">NOTES</span></span>

## <span data-ttu-id="99030-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99030-161">RELATED LINKS</span></span>

[<span data-ttu-id="99030-162">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="99030-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
