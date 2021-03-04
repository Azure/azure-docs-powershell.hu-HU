---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 994c0e85745e08d4a01e7b5a20b90a25513a983f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934833"
---
# <span data-ttu-id="6b90d-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b90d-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="6b90d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b90d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b90d-103">Hálózati felületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6b90d-103">Creates a network interface.</span></span>

## <span data-ttu-id="6b90d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b90d-104">SYNTAX</span></span>

### <span data-ttu-id="6b90d-105">SetByIpConfigurationResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b90d-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b90d-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6b90d-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b90d-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b90d-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b90d-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6b90d-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>] [-EnableIPForwarding]
 [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b90d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b90d-109">DESCRIPTION</span></span>
<span data-ttu-id="6b90d-110">A **New-AzNetworkInterface** parancsmag létrehoz egy Azure hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="6b90d-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="6b90d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b90d-111">EXAMPLES</span></span>

### <span data-ttu-id="6b90d-112">1. példa: Azure hálózati felület létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b90d-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="6b90d-113">Ez a parancs létrehoz egy NetworkInterface001 nevű hálózati felületet egy dinamikusan hozzárendelt személyes IP-címmel az Alhálózat1 szolgáltatásból a VirtualNetwork1 virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="6b90d-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="6b90d-114">A parancs két DNS-kiszolgálót is hozzárendel a hálózati felülethez.</span><span class="sxs-lookup"><span data-stu-id="6b90d-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="6b90d-115">Az IPConfiguration gyermekerőforrás automatikusan létrejön az IPConfiguration1 névvel.</span><span class="sxs-lookup"><span data-stu-id="6b90d-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="6b90d-116">2. példa: Azure hálózati felület létrehozása IP-konfigurációs objektum használatával</span><span class="sxs-lookup"><span data-stu-id="6b90d-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="6b90d-117">Ebben a példában egy IP-konfigurációs objektum használatával új hálózati felületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6b90d-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="6b90d-118">Az IP konfigurációs objektum statikus privát IPv4-címet ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="6b90d-119">Az első parancs beolvassa a második parancsban az alhálózat hozzárendeléshez használt meglévő virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="6b90d-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="6b90d-120">A második parancs létrehoz egy IPConfig1 nevű hálózatifelület-IP-konfigurációt, és az IPConfig1 nevű változóban tárolja a $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="6b90d-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="6b90d-121">A harmadik parancs létrehoz egy NetworkInterface1 nevű hálózati felületet, amely a hálózati felület IP-konfigurációját használja a $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="6b90d-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="6b90d-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="6b90d-122">Example 3</span></span>

<span data-ttu-id="6b90d-123">Hálózati felületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6b90d-123">Creates a network interface.</span></span> <span data-ttu-id="6b90d-124">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="6b90d-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="6b90d-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b90d-125">PARAMETERS</span></span>

### <span data-ttu-id="6b90d-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6b90d-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="6b90d-127">Egy **ApplicationGatewayBackendAddressPool objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6b90d-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="6b90d-129">Egy **ApplicationGatewayBackendAddressPool-objektum** azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6b90d-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="6b90d-131">Olyan alkalmazásbiztonsági csoporthivatkozások gyűjteménye, amelyekhez a hálózati felület IP-konfigurációjának tartozni kell.</span><span class="sxs-lookup"><span data-stu-id="6b90d-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6b90d-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="6b90d-133">Olyan alkalmazásbiztonsági csoporthivatkozások gyűjteménye, amelyekhez a hálózati felület IP-konfigurációjának tartozni kell.</span><span class="sxs-lookup"><span data-stu-id="6b90d-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b90d-134">-AsJob</span></span>
<span data-ttu-id="6b90d-135">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6b90d-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b90d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b90d-136">-DefaultProfile</span></span>
<span data-ttu-id="6b90d-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b90d-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b90d-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="6b90d-138">-DnsServer</span></span>
<span data-ttu-id="6b90d-139">A hálózati felület DNS-kiszolgálóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-139">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-140">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="6b90d-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="6b90d-141">Gyorsítja a hálózatépítést.</span><span class="sxs-lookup"><span data-stu-id="6b90d-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="6b90d-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="6b90d-142">-EnableIPForwarding</span></span>
<span data-ttu-id="6b90d-143">Azt jelzi, hogy ez a parancsmag ip-továbbítást tesz lehetővé a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="6b90d-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="6b90d-144">Az IP-továbbítás lehetővé teszi, hogy egy virtuális gép fogadja a más célhelyre címzett forgalmat.</span><span class="sxs-lookup"><span data-stu-id="6b90d-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="6b90d-145">-Force</span><span class="sxs-lookup"><span data-stu-id="6b90d-145">-Force</span></span>
<span data-ttu-id="6b90d-146">Még akkor is kényszeríti a hálózati felület létrehozását, ha már létezik ilyen nevű hálózati felület.</span><span class="sxs-lookup"><span data-stu-id="6b90d-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="6b90d-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="6b90d-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="6b90d-148">Az új hálózati felület belső DNS-névfeliratát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="6b90d-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b90d-149">-IpConfiguration</span></span>
<span data-ttu-id="6b90d-150">Ez a parancsmag által a hálózati felülethez használt IP-konfigurációt határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6b90d-151">-IpConfigurationName</span></span>
<span data-ttu-id="6b90d-152">Egy IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-152">Specifies the name of an IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6b90d-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="6b90d-154">Egy **BackendAddressPool objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-154">Specifies a **BackendAddressPool** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6b90d-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="6b90d-156">A **BackendAddressPool** objektum azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="6b90d-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="6b90d-158">Bejövő NAT-szabálykonfigurációt ad meg a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="6b90d-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="6b90d-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="6b90d-160">A terheléselosztás bejövő NAT-szabály-konfigurációjának azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-161">-Location</span><span class="sxs-lookup"><span data-stu-id="6b90d-161">-Location</span></span>
<span data-ttu-id="6b90d-162">A hálózati felület régióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="6b90d-163">-Name</span><span class="sxs-lookup"><span data-stu-id="6b90d-163">-Name</span></span>
<span data-ttu-id="6b90d-164">A létrehozni szükséges hálózati felület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-164">Specifies the name of the network interface to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6b90d-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="6b90d-166">**NetworkSecurityGroup-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-166">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6b90d-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="6b90d-168">Egy hálózati biztonsági csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-168">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b90d-169">-PrivateIpAddress</span></span>
<span data-ttu-id="6b90d-170">Egy statikus IPv4-es IP-címet ad meg, amely ehhez a hálózati felülethez van rendelve.</span><span class="sxs-lookup"><span data-stu-id="6b90d-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b90d-171">-PublicIpAddress</span></span>
<span data-ttu-id="6b90d-172">A hálózati felülethez hozzárendelni szükséges **PublicIPAddress** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="6b90d-173">-PublicIpAddressId</span></span>
<span data-ttu-id="6b90d-174">A hálózati felülethez hozzárendelni szükséges **PublicIPAddress** objektum azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6b90d-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="6b90d-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b90d-175">-ResourceGroupName</span></span>
<span data-ttu-id="6b90d-176">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a hálózati felület tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b90d-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="6b90d-177">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="6b90d-177">-Subnet</span></span>
<span data-ttu-id="6b90d-178">**Alhálózati objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b90d-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="6b90d-179">Ez a parancsmag létrehoz egy hálózati felületet a paraméter által megadott alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="6b90d-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6b90d-180">-SubnetId</span></span>
<span data-ttu-id="6b90d-181">Annak az alhálózatnak az azonosítója, amelyhez hálózati felületet kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="6b90d-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b90d-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b90d-182">-Tag</span></span>
<span data-ttu-id="6b90d-183">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="6b90d-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6b90d-184">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="6b90d-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6b90d-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b90d-185">-Confirm</span></span>
<span data-ttu-id="6b90d-186">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b90d-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b90d-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b90d-187">-WhatIf</span></span>
<span data-ttu-id="6b90d-188">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b90d-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b90d-189">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b90d-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b90d-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b90d-190">CommonParameters</span></span>
<span data-ttu-id="6b90d-191">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b90d-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b90d-192">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b90d-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b90d-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b90d-193">INPUTS</span></span>

### <span data-ttu-id="6b90d-194">System.String</span><span class="sxs-lookup"><span data-stu-id="6b90d-194">System.String</span></span>

### <span data-ttu-id="6b90d-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="6b90d-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="6b90d-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="6b90d-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="6b90d-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b90d-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="6b90d-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6b90d-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="6b90d-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6b90d-199">System.String[]</span></span>

### <span data-ttu-id="6b90d-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="6b90d-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="6b90d-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="6b90d-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="6b90d-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="6b90d-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="6b90d-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="6b90d-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="6b90d-204">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6b90d-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6b90d-205">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b90d-205">OUTPUTS</span></span>

### <span data-ttu-id="6b90d-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b90d-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6b90d-207">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b90d-207">NOTES</span></span>

## <span data-ttu-id="6b90d-208">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b90d-208">RELATED LINKS</span></span>

[<span data-ttu-id="6b90d-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b90d-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="6b90d-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b90d-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="6b90d-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b90d-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
