---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 0ac64d9b1aee363a1681b8d62da2ecf73574f7cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188113"
---
# <span data-ttu-id="81791-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="81791-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="81791-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81791-102">SYNOPSIS</span></span>
<span data-ttu-id="81791-103">VirtualNetworkTap-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="81791-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="81791-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81791-104">SYNTAX</span></span>

### <span data-ttu-id="81791-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81791-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81791-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="81791-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81791-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="81791-107">DESCRIPTION</span></span>
<span data-ttu-id="81791-108">A **New-AzVirtualNetworkTap** parancsmag létrehoz egy Azure Virtual Network TAP-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="81791-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="81791-109">Példák</span><span class="sxs-lookup"><span data-stu-id="81791-109">EXAMPLES</span></span>

### <span data-ttu-id="81791-110">Példa 1: Azure virtuális hálózat létrehozása koppintással</span><span class="sxs-lookup"><span data-stu-id="81791-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="81791-111">Ez a parancs virtuális hálózati koppintást hoz létre "VirtualNetworkTap1" névvel, amelyen a cél VM konfigurációs adatai (DestinationIpConfiguration, DestinationPort) jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="81791-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="81791-112">Az összes forrás koppintás: a konfigurált VM-forgalom erre a cél IP + portra fog átirányítani.</span><span class="sxs-lookup"><span data-stu-id="81791-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="81791-113">2. példa: Azure virtuális hálózat létrehozása koppintással a LoadBalancer IP-címével</span><span class="sxs-lookup"><span data-stu-id="81791-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="81791-114">Ez a parancs virtuális hálózati koppintást hoz létre "VirtualNetworkTap1" névvel, amelyen a cél VM konfigurációs adatai (FrontEndIpConfiguration) szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="81791-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="81791-115">Az összes forrás koppintás: a konfigurált VM-forgalom átirányítása a LoadBalancer IpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="81791-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="81791-116">Az alapértelmezett célport a 4789.</span><span class="sxs-lookup"><span data-stu-id="81791-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="81791-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81791-117">PARAMETERS</span></span>

### <span data-ttu-id="81791-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81791-118">-AsJob</span></span>
<span data-ttu-id="81791-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="81791-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81791-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81791-120">-DefaultProfile</span></span>
<span data-ttu-id="81791-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81791-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81791-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81791-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="81791-123">A cél kiegyenlítő előtér-végpont IP-konfigurációs erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="81791-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81791-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="81791-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="81791-125">A cél kiegyenlítő előtér-végpont IP-konfigurációs erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="81791-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81791-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81791-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="81791-127">A célként megadott hálózati kapcsolat IP-beállítási erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="81791-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81791-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="81791-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="81791-129">A célként megadott hálózati kapcsolat IP-beállítási erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="81791-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81791-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="81791-130">-DestinationPort</span></span>
<span data-ttu-id="81791-131">A csomag-gyűjtő célport</span><span class="sxs-lookup"><span data-stu-id="81791-131">The Destination Port of the packet collector</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81791-132">-Force</span><span class="sxs-lookup"><span data-stu-id="81791-132">-Force</span></span>
<span data-ttu-id="81791-133">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81791-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="81791-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="81791-134">-Location</span></span>
<span data-ttu-id="81791-135">A hely.</span><span class="sxs-lookup"><span data-stu-id="81791-135">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81791-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81791-136">-Name</span></span>
<span data-ttu-id="81791-137">A koppintás neve.</span><span class="sxs-lookup"><span data-stu-id="81791-137">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81791-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81791-138">-ResourceGroupName</span></span>
<span data-ttu-id="81791-139">A virtuális hálózat erőforráscsoport neve koppintással.</span><span class="sxs-lookup"><span data-stu-id="81791-139">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81791-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="81791-140">-Tag</span></span>
<span data-ttu-id="81791-141">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="81791-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81791-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81791-142">-Confirm</span></span>
<span data-ttu-id="81791-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81791-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81791-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81791-144">-WhatIf</span></span>
<span data-ttu-id="81791-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81791-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81791-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81791-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81791-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81791-147">CommonParameters</span></span>
<span data-ttu-id="81791-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81791-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81791-149">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81791-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81791-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81791-150">INPUTS</span></span>

### <span data-ttu-id="81791-151">System. String</span><span class="sxs-lookup"><span data-stu-id="81791-151">System.String</span></span>

### <span data-ttu-id="81791-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="81791-152">System.Int32</span></span>

### <span data-ttu-id="81791-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="81791-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="81791-154">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81791-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="81791-155">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81791-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="81791-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81791-156">OUTPUTS</span></span>

### <span data-ttu-id="81791-157">Microsoft. Azure. commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="81791-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="81791-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81791-158">NOTES</span></span>

## <span data-ttu-id="81791-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81791-159">RELATED LINKS</span></span>

[<span data-ttu-id="81791-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="81791-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="81791-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="81791-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="81791-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="81791-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
