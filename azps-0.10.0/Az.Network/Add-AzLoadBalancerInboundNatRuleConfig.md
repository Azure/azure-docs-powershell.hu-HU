---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6a699907b70256995973bfdbde4e11b08c594669
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841822"
---
# <span data-ttu-id="7a7e2-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a7e2-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="7a7e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7e2-103">Bejövő NAT-szabályok konfigurációjának hozzáadása a terheléselosztó eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="7a7e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a7e2-104">SYNTAX</span></span>

### <span data-ttu-id="7a7e2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a7e2-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a7e2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7a7e2-106">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a7e2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a7e2-107">DESCRIPTION</span></span>
<span data-ttu-id="7a7e2-108">Az **Add-AzLoadBalancerInboundNatRuleConfig** parancsmag egy bejövő hálózati címfordítási (NAT) szabály-konfigurációt ad hozzá az Azure terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="7a7e2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7a7e2-109">EXAMPLES</span></span>

### <span data-ttu-id="7a7e2-110">1. példa: bejövő CÍMFORDÍTÁSi szabály konfigurációjának hozzáadása a terheléselosztó eszközhöz</span><span class="sxs-lookup"><span data-stu-id="7a7e2-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="7a7e2-111">Az első parancs beolvassa a MyloadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="7a7e2-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a **AzLoadBalancerInboundNatRuleConfig-** hoz, ami beszámítja a beérkező NAT-szabályok konfigurációját a terheléselosztásba.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="7a7e2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a7e2-113">PARAMETERS</span></span>

### <span data-ttu-id="7a7e2-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7a7e2-114">-BackendPort</span></span>
<span data-ttu-id="7a7e2-115">A szabály-konfigurációval kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="7a7e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7e2-116">-DefaultProfile</span></span>
<span data-ttu-id="7a7e2-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a7e2-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7a7e2-118">-EnableFloatingIP</span></span>
<span data-ttu-id="7a7e2-119">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="7a7e2-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a7e2-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="7a7e2-121">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="7a7e2-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7a7e2-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="7a7e2-123">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-123">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="7a7e2-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7a7e2-124">-FrontendPort</span></span>
<span data-ttu-id="7a7e2-125">A szabály-konfigurációval egyező előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="7a7e2-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7a7e2-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7a7e2-127">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="7a7e2-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a7e2-128">-LoadBalancer</span></span>
<span data-ttu-id="7a7e2-129">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="7a7e2-130">Ez a parancsmag a bejövő NAT-szabályok konfigurációját hozzáadja a paraméter által megadott terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="7a7e2-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a7e2-131">-Name</span></span>
<span data-ttu-id="7a7e2-132">Itt adhatja meg a hozzáadni kívánt bejövő CÍMFORDÍTÁSi szabály konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="7a7e2-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7a7e2-133">-Protocol</span></span>
<span data-ttu-id="7a7e2-134">A bejövő CÍMFORDÍTÁSi szabályok által egyeztetett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="7a7e2-135">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="7a7e2-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7e2-136">CommonParameters</span></span>
<span data-ttu-id="7a7e2-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a7e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7e2-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a7e2-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7e2-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a7e2-139">INPUTS</span></span>

### <span data-ttu-id="7a7e2-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a7e2-140">PSLoadBalancer</span></span>
<span data-ttu-id="7a7e2-141">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7a7e2-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7a7e2-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a7e2-142">OUTPUTS</span></span>

### <span data-ttu-id="7a7e2-143">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a7e2-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7a7e2-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a7e2-144">NOTES</span></span>

## <span data-ttu-id="7a7e2-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a7e2-145">RELATED LINKS</span></span>

[<span data-ttu-id="7a7e2-146">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a7e2-146">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7a7e2-147">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a7e2-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7a7e2-148">Új – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a7e2-148">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7a7e2-149">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a7e2-149">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7a7e2-150">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a7e2-150">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="7a7e2-151">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a7e2-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


