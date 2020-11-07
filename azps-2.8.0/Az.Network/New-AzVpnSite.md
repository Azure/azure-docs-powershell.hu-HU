---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: fe9449eedaedfa08880548ceda769835d6eb3f7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837903"
---
# <span data-ttu-id="87bd4-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="87bd4-101">New-AzVpnSite</span></span>

## <span data-ttu-id="87bd4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="87bd4-103">Új Azure VpnSite-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="87bd4-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="87bd4-104">Ez a cikk az Azure-ra feltöltött, a cortex virtuális központtal való S2S-kapcsolathoz feltöltött ügyfél-kirendeltségek RM-beli képviselete.</span><span class="sxs-lookup"><span data-stu-id="87bd4-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="87bd4-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87bd4-105">SYNTAX</span></span>

### <span data-ttu-id="87bd4-106">ByVirtualWanNameByVpnSiteIpAddress (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87bd4-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87bd4-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="87bd4-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87bd4-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="87bd4-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87bd4-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="87bd4-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87bd4-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="87bd4-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87bd4-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="87bd4-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87bd4-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="87bd4-112">DESCRIPTION</span></span>
<span data-ttu-id="87bd4-113">Új Azure VpnSite-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="87bd4-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="87bd4-114">Ez a cikk az Azure-ra feltöltött, a cortex virtuális központtal való S2S-kapcsolathoz feltöltött ügyfél-kirendeltségek RM-beli képviselete.</span><span class="sxs-lookup"><span data-stu-id="87bd4-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="87bd4-115">Példák</span><span class="sxs-lookup"><span data-stu-id="87bd4-115">EXAMPLES</span></span>

### <span data-ttu-id="87bd4-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="87bd4-116">Example 1</span></span>

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

<span data-ttu-id="87bd4-117">A fentiekben létrehozunk egy erőforráscsoportot (virtuális WAN) a kelet-amerikai "nonlinkSite" erőforráscsoporthoz az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="87bd4-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="87bd4-118">Ezután létrehoz egy VpnSite, amely egy ügyfél-fióktelepet jelenít meg, és a virtuális WAN-ra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="87bd4-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="87bd4-119">Az IPSec-kapcsolat ezután beállítható az adott elágazással és egy VpnGateway a New-AzVpnConnection parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="87bd4-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="87bd4-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="87bd4-120">Example 2</span></span>
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

<span data-ttu-id="87bd4-121">A fentiekben létrehozunk egy erőforráscsoportot, egy virtuális WAN-csoportot és egy VpnSite, amelyben az Azure-alapú "Multilink" erőforráscsoport a kelet-amerikai VpnSiteLinks tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="87bd4-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

## <span data-ttu-id="87bd4-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87bd4-122">PARAMETERS</span></span>

### <span data-ttu-id="87bd4-123">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="87bd4-123">-AddressSpace</span></span>
<span data-ttu-id="87bd4-124">A virtuális hálózat címét előtagok.</span><span class="sxs-lookup"><span data-stu-id="87bd4-124">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="87bd4-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87bd4-125">-AsJob</span></span>
<span data-ttu-id="87bd4-126">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="87bd4-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87bd4-127">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="87bd4-127">-BgpAsn</span></span>
<span data-ttu-id="87bd4-128">A BGP ASN az ehhez a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="87bd4-128">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="87bd4-129">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="87bd4-129">-BgpPeeringAddress</span></span>
<span data-ttu-id="87bd4-130">A VpnSite.</span><span class="sxs-lookup"><span data-stu-id="87bd4-130">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="87bd4-131">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="87bd4-131">-BgpPeeringWeight</span></span>
<span data-ttu-id="87bd4-132">A BGP-súlyozási vastagság erre a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="87bd4-132">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="87bd4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87bd4-133">-DefaultProfile</span></span>
<span data-ttu-id="87bd4-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87bd4-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87bd4-135">-Eszköz típusa</span><span class="sxs-lookup"><span data-stu-id="87bd4-135">-DeviceModel</span></span>
<span data-ttu-id="87bd4-136">A távoli VPN-eszközhöz tartozó eszköz típusa.</span><span class="sxs-lookup"><span data-stu-id="87bd4-136">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="87bd4-137">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="87bd4-137">-DeviceVendor</span></span>
<span data-ttu-id="87bd4-138">A távoli VPN-eszközhöz tartozó eszköz forgalmazójával.</span><span class="sxs-lookup"><span data-stu-id="87bd4-138">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="87bd4-139">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="87bd4-139">-IpAddress</span></span>
<span data-ttu-id="87bd4-140">Az Ip_cím ehhez a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="87bd4-140">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="87bd4-141">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="87bd4-141">-LinkSpeedInMbps</span></span>
<span data-ttu-id="87bd4-142">A távoli VPN-eszközhöz tartozó eszköz típusa.</span><span class="sxs-lookup"><span data-stu-id="87bd4-142">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="87bd4-143">-Hely</span><span class="sxs-lookup"><span data-stu-id="87bd4-143">-Location</span></span>
<span data-ttu-id="87bd4-144">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="87bd4-144">The resource location.</span></span>

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

### <span data-ttu-id="87bd4-145">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87bd4-145">-Name</span></span>
<span data-ttu-id="87bd4-146">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="87bd4-146">The resource name.</span></span>

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

### <span data-ttu-id="87bd4-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87bd4-147">-ResourceGroupName</span></span>
<span data-ttu-id="87bd4-148">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="87bd4-148">The resource name.</span></span>

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

### <span data-ttu-id="87bd4-149">-Címke</span><span class="sxs-lookup"><span data-stu-id="87bd4-149">-Tag</span></span>
<span data-ttu-id="87bd4-150">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="87bd4-150">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="87bd4-151">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="87bd4-151">-VirtualWan</span></span>
<span data-ttu-id="87bd4-152">A VirtualWan ehhez a VpnSite csatlakoznia kell.</span><span class="sxs-lookup"><span data-stu-id="87bd4-152">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="87bd4-153">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="87bd4-153">-VirtualWanId</span></span>
<span data-ttu-id="87bd4-154">A ResourceId VirtualWan a VpnSite kapcsolódnia kell.</span><span class="sxs-lookup"><span data-stu-id="87bd4-154">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="87bd4-155">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="87bd4-155">-VirtualWanName</span></span>
<span data-ttu-id="87bd4-156">Annak a VirtualWan a neve, amelyhez a VpnSite csatlakoznia kell.</span><span class="sxs-lookup"><span data-stu-id="87bd4-156">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="87bd4-157">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87bd4-157">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="87bd4-158">Annak az erőforrásnak a csoportnak a neve, amelyhez a VpnSite csatlakoznia kell a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="87bd4-158">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="87bd4-159">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="87bd4-159">-VpnSiteLink</span></span>
<span data-ttu-id="87bd4-160">Annak a VpnSiteLinks a listája, amelyre ez a VpnSite van.</span><span class="sxs-lookup"><span data-stu-id="87bd4-160">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="87bd4-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87bd4-161">-Confirm</span></span>
<span data-ttu-id="87bd4-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87bd4-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87bd4-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87bd4-163">-WhatIf</span></span>
<span data-ttu-id="87bd4-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87bd4-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87bd4-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87bd4-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87bd4-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87bd4-166">CommonParameters</span></span>
<span data-ttu-id="87bd4-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87bd4-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87bd4-168">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="87bd4-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87bd4-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87bd4-169">INPUTS</span></span>

### <span data-ttu-id="87bd4-170">Nincs</span><span class="sxs-lookup"><span data-stu-id="87bd4-170">None</span></span>

## <span data-ttu-id="87bd4-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87bd4-171">OUTPUTS</span></span>

### <span data-ttu-id="87bd4-172">Microsoft. Azure. commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="87bd4-172">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="87bd4-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87bd4-173">NOTES</span></span>

## <span data-ttu-id="87bd4-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87bd4-174">RELATED LINKS</span></span>

[<span data-ttu-id="87bd4-175">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="87bd4-175">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="87bd4-176">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="87bd4-176">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="87bd4-177">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="87bd4-177">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
