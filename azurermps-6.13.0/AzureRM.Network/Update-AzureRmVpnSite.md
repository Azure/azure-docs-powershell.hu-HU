---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnSite.md
ms.openlocfilehash: fa24f61d0e638cb38e7cf882aac2191a5119b1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498263"
---
# <span data-ttu-id="d3e1f-101">Update-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="d3e1f-101">Update-AzureRmVpnSite</span></span>

## <span data-ttu-id="d3e1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e1f-103">Az ügyfél-fióktelepet egy olyan VpnSite frissíti, amelynek célja az adott cél állapota.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-103">Updates a VpnSite representing a customer branch to an intended goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3e1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3e1f-104">SYNTAX</span></span>

### <span data-ttu-id="d3e1f-105">ByVpnSiteNameNoVirtualWanUpdate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3e1f-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="d3e1f-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e1f-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="d3e1f-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="d3e1f-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e1f-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="d3e1f-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="d3e1f-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="d3e1f-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e1f-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="d3e1f-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e1f-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="d3e1f-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e1f-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3e1f-117">DESCRIPTION</span></span>
<span data-ttu-id="d3e1f-118">Az ügyfél-fióktelepet egy olyan VpnSite frissíti, amelynek célja az adott cél állapota.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-118">Updates a VpnSite representing a customer branch to an intended goal state.</span></span>

## <span data-ttu-id="d3e1f-119">Példák</span><span class="sxs-lookup"><span data-stu-id="d3e1f-119">EXAMPLES</span></span>

### <span data-ttu-id="d3e1f-120">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d3e1f-120">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 2.3.4.5
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="d3e1f-121">A fenti létrehoz egy erőforráscsoport, a Virtual WAN in West US in "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="d3e1f-122">Ezután létrehoz egy VpnSite, amely egy ügyfél-fióktelepet jelenít meg, és a virtuális WAN-ra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="d3e1f-123">Miután létrehozta a webhelyet, a Set-AzureRmVpnSite parancs segítségével frissíti a webhely IP-címeit.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-123">Once the site is created, it updates the IpAddress of the site using the Set-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="d3e1f-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3e1f-124">PARAMETERS</span></span>

### <span data-ttu-id="d3e1f-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="d3e1f-125">-AddressSpace</span></span>
<span data-ttu-id="d3e1f-126">A virtuális hálózat címét előtagok.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="d3e1f-127">Használja ezt vagy a AddressSpaceObject, de mindkettőt nem.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-127">Use this or AddressSpaceObject but not both.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3e1f-128">-AsJob</span></span>
<span data-ttu-id="d3e1f-129">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d3e1f-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3e1f-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="d3e1f-130">-BgpAsn</span></span>
<span data-ttu-id="d3e1f-131">A BGP ASN az ehhez a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="d3e1f-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="d3e1f-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="d3e1f-133">A VpnSite.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="d3e1f-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="d3e1f-135">A BGP-súlyozási vastagság erre a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="d3e1f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e1f-136">-DefaultProfile</span></span>
<span data-ttu-id="d3e1f-137">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e1f-138">-Eszköz típusa</span><span class="sxs-lookup"><span data-stu-id="d3e1f-138">-DeviceModel</span></span>
<span data-ttu-id="d3e1f-139">A távoli VPN-eszközhöz tartozó eszköz típusa.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-139">The device model of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="d3e1f-140">-DeviceVendor</span></span>
<span data-ttu-id="d3e1f-141">A távoli VPN-eszközhöz tartozó eszköz forgalmazójával.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-141">The device vendor of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3e1f-142">-InputObject</span></span>
<span data-ttu-id="d3e1f-143">A módosítani kívánt VPN-webhely objektum</span><span class="sxs-lookup"><span data-stu-id="d3e1f-143">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObjectByVirtualWanName, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteObjectNoVirtualWanUpdate
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-144">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="d3e1f-144">-IpAddress</span></span>
<span data-ttu-id="d3e1f-145">A helyi hálózati átjáró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-145">IP address of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="d3e1f-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="d3e1f-147">A távoli VPN-eszközhöz tartozó eszköz típusa.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="d3e1f-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3e1f-148">-Name</span></span>
<span data-ttu-id="d3e1f-149">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e1f-150">-ResourceGroupName</span></span>
<span data-ttu-id="d3e1f-151">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-151">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e1f-152">-ResourceId</span></span>
<span data-ttu-id="d3e1f-153">A VPN-webhely Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-153">The Azure resource ID for the vpn site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceIdByVirtualWanName, ByVpnSiteResourceIdByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanObject, ByVpnSiteResourceIdNoVirtualWanUpdate
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-154">-Címke</span><span class="sxs-lookup"><span data-stu-id="d3e1f-154">-Tag</span></span>
<span data-ttu-id="d3e1f-155">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d3e1f-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="d3e1f-156">-VirtualWan</span></span>
<span data-ttu-id="d3e1f-157">A VirtualWan ehhez a VpnSite csatlakoznia kell.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVpnSiteNameByVirtualWanObject, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteResourceIdByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="d3e1f-158">-VirtualWanId</span></span>
<span data-ttu-id="d3e1f-159">A ResourceId VirtualWan a VpnSite kapcsolódnia kell.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="d3e1f-160">-VirtualWanName</span></span>
<span data-ttu-id="d3e1f-161">Annak a VirtualWan a neve, amelyhez a VpnSite csatlakoznia kell.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e1f-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="d3e1f-163">Annak az erőforrásnak a csoportnak a neve, amelyhez a VpnSite csatlakoznia kell a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1f-164">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d3e1f-164">-Confirm</span></span>
<span data-ttu-id="d3e1f-165">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e1f-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e1f-166">-WhatIf</span></span>
<span data-ttu-id="d3e1f-167">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3e1f-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3e1f-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e1f-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e1f-169">CommonParameters</span></span>
<span data-ttu-id="d3e1f-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3e1f-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e1f-171">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3e1f-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e1f-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3e1f-172">INPUTS</span></span>

### <span data-ttu-id="d3e1f-173">Microsoft. Azure. commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="d3e1f-173">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="d3e1f-174">System. String</span><span class="sxs-lookup"><span data-stu-id="d3e1f-174">System.String</span></span>

## <span data-ttu-id="d3e1f-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3e1f-175">OUTPUTS</span></span>

### <span data-ttu-id="d3e1f-176">Microsoft. Azure. commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="d3e1f-176">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="d3e1f-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3e1f-177">NOTES</span></span>

## <span data-ttu-id="d3e1f-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3e1f-178">RELATED LINKS</span></span>
