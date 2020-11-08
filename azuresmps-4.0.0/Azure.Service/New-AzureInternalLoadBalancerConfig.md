---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C01AFE1-65E7-4C5F-B3ED-8FCD9C4D20FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: a42ffe7ded2eb47638dd961ae79b10dd21cf08ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015914"
---
# <span data-ttu-id="002e3-101">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="002e3-101">New-AzureInternalLoadBalancerConfig</span></span>

## <span data-ttu-id="002e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="002e3-102">SYNOPSIS</span></span>
<span data-ttu-id="002e3-103">Belső terheléselosztó konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="002e3-103">Creates an internal load balancer configuration.</span></span>

## <span data-ttu-id="002e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="002e3-104">SYNTAX</span></span>

### <span data-ttu-id="002e3-105">ServiceAndSlot (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="002e3-105">ServiceAndSlot (Default)</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="002e3-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="002e3-106">SubnetNameOnly</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="002e3-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="002e3-107">SubnetNameAndIP</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="002e3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="002e3-108">DESCRIPTION</span></span>
<span data-ttu-id="002e3-109">A **New-AzureInternalLoadBalancerConfig** parancsmag létrehoz egy **InternalLoadBalancerConfig** objektumot.</span><span class="sxs-lookup"><span data-stu-id="002e3-109">The **New-AzureInternalLoadBalancerConfig** cmdlet creates an **InternalLoadBalancerConfig** object.</span></span>
<span data-ttu-id="002e3-110">Az Azure virtuálisgép-telepítő létrehozásakor belső terheléselosztó konfigurációt is használhat.</span><span class="sxs-lookup"><span data-stu-id="002e3-110">You can use an internal load balancer configuration when you create an Azure virtual machine deployment.</span></span>

## <span data-ttu-id="002e3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="002e3-111">EXAMPLES</span></span>

### <span data-ttu-id="002e3-112">Példa 1: belső terheléselosztó konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="002e3-112">Example 1: Create an internal load balancer configuration</span></span>
```
PS C:\> $IlbConfig = New-AzureInternalLoadBalancerConfig -InternalLoadBalancerName "Contoso" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="002e3-113">Ez a parancs létrehoz egy belső terheléselosztási konfigurációt a FrontEndSubnet nevű alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="002e3-113">This command creates an internal load balancer configuration for the subnet named FrontEndSubnet.</span></span>
<span data-ttu-id="002e3-114">A parancs a $IlbConfig változó konfigurációját tárolja a virtuálisgép-bevezetéshez való használathoz.</span><span class="sxs-lookup"><span data-stu-id="002e3-114">The command stores the configuration in the $IlbConfig variable for you to use for a virtual machine deployment.</span></span>

## <span data-ttu-id="002e3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="002e3-115">PARAMETERS</span></span>

### <span data-ttu-id="002e3-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="002e3-116">-InformationAction</span></span>
<span data-ttu-id="002e3-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="002e3-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="002e3-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="002e3-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="002e3-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="002e3-119">Continue</span></span>
- <span data-ttu-id="002e3-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="002e3-120">Ignore</span></span>
- <span data-ttu-id="002e3-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="002e3-121">Inquire</span></span>
- <span data-ttu-id="002e3-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="002e3-122">SilentlyContinue</span></span>
- <span data-ttu-id="002e3-123">állj</span><span class="sxs-lookup"><span data-stu-id="002e3-123">Stop</span></span>
- <span data-ttu-id="002e3-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="002e3-124">Suspend</span></span>

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

### <span data-ttu-id="002e3-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="002e3-125">-InformationVariable</span></span>
<span data-ttu-id="002e3-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="002e3-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="002e3-127">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="002e3-127">-InternalLoadBalancerName</span></span>
<span data-ttu-id="002e3-128">Annak a belső terheléselosztó a nevét adja meg, amelyre a parancsmag a konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="002e3-128">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="002e3-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="002e3-129">-Profile</span></span>
<span data-ttu-id="002e3-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="002e3-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="002e3-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="002e3-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="002e3-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="002e3-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="002e3-133">Itt adhatja meg egy belső terheléselosztó virtuális hálózat IP-címét, amelyre a parancsmag a konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="002e3-133">Specifies the virtual network IP address for an internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="002e3-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="002e3-134">-SubnetName</span></span>
<span data-ttu-id="002e3-135">A belső terheléselosztó alhálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="002e3-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="002e3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002e3-136">CommonParameters</span></span>
<span data-ttu-id="002e3-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="002e3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002e3-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="002e3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002e3-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="002e3-139">INPUTS</span></span>

## <span data-ttu-id="002e3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="002e3-140">OUTPUTS</span></span>

### <span data-ttu-id="002e3-141">Microsoft. WindowsAzure. Command. ServiceManagement. Model. InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="002e3-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerConfig</span></span>

## <span data-ttu-id="002e3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="002e3-142">NOTES</span></span>

## <span data-ttu-id="002e3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="002e3-143">RELATED LINKS</span></span>

[<span data-ttu-id="002e3-144">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="002e3-144">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="002e3-145">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="002e3-145">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="002e3-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="002e3-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="002e3-147">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="002e3-147">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


