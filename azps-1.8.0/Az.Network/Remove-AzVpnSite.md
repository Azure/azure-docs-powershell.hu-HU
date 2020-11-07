---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 0215a05db7e18dad9aeb26476d7076bdc556b021
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670083"
---
# <span data-ttu-id="26e18-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="26e18-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="26e18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26e18-102">SYNOPSIS</span></span>
<span data-ttu-id="26e18-103">Azure VpnSite-erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="26e18-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="26e18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26e18-104">SYNTAX</span></span>

### <span data-ttu-id="26e18-105">ByVpnSiteName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26e18-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e18-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="26e18-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e18-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="26e18-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e18-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="26e18-108">DESCRIPTION</span></span>
<span data-ttu-id="26e18-109">Azure VpnSite-erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="26e18-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="26e18-110">Példák</span><span class="sxs-lookup"><span data-stu-id="26e18-110">EXAMPLES</span></span>

### <span data-ttu-id="26e18-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="26e18-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="26e18-112">A fenti létrehoz egy erőforráscsoport, a Virtual WAN in West US in "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="26e18-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="26e18-113">Ezután létrehoz egy VpnSite, amely egy ügyfél-fióktelepet jelenít meg, és a virtuális WAN-ra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="26e18-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="26e18-114">A webhely létrehozása után a rendszer azonnal eltávolítja azt a Remove-AzVpnSite parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="26e18-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="26e18-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="26e18-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="26e18-116">Ugyanaz, mint a példa 1, de itt az Eltávolítás a Get-AzVpnSite vezetékes kimenetének használatával történik.</span><span class="sxs-lookup"><span data-stu-id="26e18-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="26e18-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26e18-117">PARAMETERS</span></span>

### <span data-ttu-id="26e18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e18-118">-DefaultProfile</span></span>
<span data-ttu-id="26e18-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26e18-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e18-120">-Force</span><span class="sxs-lookup"><span data-stu-id="26e18-120">-Force</span></span>
<span data-ttu-id="26e18-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26e18-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="26e18-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26e18-122">-InputObject</span></span>
<span data-ttu-id="26e18-123">A törlendő vpnSite objektum.</span><span class="sxs-lookup"><span data-stu-id="26e18-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="26e18-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26e18-124">-Name</span></span>
<span data-ttu-id="26e18-125">A vpnSite neve.</span><span class="sxs-lookup"><span data-stu-id="26e18-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="26e18-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26e18-126">-PassThru</span></span>
<span data-ttu-id="26e18-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="26e18-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="26e18-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="26e18-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26e18-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e18-129">-ResourceGroupName</span></span>
<span data-ttu-id="26e18-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="26e18-130">The resource group name.</span></span>

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

### <span data-ttu-id="26e18-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e18-131">-ResourceId</span></span>
<span data-ttu-id="26e18-132">A törlendő vpnSite Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="26e18-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="26e18-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26e18-133">-Confirm</span></span>
<span data-ttu-id="26e18-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26e18-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e18-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e18-135">-WhatIf</span></span>
<span data-ttu-id="26e18-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="26e18-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26e18-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26e18-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e18-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e18-138">CommonParameters</span></span>
<span data-ttu-id="26e18-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26e18-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e18-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e18-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e18-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26e18-141">INPUTS</span></span>

### <span data-ttu-id="26e18-142">Microsoft. Azure. commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="26e18-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="26e18-143">System. String</span><span class="sxs-lookup"><span data-stu-id="26e18-143">System.String</span></span>

## <span data-ttu-id="26e18-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26e18-144">OUTPUTS</span></span>

### <span data-ttu-id="26e18-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26e18-145">System.Boolean</span></span>

## <span data-ttu-id="26e18-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26e18-146">NOTES</span></span>

## <span data-ttu-id="26e18-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26e18-147">RELATED LINKS</span></span>

[<span data-ttu-id="26e18-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="26e18-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="26e18-149">Új – AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="26e18-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="26e18-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="26e18-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
