---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159043"
---
# <span data-ttu-id="47781-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="47781-101">New-AzVpnSite</span></span>

## <span data-ttu-id="47781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47781-102">SYNOPSIS</span></span>
<span data-ttu-id="47781-103">Létrehoz egy új Azure VpnSite-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="47781-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="47781-104">Ez egy rm representation of customer branches that are uploaded to Azure for S2S connectivity with a Virtual Hub.</span><span class="sxs-lookup"><span data-stu-id="47781-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="47781-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47781-105">SYNTAX</span></span>

### <span data-ttu-id="47781-106">ByVirtualWanNameByVpnSiteIpAddress (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47781-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47781-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="47781-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47781-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="47781-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47781-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="47781-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47781-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="47781-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47781-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="47781-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47781-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47781-112">DESCRIPTION</span></span>
<span data-ttu-id="47781-113">Létrehoz egy új Azure VpnSite-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="47781-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="47781-114">Ez egy rm representation of customer branches that are uploaded to Azure for S2S connectivity with a Virtual Hub.</span><span class="sxs-lookup"><span data-stu-id="47781-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="47781-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47781-115">EXAMPLES</span></span>

### <span data-ttu-id="47781-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="47781-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="47781-117">A fenti létrehoz egy erőforráscsoportot (Virtuális WAN az Egyesült Államok keleti részén) az Azure "nonlinkSite" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="47781-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="47781-118">Ezután létrehoz egy VpnSite-t, amely egy ügyfélágat képvisel, és a virtuális WAN-hoz kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="47781-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="47781-119">Az IPSec-kapcsolatot ezután az e ágban és a VpnGatewayben is be lehet New-AzVpnConnection paranccsal.</span><span class="sxs-lookup"><span data-stu-id="47781-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="47781-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="47781-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="47781-121">A fentiekkel létrehoz egy erőforráscsoportot (Virtuális WAN és VpnSite, 1 VpnSiteLinks)az Egyesült Államok keleti részén, az Azure "multilink" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="47781-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="47781-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="47781-122">Example 3</span></span>

<span data-ttu-id="47781-123">Létrehoz egy új Azure VpnSite-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="47781-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="47781-124">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="47781-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="47781-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47781-125">PARAMETERS</span></span>

### <span data-ttu-id="47781-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="47781-126">-AddressSpace</span></span>
<span data-ttu-id="47781-127">A virtuális hálózat címelőtagja.</span><span class="sxs-lookup"><span data-stu-id="47781-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="47781-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47781-128">-AsJob</span></span>
<span data-ttu-id="47781-129">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="47781-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47781-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="47781-130">-BgpAsn</span></span>
<span data-ttu-id="47781-131">A VpnSite BGP ASN-e.</span><span class="sxs-lookup"><span data-stu-id="47781-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="47781-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="47781-133">A VpnSite BGP-társviszony-címe.</span><span class="sxs-lookup"><span data-stu-id="47781-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="47781-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="47781-135">A VpnSite BGP-társviszony-létesítő súlya.</span><span class="sxs-lookup"><span data-stu-id="47781-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47781-136">-DefaultProfile</span></span>
<span data-ttu-id="47781-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47781-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47781-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="47781-138">-DeviceModel</span></span>
<span data-ttu-id="47781-139">A távoli VPN-eszköz eszközmodelle.</span><span class="sxs-lookup"><span data-stu-id="47781-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="47781-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="47781-140">-DeviceVendor</span></span>
<span data-ttu-id="47781-141">A távoli VPN-eszköz eszköz szállítója.</span><span class="sxs-lookup"><span data-stu-id="47781-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="47781-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="47781-142">-IpAddress</span></span>
<span data-ttu-id="47781-143">A VpnSite IPAddress címe.</span><span class="sxs-lookup"><span data-stu-id="47781-143">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="47781-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="47781-145">A távoli VPN-eszköz eszközmodelle.</span><span class="sxs-lookup"><span data-stu-id="47781-145">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-146">-Location</span><span class="sxs-lookup"><span data-stu-id="47781-146">-Location</span></span>
<span data-ttu-id="47781-147">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="47781-147">The resource location.</span></span>

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

### <span data-ttu-id="47781-148">-Name</span><span class="sxs-lookup"><span data-stu-id="47781-148">-Name</span></span>
<span data-ttu-id="47781-149">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="47781-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="47781-150">-O365Policy</span></span>
<span data-ttu-id="47781-151">Az Office 365 forgalomtörési házirendje ehhez a VpnSite-hez.</span><span class="sxs-lookup"><span data-stu-id="47781-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="47781-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47781-152">-ResourceGroupName</span></span>
<span data-ttu-id="47781-153">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="47781-153">The resource name.</span></span>

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

### <span data-ttu-id="47781-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="47781-154">-Tag</span></span>
<span data-ttu-id="47781-155">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="47781-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="47781-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="47781-156">-VirtualWan</span></span>
<span data-ttu-id="47781-157">A VirtualWanhoz, a VpnSite-hez csatlakoztatni kell.</span><span class="sxs-lookup"><span data-stu-id="47781-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="47781-158">-VirtualWanId</span></span>
<span data-ttu-id="47781-159">Ehhez a VpnSite-hez csatlakoztatni kell a ResourceId VirtualWant.</span><span class="sxs-lookup"><span data-stu-id="47781-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="47781-160">-VirtualWanName</span></span>
<span data-ttu-id="47781-161">Annak a VirtualWannak a nevét, amelyhez a VpnSite-et csatlakoztatni kell.</span><span class="sxs-lookup"><span data-stu-id="47781-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47781-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="47781-163">A VirtualWan ez a VpnSite erőforráscsoport nevét csatlakoztatni kell.</span><span class="sxs-lookup"><span data-stu-id="47781-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="47781-164">-VpnSiteLink</span></span>
<span data-ttu-id="47781-165">A VpnSiteLinks listája, amelyek a VpnSite-webhelyhez vannak csatolva.</span><span class="sxs-lookup"><span data-stu-id="47781-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47781-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47781-166">-Confirm</span></span>
<span data-ttu-id="47781-167">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="47781-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47781-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47781-168">-WhatIf</span></span>
<span data-ttu-id="47781-169">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="47781-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47781-170">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47781-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47781-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47781-171">CommonParameters</span></span>
<span data-ttu-id="47781-172">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47781-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47781-173">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47781-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47781-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47781-174">INPUTS</span></span>

### <span data-ttu-id="47781-175">Nincs</span><span class="sxs-lookup"><span data-stu-id="47781-175">None</span></span>

## <span data-ttu-id="47781-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47781-176">OUTPUTS</span></span>

### <span data-ttu-id="47781-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="47781-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="47781-178">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47781-178">NOTES</span></span>

## <span data-ttu-id="47781-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47781-179">RELATED LINKS</span></span>

[<span data-ttu-id="47781-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="47781-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="47781-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="47781-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="47781-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="47781-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
