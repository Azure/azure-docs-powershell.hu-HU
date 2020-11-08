---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015733"
---
# <span data-ttu-id="26843-101">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="26843-101">Add-AzureEndpoint</span></span>

## <span data-ttu-id="26843-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26843-102">SYNOPSIS</span></span>
<span data-ttu-id="26843-103">Végpontot ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="26843-103">Adds an endpoint to a virtual machine.</span></span>

## <span data-ttu-id="26843-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26843-104">SYNTAX</span></span>

### <span data-ttu-id="26843-105">NoLB (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26843-105">NoLB (Default)</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="26843-106">LBNoProbe</span><span class="sxs-lookup"><span data-stu-id="26843-106">LBNoProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="26843-107">LBDefaultProbe</span><span class="sxs-lookup"><span data-stu-id="26843-107">LBDefaultProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="26843-108">LBCustomProbe</span><span class="sxs-lookup"><span data-stu-id="26843-108">LBCustomProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="26843-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="26843-109">DESCRIPTION</span></span>
<span data-ttu-id="26843-110">Az **Add-AzureEndpoint** parancsmag az Azure Virtual Machine-objektum végpontját adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="26843-110">The **Add-AzureEndpoint** cmdlet adds an endpoint to an Azure virtual machine object.</span></span>

## <span data-ttu-id="26843-111">Példák</span><span class="sxs-lookup"><span data-stu-id="26843-111">EXAMPLES</span></span>

### <span data-ttu-id="26843-112">1. példa: végpont hozzáadása</span><span class="sxs-lookup"><span data-stu-id="26843-112">Example 1: Add an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

<span data-ttu-id="26843-113">Ez a parancs a **Get-AzureVM** parancsmag használatával lekérdezi a VirtualMachine01 nevű virtuális gép konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="26843-113">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="26843-114">A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="26843-114">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="26843-115">Ez a parancsmag hozzáadja a HttpIn nevű végpontot.</span><span class="sxs-lookup"><span data-stu-id="26843-115">This cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="26843-116">A végponthoz tartozik egy 80-es nyilvános port és a 8080-es helyi port.</span><span class="sxs-lookup"><span data-stu-id="26843-116">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="26843-117">A parancs átadja a virtuális gép objektumát a **Update-AzureVM** parancsmagnak, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="26843-117">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="26843-118">2. példa: terheléselosztási csoportba tartozó végpont felvétele</span><span class="sxs-lookup"><span data-stu-id="26843-118">Example 2: Add an endpoint that belongs to a load balanced group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

<span data-ttu-id="26843-119">Ez a parancs beolvassa a VirtualMachine07 nevű virtuális gép konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="26843-119">This command retrieves the configuration of a virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="26843-120">Az aktuális parancsmag hozzáadja a HttpIn nevű végpontot.</span><span class="sxs-lookup"><span data-stu-id="26843-120">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="26843-121">A végponthoz tartozik egy 80-es nyilvános port és a 8080-es helyi port.</span><span class="sxs-lookup"><span data-stu-id="26843-121">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="26843-122">A végpont a webfarm nevű megosztott terheléselosztási csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="26843-122">The endpoint belongs to the shared load balanced group named WebFarm.</span></span>
<span data-ttu-id="26843-123">Egy HTTP-szonda a 80-es porton, ahol a "/" elérési út követi a végpont elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="26843-123">An HTTP probe on port 80 with a path of '/' monitors the availability of the endpoint.</span></span>
<span data-ttu-id="26843-124">A parancs végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="26843-124">The command implements your changes.</span></span>

### <span data-ttu-id="26843-125">3. példa: virtuális IP hozzárendelése végponthoz</span><span class="sxs-lookup"><span data-stu-id="26843-125">Example 3: Associate a virtual IP to an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

<span data-ttu-id="26843-126">Ez a parancs beolvassa a VirtualMachine25 nevű virtuális gép konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="26843-126">This command retrieves the configuration of a virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="26843-127">Az aktuális parancsmag hozzáadja a HttpIn nevű végpontot.</span><span class="sxs-lookup"><span data-stu-id="26843-127">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="26843-128">A végponthoz tartozik egy 80-es nyilvános port és a 8080-es helyi port.</span><span class="sxs-lookup"><span data-stu-id="26843-128">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="26843-129">Ez a parancs egy virtuális IP-címet társít a végponthoz.</span><span class="sxs-lookup"><span data-stu-id="26843-129">This command associates a virtual IP to the endpoint.</span></span>
<span data-ttu-id="26843-130">A parancs végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="26843-130">The command implements your changes.</span></span>

## <span data-ttu-id="26843-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26843-131">PARAMETERS</span></span>

### <span data-ttu-id="26843-132">-ACL</span><span class="sxs-lookup"><span data-stu-id="26843-132">-ACL</span></span>
<span data-ttu-id="26843-133">A végponthoz tartozó hozzáférés-vezérlési lista (ACL) beállítása.</span><span class="sxs-lookup"><span data-stu-id="26843-133">Specifies an access control list (ACL) configuration object for the endpoint.</span></span>

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

### <span data-ttu-id="26843-134">-DefaultProbe</span><span class="sxs-lookup"><span data-stu-id="26843-134">-DefaultProbe</span></span>
<span data-ttu-id="26843-135">Azt jelzi, hogy ez a parancsmag az alapértelmezett szonda beállítást használja.</span><span class="sxs-lookup"><span data-stu-id="26843-135">Indicates that this cmdlet uses the default probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-136">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="26843-136">-DirectServerReturn</span></span>
<span data-ttu-id="26843-137">Annak megadása, hogy a parancsmag engedélyezi-e a közvetlen kiszolgáló visszaadását.</span><span class="sxs-lookup"><span data-stu-id="26843-137">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="26843-138">Adja meg az engedélyezni vagy letiltani $True $Falset.</span><span class="sxs-lookup"><span data-stu-id="26843-138">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="26843-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="26843-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="26843-140">A végponthoz tartozó TCP Idle időtúllépési időszakát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="26843-140">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="26843-141">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="26843-141">-InformationAction</span></span>
<span data-ttu-id="26843-142">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="26843-142">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="26843-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="26843-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26843-144">Folytassa</span><span class="sxs-lookup"><span data-stu-id="26843-144">Continue</span></span>
- <span data-ttu-id="26843-145">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="26843-145">Ignore</span></span>
- <span data-ttu-id="26843-146">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="26843-146">Inquire</span></span>
- <span data-ttu-id="26843-147">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="26843-147">SilentlyContinue</span></span>
- <span data-ttu-id="26843-148">állj</span><span class="sxs-lookup"><span data-stu-id="26843-148">Stop</span></span>
- <span data-ttu-id="26843-149">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="26843-149">Suspend</span></span>

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

### <span data-ttu-id="26843-150">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="26843-150">-InformationVariable</span></span>
<span data-ttu-id="26843-151">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="26843-151">Specifies an information variable.</span></span>

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

### <span data-ttu-id="26843-152">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="26843-152">-InternalLoadBalancerName</span></span>
<span data-ttu-id="26843-153">A belső terheléselosztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-153">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="26843-154">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="26843-154">-LBSetName</span></span>
<span data-ttu-id="26843-155">A végponthoz tartozó terheléselosztó halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-155">Specifies the name of the load balancer set for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-156">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="26843-156">-LoadBalancerDistribution</span></span>
<span data-ttu-id="26843-157">A terheléselosztó terjesztési algoritmusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-157">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="26843-158">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="26843-158">Valid values are:</span></span> 

- <span data-ttu-id="26843-159">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="26843-159">sourceIP.</span></span>
<span data-ttu-id="26843-160">Két rekordos affinitás: Source IP, cél IP</span><span class="sxs-lookup"><span data-stu-id="26843-160">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="26843-161">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="26843-161">sourceIPProtocol.</span></span>
<span data-ttu-id="26843-162">Három rekordos affinitás: Source IP, cél IP, Protocol</span><span class="sxs-lookup"><span data-stu-id="26843-162">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="26843-163">nincs.</span><span class="sxs-lookup"><span data-stu-id="26843-163">none.</span></span>
<span data-ttu-id="26843-164">Öt rekordos affinitás: Source IP, Source port, cél IP, cél port, Protocol</span><span class="sxs-lookup"><span data-stu-id="26843-164">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="26843-165">Az alapértelmezett érték a nincs.</span><span class="sxs-lookup"><span data-stu-id="26843-165">The default value is none.</span></span>

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

### <span data-ttu-id="26843-166">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="26843-166">-LocalPort</span></span>
<span data-ttu-id="26843-167">A végpont által használt helyi, privát portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-167">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="26843-168">A virtuális gépen futó alkalmazások ebben a portban figyelik ezt a portot a végponthoz tartozó szolgáltatási kérelmekben.</span><span class="sxs-lookup"><span data-stu-id="26843-168">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-169">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26843-169">-Name</span></span>
<span data-ttu-id="26843-170">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-170">Specifies a name for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-171">-Probléma</span><span class="sxs-lookup"><span data-stu-id="26843-171">-NoProbe</span></span>
<span data-ttu-id="26843-172">Azt jelzi, hogy ez a parancsmag a No Probe beállítást használja.</span><span class="sxs-lookup"><span data-stu-id="26843-172">Indicates that this cmdlet uses the no probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-173">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="26843-173">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="26843-174">A végponthoz tartozó valószínűségi lekérdezési intervallumot adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="26843-174">Specifies the probe polling interval, in seconds, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-175">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="26843-175">-ProbePath</span></span>
<span data-ttu-id="26843-176">A HTTP-szonda relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-176">Specifies the relative path to the HTTP probe.</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-177">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="26843-177">-ProbePort</span></span>
<span data-ttu-id="26843-178">A végpont által használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-178">Specifies the port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-179">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="26843-179">-ProbeProtocol</span></span>
<span data-ttu-id="26843-180">A port protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-180">Specifies the port protocol.</span></span>
<span data-ttu-id="26843-181">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="26843-181">Valid values are:</span></span> 

- <span data-ttu-id="26843-182">TCP</span><span class="sxs-lookup"><span data-stu-id="26843-182">tcp</span></span> 
- <span data-ttu-id="26843-183">http</span><span class="sxs-lookup"><span data-stu-id="26843-183">http</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-184">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="26843-184">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="26843-185">A szondával való szavazás időpontját másodpercben kifejezve adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-185">Specifies the probe polling time-out period in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-186">-Profil</span><span class="sxs-lookup"><span data-stu-id="26843-186">-Profile</span></span>
<span data-ttu-id="26843-187">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="26843-187">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="26843-188">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="26843-188">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26843-189">-Protocol</span><span class="sxs-lookup"><span data-stu-id="26843-189">-Protocol</span></span>
<span data-ttu-id="26843-190">A végpont protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-190">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="26843-191">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="26843-191">Valid values are:</span></span> 

- <span data-ttu-id="26843-192">TCP</span><span class="sxs-lookup"><span data-stu-id="26843-192">tcp</span></span> 
- <span data-ttu-id="26843-193">UDP</span><span class="sxs-lookup"><span data-stu-id="26843-193">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26843-194">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="26843-194">-PublicPort</span></span>
<span data-ttu-id="26843-195">A végpont által használt nyilvános portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="26843-195">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="26843-196">Ha nem ad meg értéket, az Azure kiosztja az elérhető portot.</span><span class="sxs-lookup"><span data-stu-id="26843-196">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="26843-197">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="26843-197">-VirtualIPName</span></span>
<span data-ttu-id="26843-198">Annak a virtuális IP-címnek a nevét adja meg, amely az Azure-t a végponthoz társítja.</span><span class="sxs-lookup"><span data-stu-id="26843-198">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="26843-199">A szolgáltatás több virtuális IP-t is tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="26843-199">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="26843-200">A virtuális IP-k létrehozásához használja az **Add-AzureVirtualIP** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="26843-200">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="26843-201">-VM</span><span class="sxs-lookup"><span data-stu-id="26843-201">-VM</span></span>
<span data-ttu-id="26843-202">Annak a virtuális gépnek a megadása, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="26843-202">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26843-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26843-203">CommonParameters</span></span>
<span data-ttu-id="26843-204">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26843-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26843-205">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26843-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26843-206">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26843-206">INPUTS</span></span>

## <span data-ttu-id="26843-207">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26843-207">OUTPUTS</span></span>

### <span data-ttu-id="26843-208">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="26843-208">System.Object</span></span>

## <span data-ttu-id="26843-209">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26843-209">NOTES</span></span>

## <span data-ttu-id="26843-210">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26843-210">RELATED LINKS</span></span>

[<span data-ttu-id="26843-211">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="26843-211">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="26843-212">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="26843-212">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="26843-213">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="26843-213">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="26843-214">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="26843-214">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="26843-215">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="26843-215">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="26843-216">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="26843-216">Update-AzureVM</span></span>](./Update-AzureVM.md)


