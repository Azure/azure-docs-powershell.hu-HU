---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: fad24c7cb9b6146ecb5fa1f0c2c21e1f2c0adbf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679395"
---
# <span data-ttu-id="7cf99-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf99-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="7cf99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cf99-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf99-103">Szabály-konfigurációt hoz létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="7cf99-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cf99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cf99-104">SYNTAX</span></span>

### <span data-ttu-id="7cf99-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf99-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cf99-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7cf99-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cf99-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cf99-107">DESCRIPTION</span></span>
<span data-ttu-id="7cf99-108">A **New-AzureRmLoadBalancerRuleConfig** parancsmag létrehoz egy szabály-konfigurációt az Azure terheléselosztó szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="7cf99-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="7cf99-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7cf99-109">EXAMPLES</span></span>

### <span data-ttu-id="7cf99-110">1: szabály-konfiguráció létrehozása Azure-terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="7cf99-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="7cf99-111">Az első három parancs a nyilvános IP-címet, az előtér-előnézetet, valamint a szabály konfigurációjának megfelelő szondát tartalmaz a Forth parancsban.</span><span class="sxs-lookup"><span data-stu-id="7cf99-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="7cf99-112">A Forth parancs új szabályt hoz létre, amelynek neve MyLBrule bizonyos előírásokkal.</span><span class="sxs-lookup"><span data-stu-id="7cf99-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="7cf99-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cf99-113">PARAMETERS</span></span>

### <span data-ttu-id="7cf99-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7cf99-114">-BackendAddressPool</span></span>
<span data-ttu-id="7cf99-115">Itt adhatja meg azt a **BackendAddressPool** -objektumot, amellyel társítani szeretné a terheléselosztó szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="7cf99-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf99-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7cf99-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="7cf99-117">Annak a **BackendAddressPool** -objektumnak az azonosítóját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="7cf99-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7cf99-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7cf99-118">-BackendPort</span></span>
<span data-ttu-id="7cf99-119">A terheléselosztási szabály konfigurációjának megfelelő adatforgalomhoz tartozó backend-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cf99-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7cf99-120">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="7cf99-120">-DisableOutboundSNAT</span></span>
<span data-ttu-id="7cf99-121">Beállítja a SNAT a VMs-rendszerhez a backend-készletben, hogy a terheléselosztási szabály publicIP megadott címet használja.</span><span class="sxs-lookup"><span data-stu-id="7cf99-121">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="7cf99-122">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7cf99-122">-EnableFloatingIP</span></span>
<span data-ttu-id="7cf99-123">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="7cf99-123">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="7cf99-124">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cf99-124">-FrontendIpConfiguration</span></span>
<span data-ttu-id="7cf99-125">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cf99-125">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7cf99-126">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7cf99-126">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="7cf99-127">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cf99-127">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="7cf99-128">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7cf99-128">-FrontendPort</span></span>
<span data-ttu-id="7cf99-129">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cf99-129">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7cf99-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7cf99-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7cf99-131">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="7cf99-131">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="7cf99-132">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="7cf99-132">-LoadDistribution</span></span>
<span data-ttu-id="7cf99-133">A betöltő eloszlását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cf99-133">Specifies a load distribution.</span></span>
<span data-ttu-id="7cf99-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7cf99-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7cf99-135">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="7cf99-135">Default</span></span>
- <span data-ttu-id="7cf99-136">SourceIP</span><span class="sxs-lookup"><span data-stu-id="7cf99-136">SourceIP</span></span>
- <span data-ttu-id="7cf99-137">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="7cf99-137">SourceIPProtocol</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf99-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cf99-138">-Name</span></span>
<span data-ttu-id="7cf99-139">A parancsmag által létrehozott terheléselosztási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cf99-139">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7cf99-140">-Szonda</span><span class="sxs-lookup"><span data-stu-id="7cf99-140">-Probe</span></span>
<span data-ttu-id="7cf99-141">Itt adhatja meg azt a szondát, amellyel társítani lehet egy terheléselosztó szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7cf99-141">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf99-142">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="7cf99-142">-ProbeId</span></span>
<span data-ttu-id="7cf99-143">Annak a szondanak az AZONOSÍTÓját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="7cf99-143">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7cf99-144">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7cf99-144">-Protocol</span></span>
<span data-ttu-id="7cf99-145">A terheléselosztási szabályok konfigurációjának megfelelő protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cf99-145">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="7cf99-146">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="7cf99-146">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="7cf99-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf99-147">-DefaultProfile</span></span>
<span data-ttu-id="7cf99-148">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cf99-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf99-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf99-149">CommonParameters</span></span>
<span data-ttu-id="7cf99-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cf99-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf99-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf99-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf99-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cf99-152">INPUTS</span></span>

## <span data-ttu-id="7cf99-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cf99-153">OUTPUTS</span></span>

### <span data-ttu-id="7cf99-154">Microsoft. Azure. commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="7cf99-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="7cf99-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cf99-155">NOTES</span></span>

## <span data-ttu-id="7cf99-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cf99-156">RELATED LINKS</span></span>

[<span data-ttu-id="7cf99-157">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf99-157">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="7cf99-158">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf99-158">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="7cf99-159">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf99-159">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="7cf99-160">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf99-160">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


