---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
ms.openlocfilehash: ac0513b7d411c2c95864aa6f619e80d2373a3554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495867"
---
# <span data-ttu-id="154fc-101">Remove-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="154fc-101">Remove-AzureRmVpnSite</span></span>

## <span data-ttu-id="154fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="154fc-102">SYNOPSIS</span></span>
<span data-ttu-id="154fc-103">Azure VpnSite-erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="154fc-103">Removes an Azure VpnSite resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="154fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="154fc-104">SYNTAX</span></span>

### <span data-ttu-id="154fc-105">ByVpnSiteName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="154fc-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="154fc-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="154fc-106">ByVpnSiteObject</span></span>
```
Remove-AzureRmVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="154fc-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="154fc-107">ByVpnSiteResourceId</span></span>
```
Remove-AzureRmVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="154fc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="154fc-108">DESCRIPTION</span></span>
<span data-ttu-id="154fc-109">Azure VpnSite-erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="154fc-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="154fc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="154fc-110">EXAMPLES</span></span>

### <span data-ttu-id="154fc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="154fc-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="154fc-112">A fenti létrehoz egy erőforráscsoport, a Virtual WAN in West US in "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="154fc-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="154fc-113">Ezután létrehoz egy VpnSite, amely egy ügyfél-fióktelepet jelenít meg, és a virtuális WAN-ra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="154fc-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="154fc-114">A webhely létrehozása után a rendszer azonnal eltávolítja azt a Remove-AzureRmVpnSite parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="154fc-114">Once the site is created, it is immediately removed using the Remove-AzureRmVpnSite command.</span></span>

### <span data-ttu-id="154fc-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="154fc-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzureRmVpnSite
```

<span data-ttu-id="154fc-116">Ugyanaz, mint a példa 1, de itt az Eltávolítás a Get-AzureRmVpnSite vezetékes kimenetének használatával történik.</span><span class="sxs-lookup"><span data-stu-id="154fc-116">Same as example 1 but here the removal happens using the piped output from Get-AzureRmVpnSite.</span></span>

## <span data-ttu-id="154fc-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="154fc-117">PARAMETERS</span></span>

### <span data-ttu-id="154fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154fc-118">-DefaultProfile</span></span>
<span data-ttu-id="154fc-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="154fc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="154fc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="154fc-120">-Force</span></span>
<span data-ttu-id="154fc-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="154fc-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154fc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="154fc-122">-InputObject</span></span>
<span data-ttu-id="154fc-123">A törlendő vpnSite objektum.</span><span class="sxs-lookup"><span data-stu-id="154fc-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="154fc-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="154fc-124">-Name</span></span>
<span data-ttu-id="154fc-125">A vpnSite neve.</span><span class="sxs-lookup"><span data-stu-id="154fc-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154fc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="154fc-126">-PassThru</span></span>
<span data-ttu-id="154fc-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="154fc-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="154fc-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="154fc-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154fc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="154fc-129">-ResourceGroupName</span></span>
<span data-ttu-id="154fc-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="154fc-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154fc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="154fc-131">-ResourceId</span></span>
<span data-ttu-id="154fc-132">A törlendő vpnSite Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="154fc-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154fc-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="154fc-133">-Confirm</span></span>
<span data-ttu-id="154fc-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="154fc-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154fc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="154fc-135">-WhatIf</span></span>
<span data-ttu-id="154fc-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="154fc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="154fc-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="154fc-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154fc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154fc-138">CommonParameters</span></span>
<span data-ttu-id="154fc-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="154fc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154fc-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="154fc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154fc-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="154fc-141">INPUTS</span></span>

### <span data-ttu-id="154fc-142">Microsoft. Azure. commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="154fc-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="154fc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="154fc-143">System.String</span></span>

## <span data-ttu-id="154fc-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="154fc-144">OUTPUTS</span></span>

### <span data-ttu-id="154fc-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="154fc-145">System.Boolean</span></span>

## <span data-ttu-id="154fc-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="154fc-146">NOTES</span></span>

## <span data-ttu-id="154fc-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="154fc-147">RELATED LINKS</span></span>
