---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015724"
---
# <span data-ttu-id="e94c3-101">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e94c3-101">Add-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="e94c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e94c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e94c3-103">Belső terheléselosztást ad hozzá egy Azure-szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e94c3-103">Adds an internal load balancer to an Azure service.</span></span>

## <span data-ttu-id="e94c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e94c3-104">SYNTAX</span></span>

### <span data-ttu-id="e94c3-105">ServiceAndSlot (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e94c3-105">ServiceAndSlot (Default)</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e94c3-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="e94c3-106">SubnetNameOnly</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e94c3-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="e94c3-107">SubnetNameAndIP</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e94c3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e94c3-108">DESCRIPTION</span></span>
<span data-ttu-id="e94c3-109">Az **Add-AzureInternalLoadBalancer** parancsmag belső terheléselosztási konfigurációt ad egy Azure-szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e94c3-109">The **Add-AzureInternalLoadBalancer** cmdlet adds an internal load balancer configuration to an Azure service.</span></span>
<span data-ttu-id="e94c3-110">Virtuális hálózat esetén megadhatja a belső terheléselosztó alhálózatát vagy IP-címét.</span><span class="sxs-lookup"><span data-stu-id="e94c3-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="e94c3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e94c3-111">EXAMPLES</span></span>

### <span data-ttu-id="e94c3-112">Példa 1: belső terheléselosztó hozzáadása</span><span class="sxs-lookup"><span data-stu-id="e94c3-112">Example 1: Add an internal load balancer</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

<span data-ttu-id="e94c3-113">Ez a parancs hozzáadja a ContosoILB nevű belső terheléselosztó szolgáltatást a ContosoWebsite01 nevű szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e94c3-113">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>

### <span data-ttu-id="e94c3-114">2. példa: belső terheléselosztó beállítása adott alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="e94c3-114">Example 2: Add an internal load balancer for a specified subnet</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="e94c3-115">Ez a parancs hozzáadja a ContosoILB nevű belső terheléselosztó szolgáltatást a ContosoWebsite01 nevű szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e94c3-115">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="e94c3-116">A parancs a FrontEndSubnet nevű alhálózatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e94c3-116">The command specifies the subnet named FrontEndSubnet.</span></span>

### <span data-ttu-id="e94c3-117">3. példa: belső terheléselosztó beállítása meghatározott alhálózathoz és címhez</span><span class="sxs-lookup"><span data-stu-id="e94c3-117">Example 3: Add an internal load balancer for a specified subnet and address</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

<span data-ttu-id="e94c3-118">Ez a parancs hozzáadja a ContosoILB nevű belső terheléselosztó szolgáltatást a ContosoWebsite01 nevű szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e94c3-118">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="e94c3-119">A parancs a FrontEndSubnet nevű alhálózatot és a virtuális hálózat statikus címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e94c3-119">The command specifies the subnet named FrontEndSubnet and the static address of the virtual network.</span></span>

## <span data-ttu-id="e94c3-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e94c3-120">PARAMETERS</span></span>

### <span data-ttu-id="e94c3-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e94c3-121">-InformationAction</span></span>
<span data-ttu-id="e94c3-122">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="e94c3-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e94c3-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e94c3-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e94c3-124">Folytassa</span><span class="sxs-lookup"><span data-stu-id="e94c3-124">Continue</span></span>
- <span data-ttu-id="e94c3-125">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="e94c3-125">Ignore</span></span>
- <span data-ttu-id="e94c3-126">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="e94c3-126">Inquire</span></span>
- <span data-ttu-id="e94c3-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e94c3-127">SilentlyContinue</span></span>
- <span data-ttu-id="e94c3-128">állj</span><span class="sxs-lookup"><span data-stu-id="e94c3-128">Stop</span></span>
- <span data-ttu-id="e94c3-129">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="e94c3-129">Suspend</span></span>

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

### <span data-ttu-id="e94c3-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e94c3-130">-InformationVariable</span></span>
<span data-ttu-id="e94c3-131">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="e94c3-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e94c3-132">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="e94c3-132">-InternalLoadBalancerName</span></span>
<span data-ttu-id="e94c3-133">Annak a belső terheléselosztásnak a neve, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="e94c3-133">Specifies the name of the internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e94c3-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="e94c3-134">-Profile</span></span>
<span data-ttu-id="e94c3-135">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e94c3-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e94c3-136">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e94c3-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e94c3-137">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="e94c3-137">-ServiceName</span></span>
<span data-ttu-id="e94c3-138">Annak a szolgáltatásnak a nevét adja meg, amelyre a parancsmag egy belső terheléselosztó bővítményt ad.</span><span class="sxs-lookup"><span data-stu-id="e94c3-138">Specifies the name of the service to which this cmdlet adds an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94c3-139">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="e94c3-139">-StaticVNetIPAddress</span></span>
<span data-ttu-id="e94c3-140">Megadja a parancsmag által hozzáadott belső terheléselosztó virtuális hálózati IP-címét.</span><span class="sxs-lookup"><span data-stu-id="e94c3-140">Specifies the virtual network IP address for an internal load balancer that this cmdlet adds.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94c3-141">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e94c3-141">-SubnetName</span></span>
<span data-ttu-id="e94c3-142">Annak az alhálózatnak a nevét adja meg, amely a parancsmag által hozzáadott belső terheléselosztást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e94c3-142">Specifies the name of the subnet for an internal load balancer that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94c3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94c3-143">CommonParameters</span></span>
<span data-ttu-id="e94c3-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e94c3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94c3-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e94c3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94c3-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e94c3-146">INPUTS</span></span>

## <span data-ttu-id="e94c3-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e94c3-147">OUTPUTS</span></span>

### <span data-ttu-id="e94c3-148">Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e94c3-148">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="e94c3-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e94c3-149">NOTES</span></span>

## <span data-ttu-id="e94c3-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e94c3-150">RELATED LINKS</span></span>

[<span data-ttu-id="e94c3-151">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e94c3-151">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="e94c3-152">Új – AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="e94c3-152">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="e94c3-153">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e94c3-153">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="e94c3-154">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e94c3-154">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


