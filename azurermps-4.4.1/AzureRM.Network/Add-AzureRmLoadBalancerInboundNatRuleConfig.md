---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ee0a001894570c66145ac7f75d12451df5faaab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673106"
---
# <span data-ttu-id="785c4-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="785c4-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="785c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="785c4-102">SYNOPSIS</span></span>
<span data-ttu-id="785c4-103">Bejövő NAT-szabályok konfigurációjának hozzáadása a terheléselosztó eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="785c4-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="785c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="785c4-104">SYNTAX</span></span>

### <span data-ttu-id="785c4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="785c4-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="785c4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="785c4-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="785c4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="785c4-107">DESCRIPTION</span></span>
<span data-ttu-id="785c4-108">Az **Add-AzureRmLoadBalancerInboundNatRuleConfig** parancsmag egy bejövő hálózati címfordítási (NAT) szabály-konfigurációt ad hozzá az Azure terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="785c4-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="785c4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="785c4-109">EXAMPLES</span></span>

### <span data-ttu-id="785c4-110">1. példa: bejövő CÍMFORDÍTÁSi szabály konfigurációjának hozzáadása a terheléselosztó eszközhöz</span><span class="sxs-lookup"><span data-stu-id="785c4-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="785c4-111">Az első parancs beolvassa a MyloadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="785c4-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="785c4-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a **AzureRmLoadBalancerInboundNatRuleConfig-** hoz, ami beszámítja a beérkező NAT-szabályok konfigurációját a terheléselosztásba.</span><span class="sxs-lookup"><span data-stu-id="785c4-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="785c4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="785c4-113">PARAMETERS</span></span>

### <span data-ttu-id="785c4-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="785c4-114">-BackendPort</span></span>
<span data-ttu-id="785c4-115">A szabály-konfigurációval kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="785c4-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785c4-116">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="785c4-116">-EnableFloatingIP</span></span>
<span data-ttu-id="785c4-117">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="785c4-117">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="785c4-118">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="785c4-118">-FrontendIpConfiguration</span></span>
<span data-ttu-id="785c4-119">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="785c4-119">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785c4-120">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="785c4-120">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="785c4-121">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="785c4-121">Specifies an ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785c4-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="785c4-122">-FrontendPort</span></span>
<span data-ttu-id="785c4-123">A szabály-konfigurációval egyező előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="785c4-123">Specifies the front-end port that is matched by a rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785c4-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="785c4-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="785c4-125">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="785c4-125">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785c4-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="785c4-126">-LoadBalancer</span></span>
<span data-ttu-id="785c4-127">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="785c4-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="785c4-128">Ez a parancsmag a bejövő NAT-szabályok konfigurációját hozzáadja a paraméter által megadott terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="785c4-128">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="785c4-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="785c4-129">-Name</span></span>
<span data-ttu-id="785c4-130">Itt adhatja meg a hozzáadni kívánt bejövő CÍMFORDÍTÁSi szabály konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="785c4-130">Specifies the name of the inbound NAT rule configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785c4-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="785c4-131">-Protocol</span></span>
<span data-ttu-id="785c4-132">A bejövő CÍMFORDÍTÁSi szabályok által egyeztetett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="785c4-132">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="785c4-133">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="785c4-133">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785c4-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="785c4-134">-DefaultProfile</span></span>
<span data-ttu-id="785c4-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="785c4-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="785c4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785c4-136">CommonParameters</span></span>
<span data-ttu-id="785c4-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="785c4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785c4-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="785c4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785c4-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="785c4-139">INPUTS</span></span>

### <span data-ttu-id="785c4-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="785c4-140">PSLoadBalancer</span></span>
<span data-ttu-id="785c4-141">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="785c4-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="785c4-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="785c4-142">OUTPUTS</span></span>

### <span data-ttu-id="785c4-143">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="785c4-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="785c4-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="785c4-144">NOTES</span></span>

## <span data-ttu-id="785c4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="785c4-145">RELATED LINKS</span></span>

[<span data-ttu-id="785c4-146">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="785c4-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="785c4-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="785c4-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="785c4-148">Új – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="785c4-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="785c4-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="785c4-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="785c4-150">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="785c4-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="785c4-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="785c4-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


