---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 980b84fd1b23cb7e4b034dee485b785b96893f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670237"
---
# <span data-ttu-id="9bba9-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9bba9-101">New-AzVpnSite</span></span>

## <span data-ttu-id="9bba9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bba9-102">SYNOPSIS</span></span>
<span data-ttu-id="9bba9-103">Új Azure VpnSite-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="9bba9-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="9bba9-104">Ez a cikk az Azure-ra feltöltött, a cortex virtuális központtal való S2S-kapcsolathoz feltöltött ügyfél-kirendeltségek RM-beli képviselete.</span><span class="sxs-lookup"><span data-stu-id="9bba9-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="9bba9-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bba9-105">SYNTAX</span></span>

### <span data-ttu-id="9bba9-106">ByVirtualWanName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9bba9-106">ByVirtualWanName (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bba9-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9bba9-107">ByVirtualWanObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bba9-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9bba9-108">ByVirtualWanResourceId</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bba9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bba9-109">DESCRIPTION</span></span>
<span data-ttu-id="9bba9-110">Új Azure VpnSite-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="9bba9-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="9bba9-111">Ez a cikk az Azure-ra feltöltött, a cortex virtuális központtal való S2S-kapcsolathoz feltöltött ügyfél-kirendeltségek RM-beli képviselete.</span><span class="sxs-lookup"><span data-stu-id="9bba9-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="9bba9-112">Példák</span><span class="sxs-lookup"><span data-stu-id="9bba9-112">EXAMPLES</span></span>

### <span data-ttu-id="9bba9-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9bba9-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="9bba9-114">A fenti létrehoz egy erőforráscsoport, a Virtual WAN in West US in "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="9bba9-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="9bba9-115">Ezután létrehoz egy VpnSite, amely egy ügyfél-fióktelepet jelenít meg, és a virtuális WAN-ra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="9bba9-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="9bba9-116">Az IPSec-kapcsolat ezután beállítható az adott elágazással és egy VpnGateway a New-AzVpnConnection parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="9bba9-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="9bba9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bba9-117">PARAMETERS</span></span>

### <span data-ttu-id="9bba9-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="9bba9-118">-AddressSpace</span></span>
<span data-ttu-id="9bba9-119">A virtuális hálózat címét előtagok.</span><span class="sxs-lookup"><span data-stu-id="9bba9-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="9bba9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bba9-120">-AsJob</span></span>
<span data-ttu-id="9bba9-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9bba9-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bba9-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="9bba9-122">-BgpAsn</span></span>
<span data-ttu-id="9bba9-123">A BGP ASN az ehhez a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9bba9-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="9bba9-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="9bba9-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="9bba9-125">A VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9bba9-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="9bba9-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="9bba9-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="9bba9-127">A BGP-súlyozási vastagság erre a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9bba9-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="9bba9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bba9-128">-DefaultProfile</span></span>
<span data-ttu-id="9bba9-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bba9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bba9-130">-Eszköz típusa</span><span class="sxs-lookup"><span data-stu-id="9bba9-130">-DeviceModel</span></span>
<span data-ttu-id="9bba9-131">A távoli VPN-eszközhöz tartozó eszköz típusa.</span><span class="sxs-lookup"><span data-stu-id="9bba9-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="9bba9-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="9bba9-132">-DeviceVendor</span></span>
<span data-ttu-id="9bba9-133">A távoli VPN-eszközhöz tartozó eszköz forgalmazójával.</span><span class="sxs-lookup"><span data-stu-id="9bba9-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="9bba9-134">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="9bba9-134">-IpAddress</span></span>
<span data-ttu-id="9bba9-135">Az Ip_cím ehhez a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9bba9-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="9bba9-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="9bba9-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="9bba9-137">A távoli VPN-eszközhöz tartozó eszköz típusa.</span><span class="sxs-lookup"><span data-stu-id="9bba9-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="9bba9-138">-Hely</span><span class="sxs-lookup"><span data-stu-id="9bba9-138">-Location</span></span>
<span data-ttu-id="9bba9-139">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="9bba9-139">The resource location.</span></span>

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

### <span data-ttu-id="9bba9-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9bba9-140">-Name</span></span>
<span data-ttu-id="9bba9-141">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="9bba9-141">The resource name.</span></span>

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

### <span data-ttu-id="9bba9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bba9-142">-ResourceGroupName</span></span>
<span data-ttu-id="9bba9-143">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="9bba9-143">The resource name.</span></span>

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

### <span data-ttu-id="9bba9-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="9bba9-144">-Tag</span></span>
<span data-ttu-id="9bba9-145">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9bba9-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9bba9-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="9bba9-146">-VirtualWan</span></span>
<span data-ttu-id="9bba9-147">A VirtualWan ehhez a VpnSite csatlakoznia kell.</span><span class="sxs-lookup"><span data-stu-id="9bba9-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bba9-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="9bba9-148">-VirtualWanId</span></span>
<span data-ttu-id="9bba9-149">A ResourceId VirtualWan a VpnSite kapcsolódnia kell.</span><span class="sxs-lookup"><span data-stu-id="9bba9-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bba9-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9bba9-150">-VirtualWanName</span></span>
<span data-ttu-id="9bba9-151">Annak a VirtualWan a neve, amelyhez a VpnSite csatlakoznia kell.</span><span class="sxs-lookup"><span data-stu-id="9bba9-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bba9-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bba9-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="9bba9-153">Annak az erőforrásnak a csoportnak a neve, amelyhez a VpnSite csatlakoznia kell a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="9bba9-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bba9-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9bba9-154">-Confirm</span></span>
<span data-ttu-id="9bba9-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9bba9-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bba9-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bba9-156">-WhatIf</span></span>
<span data-ttu-id="9bba9-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9bba9-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bba9-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9bba9-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bba9-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bba9-159">CommonParameters</span></span>
<span data-ttu-id="9bba9-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bba9-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bba9-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bba9-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bba9-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bba9-162">INPUTS</span></span>

### <span data-ttu-id="9bba9-163">Nincs</span><span class="sxs-lookup"><span data-stu-id="9bba9-163">None</span></span>

## <span data-ttu-id="9bba9-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bba9-164">OUTPUTS</span></span>

### <span data-ttu-id="9bba9-165">Microsoft. Azure. commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="9bba9-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="9bba9-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bba9-166">NOTES</span></span>

## <span data-ttu-id="9bba9-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bba9-167">RELATED LINKS</span></span>

[<span data-ttu-id="9bba9-168">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9bba9-168">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="9bba9-169">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9bba9-169">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="9bba9-170">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9bba9-170">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
