---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 50e335825fb43a85286be5f95696c1dd1a537129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923953"
---
# <span data-ttu-id="7c326-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="7c326-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="7c326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c326-102">SYNOPSIS</span></span>
<span data-ttu-id="7c326-103">Eltávolít egy Azure VpnSite-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="7c326-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="7c326-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c326-104">SYNTAX</span></span>

### <span data-ttu-id="7c326-105">ByVpnSiteName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c326-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c326-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="7c326-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c326-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="7c326-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c326-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c326-108">DESCRIPTION</span></span>
<span data-ttu-id="7c326-109">Eltávolít egy Azure VpnSite-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="7c326-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="7c326-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c326-110">EXAMPLES</span></span>

### <span data-ttu-id="7c326-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7c326-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="7c326-112">A fenti létrehoz egy erőforráscsoportot (Virtuális WAN az Egyesült Államok nyugati részén, az "testRG" erőforráscsoportot az Azure-ban).</span><span class="sxs-lookup"><span data-stu-id="7c326-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="7c326-113">Ezután létrehoz egy VpnSite-t, amely egy ügyfélágat képvisel, és a virtuális WAN-hoz kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="7c326-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="7c326-114">A webhely létrehozása után a webhely azonnal törlődik a Remove-AzVpnSite paranccsal.</span><span class="sxs-lookup"><span data-stu-id="7c326-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="7c326-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="7c326-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="7c326-116">Ugyanaz, mint az 1. példában, de az eltávolítás a Get-AzVpnSite-ból származó bevezető kimenettel történik.</span><span class="sxs-lookup"><span data-stu-id="7c326-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="7c326-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c326-117">PARAMETERS</span></span>

### <span data-ttu-id="7c326-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c326-118">-DefaultProfile</span></span>
<span data-ttu-id="7c326-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c326-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c326-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7c326-120">-Force</span></span>
<span data-ttu-id="7c326-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c326-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7c326-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c326-122">-InputObject</span></span>
<span data-ttu-id="7c326-123">A törölt vpnSite-objektum.</span><span class="sxs-lookup"><span data-stu-id="7c326-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="7c326-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7c326-124">-Name</span></span>
<span data-ttu-id="7c326-125">A vpnSite neve.</span><span class="sxs-lookup"><span data-stu-id="7c326-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="7c326-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c326-126">-PassThru</span></span>
<span data-ttu-id="7c326-127">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="7c326-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="7c326-128">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7c326-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c326-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c326-129">-ResourceGroupName</span></span>
<span data-ttu-id="7c326-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c326-130">The resource group name.</span></span>

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

### <span data-ttu-id="7c326-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c326-131">-ResourceId</span></span>
<span data-ttu-id="7c326-132">A vpnSite-hez szükséges Azure-erőforrásazonosítót törölni kell.</span><span class="sxs-lookup"><span data-stu-id="7c326-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="7c326-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c326-133">-Confirm</span></span>
<span data-ttu-id="7c326-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c326-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c326-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c326-135">-WhatIf</span></span>
<span data-ttu-id="7c326-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c326-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c326-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c326-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c326-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c326-138">CommonParameters</span></span>
<span data-ttu-id="7c326-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c326-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c326-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c326-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c326-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c326-141">INPUTS</span></span>

### <span data-ttu-id="7c326-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="7c326-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="7c326-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7c326-143">System.String</span></span>

## <span data-ttu-id="7c326-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c326-144">OUTPUTS</span></span>

### <span data-ttu-id="7c326-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c326-145">System.Boolean</span></span>

## <span data-ttu-id="7c326-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c326-146">NOTES</span></span>

## <span data-ttu-id="7c326-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c326-147">RELATED LINKS</span></span>

[<span data-ttu-id="7c326-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="7c326-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="7c326-149">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="7c326-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="7c326-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="7c326-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
