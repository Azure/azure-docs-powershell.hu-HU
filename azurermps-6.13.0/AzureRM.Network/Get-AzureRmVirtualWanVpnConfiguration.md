---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
ms.openlocfilehash: be0fbc9b9fc6d91a5bf94344f432b67dfc38cab3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495070"
---
# <span data-ttu-id="7be1d-101">Get-AzureRmVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="7be1d-101">Get-AzureRmVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="7be1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7be1d-102">SYNOPSIS</span></span>
<span data-ttu-id="7be1d-103">Beolvassa a VPN-konfigurációt a WAN-kapcsolaton keresztül a VpnConnections-ra kapcsolt VpnSites részhalmazához.</span><span class="sxs-lookup"><span data-stu-id="7be1d-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="7be1d-104">Feltölti a generált VPN-konfigurációt az ügyfél által megadott tárterület-blobra.</span><span class="sxs-lookup"><span data-stu-id="7be1d-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7be1d-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7be1d-105">SYNTAX</span></span>

### <span data-ttu-id="7be1d-106">ByVirtualWanNameByVpnSiteObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7be1d-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7be1d-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="7be1d-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7be1d-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="7be1d-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7be1d-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="7be1d-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7be1d-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="7be1d-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7be1d-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="7be1d-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7be1d-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="7be1d-112">DESCRIPTION</span></span>
<span data-ttu-id="7be1d-113">Beolvassa a VPN-konfigurációt a WAN-kapcsolaton keresztül a VpnConnections-ra kapcsolt VpnSites részhalmazához.</span><span class="sxs-lookup"><span data-stu-id="7be1d-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="7be1d-114">Feltölti a generált VPN-konfigurációt az ügyfél által megadott tárterület-blobra.</span><span class="sxs-lookup"><span data-stu-id="7be1d-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="7be1d-115">Példák</span><span class="sxs-lookup"><span data-stu-id="7be1d-115">EXAMPLES</span></span>

### <span data-ttu-id="7be1d-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7be1d-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzureRmVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="7be1d-117">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="7be1d-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7be1d-118">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="7be1d-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7be1d-119">Miután létrehozta az átjárót, az a New-AzureRmVpnConnection parancs segítségével csatlakozik a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="7be1d-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="7be1d-120">Ekkor a rendszer ezzel a parancsmagot tölti le a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7be1d-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="7be1d-121">Ha a parancsmagot sikeres, akkor a letöltési konfiguráció a SignedSasUrl által jelzett blobra lesz írva.</span><span class="sxs-lookup"><span data-stu-id="7be1d-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="7be1d-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7be1d-122">PARAMETERS</span></span>

### <span data-ttu-id="7be1d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be1d-123">-DefaultProfile</span></span>
<span data-ttu-id="7be1d-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7be1d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7be1d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7be1d-125">-InputObject</span></span>
<span data-ttu-id="7be1d-126">A módosítani kívánt VPN-webhely objektum</span><span class="sxs-lookup"><span data-stu-id="7be1d-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7be1d-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7be1d-127">-Name</span></span>
<span data-ttu-id="7be1d-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7be1d-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be1d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be1d-129">-ResourceGroupName</span></span>
<span data-ttu-id="7be1d-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7be1d-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be1d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7be1d-131">-ResourceId</span></span>
<span data-ttu-id="7be1d-132">A virtuális WAN Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="7be1d-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be1d-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="7be1d-133">-StorageSasUrl</span></span>
<span data-ttu-id="7be1d-134">Annak a tárolási helynek a SAS-URL-címe, ahol a konfigurációt létre szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="7be1d-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="7be1d-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7be1d-135">-VpnSite</span></span>
<span data-ttu-id="7be1d-136">Azoknak a VpnSite-erőforrás-azonosítóknak a listája, amelyekhez konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7be1d-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be1d-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="7be1d-137">-VpnSiteId</span></span>
<span data-ttu-id="7be1d-138">Azoknak a VpnSite-erőforrás-azonosítóknak a listája, amelyekhez konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7be1d-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be1d-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7be1d-139">-Confirm</span></span>
<span data-ttu-id="7be1d-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7be1d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7be1d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7be1d-141">-WhatIf</span></span>
<span data-ttu-id="7be1d-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7be1d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7be1d-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7be1d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7be1d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be1d-144">CommonParameters</span></span>
<span data-ttu-id="7be1d-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7be1d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be1d-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7be1d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be1d-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7be1d-147">INPUTS</span></span>

### <span data-ttu-id="7be1d-148">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7be1d-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="7be1d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7be1d-149">System.String</span></span>

## <span data-ttu-id="7be1d-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7be1d-150">OUTPUTS</span></span>

### <span data-ttu-id="7be1d-151">Microsoft. Azure. commands. Network. models. PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="7be1d-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="7be1d-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7be1d-152">NOTES</span></span>

## <span data-ttu-id="7be1d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7be1d-153">RELATED LINKS</span></span>
