---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 52e1759f82ba6663215907a93f89f562df1b6afa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841810"
---
# <span data-ttu-id="4d521-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d521-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="4d521-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d521-102">SYNOPSIS</span></span>
<span data-ttu-id="4d521-103">Egy szabály-konfigurációt ad hozzá a terheléselosztó bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="4d521-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="4d521-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d521-104">SYNTAX</span></span>

### <span data-ttu-id="4d521-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d521-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d521-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4d521-106">SetByResource</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d521-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d521-107">DESCRIPTION</span></span>
<span data-ttu-id="4d521-108">Az **Add-AzLoadBalancerRuleConfig** parancsmag egy szabály-konfigurációt ad az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="4d521-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="4d521-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4d521-109">EXAMPLES</span></span>

### <span data-ttu-id="4d521-110">1. példa: szabály-konfiguráció hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="4d521-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="4d521-111">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="4d521-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="4d521-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb **-AzLoadBalancerRuleConfig** , amely hozzáadja a NewRule nevű szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="4d521-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="4d521-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d521-113">PARAMETERS</span></span>

### <span data-ttu-id="4d521-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4d521-114">-BackendAddressPool</span></span>
<span data-ttu-id="4d521-115">Annak a backend-címkészletet adja meg, amely a terheléselosztó szabály konfigurációjával van társítva.</span><span class="sxs-lookup"><span data-stu-id="4d521-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4d521-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="4d521-117">Annak a **BackendAddressPool** -objektumnak az azonosítóját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="4d521-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4d521-118">-BackendPort</span></span>
<span data-ttu-id="4d521-119">A terheléselosztási szabályok konfigurációjának megfelelő adatforgalomhoz tartozó backend-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d521-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d521-120">-DefaultProfile</span></span>
<span data-ttu-id="4d521-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d521-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d521-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="4d521-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="4d521-123">Beállítja a SNAT a VMs-rendszerhez a backend-készletben, hogy a terheléselosztási szabály publicIP megadott címet használja.</span><span class="sxs-lookup"><span data-stu-id="4d521-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="4d521-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4d521-124">-EnableFloatingIP</span></span>
<span data-ttu-id="4d521-125">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="4d521-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="4d521-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d521-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4d521-127">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d521-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4d521-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="4d521-129">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d521-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4d521-130">-FrontendPort</span></span>
<span data-ttu-id="4d521-131">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d521-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4d521-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4d521-133">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztó lapon.</span><span class="sxs-lookup"><span data-stu-id="4d521-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d521-134">-LoadBalancer</span></span>
<span data-ttu-id="4d521-135">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4d521-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="4d521-136">Ez a parancsmag egy szabály-konfigurációt szúr be a paraméter által megadott terheléselosztó értékhez.</span><span class="sxs-lookup"><span data-stu-id="4d521-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="4d521-137">-LoadDistribution</span></span>
<span data-ttu-id="4d521-138">A betöltő eloszlását adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d521-138">Specifies a load distribution.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d521-139">-Name</span></span>
<span data-ttu-id="4d521-140">A terheléselosztó szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d521-140">Specifies the name of the load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-141">-Szonda</span><span class="sxs-lookup"><span data-stu-id="4d521-141">-Probe</span></span>
<span data-ttu-id="4d521-142">Itt adhatja meg azt a szondát, amellyel társítani lehet egy terheléselosztó szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="4d521-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-143">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="4d521-143">-ProbeId</span></span>
<span data-ttu-id="4d521-144">Annak a szondanak az AZONOSÍTÓját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="4d521-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-145">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4d521-145">-Protocol</span></span>
<span data-ttu-id="4d521-146">Specfies a terheléselosztási szabályok által egyeztetett protokollt.</span><span class="sxs-lookup"><span data-stu-id="4d521-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="4d521-147">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="4d521-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d521-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d521-148">CommonParameters</span></span>
<span data-ttu-id="4d521-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d521-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d521-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d521-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d521-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d521-151">INPUTS</span></span>

### <span data-ttu-id="4d521-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d521-152">PSLoadBalancer</span></span>
<span data-ttu-id="4d521-153">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4d521-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4d521-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d521-154">OUTPUTS</span></span>

### <span data-ttu-id="4d521-155">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d521-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4d521-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d521-156">NOTES</span></span>

## <span data-ttu-id="4d521-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d521-157">RELATED LINKS</span></span>

[<span data-ttu-id="4d521-158">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d521-158">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4d521-159">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d521-159">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4d521-160">Új – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d521-160">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4d521-161">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d521-161">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4d521-162">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d521-162">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


