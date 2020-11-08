---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016348"
---
# <span data-ttu-id="9d73d-101">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="9d73d-101">Get-AzureIPForwarding</span></span>

## <span data-ttu-id="9d73d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d73d-102">SYNOPSIS</span></span>
<span data-ttu-id="9d73d-103">Megkapja az IP-továbbítás állapotát.</span><span class="sxs-lookup"><span data-stu-id="9d73d-103">Gets the status of IP forwarding.</span></span>

## <span data-ttu-id="9d73d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d73d-104">SYNTAX</span></span>

### <span data-ttu-id="9d73d-105">IaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="9d73d-105">IaaSIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d73d-106">SlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="9d73d-106">SlotIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d73d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d73d-107">DESCRIPTION</span></span>
<span data-ttu-id="9d73d-108">A **Get-AzureIPForwarding** parancsmag az IP-továbbítás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9d73d-108">The **Get-AzureIPForwarding** cmdlet gets the status of IP forwarding.</span></span>

## <span data-ttu-id="9d73d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9d73d-109">EXAMPLES</span></span>

### <span data-ttu-id="9d73d-110">Példa 1: IP-továbbítási állapot beszerzése virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="9d73d-110">Example 1: Get IP forwarding status for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

<span data-ttu-id="9d73d-111">Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="9d73d-111">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="9d73d-112">Az aktuális parancsmag a virtuális gép IP-továbbítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9d73d-112">The current cmdlet gets the status of IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="9d73d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d73d-113">PARAMETERS</span></span>

### <span data-ttu-id="9d73d-114">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="9d73d-114">-NetworkInterfaceName</span></span>
<span data-ttu-id="9d73d-115">Annak a hálózati adapternek a neve, amelyhez a parancsmag IP-továbbítási állapotot kap.</span><span class="sxs-lookup"><span data-stu-id="9d73d-115">Specifies the name of the network adapter for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="9d73d-116">-Profile</span></span>
<span data-ttu-id="9d73d-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9d73d-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9d73d-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9d73d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d73d-119">-RoleName</span><span class="sxs-lookup"><span data-stu-id="9d73d-119">-RoleName</span></span>
<span data-ttu-id="9d73d-120">Itt adhatja meg annak a Pásti-szerepnek a nevét, amelynek a parancsmagja IP-továbbítási állapotot kap.</span><span class="sxs-lookup"><span data-stu-id="9d73d-120">Specifies the name of a PaaS role for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-121">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="9d73d-121">-ServiceName</span></span>
<span data-ttu-id="9d73d-122">Egy felhőalapú szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d73d-122">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="9d73d-123">A Péter-szerep a paraméter által megadott szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="9d73d-123">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="9d73d-124">-Slot</span></span>
<span data-ttu-id="9d73d-125">A Péter-bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d73d-125">Specifies a PaaS slot.</span></span>
<span data-ttu-id="9d73d-126">Az a Péter-szerep, amelyre a parancsmag átirányítást kap, a paraméter által megadott bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d73d-126">The PaaS role for which this cmdlet gets forwarding status has the slot that this parameter specifies.</span></span>
<span data-ttu-id="9d73d-127">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="9d73d-127">Valid values are:</span></span> 

- <span data-ttu-id="9d73d-128">Production</span><span class="sxs-lookup"><span data-stu-id="9d73d-128">Production</span></span>
- <span data-ttu-id="9d73d-129">Átmeneti tárolásra szolgáló</span><span class="sxs-lookup"><span data-stu-id="9d73d-129">Staging</span></span> 

<span data-ttu-id="9d73d-130">Az alapértelmezett érték a termelés.</span><span class="sxs-lookup"><span data-stu-id="9d73d-130">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-131">-VM</span><span class="sxs-lookup"><span data-stu-id="9d73d-131">-VM</span></span>
<span data-ttu-id="9d73d-132">Annak a virtuálisgép-objektumnak a megadása, amelyhez ez a parancsmag IP-továbbítási állapotot kap.</span><span class="sxs-lookup"><span data-stu-id="9d73d-132">Specifies the virtual machine object for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d73d-133">CommonParameters</span></span>
<span data-ttu-id="9d73d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d73d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d73d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d73d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d73d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d73d-136">INPUTS</span></span>

## <span data-ttu-id="9d73d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d73d-137">OUTPUTS</span></span>

### <span data-ttu-id="9d73d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9d73d-138">System.String</span></span>

## <span data-ttu-id="9d73d-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d73d-139">NOTES</span></span>

## <span data-ttu-id="9d73d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d73d-140">RELATED LINKS</span></span>

[<span data-ttu-id="9d73d-141">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="9d73d-141">Set-AzureIPForwarding</span></span>](./Set-AzureIPForwarding.md)


