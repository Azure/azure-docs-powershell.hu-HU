---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c8de559b6a2b6da9212cb6d9e2607392cf787bf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843633"
---
# <span data-ttu-id="427d4-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="427d4-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="427d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="427d4-102">SYNOPSIS</span></span>
<span data-ttu-id="427d4-103">Bejövő hálózati címfordítási szabály konfigurációjának beállítása terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="427d4-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="427d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="427d4-104">SYNTAX</span></span>

### <span data-ttu-id="427d4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="427d4-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="427d4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="427d4-106">SetByResource</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="427d4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="427d4-107">DESCRIPTION</span></span>
<span data-ttu-id="427d4-108">A **set-AzLoadBalancerInboundNatRuleConfig** parancsmag egy beérkező hálózati címfordítási (NAT) szabály-konfigurációt állít be egy Azure-terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="427d4-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="427d4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="427d4-109">EXAMPLES</span></span>

### <span data-ttu-id="427d4-110">Példa 1: a bejövő CÍMFORDÍTÁSi szabály konfigurációjának módosítása a terheléselosztó eszközön</span><span class="sxs-lookup"><span data-stu-id="427d4-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="427d4-111">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="427d4-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="427d4-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzLoadBalancerInboundNatRuleConfig-hoz, ami beérkező hálózati címfordítási szabály konfigurációját adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="427d4-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="427d4-113">A harmadik parancs átadja a kiegyenlítőt a **set-AzLoadBalancerInboundNatRuleConfig** , amely menti és FRISSÍTI a NAT-szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="427d4-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="427d4-114">Fontos tudni, hogy a szabály konfigurációja a lebegő IP engedélyezése nélkül volt beállítva, amelyet az előző parancs engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="427d4-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="427d4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="427d4-115">PARAMETERS</span></span>

### <span data-ttu-id="427d4-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="427d4-116">-BackendPort</span></span>
<span data-ttu-id="427d4-117">A beállítás által kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="427d4-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="427d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="427d4-118">-DefaultProfile</span></span>
<span data-ttu-id="427d4-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="427d4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="427d4-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="427d4-120">-EnableFloatingIP</span></span>
<span data-ttu-id="427d4-121">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="427d4-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="427d4-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="427d4-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="427d4-123">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="427d4-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="427d4-124">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="427d4-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="427d4-125">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="427d4-125">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="427d4-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="427d4-126">-FrontendPort</span></span>
<span data-ttu-id="427d4-127">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="427d4-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="427d4-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="427d4-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="427d4-129">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="427d4-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="427d4-130">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="427d4-130">-LoadBalancer</span></span>
<span data-ttu-id="427d4-131">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="427d4-131">Specifies a load balancer.</span></span>
<span data-ttu-id="427d4-132">Ez a parancsmag bejelöli a hálózati címfordítási szabály konfigurációját a paraméter által megadott terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="427d4-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="427d4-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="427d4-133">-Name</span></span>
<span data-ttu-id="427d4-134">A beérkező NAT-szabályok konfigurációjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="427d4-134">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="427d4-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="427d4-135">-Protocol</span></span>
<span data-ttu-id="427d4-136">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjának megfelelő protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="427d4-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="427d4-137">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="427d4-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="427d4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="427d4-138">CommonParameters</span></span>
<span data-ttu-id="427d4-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="427d4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="427d4-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="427d4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="427d4-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="427d4-141">INPUTS</span></span>

### <span data-ttu-id="427d4-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="427d4-142">PSLoadBalancer</span></span>
<span data-ttu-id="427d4-143">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="427d4-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="427d4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="427d4-144">OUTPUTS</span></span>

### <span data-ttu-id="427d4-145">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="427d4-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="427d4-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="427d4-146">NOTES</span></span>

## <span data-ttu-id="427d4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="427d4-147">RELATED LINKS</span></span>

[<span data-ttu-id="427d4-148">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="427d4-148">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="427d4-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="427d4-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="427d4-150">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="427d4-150">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="427d4-151">Új – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="427d4-151">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="427d4-152">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="427d4-152">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


