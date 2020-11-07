---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 39fb3223b1a80b831874bbd833d6d0c97aace53f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845210"
---
# <span data-ttu-id="d07cc-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d07cc-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="d07cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d07cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d07cc-103">Frissítsen egy meglévő P2SVpnGateway a VirtualHub csoportban a webhely-kapcsolat pontra.</span><span class="sxs-lookup"><span data-stu-id="d07cc-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="d07cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d07cc-104">SYNTAX</span></span>

### <span data-ttu-id="d07cc-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d07cc-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07cc-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d07cc-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07cc-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d07cc-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07cc-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="d07cc-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07cc-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d07cc-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07cc-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d07cc-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07cc-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="d07cc-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d07cc-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d07cc-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07cc-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d07cc-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d07cc-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="d07cc-114">DESCRIPTION</span></span>
<span data-ttu-id="d07cc-115">Az **Update-AzP2sVpnGateway** parancsmag lehetővé teszi, hogy egy meglévő P2SVpnGateway frissítsen a VirtualHub-ban az új VpnClientAddressPool vagy az új VpnServerConfiguration vagy a VpnGatewayScaleUnit módosításával.</span><span class="sxs-lookup"><span data-stu-id="d07cc-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="d07cc-116">Példák</span><span class="sxs-lookup"><span data-stu-id="d07cc-116">EXAMPLES</span></span>

### <span data-ttu-id="d07cc-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d07cc-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces                                    

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
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="d07cc-118">Az **Update-AzP2sVpnGateway** parancsmag lehetővé teszi, hogy egy meglévő P2SVpnGateway frissítsen a VirtualHub-ban az új VpnClientAddressPool.</span><span class="sxs-lookup"><span data-stu-id="d07cc-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="d07cc-119">Amikor a webhely ügyfélprogramja csatlakozik ezzel a P2SVpnGateway, az adott VpnClientAddressPool tartozó IP-címet az ügyfél kapja.</span><span class="sxs-lookup"><span data-stu-id="d07cc-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

## <span data-ttu-id="d07cc-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d07cc-120">PARAMETERS</span></span>

### <span data-ttu-id="d07cc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d07cc-121">-AsJob</span></span>
<span data-ttu-id="d07cc-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d07cc-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d07cc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07cc-123">-DefaultProfile</span></span>
<span data-ttu-id="d07cc-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d07cc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d07cc-125">-InputObject</span></span>
<span data-ttu-id="d07cc-126">A módosítani kívánt p2s VPN-átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="d07cc-126">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d07cc-127">-Name</span></span>
<span data-ttu-id="d07cc-128">A P2S VPN-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="d07cc-128">The P2S vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07cc-129">-ResourceGroupName</span></span>
<span data-ttu-id="d07cc-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d07cc-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d07cc-131">-ResourceId</span></span>
<span data-ttu-id="d07cc-132">A módosítani kívánt P2SVpnGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="d07cc-132">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="d07cc-133">-Tag</span></span>
<span data-ttu-id="d07cc-134">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d07cc-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-135">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="d07cc-135">-VpnClientAddressPool</span></span>
<span data-ttu-id="d07cc-136">P2S VpnClient AddressPool a P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d07cc-136">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-137">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="d07cc-137">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="d07cc-138">A P2SVpnGateway méretarányos egysége.</span><span class="sxs-lookup"><span data-stu-id="d07cc-138">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-139">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d07cc-139">-VpnServerConfiguration</span></span>
<span data-ttu-id="d07cc-140">A P2SVpnGateway csatolni kívánt VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d07cc-140">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-141">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d07cc-141">-VpnServerConfigurationId</span></span>
<span data-ttu-id="d07cc-142">A VPN-kiszolgáló konfigurációja objektum azonosítója, amelyhez a P2SVpnGateway hozzá lesz rendelve.</span><span class="sxs-lookup"><span data-stu-id="d07cc-142">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d07cc-143">-Confirm</span></span>
<span data-ttu-id="d07cc-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d07cc-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d07cc-145">-WhatIf</span></span>
<span data-ttu-id="d07cc-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d07cc-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d07cc-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d07cc-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07cc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07cc-148">CommonParameters</span></span>
<span data-ttu-id="d07cc-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d07cc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07cc-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d07cc-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07cc-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d07cc-151">INPUTS</span></span>

### <span data-ttu-id="d07cc-152">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d07cc-152">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="d07cc-153">System. String Microsoft. Azure. commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d07cc-153">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="d07cc-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d07cc-154">OUTPUTS</span></span>

### <span data-ttu-id="d07cc-155">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d07cc-155">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="d07cc-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d07cc-156">NOTES</span></span>

## <span data-ttu-id="d07cc-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d07cc-157">RELATED LINKS</span></span>
