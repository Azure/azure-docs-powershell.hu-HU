---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160491"
---
# <span data-ttu-id="c5e3c-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c5e3c-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="c5e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e3c-103">Frissíti a VPN-webhelyet.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-103">Updates a VPN site.</span></span>

## <span data-ttu-id="c5e3c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5e3c-104">SYNTAX</span></span>

### <span data-ttu-id="c5e3c-105">ByVpnSiteNameNoVirtualWanUpdate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5e3c-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c5e3c-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c5e3c-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c5e3c-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c5e3c-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c5e3c-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c5e3c-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="c5e3c-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c5e3c-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c5e3c-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c5e3c-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5e3c-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="c5e3c-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5e3c-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5e3c-117">DESCRIPTION</span></span>
<span data-ttu-id="c5e3c-118">Az **Update-AzVpnSite** parancsmag frissíti a VPN-webhelyet.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="c5e3c-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5e3c-119">EXAMPLES</span></span>

### <span data-ttu-id="c5e3c-120">1. példa</span><span class="sxs-lookup"><span data-stu-id="c5e3c-120">Example 1</span></span>

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

<span data-ttu-id="c5e3c-121">A fenti létrehoz egy erőforráscsoportot (Virtuális WAN az Egyesült Államok nyugati részén, "testRG" erőforráscsoportként az Azure-ban).</span><span class="sxs-lookup"><span data-stu-id="c5e3c-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="c5e3c-122">Ezután létrehoz egy VpnSite-t, amely egy ügyfélágat képvisel, és a virtuális WAN-hoz kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="c5e3c-123">A webhely létrehozása után a webhely IpAddress címét a Set-AzVpnSite paranccsal.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="c5e3c-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5e3c-124">PARAMETERS</span></span>

### <span data-ttu-id="c5e3c-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="c5e3c-125">-AddressSpace</span></span>
<span data-ttu-id="c5e3c-126">A virtuális hálózat címelőtagja.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="c5e3c-127">Használja ezt vagy a AddressSpaceObject címet, de ne mindkettőt.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="c5e3c-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5e3c-128">-AsJob</span></span>
<span data-ttu-id="c5e3c-129">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c5e3c-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5e3c-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="c5e3c-130">-BgpAsn</span></span>
<span data-ttu-id="c5e3c-131">A VpnSite BGP ASN-e.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="c5e3c-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="c5e3c-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="c5e3c-133">A VpnSite BGP-társviszony-címe.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="c5e3c-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="c5e3c-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="c5e3c-135">A VpnSite BGP-társviszony-létesítő súlya.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="c5e3c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e3c-136">-DefaultProfile</span></span>
<span data-ttu-id="c5e3c-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5e3c-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="c5e3c-138">-DeviceModel</span></span>
<span data-ttu-id="c5e3c-139">A távoli VPN-eszköz eszközmodelle.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="c5e3c-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="c5e3c-140">-DeviceVendor</span></span>
<span data-ttu-id="c5e3c-141">A távoli VPN-eszköz eszköz szállítója.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="c5e3c-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5e3c-142">-InputObject</span></span>
<span data-ttu-id="c5e3c-143">A módosítható VPN-webhelyobjektum</span><span class="sxs-lookup"><span data-stu-id="c5e3c-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="c5e3c-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="c5e3c-144">-IpAddress</span></span>
<span data-ttu-id="c5e3c-145">A helyi hálózati átjáró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="c5e3c-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="c5e3c-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="c5e3c-147">A távoli VPN-eszköz eszközmodelle.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="c5e3c-148">-Name</span><span class="sxs-lookup"><span data-stu-id="c5e3c-148">-Name</span></span>
<span data-ttu-id="c5e3c-149">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-149">The resource name.</span></span>

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

### <span data-ttu-id="c5e3c-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="c5e3c-150">-O365Policy</span></span>
<span data-ttu-id="c5e3c-151">Az Office 365 forgalomtörési házirendje ehhez a VpnSite-hez.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e3c-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e3c-152">-ResourceGroupName</span></span>
<span data-ttu-id="c5e3c-153">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-153">The resource group name.</span></span>

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

### <span data-ttu-id="c5e3c-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5e3c-154">-ResourceId</span></span>
<span data-ttu-id="c5e3c-155">A vpn-webhely Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-155">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="c5e3c-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="c5e3c-156">-Tag</span></span>
<span data-ttu-id="c5e3c-157">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c5e3c-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="c5e3c-158">-VirtualWan</span></span>
<span data-ttu-id="c5e3c-159">A VirtualWanhoz, a VpnSite-hez csatlakoztatni kell.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="c5e3c-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="c5e3c-160">-VirtualWanId</span></span>
<span data-ttu-id="c5e3c-161">Ehhez a VpnSite-hez csatlakoztatni kell a ResourceId VirtualWant.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="c5e3c-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c5e3c-162">-VirtualWanName</span></span>
<span data-ttu-id="c5e3c-163">Annak a VirtualWannak a nevét, amelyhez a VpnSite-et csatlakoztatni kell.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="c5e3c-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e3c-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="c5e3c-165">Annak a VirtualWannak az erőforráscsoportnevét, amelyhez a VpnSite-et csatlakoztatni kell.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="c5e3c-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c5e3c-166">-VpnSiteLink</span></span>
<span data-ttu-id="c5e3c-167">A VpnSiteLinks listája, amelyek a VpnSite-webhelyhez vannak csatolva.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e3c-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5e3c-168">-Confirm</span></span>
<span data-ttu-id="c5e3c-169">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5e3c-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e3c-170">-WhatIf</span></span>
<span data-ttu-id="c5e3c-171">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e3c-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5e3c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e3c-173">CommonParameters</span></span>
<span data-ttu-id="c5e3c-174">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e3c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e3c-175">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5e3c-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e3c-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5e3c-176">INPUTS</span></span>

### <span data-ttu-id="c5e3c-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="c5e3c-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="c5e3c-178">System.String</span><span class="sxs-lookup"><span data-stu-id="c5e3c-178">System.String</span></span>

## <span data-ttu-id="c5e3c-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5e3c-179">OUTPUTS</span></span>

### <span data-ttu-id="c5e3c-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="c5e3c-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="c5e3c-181">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5e3c-181">NOTES</span></span>

## <span data-ttu-id="c5e3c-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5e3c-182">RELATED LINKS</span></span>

[<span data-ttu-id="c5e3c-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c5e3c-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="c5e3c-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c5e3c-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="c5e3c-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c5e3c-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
