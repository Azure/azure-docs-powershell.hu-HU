---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ed21aec1be522ac145fe255065b650ca4c09dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680657"
---
# <span data-ttu-id="9c73b-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c73b-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="9c73b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c73b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c73b-103">Egy szabály-konfigurációt ad hozzá a terheléselosztó bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="9c73b-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c73b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c73b-104">SYNTAX</span></span>

### <span data-ttu-id="9c73b-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c73b-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c73b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c73b-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c73b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c73b-107">DESCRIPTION</span></span>
<span data-ttu-id="9c73b-108">Az **Add-AzureRmLoadBalancerRuleConfig** parancsmag egy szabály-konfigurációt ad az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="9c73b-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="9c73b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9c73b-109">EXAMPLES</span></span>

### <span data-ttu-id="9c73b-110">1. példa: szabály-konfiguráció hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="9c73b-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="9c73b-111">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="9c73b-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="9c73b-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb **-AzureRmLoadBalancerRuleConfig** , amely hozzáadja a NewRule nevű szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="9c73b-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="9c73b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c73b-113">PARAMETERS</span></span>

### <span data-ttu-id="9c73b-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9c73b-114">-BackendAddressPool</span></span>
<span data-ttu-id="9c73b-115">Annak a backend-címkészletet adja meg, amely a terheléselosztó szabály konfigurációjával van társítva.</span><span class="sxs-lookup"><span data-stu-id="9c73b-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c73b-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9c73b-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="9c73b-117">Annak a **BackendAddressPool** -objektumnak az azonosítóját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="9c73b-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c73b-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9c73b-118">-BackendPort</span></span>
<span data-ttu-id="9c73b-119">A terheléselosztási szabályok konfigurációjának megfelelő adatforgalomhoz tartozó backend-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c73b-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c73b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c73b-120">-DefaultProfile</span></span>
<span data-ttu-id="9c73b-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c73b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c73b-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="9c73b-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="9c73b-123">Beállítja a SNAT a VMs-rendszerhez a backend-készletben, hogy a terheléselosztási szabály publicIP megadott címet használja.</span><span class="sxs-lookup"><span data-stu-id="9c73b-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="9c73b-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="9c73b-124">-EnableFloatingIP</span></span>
<span data-ttu-id="9c73b-125">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="9c73b-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="9c73b-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9c73b-126">-EnableTcpReset</span></span>
<span data-ttu-id="9c73b-127">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="9c73b-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="9c73b-128">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="9c73b-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9c73b-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c73b-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9c73b-130">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c73b-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c73b-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9c73b-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="9c73b-132">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c73b-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="9c73b-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9c73b-133">-FrontendPort</span></span>
<span data-ttu-id="9c73b-134">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c73b-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c73b-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9c73b-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9c73b-136">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztó lapon.</span><span class="sxs-lookup"><span data-stu-id="9c73b-136">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="9c73b-137">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c73b-137">-LoadBalancer</span></span>
<span data-ttu-id="9c73b-138">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9c73b-138">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="9c73b-139">Ez a parancsmag egy szabály-konfigurációt szúr be a paraméter által megadott terheléselosztó értékhez.</span><span class="sxs-lookup"><span data-stu-id="9c73b-139">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c73b-140">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="9c73b-140">-LoadDistribution</span></span>
<span data-ttu-id="9c73b-141">A betöltő eloszlását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c73b-141">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="9c73b-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9c73b-142">-Name</span></span>
<span data-ttu-id="9c73b-143">A terheléselosztó szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c73b-143">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c73b-144">-Szonda</span><span class="sxs-lookup"><span data-stu-id="9c73b-144">-Probe</span></span>
<span data-ttu-id="9c73b-145">Itt adhatja meg azt a szondát, amellyel társítani lehet egy terheléselosztó szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="9c73b-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c73b-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="9c73b-146">-ProbeId</span></span>
<span data-ttu-id="9c73b-147">Annak a szondanak az AZONOSÍTÓját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="9c73b-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c73b-148">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9c73b-148">-Protocol</span></span>
<span data-ttu-id="9c73b-149">Specfies a terheléselosztási szabályok által egyeztetett protokollt.</span><span class="sxs-lookup"><span data-stu-id="9c73b-149">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="9c73b-150">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="9c73b-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="9c73b-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c73b-151">-Confirm</span></span>
<span data-ttu-id="9c73b-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c73b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c73b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c73b-153">-WhatIf</span></span>
<span data-ttu-id="9c73b-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c73b-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c73b-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c73b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c73b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c73b-156">CommonParameters</span></span>
<span data-ttu-id="9c73b-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c73b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c73b-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c73b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c73b-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c73b-159">INPUTS</span></span>

### <span data-ttu-id="9c73b-160">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c73b-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="9c73b-161">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9c73b-161">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="9c73b-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c73b-162">OUTPUTS</span></span>

### <span data-ttu-id="9c73b-163">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c73b-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9c73b-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c73b-164">NOTES</span></span>

## <span data-ttu-id="9c73b-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c73b-165">RELATED LINKS</span></span>

[<span data-ttu-id="9c73b-166">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c73b-166">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="9c73b-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c73b-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="9c73b-168">Új – AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c73b-168">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="9c73b-169">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c73b-169">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="9c73b-170">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c73b-170">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


