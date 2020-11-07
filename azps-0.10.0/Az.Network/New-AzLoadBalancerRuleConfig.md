---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 657a03dbf69df1fe11cf0ceff1c5f594cabc9b41
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841326"
---
# <span data-ttu-id="8b956-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b956-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="8b956-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b956-102">SYNOPSIS</span></span>
<span data-ttu-id="8b956-103">Szabály-konfigurációt hoz létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="8b956-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="8b956-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b956-104">SYNTAX</span></span>

### <span data-ttu-id="8b956-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b956-105">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b956-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8b956-106">SetByResource</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b956-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b956-107">DESCRIPTION</span></span>
<span data-ttu-id="8b956-108">A **New-AzLoadBalancerRuleConfig** parancsmag létrehoz egy szabály-konfigurációt az Azure terheléselosztó szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="8b956-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8b956-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8b956-109">EXAMPLES</span></span>

### <span data-ttu-id="8b956-110">1: szabály-konfiguráció létrehozása Azure-terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="8b956-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="8b956-111">Az első három parancs a nyilvános IP-címet, az előtér-előnézetet, valamint a szabály konfigurációjának megfelelő szondát tartalmaz a Forth parancsban.</span><span class="sxs-lookup"><span data-stu-id="8b956-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="8b956-112">A Forth parancs új szabályt hoz létre, amelynek neve MyLBrule bizonyos előírásokkal.</span><span class="sxs-lookup"><span data-stu-id="8b956-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="8b956-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b956-113">PARAMETERS</span></span>

### <span data-ttu-id="8b956-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8b956-114">-BackendAddressPool</span></span>
<span data-ttu-id="8b956-115">Itt adhatja meg azt a **BackendAddressPool** -objektumot, amellyel társítani szeretné a terheléselosztó szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="8b956-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8b956-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8b956-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="8b956-117">Annak a **BackendAddressPool** -objektumnak az azonosítóját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="8b956-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8b956-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8b956-118">-BackendPort</span></span>
<span data-ttu-id="8b956-119">A terheléselosztási szabály konfigurációjának megfelelő adatforgalomhoz tartozó backend-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b956-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8b956-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b956-120">-DefaultProfile</span></span>
<span data-ttu-id="8b956-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b956-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b956-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="8b956-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="8b956-123">Beállítja a SNAT a VMs-rendszerhez a backend-készletben, hogy a terheléselosztási szabály publicIP megadott címet használja.</span><span class="sxs-lookup"><span data-stu-id="8b956-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="8b956-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="8b956-124">-EnableFloatingIP</span></span>
<span data-ttu-id="8b956-125">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="8b956-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="8b956-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b956-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="8b956-127">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b956-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8b956-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8b956-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="8b956-129">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b956-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="8b956-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="8b956-130">-FrontendPort</span></span>
<span data-ttu-id="8b956-131">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b956-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8b956-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8b956-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8b956-133">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="8b956-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="8b956-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="8b956-134">-LoadDistribution</span></span>
<span data-ttu-id="8b956-135">A betöltő eloszlását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b956-135">Specifies a load distribution.</span></span>
<span data-ttu-id="8b956-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8b956-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8b956-137">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="8b956-137">Default</span></span>
- <span data-ttu-id="8b956-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="8b956-138">SourceIP</span></span>
- <span data-ttu-id="8b956-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="8b956-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="8b956-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b956-140">-Name</span></span>
<span data-ttu-id="8b956-141">A parancsmag által létrehozott terheléselosztási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b956-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8b956-142">-Szonda</span><span class="sxs-lookup"><span data-stu-id="8b956-142">-Probe</span></span>
<span data-ttu-id="8b956-143">Itt adhatja meg azt a szondát, amellyel társítani lehet egy terheléselosztó szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="8b956-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8b956-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="8b956-144">-ProbeId</span></span>
<span data-ttu-id="8b956-145">Annak a szondanak az AZONOSÍTÓját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="8b956-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8b956-146">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8b956-146">-Protocol</span></span>
<span data-ttu-id="8b956-147">A terheléselosztási szabályok konfigurációjának megfelelő protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b956-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="8b956-148">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="8b956-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="8b956-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b956-149">CommonParameters</span></span>
<span data-ttu-id="8b956-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b956-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b956-151">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b956-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b956-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b956-152">INPUTS</span></span>

## <span data-ttu-id="8b956-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b956-153">OUTPUTS</span></span>

### <span data-ttu-id="8b956-154">Microsoft. Azure. commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="8b956-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="8b956-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b956-155">NOTES</span></span>

## <span data-ttu-id="8b956-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b956-156">RELATED LINKS</span></span>

[<span data-ttu-id="8b956-157">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b956-157">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8b956-158">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b956-158">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8b956-159">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b956-159">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8b956-160">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b956-160">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


