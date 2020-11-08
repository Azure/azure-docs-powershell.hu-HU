---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 682f6bdb8eb0ce80d4b81dc12b9ed8d09de4713a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182967"
---
# <span data-ttu-id="11a2f-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="11a2f-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="11a2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="11a2f-103">Frissítsen egy meglévő P2SVpnGateway a VirtualHub csoportban a webhely-kapcsolat pontra.</span><span class="sxs-lookup"><span data-stu-id="11a2f-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="11a2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11a2f-104">SYNTAX</span></span>

### <span data-ttu-id="11a2f-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11a2f-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11a2f-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="11a2f-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11a2f-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="11a2f-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11a2f-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="11a2f-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11a2f-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="11a2f-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>]
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11a2f-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="11a2f-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11a2f-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="11a2f-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11a2f-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="11a2f-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11a2f-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="11a2f-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11a2f-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="11a2f-114">DESCRIPTION</span></span>
<span data-ttu-id="11a2f-115">Az **Update-AzP2sVpnGateway** parancsmag lehetővé teszi, hogy egy meglévő P2SVpnGateway frissítsen a VirtualHub-ban az új VpnClientAddressPool vagy az új VpnServerConfiguration vagy a VpnGatewayScaleUnit módosításával.</span><span class="sxs-lookup"><span data-stu-id="11a2f-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="11a2f-116">Példák</span><span class="sxs-lookup"><span data-stu-id="11a2f-116">EXAMPLES</span></span>

### <span data-ttu-id="11a2f-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="11a2f-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces -EnableInternetSecurityFlag                                

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/NilamdWestUsVirtualH
                                 ub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/NilamdWe
                                 stUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "101.10.0.0/16"
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
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="11a2f-118">Az **Update-AzP2sVpnGateway** parancsmag lehetővé teszi, hogy egy meglévő P2SVpnGateway frissítsen a VirtualHub-ban az új VpnClientAddressPool.</span><span class="sxs-lookup"><span data-stu-id="11a2f-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="11a2f-119">Amikor a webhely ügyfélprogramja csatlakozik ezzel a P2SVpnGateway, az adott VpnClientAddressPool tartozó IP-címet az ügyfél kapja.</span><span class="sxs-lookup"><span data-stu-id="11a2f-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

### <span data-ttu-id="11a2f-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="11a2f-120">Example 2</span></span>

<span data-ttu-id="11a2f-121">Frissítsen egy meglévő P2SVpnGateway a VirtualHub csoportban a webhely-kapcsolat pontra.</span><span class="sxs-lookup"><span data-stu-id="11a2f-121">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span> <span data-ttu-id="11a2f-122">autogenerated</span><span class="sxs-lookup"><span data-stu-id="11a2f-122">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzP2sVpnGateway -AsJob -Name 00000000-0000-0000-0000-00000000000000000-westus-gw -ResourceGroupName P2SCortexGATesting -VpnClientAddressPool <String[]> -VpnGatewayScaleUnit 1 -VpnServerConfiguration <PSVpnServerConfiguration>
```

## <span data-ttu-id="11a2f-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11a2f-123">PARAMETERS</span></span>

### <span data-ttu-id="11a2f-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11a2f-124">-AsJob</span></span>
<span data-ttu-id="11a2f-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="11a2f-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11a2f-126">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="11a2f-126">-CustomDnsServer</span></span>
<span data-ttu-id="11a2f-127">Az egyéni DNS-kiszolgálók listája.</span><span class="sxs-lookup"><span data-stu-id="11a2f-127">The list of Custom Dns Servers.</span></span>

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

### <span data-ttu-id="11a2f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a2f-128">-DefaultProfile</span></span>
<span data-ttu-id="11a2f-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11a2f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11a2f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11a2f-130">-InputObject</span></span>
<span data-ttu-id="11a2f-131">A módosítani kívánt p2s VPN-átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="11a2f-131">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11a2f-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11a2f-132">-Name</span></span>
<span data-ttu-id="11a2f-133">A P2S VPN-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="11a2f-133">The P2S vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a2f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11a2f-134">-ResourceGroupName</span></span>
<span data-ttu-id="11a2f-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="11a2f-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a2f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11a2f-136">-ResourceId</span></span>
<span data-ttu-id="11a2f-137">A módosítani kívánt P2SVpnGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="11a2f-137">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11a2f-138">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="11a2f-138">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="11a2f-139">Az Internet Security Flag engedélyezése e P2SVpnGateway-kapcsolatokhoz</span><span class="sxs-lookup"><span data-stu-id="11a2f-139">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="11a2f-140">-DisableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="11a2f-140">-DisableInternetSecurityFlag</span></span>
<span data-ttu-id="11a2f-141">Az Internet Security Flag letiltása ehhez a P2SVpnGateway-kapcsolatokhoz</span><span class="sxs-lookup"><span data-stu-id="11a2f-141">Disable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="11a2f-142">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="11a2f-142">-RoutingConfiguration</span></span>
<span data-ttu-id="11a2f-143">A kapcsolat útválasztási konfigurációja</span><span class="sxs-lookup"><span data-stu-id="11a2f-143">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="11a2f-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="11a2f-144">-Tag</span></span>
<span data-ttu-id="11a2f-145">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="11a2f-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="11a2f-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="11a2f-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="11a2f-147">P2S VpnClient AddressPool a P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="11a2f-147">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a2f-148">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="11a2f-148">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="11a2f-149">A P2SVpnGateway méretarányos egysége.</span><span class="sxs-lookup"><span data-stu-id="11a2f-149">The scale unit for this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="11a2f-150">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="11a2f-150">-VpnServerConfiguration</span></span>
<span data-ttu-id="11a2f-151">A P2SVpnGateway csatolni kívánt VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="11a2f-151">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11a2f-152">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="11a2f-152">-VpnServerConfigurationId</span></span>
<span data-ttu-id="11a2f-153">A VPN-kiszolgáló konfigurációja objektum azonosítója, amelyhez a P2SVpnGateway hozzá lesz rendelve.</span><span class="sxs-lookup"><span data-stu-id="11a2f-153">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11a2f-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11a2f-154">-Confirm</span></span>
<span data-ttu-id="11a2f-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11a2f-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11a2f-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11a2f-156">-WhatIf</span></span>
<span data-ttu-id="11a2f-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11a2f-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11a2f-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11a2f-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11a2f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a2f-159">CommonParameters</span></span>
<span data-ttu-id="11a2f-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11a2f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a2f-161">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11a2f-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a2f-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11a2f-162">INPUTS</span></span>

### <span data-ttu-id="11a2f-163">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="11a2f-163">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="11a2f-164">System. String Microsoft. Azure. commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="11a2f-164">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="11a2f-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11a2f-165">OUTPUTS</span></span>

### <span data-ttu-id="11a2f-166">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="11a2f-166">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="11a2f-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11a2f-167">NOTES</span></span>

## <span data-ttu-id="11a2f-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11a2f-168">RELATED LINKS</span></span>

[<span data-ttu-id="11a2f-169">Új – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="11a2f-169">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
