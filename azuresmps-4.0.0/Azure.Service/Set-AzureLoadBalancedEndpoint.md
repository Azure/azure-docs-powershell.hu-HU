---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015953"
---
# <span data-ttu-id="c7687-101">Set-AzureLoadBalancedEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7687-101">Set-AzureLoadBalancedEndpoint</span></span>

## <span data-ttu-id="c7687-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7687-102">SYNOPSIS</span></span>
<span data-ttu-id="c7687-103">Egy Azure-szolgáltatáson belül a terheléselosztásban beállított összes végpontot módosítja.</span><span class="sxs-lookup"><span data-stu-id="c7687-103">Modifies all of the endpoints in a load balancer set within an Azure service.</span></span>

## <span data-ttu-id="c7687-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7687-104">SYNTAX</span></span>

### <span data-ttu-id="c7687-105">DefaultProbe (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7687-105">DefaultProbe (Default)</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c7687-106">TCPProbe</span><span class="sxs-lookup"><span data-stu-id="c7687-106">TCPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c7687-107">HTTPProbe</span><span class="sxs-lookup"><span data-stu-id="c7687-107">HTTPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c7687-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7687-108">DESCRIPTION</span></span>
<span data-ttu-id="c7687-109">A **set-AzureLoadBalancedEndpoint** parancsmag az Azure-szolgáltatásokban beállított terheléselosztó összes végpontját módosítja.</span><span class="sxs-lookup"><span data-stu-id="c7687-109">The **Set-AzureLoadBalancedEndpoint** cmdlet modifies all of the endpoints in a load balancer set in an Azure service.</span></span>

## <span data-ttu-id="c7687-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c7687-110">EXAMPLES</span></span>

### <span data-ttu-id="c7687-111">Példa 1: a terheléselosztási halmazban lévő végpontok módosítása</span><span class="sxs-lookup"><span data-stu-id="c7687-111">Example 1: Modify the endpoints in a load balancer set</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

<span data-ttu-id="c7687-112">Ez a parancs a LBSet01 nevű terheléselosztó készlet minden végpontját módosítja a TCP-protokoll és a 80-as privát port használata esetén.</span><span class="sxs-lookup"><span data-stu-id="c7687-112">This command modifies all endpoints in the load balancer set named LBSet01 to use the TCP protocol and private port 80.</span></span>
<span data-ttu-id="c7687-113">A kiegyenlítő szondát beállító parancs a 8080-es porton lévő TCP-protokollt használja.</span><span class="sxs-lookup"><span data-stu-id="c7687-113">The command sets the load balancer probe to use the TCP protocol on port 8080.</span></span>

### <span data-ttu-id="c7687-114">2. példa: adjon meg egy másik virtuális IP-címet.</span><span class="sxs-lookup"><span data-stu-id="c7687-114">Example 2: Specify a different virtual IP</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

<span data-ttu-id="c7687-115">Ez a parancs módosítja azt a terheléselosztást, amely a terheléselosztó készlet nevében a virtuális IP nevű Vip01.</span><span class="sxs-lookup"><span data-stu-id="c7687-115">This command modifies the load balancer that has the load balancer set name to use a virtual IP named Vip01.</span></span>

## <span data-ttu-id="c7687-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7687-116">PARAMETERS</span></span>

### <span data-ttu-id="c7687-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="c7687-117">-ACL</span></span>
<span data-ttu-id="c7687-118">Olyan hozzáférés-vezérlési lista (ACL) konfigurációs objektumát adja meg, amelyre a parancsmag a végpontokra érvényes.</span><span class="sxs-lookup"><span data-stu-id="c7687-118">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoints.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-119">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="c7687-119">-DirectServerReturn</span></span>
<span data-ttu-id="c7687-120">Annak megadása, hogy a parancsmag engedélyezi-e a közvetlen kiszolgáló visszaadását.</span><span class="sxs-lookup"><span data-stu-id="c7687-120">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="c7687-121">Adja meg az engedélyezni vagy letiltani $True $Falset.</span><span class="sxs-lookup"><span data-stu-id="c7687-121">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-122">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c7687-122">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c7687-123">A TCP üresjárati időtúllépési időszakát adja meg percben a végpontok esetében.</span><span class="sxs-lookup"><span data-stu-id="c7687-123">Specifies the TCP idle time-out period, in minutes, for the endpoints.</span></span>

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

### <span data-ttu-id="c7687-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c7687-124">-InformationAction</span></span>
<span data-ttu-id="c7687-125">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="c7687-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c7687-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c7687-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7687-127">Folytassa</span><span class="sxs-lookup"><span data-stu-id="c7687-127">Continue</span></span>
- <span data-ttu-id="c7687-128">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="c7687-128">Ignore</span></span>
- <span data-ttu-id="c7687-129">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="c7687-129">Inquire</span></span>
- <span data-ttu-id="c7687-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c7687-130">SilentlyContinue</span></span>
- <span data-ttu-id="c7687-131">állj</span><span class="sxs-lookup"><span data-stu-id="c7687-131">Stop</span></span>
- <span data-ttu-id="c7687-132">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="c7687-132">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c7687-133">-InformationVariable</span></span>
<span data-ttu-id="c7687-134">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="c7687-134">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-135">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="c7687-135">-InternalLoadBalancerName</span></span>
<span data-ttu-id="c7687-136">Annak a belső terheléselosztó a nevét adja meg, amelyre a parancsmag a konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c7687-136">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-137">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="c7687-137">-LBSetName</span></span>
<span data-ttu-id="c7687-138">Annak a terheléselosztó készletnek a nevét adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="c7687-138">Specifies the name of the load balancer set that this cmdlet updates.</span></span>

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

### <span data-ttu-id="c7687-139">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="c7687-139">-LoadBalancerDistribution</span></span>
<span data-ttu-id="c7687-140">A terheléselosztó terjesztési algoritmusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7687-140">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="c7687-141">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="c7687-141">Valid values are:</span></span> 

- <span data-ttu-id="c7687-142">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="c7687-142">sourceIP.</span></span>
<span data-ttu-id="c7687-143">Két rekordos affinitás: Source IP, cél IP</span><span class="sxs-lookup"><span data-stu-id="c7687-143">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="c7687-144">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="c7687-144">sourceIPProtocol.</span></span>
<span data-ttu-id="c7687-145">Három rekordos affinitás: Source IP, cél IP, Protocol</span><span class="sxs-lookup"><span data-stu-id="c7687-145">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="c7687-146">nincs.</span><span class="sxs-lookup"><span data-stu-id="c7687-146">none.</span></span>
<span data-ttu-id="c7687-147">Öt rekordos affinitás: Source IP, Source port, cél IP, cél port, Protocol</span><span class="sxs-lookup"><span data-stu-id="c7687-147">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="c7687-148">Az alapértelmezett érték a nincs.</span><span class="sxs-lookup"><span data-stu-id="c7687-148">The default value is none.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-149">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="c7687-149">-LocalPort</span></span>
<span data-ttu-id="c7687-150">Itt adhatja meg az adott végpontok által használt helyi, privát portot.</span><span class="sxs-lookup"><span data-stu-id="c7687-150">Specifies the local, private, port that these endpoints use.</span></span>
<span data-ttu-id="c7687-151">A virtuális gépen futó alkalmazások ebben a portban figyelik ezt a portot a végponthoz tartozó bejelentkezési kérelmekhez.</span><span class="sxs-lookup"><span data-stu-id="c7687-151">Applications in the virtual machine listen on this port for service input requests for this endpoint.</span></span>

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

### <span data-ttu-id="c7687-152">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c7687-152">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="c7687-153">A végpontok lekérdezési gyakoriságát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c7687-153">Specifies the probe polling interval, in seconds, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-154">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="c7687-154">-ProbePath</span></span>
<span data-ttu-id="c7687-155">A HTTP-szonda relatív elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7687-155">Specifies the relative path of the HTTP Probe.</span></span>

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-156">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="c7687-156">-ProbePort</span></span>
<span data-ttu-id="c7687-157">A terheléselosztó szondát használó portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7687-157">Specifies the port that the load balancer probe uses.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-158">-ProbeProtocolHTTP</span><span class="sxs-lookup"><span data-stu-id="c7687-158">-ProbeProtocolHTTP</span></span>
<span data-ttu-id="c7687-159">Megadja, hogy a terheléselosztási végpontok HTTP-szondát használjanak.</span><span class="sxs-lookup"><span data-stu-id="c7687-159">Specifies that the load balancer endpoints use an HTTP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-160">-ProbeProtocolTCP</span><span class="sxs-lookup"><span data-stu-id="c7687-160">-ProbeProtocolTCP</span></span>
<span data-ttu-id="c7687-161">Azt adja meg, hogy a terheléselosztási végpontok TCP-szondát használjanak.</span><span class="sxs-lookup"><span data-stu-id="c7687-161">Specifies that the load balancer endpoints use a TCP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-162">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="c7687-162">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="c7687-163">A szondával való szavazás időpontját adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c7687-163">Specifies the probe polling time-out in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-164">-Profil</span><span class="sxs-lookup"><span data-stu-id="c7687-164">-Profile</span></span>
<span data-ttu-id="c7687-165">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c7687-165">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7687-166">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c7687-166">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-167">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c7687-167">-Protocol</span></span>
<span data-ttu-id="c7687-168">A végpontok protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7687-168">Specifies the protocol of the endpoints.</span></span>
<span data-ttu-id="c7687-169">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="c7687-169">Valid values are:</span></span> 

- <span data-ttu-id="c7687-170">TCP</span><span class="sxs-lookup"><span data-stu-id="c7687-170">TCP</span></span> 
- <span data-ttu-id="c7687-171">UDP</span><span class="sxs-lookup"><span data-stu-id="c7687-171">UDP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-172">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="c7687-172">-PublicPort</span></span>
<span data-ttu-id="c7687-173">A végpont által használt nyilvános portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7687-173">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="c7687-174">Ha nem ad meg értéket, az Azure kiosztja az elérhető portot.</span><span class="sxs-lookup"><span data-stu-id="c7687-174">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="c7687-175">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="c7687-175">-ServiceName</span></span>
<span data-ttu-id="c7687-176">Annak az Azure-szolgáltatásnak a neve, amely a parancsmag által módosított végpontokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c7687-176">Specifies the name of the Azure service that contains the endpoints that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-177">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="c7687-177">-VirtualIPName</span></span>
<span data-ttu-id="c7687-178">Annak a virtuális IP-címnek a nevét adja meg, amely az Azure-t a végpontokhoz társítja.</span><span class="sxs-lookup"><span data-stu-id="c7687-178">Specifies the name of a virtual IP address that Azure associates to the endpoints.</span></span>
<span data-ttu-id="c7687-179">Ha virtuális IP-ket szeretne hozzáadni a szolgáltatáshoz, használja az **Add-AzureVirtualIP** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c7687-179">To add virtual IPs to your service, use the **Add-AzureVirtualIP** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7687-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7687-180">CommonParameters</span></span>
<span data-ttu-id="c7687-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7687-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7687-182">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7687-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7687-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7687-183">INPUTS</span></span>

## <span data-ttu-id="c7687-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7687-184">OUTPUTS</span></span>

## <span data-ttu-id="c7687-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7687-185">NOTES</span></span>

## <span data-ttu-id="c7687-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7687-186">RELATED LINKS</span></span>

[<span data-ttu-id="c7687-187">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="c7687-187">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="c7687-188">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7687-188">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


