---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: feefe02c5056556d360a54819ea429cd39b84b62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012136"
---
# <span data-ttu-id="cc4a0-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cc4a0-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="cc4a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc4a0-102">SYNOPSIS</span></span>
<span data-ttu-id="cc4a0-103">Hálózati felületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-103">Creates a network interface.</span></span>

## <span data-ttu-id="cc4a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc4a0-104">SYNTAX</span></span>

### <span data-ttu-id="cc4a0-105">SetByIpConfigurationResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc4a0-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc4a0-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="cc4a0-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc4a0-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc4a0-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc4a0-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cc4a0-108">SetByResource</span></span>
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

## <span data-ttu-id="cc4a0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc4a0-109">DESCRIPTION</span></span>
<span data-ttu-id="cc4a0-110">A **New-AzNetworkInterface** parancsmag Azure hálózati felületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="cc4a0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cc4a0-111">EXAMPLES</span></span>

### <span data-ttu-id="cc4a0-112">1. példa: Azure-hálózati felület létrehozása</span><span class="sxs-lookup"><span data-stu-id="cc4a0-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="cc4a0-113">Ez a parancs létrehoz egy NetworkInterface001 nevű hálózati felületet egy dinamikusan kiosztott privát IP-címmel a Subnet1-ról a VirtualNetwork1 nevű virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="cc4a0-114">A parancs két DNS-kiszolgálót is hozzárendel a hálózati kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="cc4a0-115">A program automatikusan létrehozza a IPConfiguration-gyermek erőforrást a IPConfiguration1 név használatával.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="cc4a0-116">2. példa: Azure-hálózati kapcsolat létrehozása IP-konfigurációs objektum használatával</span><span class="sxs-lookup"><span data-stu-id="cc4a0-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="cc4a0-117">Ez a példa egy új hálózati felületet hoz létre egy IP-konfigurációs objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="cc4a0-118">Az IP Configuration objektum egy statikus privát IPv4-címet ad meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="cc4a0-119">Az első parancs a meglévő, a második parancsban hozzárendelt virtuális hálózatot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="cc4a0-120">A második parancs létrehozza a IPConfig1 nevű hálózati kapcsolat IP-konfigurációját, és a konfigurációt a $IPconfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="cc4a0-121">A harmadik parancs létrehoz egy NetworkInterface1 nevű hálózati felületet, amely a $IPconfig nevű változóban tárolt hálózati kapcsolat IP-konfigurációját használja.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="cc4a0-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc4a0-122">PARAMETERS</span></span>

### <span data-ttu-id="cc4a0-123">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cc4a0-123">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="cc4a0-124">Egy **ApplicationGatewayBackendAddressPool** objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-124">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cc4a0-125">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cc4a0-125">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="cc4a0-126">Egy **ApplicationGatewayBackendAddressPool** -objektum azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-126">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cc4a0-127">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc4a0-127">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="cc4a0-128">Az alkalmazás biztonsági csoportjának hivatkozását adja meg, amelyre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-128">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="cc4a0-129">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cc4a0-129">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="cc4a0-130">Az alkalmazás biztonsági csoportjának hivatkozását adja meg, amelyre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-130">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="cc4a0-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc4a0-131">-AsJob</span></span>
<span data-ttu-id="cc4a0-132">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cc4a0-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc4a0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc4a0-133">-DefaultProfile</span></span>
<span data-ttu-id="cc4a0-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc4a0-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="cc4a0-135">-DnsServer</span></span>
<span data-ttu-id="cc4a0-136">A hálózati kapcsolat DNS-kiszolgálóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-136">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="cc4a0-137">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="cc4a0-137">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="cc4a0-138">Gyorsított hálózatokat tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-138">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="cc4a0-139">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="cc4a0-139">-EnableIPForwarding</span></span>
<span data-ttu-id="cc4a0-140">Jelzi, hogy ez a parancsmag engedélyezi az IP-továbbítást a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-140">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="cc4a0-141">Az IP-továbbítás lehetővé teszi a virtuális gép számára az egyéb rendeltetési helyekre címzett forgalom átvételét.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-141">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="cc4a0-142">-Force</span><span class="sxs-lookup"><span data-stu-id="cc4a0-142">-Force</span></span>
<span data-ttu-id="cc4a0-143">Akkor is kényszeríti a hálózati felület létrehozását, ha már létezik azonos nevű hálózati kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-143">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="cc4a0-144">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="cc4a0-144">-InternalDnsNameLabel</span></span>
<span data-ttu-id="cc4a0-145">Az új hálózati kapcsolat belső DNS-név címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-145">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="cc4a0-146">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc4a0-146">-IpConfiguration</span></span>
<span data-ttu-id="cc4a0-147">A parancsmag által a hálózati kapcsolathoz használt IP-konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-147">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="cc4a0-148">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cc4a0-148">-IpConfigurationName</span></span>
<span data-ttu-id="cc4a0-149">Az IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-149">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="cc4a0-150">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cc4a0-150">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="cc4a0-151">Egy **BackendAddressPool** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-151">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cc4a0-152">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cc4a0-152">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="cc4a0-153">Egy **BackendAddressPool** -objektum azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-153">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cc4a0-154">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="cc4a0-154">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="cc4a0-155">Bejövő hálózati címfordítási szabály konfigurációját adja meg a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-155">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="cc4a0-156">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="cc4a0-156">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="cc4a0-157">A terheléselosztáshoz tartozó bejövő CÍMFORDÍTÁSi szabályok konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-157">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="cc4a0-158">-Hely</span><span class="sxs-lookup"><span data-stu-id="cc4a0-158">-Location</span></span>
<span data-ttu-id="cc4a0-159">Egy hálózati kapcsolat területét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-159">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="cc4a0-160">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc4a0-160">-Name</span></span>
<span data-ttu-id="cc4a0-161">A létrehozandó hálózati csatoló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-161">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="cc4a0-162">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc4a0-162">-NetworkSecurityGroup</span></span>
<span data-ttu-id="cc4a0-163">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-163">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="cc4a0-164">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cc4a0-164">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="cc4a0-165">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-165">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="cc4a0-166">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="cc4a0-166">-PrivateIpAddress</span></span>
<span data-ttu-id="cc4a0-167">Megadja a hálózati kapcsolathoz hozzárendelni kívánt statikus IPv4 IP-címet.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-167">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="cc4a0-168">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cc4a0-168">-PublicIpAddress</span></span>
<span data-ttu-id="cc4a0-169">Itt adhatja meg azt a **PublicIPAddress** objektumot, amelyet hálózati kapcsolathoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-169">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="cc4a0-170">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="cc4a0-170">-PublicIpAddressId</span></span>
<span data-ttu-id="cc4a0-171">Annak a **PublicIPAddress** -objektumnak az azonosítóját adja meg, amelyet egy hálózati kapcsolathoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-171">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="cc4a0-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc4a0-172">-ResourceGroupName</span></span>
<span data-ttu-id="cc4a0-173">Annak a csoportnak a neve, amelyhez a hálózati kapcsolat tartozik.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-173">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="cc4a0-174">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="cc4a0-174">-Subnet</span></span>
<span data-ttu-id="cc4a0-175">**Alhálózat** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-175">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="cc4a0-176">Ez a parancsmag létrehoz egy hálózati felületet annak az alhálózatnak, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-176">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="cc4a0-177">– NetI</span><span class="sxs-lookup"><span data-stu-id="cc4a0-177">-SubnetId</span></span>
<span data-ttu-id="cc4a0-178">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyhez hálózati felületet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-178">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="cc4a0-179">-Címke</span><span class="sxs-lookup"><span data-stu-id="cc4a0-179">-Tag</span></span>
<span data-ttu-id="cc4a0-180">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-180">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cc4a0-181">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="cc4a0-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cc4a0-182">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc4a0-182">-Confirm</span></span>
<span data-ttu-id="cc4a0-183">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc4a0-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc4a0-184">-WhatIf</span></span>
<span data-ttu-id="cc4a0-185">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc4a0-186">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc4a0-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc4a0-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc4a0-187">CommonParameters</span></span>
<span data-ttu-id="cc4a0-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc4a0-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc4a0-189">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc4a0-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc4a0-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc4a0-190">INPUTS</span></span>

### <span data-ttu-id="cc4a0-191">System. String</span><span class="sxs-lookup"><span data-stu-id="cc4a0-191">System.String</span></span>

### <span data-ttu-id="cc4a0-192">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="cc4a0-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="cc4a0-193">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cc4a0-193">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="cc4a0-194">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cc4a0-194">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="cc4a0-195">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc4a0-195">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="cc4a0-196">System. string []</span><span class="sxs-lookup"><span data-stu-id="cc4a0-196">System.String[]</span></span>

### <span data-ttu-id="cc4a0-197">Microsoft. Azure. commands. Network. models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="cc4a0-197">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="cc4a0-198">Microsoft. Azure. commands. Network. models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="cc4a0-198">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="cc4a0-199">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="cc4a0-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="cc4a0-200">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="cc4a0-200">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="cc4a0-201">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cc4a0-201">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cc4a0-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc4a0-202">OUTPUTS</span></span>

### <span data-ttu-id="cc4a0-203">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cc4a0-203">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="cc4a0-204">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc4a0-204">NOTES</span></span>

## <span data-ttu-id="cc4a0-205">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc4a0-205">RELATED LINKS</span></span>

[<span data-ttu-id="cc4a0-206">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cc4a0-206">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="cc4a0-207">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cc4a0-207">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="cc4a0-208">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cc4a0-208">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
