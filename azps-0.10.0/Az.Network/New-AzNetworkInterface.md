---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: a4a40f67eef901cd1e93ac004fa01a3224ab222e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841321"
---
# <span data-ttu-id="f5ced-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f5ced-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="f5ced-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5ced-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ced-103">Hálózati felületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f5ced-103">Creates a network interface.</span></span>

## <span data-ttu-id="f5ced-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5ced-104">SYNTAX</span></span>

### <span data-ttu-id="f5ced-105">SetByIpConfigurationResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5ced-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5ced-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="f5ced-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5ced-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5ced-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5ced-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f5ced-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5ced-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5ced-109">DESCRIPTION</span></span>
<span data-ttu-id="f5ced-110">A **New-AzNetworkInterface** parancsmag Azure hálózati felületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f5ced-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="f5ced-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f5ced-111">EXAMPLES</span></span>

### <span data-ttu-id="f5ced-112">1. példa: Azure-hálózati felület létrehozása</span><span class="sxs-lookup"><span data-stu-id="f5ced-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="f5ced-113">Ez a parancs létrehoz egy NetworkInterface001 nevű hálózati felületet egy dinamikusan kiosztott privát IP-címmel a Subnet1-ról a VirtualNetwork1 nevű virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="f5ced-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="f5ced-114">A parancs két DNS-kiszolgálót is hozzárendel a hálózati kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="f5ced-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="f5ced-115">A program automatikusan létrehozza a IPConfiguration-gyermek erőforrást a IPConfiguration1 név használatával.</span><span class="sxs-lookup"><span data-stu-id="f5ced-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="f5ced-116">2. példa: Azure-hálózati kapcsolat létrehozása IP-konfigurációs objektum használatával</span><span class="sxs-lookup"><span data-stu-id="f5ced-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="f5ced-117">Ez a példa egy új hálózati felületet hoz létre egy IP-konfigurációs objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="f5ced-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="f5ced-118">Az IP Configuration objektum egy statikus privát IPv4-címet ad meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="f5ced-119">Az első parancs létrehozza a IPConfig1 nevű hálózati kapcsolat IP-konfigurációját, és a konfigurációt a $IPconfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f5ced-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="f5ced-120">A második parancs létrehoz egy NetworkInterface1 nevű hálózati felületet, amely a $IPconfig nevű változóban tárolt hálózati kapcsolat IP-konfigurációját használja.</span><span class="sxs-lookup"><span data-stu-id="f5ced-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="f5ced-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5ced-121">PARAMETERS</span></span>

### <span data-ttu-id="f5ced-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f5ced-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="f5ced-123">Egy **ApplicationGatewayBackendAddressPool** objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f5ced-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="f5ced-125">Egy **ApplicationGatewayBackendAddressPool** -objektum azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f5ced-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="f5ced-127">Az alkalmazás biztonsági csoportjának hivatkozását adja meg, amelyre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="f5ced-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f5ced-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="f5ced-129">Az alkalmazás biztonsági csoportjának hivatkozását adja meg, amelyre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="f5ced-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5ced-130">-AsJob</span></span>
<span data-ttu-id="f5ced-131">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f5ced-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ced-132">-DefaultProfile</span></span>
<span data-ttu-id="f5ced-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5ced-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="f5ced-134">-DnsServer</span></span>
<span data-ttu-id="f5ced-135">A hálózati kapcsolat DNS-kiszolgálóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-135">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="f5ced-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="f5ced-137">Gyorsított hálózatokat tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="f5ced-137">Enables accelerated networking.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="f5ced-138">-EnableIPForwarding</span></span>
<span data-ttu-id="f5ced-139">Jelzi, hogy ez a parancsmag engedélyezi az IP-továbbítást a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="f5ced-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="f5ced-140">Az IP-továbbítás lehetővé teszi a virtuális gép számára az egyéb rendeltetési helyekre címzett forgalom átvételét.</span><span class="sxs-lookup"><span data-stu-id="f5ced-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-141">-Force</span><span class="sxs-lookup"><span data-stu-id="f5ced-141">-Force</span></span>
<span data-ttu-id="f5ced-142">Akkor is kényszeríti a hálózati felület létrehozását, ha már létezik azonos nevű hálózati kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="f5ced-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="f5ced-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="f5ced-144">Az új hálózati kapcsolat belső DNS-név címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-144">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5ced-145">-IpConfiguration</span></span>
<span data-ttu-id="f5ced-146">A parancsmag által a hálózati kapcsolathoz használt IP-konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f5ced-147">-IpConfigurationName</span></span>
<span data-ttu-id="f5ced-148">Az IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-148">Specifies the name of an IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f5ced-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="f5ced-150">Egy **BackendAddressPool** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-150">Specifies a **BackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f5ced-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="f5ced-152">Egy **BackendAddressPool** -objektum azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="f5ced-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="f5ced-154">Bejövő hálózati címfordítási szabály konfigurációját adja meg a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="f5ced-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="f5ced-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="f5ced-156">A terheléselosztáshoz tartozó bejövő CÍMFORDÍTÁSi szabályok konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-157">-Hely</span><span class="sxs-lookup"><span data-stu-id="f5ced-157">-Location</span></span>
<span data-ttu-id="f5ced-158">Egy hálózati kapcsolat területét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-158">Specifies the region for a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-159">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5ced-159">-Name</span></span>
<span data-ttu-id="f5ced-160">A létrehozandó hálózati csatoló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-160">Specifies the name of the network interface to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f5ced-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f5ced-162">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-162">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f5ced-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="f5ced-164">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-164">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f5ced-165">-PrivateIpAddress</span></span>
<span data-ttu-id="f5ced-166">Megadja a hálózati kapcsolathoz hozzárendelni kívánt statikus IPv4 IP-címet.</span><span class="sxs-lookup"><span data-stu-id="f5ced-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f5ced-167">-PublicIpAddress</span></span>
<span data-ttu-id="f5ced-168">Itt adhatja meg azt a **PublicIPAddress** objektumot, amelyet hálózati kapcsolathoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="f5ced-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f5ced-169">-PublicIpAddressId</span></span>
<span data-ttu-id="f5ced-170">Annak a **PublicIPAddress** -objektumnak az azonosítóját adja meg, amelyet egy hálózati kapcsolathoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="f5ced-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ced-171">-ResourceGroupName</span></span>
<span data-ttu-id="f5ced-172">Annak a csoportnak a neve, amelyhez a hálózati kapcsolat tartozik.</span><span class="sxs-lookup"><span data-stu-id="f5ced-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-173">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="f5ced-173">-Subnet</span></span>
<span data-ttu-id="f5ced-174">**Alhálózat** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="f5ced-175">Ez a parancsmag létrehoz egy hálózati felületet annak az alhálózatnak, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f5ced-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-176">– NetI</span><span class="sxs-lookup"><span data-stu-id="f5ced-176">-SubnetId</span></span>
<span data-ttu-id="f5ced-177">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyhez hálózati felületet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="f5ced-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-178">-Címke</span><span class="sxs-lookup"><span data-stu-id="f5ced-178">-Tag</span></span>
<span data-ttu-id="f5ced-179">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="f5ced-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f5ced-180">Példa:</span><span class="sxs-lookup"><span data-stu-id="f5ced-180">For example:</span></span>

<span data-ttu-id="f5ced-181">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="f5ced-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-182">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5ced-182">-Confirm</span></span>
<span data-ttu-id="f5ced-183">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5ced-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ced-184">-WhatIf</span></span>
<span data-ttu-id="f5ced-185">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5ced-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5ced-186">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5ced-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ced-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ced-187">CommonParameters</span></span>
<span data-ttu-id="f5ced-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5ced-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ced-189">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ced-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ced-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5ced-190">INPUTS</span></span>

## <span data-ttu-id="f5ced-191">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5ced-191">OUTPUTS</span></span>

### <span data-ttu-id="f5ced-192">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f5ced-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f5ced-193">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5ced-193">NOTES</span></span>

## <span data-ttu-id="f5ced-194">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5ced-194">RELATED LINKS</span></span>

[<span data-ttu-id="f5ced-195">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f5ced-195">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="f5ced-196">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f5ced-196">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="f5ced-197">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f5ced-197">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
