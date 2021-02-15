---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 0ac64d9b1aee363a1681b8d62da2ecf73574f7cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202684"
---
# <span data-ttu-id="21fe4-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="21fe4-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="21fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="21fe4-103">VirtualNetworkTap erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="21fe4-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="21fe4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="21fe4-104">SYNTAX</span></span>

### <span data-ttu-id="21fe4-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21fe4-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21fe4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="21fe4-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21fe4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="21fe4-107">DESCRIPTION</span></span>
<span data-ttu-id="21fe4-108">A **New-AzVirtualNetworkTap** parancsmag létrehoz egy Azure virtuális hálózat koppintás-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="21fe4-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="21fe4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="21fe4-109">EXAMPLES</span></span>

### <span data-ttu-id="21fe4-110">1. példa: Virtuális Azure-hálózat létrehozása koppintás</span><span class="sxs-lookup"><span data-stu-id="21fe4-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="21fe4-111">Ez a parancs létrehoz egy virtuális hálózatra vonatkozó "VirtualNetworkTap1" nevet, amely tartalmazza a cél VIRTUÁLIS GÉP konfigurációs adatait (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="21fe4-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="21fe4-112">A VM-hez konfigurált forrássikon összes adatforgalma erre a cél IP-címre + portra lesz irányítva.</span><span class="sxs-lookup"><span data-stu-id="21fe4-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="21fe4-113">2. példa: Virtuális Azure-hálózatra való koppintás a LoadBalancer IP protokollal</span><span class="sxs-lookup"><span data-stu-id="21fe4-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="21fe4-114">Ez a parancs létrehoz egy virtuális hálózatra vonatkozó "VirtualNetworkTap1" nevet, amely tartalmazza a cél VIRTUÁLIS GÉP konfigurációs adatait (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="21fe4-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="21fe4-115">A VM-hez konfigurált összes forrássérintés ebbe a LoadBalancer IpConfigurationba lesz irányítva.</span><span class="sxs-lookup"><span data-stu-id="21fe4-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="21fe4-116">Az alapértelmezett célport 4789.</span><span class="sxs-lookup"><span data-stu-id="21fe4-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="21fe4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21fe4-117">PARAMETERS</span></span>

### <span data-ttu-id="21fe4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21fe4-118">-AsJob</span></span>
<span data-ttu-id="21fe4-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="21fe4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21fe4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fe4-120">-DefaultProfile</span></span>
<span data-ttu-id="21fe4-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21fe4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21fe4-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="21fe4-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="21fe4-123">A cél terheléselosztási elülső IP-konfigurációs erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="21fe4-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="21fe4-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="21fe4-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="21fe4-125">A cél terheléselosztási elülső IP-konfigurációs erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="21fe4-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="21fe4-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="21fe4-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="21fe4-127">A célhálózati IP-konfigurációs erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="21fe4-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="21fe4-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="21fe4-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="21fe4-129">A célhálózati IP-konfigurációs erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="21fe4-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="21fe4-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="21fe4-130">-DestinationPort</span></span>
<span data-ttu-id="21fe4-131">A csomagcsomag célportja</span><span class="sxs-lookup"><span data-stu-id="21fe4-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="21fe4-132">-Force</span><span class="sxs-lookup"><span data-stu-id="21fe4-132">-Force</span></span>
<span data-ttu-id="21fe4-133">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="21fe4-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="21fe4-134">-Location</span><span class="sxs-lookup"><span data-stu-id="21fe4-134">-Location</span></span>
<span data-ttu-id="21fe4-135">A hely.</span><span class="sxs-lookup"><span data-stu-id="21fe4-135">The location.</span></span>

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

### <span data-ttu-id="21fe4-136">-Name</span><span class="sxs-lookup"><span data-stu-id="21fe4-136">-Name</span></span>
<span data-ttu-id="21fe4-137">A koppintás neve.</span><span class="sxs-lookup"><span data-stu-id="21fe4-137">The name of the tap.</span></span>

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

### <span data-ttu-id="21fe4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21fe4-138">-ResourceGroupName</span></span>
<span data-ttu-id="21fe4-139">A virtuális hálózat erőforráscsoportneve koppintás.</span><span class="sxs-lookup"><span data-stu-id="21fe4-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="21fe4-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="21fe4-140">-Tag</span></span>
<span data-ttu-id="21fe4-141">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="21fe4-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="21fe4-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21fe4-142">-Confirm</span></span>
<span data-ttu-id="21fe4-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="21fe4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21fe4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21fe4-144">-WhatIf</span></span>
<span data-ttu-id="21fe4-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="21fe4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21fe4-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21fe4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21fe4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21fe4-147">CommonParameters</span></span>
<span data-ttu-id="21fe4-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21fe4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21fe4-149">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21fe4-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21fe4-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21fe4-150">INPUTS</span></span>

### <span data-ttu-id="21fe4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="21fe4-151">System.String</span></span>

### <span data-ttu-id="21fe4-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="21fe4-152">System.Int32</span></span>

### <span data-ttu-id="21fe4-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="21fe4-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="21fe4-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="21fe4-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="21fe4-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="21fe4-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="21fe4-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21fe4-156">OUTPUTS</span></span>

### <span data-ttu-id="21fe4-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="21fe4-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="21fe4-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="21fe4-158">NOTES</span></span>

## <span data-ttu-id="21fe4-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21fe4-159">RELATED LINKS</span></span>

[<span data-ttu-id="21fe4-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="21fe4-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="21fe4-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="21fe4-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="21fe4-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="21fe4-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
