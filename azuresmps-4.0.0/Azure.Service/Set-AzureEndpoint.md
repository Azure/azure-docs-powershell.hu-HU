---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016057"
---
# <span data-ttu-id="0a8c5-101">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a8c5-101">Set-AzureEndpoint</span></span>

## <span data-ttu-id="0a8c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a8c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8c5-103">Módosítja egy virtuális géphez rendelt végpontot.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-103">Modifies an endpoint assigned to a virtual machine.</span></span>

## <span data-ttu-id="0a8c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a8c5-104">SYNTAX</span></span>

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0a8c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a8c5-105">DESCRIPTION</span></span>
<span data-ttu-id="0a8c5-106">A **set-AzureEndpoint** parancsmag módosította az Azure Virtual Machine rendszerhez rendelt végpontot.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-106">The **Set-AzureEndpoint** cmdlet modifies an endpoint assigned to an Azure virtual machine.</span></span>
<span data-ttu-id="0a8c5-107">Megadhatja az olyan végpontok módosításait is, amelyek nem töltődnek be a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-107">You can specify changes to an endpoint that is not load balanced.</span></span>

## <span data-ttu-id="0a8c5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0a8c5-108">EXAMPLES</span></span>

### <span data-ttu-id="0a8c5-109">1. példa: a végpontok módosítása a port figyeléséhez</span><span class="sxs-lookup"><span data-stu-id="0a8c5-109">Example 1: Modify an endpoint to listen on a port</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

<span data-ttu-id="0a8c5-110">Ez a parancs a **Get-AzureVM** parancsmag használatával lekérdezi a VirtualMachine01 nevű virtuális gép konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-110">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="0a8c5-111">A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-111">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0a8c5-112">Ez a parancsmag módosítja a Web nevű végpontot a 443-es port figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-112">This cmdlet modifies the endpoint named Web to listen on port 443.</span></span>
<span data-ttu-id="0a8c5-113">A parancs átadja a virtuális gép objektumát a **Update-AzureVM** parancsmagnak, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-113">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="0a8c5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a8c5-114">PARAMETERS</span></span>

### <span data-ttu-id="0a8c5-115">-ACL</span><span class="sxs-lookup"><span data-stu-id="0a8c5-115">-ACL</span></span>
<span data-ttu-id="0a8c5-116">Olyan hozzáférés-vezérlési lista (ACL) konfigurációs objektumát adja meg, amelyre a parancsmag érvényes a végpontra.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-116">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoint.</span></span>

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

### <span data-ttu-id="0a8c5-117">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="0a8c5-117">-DirectServerReturn</span></span>
<span data-ttu-id="0a8c5-118">Annak megadása, hogy a parancsmag engedélyezi-e a közvetlen kiszolgáló visszaadását.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-118">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="0a8c5-119">Adja meg az engedélyezni vagy letiltani $True $Falset.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-119">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="0a8c5-120">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0a8c5-120">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0a8c5-121">A végponthoz tartozó TCP Idle időtúllépési időszakát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-121">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="0a8c5-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0a8c5-122">-InformationAction</span></span>
<span data-ttu-id="0a8c5-123">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0a8c5-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0a8c5-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a8c5-125">Folytassa</span><span class="sxs-lookup"><span data-stu-id="0a8c5-125">Continue</span></span>
- <span data-ttu-id="0a8c5-126">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="0a8c5-126">Ignore</span></span>
- <span data-ttu-id="0a8c5-127">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="0a8c5-127">Inquire</span></span>
- <span data-ttu-id="0a8c5-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0a8c5-128">SilentlyContinue</span></span>
- <span data-ttu-id="0a8c5-129">állj</span><span class="sxs-lookup"><span data-stu-id="0a8c5-129">Stop</span></span>
- <span data-ttu-id="0a8c5-130">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="0a8c5-130">Suspend</span></span>

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

### <span data-ttu-id="0a8c5-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0a8c5-131">-InformationVariable</span></span>
<span data-ttu-id="0a8c5-132">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0a8c5-133">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="0a8c5-133">-InternalLoadBalancerName</span></span>
<span data-ttu-id="0a8c5-134">A belső terheléselosztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-134">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="0a8c5-135">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="0a8c5-135">-LoadBalancerDistribution</span></span>
<span data-ttu-id="0a8c5-136">A terheléselosztó terjesztési algoritmusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-136">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="0a8c5-137">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="0a8c5-137">Valid values are:</span></span> 

- <span data-ttu-id="0a8c5-138">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-138">sourceIP.</span></span>
<span data-ttu-id="0a8c5-139">Két rekordos affinitás: Source IP, cél IP</span><span class="sxs-lookup"><span data-stu-id="0a8c5-139">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="0a8c5-140">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-140">sourceIPProtocol.</span></span>
<span data-ttu-id="0a8c5-141">Három rekordos affinitás: Source IP, cél IP, Protocol</span><span class="sxs-lookup"><span data-stu-id="0a8c5-141">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="0a8c5-142">nincs.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-142">none.</span></span>
<span data-ttu-id="0a8c5-143">Öt rekordos affinitás: Source IP, Source port, cél IP, cél port, Protocol</span><span class="sxs-lookup"><span data-stu-id="0a8c5-143">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="0a8c5-144">Az alapértelmezett érték a nincs.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-144">The default value is none.</span></span>

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

### <span data-ttu-id="0a8c5-145">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="0a8c5-145">-LocalPort</span></span>
<span data-ttu-id="0a8c5-146">A végpont által használt helyi, privát portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-146">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="0a8c5-147">A virtuális gépen futó alkalmazások ebben a portban figyelik ezt a portot a végponthoz tartozó szolgáltatási kérelmekben.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-147">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c5-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a8c5-148">-Name</span></span>
<span data-ttu-id="0a8c5-149">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-149">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="0a8c5-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="0a8c5-150">-Profile</span></span>
<span data-ttu-id="0a8c5-151">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a8c5-152">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a8c5-153">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0a8c5-153">-Protocol</span></span>
<span data-ttu-id="0a8c5-154">A végpont protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-154">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="0a8c5-155">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="0a8c5-155">Valid values are:</span></span> 

- <span data-ttu-id="0a8c5-156">TCP</span><span class="sxs-lookup"><span data-stu-id="0a8c5-156">tcp</span></span> 
- <span data-ttu-id="0a8c5-157">UDP</span><span class="sxs-lookup"><span data-stu-id="0a8c5-157">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c5-158">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="0a8c5-158">-PublicPort</span></span>
<span data-ttu-id="0a8c5-159">A végpont által használt nyilvános portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-159">Specifies the public port that the endpoint uses.</span></span>

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

### <span data-ttu-id="0a8c5-160">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="0a8c5-160">-VirtualIPName</span></span>
<span data-ttu-id="0a8c5-161">Annak a virtuális IP-címnek a nevét adja meg, amely az Azure-t a végponthoz társítja.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-161">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="0a8c5-162">A szolgáltatás több virtuális IP-t is tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-162">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="0a8c5-163">A virtuális IP-k létrehozásához használja az **Add-AzureVirtualIP** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-163">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="0a8c5-164">-VM</span><span class="sxs-lookup"><span data-stu-id="0a8c5-164">-VM</span></span>
<span data-ttu-id="0a8c5-165">Annak a virtuális gépnek a megadása, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-165">Specifies the virtual machine to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0a8c5-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8c5-166">CommonParameters</span></span>
<span data-ttu-id="0a8c5-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a8c5-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8c5-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a8c5-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8c5-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a8c5-169">INPUTS</span></span>

## <span data-ttu-id="0a8c5-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a8c5-170">OUTPUTS</span></span>

### <span data-ttu-id="0a8c5-171">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="0a8c5-171">System.Object</span></span>

## <span data-ttu-id="0a8c5-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a8c5-172">NOTES</span></span>

## <span data-ttu-id="0a8c5-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a8c5-173">RELATED LINKS</span></span>

[<span data-ttu-id="0a8c5-174">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a8c5-174">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="0a8c5-175">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="0a8c5-175">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="0a8c5-176">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a8c5-176">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="0a8c5-177">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0a8c5-177">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="0a8c5-178">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a8c5-178">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="0a8c5-179">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0a8c5-179">Update-AzureVM</span></span>](./Update-AzureVM.md)


