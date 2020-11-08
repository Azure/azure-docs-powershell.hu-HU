---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6D23ECB-C06E-4EB7-8096-33787E39694D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66f6bac80b219a2b3629b399bb568140a5cef217
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015954"
---
# <span data-ttu-id="30d79-101">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30d79-101">Set-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="30d79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30d79-102">SYNOPSIS</span></span>
<span data-ttu-id="30d79-103">Belső terheléselosztó konfigurációt módosít egy Azure-szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="30d79-103">Modifies an internal load balancer configuration in an Azure service.</span></span>

## <span data-ttu-id="30d79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30d79-104">SYNTAX</span></span>

### <span data-ttu-id="30d79-105">ServiceAndSlot (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30d79-105">ServiceAndSlot (Default)</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="30d79-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="30d79-106">SubnetNameOnly</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="30d79-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="30d79-107">SubnetNameAndIP</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="30d79-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="30d79-108">DESCRIPTION</span></span>
<span data-ttu-id="30d79-109">A **set-AzureInternalLoadBalancer** parancsmag az Azure-szolgáltatásokban egy belső terheléselosztó konfigurációt módosít.</span><span class="sxs-lookup"><span data-stu-id="30d79-109">The **Set-AzureInternalLoadBalancer** cmdlet modifies an internal load balancer configuration in an Azure service.</span></span>
<span data-ttu-id="30d79-110">Virtuális hálózat esetén megadhatja a belső terheléselosztó alhálózatát vagy IP-címét.</span><span class="sxs-lookup"><span data-stu-id="30d79-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="30d79-111">Példák</span><span class="sxs-lookup"><span data-stu-id="30d79-111">EXAMPLES</span></span>

### <span data-ttu-id="30d79-112">1:</span><span class="sxs-lookup"><span data-stu-id="30d79-112">1:</span></span>
```

```

## <span data-ttu-id="30d79-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30d79-113">PARAMETERS</span></span>

### <span data-ttu-id="30d79-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="30d79-114">-InformationAction</span></span>
<span data-ttu-id="30d79-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="30d79-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="30d79-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="30d79-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30d79-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="30d79-117">Continue</span></span>
- <span data-ttu-id="30d79-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="30d79-118">Ignore</span></span>
- <span data-ttu-id="30d79-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="30d79-119">Inquire</span></span>
- <span data-ttu-id="30d79-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="30d79-120">SilentlyContinue</span></span>
- <span data-ttu-id="30d79-121">állj</span><span class="sxs-lookup"><span data-stu-id="30d79-121">Stop</span></span>
- <span data-ttu-id="30d79-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="30d79-122">Suspend</span></span>

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

### <span data-ttu-id="30d79-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="30d79-123">-InformationVariable</span></span>
<span data-ttu-id="30d79-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="30d79-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="30d79-125">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="30d79-125">-InternalLoadBalancerName</span></span>
<span data-ttu-id="30d79-126">Annak a belső terheléselosztásnak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="30d79-126">Specifies the name of the internal load balancer that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="30d79-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="30d79-127">-Profile</span></span>
<span data-ttu-id="30d79-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="30d79-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30d79-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="30d79-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30d79-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="30d79-130">-ServiceName</span></span>
<span data-ttu-id="30d79-131">Annak a szolgáltatásnak a nevét adja meg, amelyben a parancsmag módosította a belső terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="30d79-131">Specifies the name of the service in which this cmdlet modifies an internal load balancer.</span></span>

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

### <span data-ttu-id="30d79-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="30d79-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="30d79-133">A belső terheléselosztó virtuális hálózati IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30d79-133">Specifies the virtual network IP address for an internal load balancer.</span></span>

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

### <span data-ttu-id="30d79-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="30d79-134">-SubnetName</span></span>
<span data-ttu-id="30d79-135">A belső terheléselosztó alhálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30d79-135">Specifies the name of the subnet for an internal load balancer.</span></span>

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

### <span data-ttu-id="30d79-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d79-136">CommonParameters</span></span>
<span data-ttu-id="30d79-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30d79-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d79-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d79-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d79-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30d79-139">INPUTS</span></span>

## <span data-ttu-id="30d79-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30d79-140">OUTPUTS</span></span>

## <span data-ttu-id="30d79-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30d79-141">NOTES</span></span>

## <span data-ttu-id="30d79-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30d79-142">RELATED LINKS</span></span>

[<span data-ttu-id="30d79-143">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30d79-143">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="30d79-144">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30d79-144">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="30d79-145">Új – AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="30d79-145">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="30d79-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30d79-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)


