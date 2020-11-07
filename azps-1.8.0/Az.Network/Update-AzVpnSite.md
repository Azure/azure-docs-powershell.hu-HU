---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: 30e8113cee3a544e514bb10ef4592995e50a0353
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669920"
---
# <span data-ttu-id="c4bf7-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c4bf7-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="c4bf7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bf7-103">Virtuális magánhálózati webhely frissítése</span><span class="sxs-lookup"><span data-stu-id="c4bf7-103">Updates a VPN site.</span></span>

## <span data-ttu-id="c4bf7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4bf7-104">SYNTAX</span></span>

### <span data-ttu-id="c4bf7-105">ByVpnSiteNameNoVirtualWanUpdate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4bf7-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c4bf7-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c4bf7-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c4bf7-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c4bf7-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c4bf7-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c4bf7-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="c4bf7-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c4bf7-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c4bf7-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c4bf7-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf7-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="c4bf7-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4bf7-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4bf7-117">DESCRIPTION</span></span>
<span data-ttu-id="c4bf7-118">Az **Update-AzVpnSite** parancsmag FRISSÍTI a VPN-webhelyeket.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="c4bf7-119">Példák</span><span class="sxs-lookup"><span data-stu-id="c4bf7-119">EXAMPLES</span></span>

### <span data-ttu-id="c4bf7-120">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c4bf7-120">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

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

<span data-ttu-id="c4bf7-121">A fenti létrehoz egy erőforráscsoport, a Virtual WAN in West US in "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="c4bf7-122">Ezután létrehoz egy VpnSite, amely egy ügyfél-fióktelepet jelenít meg, és a virtuális WAN-ra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="c4bf7-123">Miután létrehozta a webhelyet, a Set-AzVpnSite parancs segítségével frissíti a webhely IP-címeit.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="c4bf7-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4bf7-124">PARAMETERS</span></span>

### <span data-ttu-id="c4bf7-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="c4bf7-125">-AddressSpace</span></span>
<span data-ttu-id="c4bf7-126">A virtuális hálózat címét előtagok.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="c4bf7-127">Használja ezt vagy a AddressSpaceObject, de mindkettőt nem.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="c4bf7-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4bf7-128">-AsJob</span></span>
<span data-ttu-id="c4bf7-129">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c4bf7-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4bf7-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="c4bf7-130">-BgpAsn</span></span>
<span data-ttu-id="c4bf7-131">A BGP ASN az ehhez a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="c4bf7-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="c4bf7-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="c4bf7-133">A VpnSite.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="c4bf7-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="c4bf7-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="c4bf7-135">A BGP-súlyozási vastagság erre a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="c4bf7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bf7-136">-DefaultProfile</span></span>
<span data-ttu-id="c4bf7-137">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4bf7-138">-Eszköz típusa</span><span class="sxs-lookup"><span data-stu-id="c4bf7-138">-DeviceModel</span></span>
<span data-ttu-id="c4bf7-139">A távoli VPN-eszközhöz tartozó eszköz típusa.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="c4bf7-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="c4bf7-140">-DeviceVendor</span></span>
<span data-ttu-id="c4bf7-141">A távoli VPN-eszközhöz tartozó eszköz forgalmazójával.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="c4bf7-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4bf7-142">-InputObject</span></span>
<span data-ttu-id="c4bf7-143">A módosítani kívánt VPN-webhely objektum</span><span class="sxs-lookup"><span data-stu-id="c4bf7-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="c4bf7-144">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="c4bf7-144">-IpAddress</span></span>
<span data-ttu-id="c4bf7-145">A helyi hálózati átjáró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="c4bf7-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="c4bf7-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="c4bf7-147">A távoli VPN-eszközhöz tartozó eszköz típusa.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="c4bf7-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4bf7-148">-Name</span></span>
<span data-ttu-id="c4bf7-149">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-149">The resource name.</span></span>

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

### <span data-ttu-id="c4bf7-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4bf7-150">-ResourceGroupName</span></span>
<span data-ttu-id="c4bf7-151">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-151">The resource group name.</span></span>

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

### <span data-ttu-id="c4bf7-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4bf7-152">-ResourceId</span></span>
<span data-ttu-id="c4bf7-153">A VPN-webhely Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-153">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="c4bf7-154">-Címke</span><span class="sxs-lookup"><span data-stu-id="c4bf7-154">-Tag</span></span>
<span data-ttu-id="c4bf7-155">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c4bf7-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="c4bf7-156">-VirtualWan</span></span>
<span data-ttu-id="c4bf7-157">A VirtualWan ehhez a VpnSite csatlakoznia kell.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="c4bf7-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="c4bf7-158">-VirtualWanId</span></span>
<span data-ttu-id="c4bf7-159">A ResourceId VirtualWan a VpnSite kapcsolódnia kell.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="c4bf7-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c4bf7-160">-VirtualWanName</span></span>
<span data-ttu-id="c4bf7-161">Annak a VirtualWan a neve, amelyhez a VpnSite csatlakoznia kell.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="c4bf7-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4bf7-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="c4bf7-163">Annak az erőforrásnak a csoportnak a neve, amelyhez a VpnSite csatlakoznia kell a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="c4bf7-164">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c4bf7-164">-Confirm</span></span>
<span data-ttu-id="c4bf7-165">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4bf7-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4bf7-166">-WhatIf</span></span>
<span data-ttu-id="c4bf7-167">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4bf7-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4bf7-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bf7-169">CommonParameters</span></span>
<span data-ttu-id="c4bf7-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4bf7-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bf7-171">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4bf7-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bf7-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4bf7-172">INPUTS</span></span>

### <span data-ttu-id="c4bf7-173">Microsoft. Azure. commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="c4bf7-173">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="c4bf7-174">System. String</span><span class="sxs-lookup"><span data-stu-id="c4bf7-174">System.String</span></span>

## <span data-ttu-id="c4bf7-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4bf7-175">OUTPUTS</span></span>

### <span data-ttu-id="c4bf7-176">Microsoft. Azure. commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="c4bf7-176">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="c4bf7-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4bf7-177">NOTES</span></span>

## <span data-ttu-id="c4bf7-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4bf7-178">RELATED LINKS</span></span>

[<span data-ttu-id="c4bf7-179">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c4bf7-179">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="c4bf7-180">Új – AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c4bf7-180">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="c4bf7-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c4bf7-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
