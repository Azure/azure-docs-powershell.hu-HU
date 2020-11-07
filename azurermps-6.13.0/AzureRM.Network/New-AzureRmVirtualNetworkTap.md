---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: d40d9c378afdbbc9380114a7b5998b173cb4652f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680322"
---
# <span data-ttu-id="c064c-101">New-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c064c-101">New-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="c064c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c064c-102">SYNOPSIS</span></span>
<span data-ttu-id="c064c-103">VirtualNetworkTap-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c064c-103">Creates a VirtualNetworkTap resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c064c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c064c-104">SYNTAX</span></span>

### <span data-ttu-id="c064c-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c064c-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c064c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c064c-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c064c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c064c-107">DESCRIPTION</span></span>
<span data-ttu-id="c064c-108">A **New-AzureRmVirtualNetworkTap** parancsmag létrehoz egy Azure Virtual Network TAP-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="c064c-108">The **New-AzureRmVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="c064c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c064c-109">EXAMPLES</span></span>

### <span data-ttu-id="c064c-110">Példa 1: Azure virtuális hálózat létrehozása koppintással</span><span class="sxs-lookup"><span data-stu-id="c064c-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzureRmVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="c064c-111">Ez a parancs virtuális hálózati koppintást hoz létre "VirtualNetworkTap1" névvel, amelyen a cél VM konfigurációs adatai (DestinationIpConfiguration, DestinationPort) jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="c064c-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="c064c-112">Az összes forrás koppintás: a konfigurált VM-forgalom erre a cél IP + portra fog átirányítani.</span><span class="sxs-lookup"><span data-stu-id="c064c-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="c064c-113">2. példa: Azure virtuális hálózat létrehozása koppintással a LoadBalancer IP-címével</span><span class="sxs-lookup"><span data-stu-id="c064c-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzureRmVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="c064c-114">Ez a parancs virtuális hálózati koppintást hoz létre "VirtualNetworkTap1" névvel, amelyen a cél VM konfigurációs adatai (FrontEndIpConfiguration) szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="c064c-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="c064c-115">Az összes forrás koppintás: a konfigurált VM-forgalom átirányítása a LoadBalancer IpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c064c-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="c064c-116">Az alapértelmezett célport a 4789.</span><span class="sxs-lookup"><span data-stu-id="c064c-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="c064c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c064c-117">PARAMETERS</span></span>

### <span data-ttu-id="c064c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c064c-118">-AsJob</span></span>
<span data-ttu-id="c064c-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c064c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c064c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c064c-120">-DefaultProfile</span></span>
<span data-ttu-id="c064c-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c064c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c064c-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c064c-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="c064c-123">A cél kiegyenlítő előtér-végpont IP-konfigurációs erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="c064c-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="c064c-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c064c-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="c064c-125">A cél kiegyenlítő előtér-végpont IP-konfigurációs erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="c064c-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="c064c-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c064c-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="c064c-127">A célként megadott hálózati kapcsolat IP-beállítási erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="c064c-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="c064c-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c064c-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="c064c-129">A célként megadott hálózati kapcsolat IP-beállítási erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="c064c-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="c064c-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="c064c-130">-DestinationPort</span></span>
<span data-ttu-id="c064c-131">A csomag-gyűjtő célport</span><span class="sxs-lookup"><span data-stu-id="c064c-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="c064c-132">-Force</span><span class="sxs-lookup"><span data-stu-id="c064c-132">-Force</span></span>
<span data-ttu-id="c064c-133">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c064c-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c064c-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="c064c-134">-Location</span></span>
<span data-ttu-id="c064c-135">A hely.</span><span class="sxs-lookup"><span data-stu-id="c064c-135">The location.</span></span>

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

### <span data-ttu-id="c064c-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c064c-136">-Name</span></span>
<span data-ttu-id="c064c-137">A koppintás neve.</span><span class="sxs-lookup"><span data-stu-id="c064c-137">The name of the tap.</span></span>

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

### <span data-ttu-id="c064c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c064c-138">-ResourceGroupName</span></span>
<span data-ttu-id="c064c-139">A virtuális hálózat erőforráscsoport neve koppintással.</span><span class="sxs-lookup"><span data-stu-id="c064c-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="c064c-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="c064c-140">-Tag</span></span>
<span data-ttu-id="c064c-141">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c064c-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c064c-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c064c-142">-Confirm</span></span>
<span data-ttu-id="c064c-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c064c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c064c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c064c-144">-WhatIf</span></span>
<span data-ttu-id="c064c-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c064c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c064c-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c064c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c064c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c064c-147">CommonParameters</span></span>
<span data-ttu-id="c064c-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c064c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c064c-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c064c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c064c-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c064c-150">INPUTS</span></span>

### <span data-ttu-id="c064c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c064c-151">System.String</span></span>

### <span data-ttu-id="c064c-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c064c-152">System.Int32</span></span>

### <span data-ttu-id="c064c-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c064c-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c064c-154">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c064c-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="c064c-155">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c064c-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="c064c-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c064c-156">OUTPUTS</span></span>

### <span data-ttu-id="c064c-157">Microsoft. Azure. commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c064c-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="c064c-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c064c-158">NOTES</span></span>

## <span data-ttu-id="c064c-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c064c-159">RELATED LINKS</span></span>
