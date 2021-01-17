---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 825090358ea94223d483fe418d06896f1f741045
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385165"
---
# <span data-ttu-id="ad268-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ad268-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="ad268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad268-102">SYNOPSIS</span></span>
<span data-ttu-id="ad268-103">Eltávolítja a VpnConnectiont.</span><span class="sxs-lookup"><span data-stu-id="ad268-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="ad268-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad268-104">SYNTAX</span></span>

### <span data-ttu-id="ad268-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad268-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad268-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="ad268-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad268-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="ad268-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad268-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad268-108">DESCRIPTION</span></span>
<span data-ttu-id="ad268-109">Eltávolítja a VpnConnectiont.</span><span class="sxs-lookup"><span data-stu-id="ad268-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="ad268-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad268-110">EXAMPLES</span></span>

### <span data-ttu-id="ad268-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ad268-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="ad268-112">A fentiekkel létrehozhat egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub és VpnSite in West US in "testRG" resource group in Azure.</span><span class="sxs-lookup"><span data-stu-id="ad268-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ad268-113">Ezután létrejön egy VPN-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="ad268-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="ad268-114">Miután létrehozta az átjárót, a virtuális magánhálózathoz csatlakozik a New-AzVpnConnection paranccsal.</span><span class="sxs-lookup"><span data-stu-id="ad268-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="ad268-115">Ezután eltávolítja a kapcsolatot a kapcsolat nevével.</span><span class="sxs-lookup"><span data-stu-id="ad268-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="ad268-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="ad268-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="ad268-117">Ugyanaz, mint az 1. példa, de most már eltávolítja a kapcsolatot a bevezető objektummal a Get-AzVpnConnectionból.</span><span class="sxs-lookup"><span data-stu-id="ad268-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="ad268-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad268-118">PARAMETERS</span></span>

### <span data-ttu-id="ad268-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad268-119">-DefaultProfile</span></span>
<span data-ttu-id="ad268-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad268-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad268-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ad268-121">-Force</span></span>
<span data-ttu-id="ad268-122">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="ad268-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ad268-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad268-123">-InputObject</span></span>
<span data-ttu-id="ad268-124">A frissítendve a VpnConnection objektum.</span><span class="sxs-lookup"><span data-stu-id="ad268-124">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad268-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ad268-125">-Name</span></span>
<span data-ttu-id="ad268-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ad268-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad268-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ad268-127">-ParentResourceName</span></span>
<span data-ttu-id="ad268-128">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ad268-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad268-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad268-129">-PassThru</span></span>
<span data-ttu-id="ad268-130">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="ad268-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ad268-131">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ad268-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ad268-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad268-132">-ResourceGroupName</span></span>
<span data-ttu-id="ad268-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ad268-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad268-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad268-134">-ResourceId</span></span>
<span data-ttu-id="ad268-135">A törölni kívánt VpnConnection-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ad268-135">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad268-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad268-136">-Confirm</span></span>
<span data-ttu-id="ad268-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ad268-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad268-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad268-138">-WhatIf</span></span>
<span data-ttu-id="ad268-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ad268-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad268-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad268-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad268-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad268-141">CommonParameters</span></span>
<span data-ttu-id="ad268-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad268-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad268-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad268-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad268-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad268-144">INPUTS</span></span>

### <span data-ttu-id="ad268-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ad268-145">System.String</span></span>

### <span data-ttu-id="ad268-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ad268-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="ad268-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad268-147">OUTPUTS</span></span>

### <span data-ttu-id="ad268-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ad268-148">System.Boolean</span></span>

## <span data-ttu-id="ad268-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad268-149">NOTES</span></span>

## <span data-ttu-id="ad268-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad268-150">RELATED LINKS</span></span>

[<span data-ttu-id="ad268-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ad268-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="ad268-152">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ad268-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="ad268-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ad268-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
