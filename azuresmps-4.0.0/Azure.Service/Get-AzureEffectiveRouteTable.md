---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016353"
---
# <span data-ttu-id="52894-101">Get-AzureEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="52894-101">Get-AzureEffectiveRouteTable</span></span>

## <span data-ttu-id="52894-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52894-102">SYNOPSIS</span></span>
<span data-ttu-id="52894-103">A virtuális gép által alkalmazott útvonal beolvasása.</span><span class="sxs-lookup"><span data-stu-id="52894-103">Gets the route applied in a virtual machine.</span></span>

## <span data-ttu-id="52894-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52894-104">SYNTAX</span></span>

### <span data-ttu-id="52894-105">IaaSGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="52894-105">IaaSGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="52894-106">SlotGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="52894-106">SlotGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="52894-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="52894-107">DESCRIPTION</span></span>
<span data-ttu-id="52894-108">A **Get-AzureEffectiveRouteTable** parancsmag a virtuális gépeken alkalmazott útvonalat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="52894-108">The **Get-AzureEffectiveRouteTable** cmdlet gets the route applied in a virtual machine.</span></span>
<span data-ttu-id="52894-109">Ez a művelet néhány másodpercig eltarthat.</span><span class="sxs-lookup"><span data-stu-id="52894-109">This operation could take several seconds to finish.</span></span>

## <span data-ttu-id="52894-110">Példák</span><span class="sxs-lookup"><span data-stu-id="52894-110">EXAMPLES</span></span>

### <span data-ttu-id="52894-111">Példa 1: a tényleges útvonal beszerzése virtuális gépet alkalmazva</span><span class="sxs-lookup"><span data-stu-id="52894-111">Example 1: Get the effective route applied a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

<span data-ttu-id="52894-112">Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="52894-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="52894-113">Az aktuális parancsmag a virtuális gépre alkalmazott útvonalat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="52894-113">The current cmdlet gets the route applied to that virtual machine.</span></span>

## <span data-ttu-id="52894-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52894-114">PARAMETERS</span></span>

### <span data-ttu-id="52894-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="52894-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="52894-116">Annak a hálózati adapternek a nevét adja meg, amelyhez ez a parancsmag hatékony útvonalakat kap.</span><span class="sxs-lookup"><span data-stu-id="52894-116">Specifies the name of the network adapter for which this cmdlet gets effective routes.</span></span>

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

### <span data-ttu-id="52894-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="52894-117">-Profile</span></span>
<span data-ttu-id="52894-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="52894-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="52894-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="52894-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52894-120">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="52894-120">-RoleInstanceName</span></span>
<span data-ttu-id="52894-121">Annak a Pásti-szerepnek a nevét adja meg, amelynek a parancsmagja hatékony útvonalakat kap.</span><span class="sxs-lookup"><span data-stu-id="52894-121">Specifies the name of a PaaS role for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52894-122">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="52894-122">-ServiceName</span></span>
<span data-ttu-id="52894-123">Egy felhőalapú szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52894-123">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="52894-124">A Péter szerepkör, amelyhez ez a parancsmag érvényes útvonalú, a paraméter által megadott szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="52894-124">The PaaS role for which this cmdlet gets effective routes belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="52894-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="52894-125">-Slot</span></span>
<span data-ttu-id="52894-126">A Péter-bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="52894-126">Specifies a PaaS slot.</span></span>
<span data-ttu-id="52894-127">Az a Péter-szerep, amelynek a parancsmagja hatékony útvonalon van, a paraméter által megadott bővítőhely van megadható.</span><span class="sxs-lookup"><span data-stu-id="52894-127">The PaaS role for which this cmdlet gets effective routes has the slot that this parameter specifies.</span></span>
<span data-ttu-id="52894-128">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="52894-128">Valid values are:</span></span> 

- <span data-ttu-id="52894-129">Production</span><span class="sxs-lookup"><span data-stu-id="52894-129">Production</span></span>
- <span data-ttu-id="52894-130">Átmeneti tárolásra szolgáló</span><span class="sxs-lookup"><span data-stu-id="52894-130">Staging</span></span> 

<span data-ttu-id="52894-131">Az alapértelmezett érték a termelés.</span><span class="sxs-lookup"><span data-stu-id="52894-131">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52894-132">-VM</span><span class="sxs-lookup"><span data-stu-id="52894-132">-VM</span></span>
<span data-ttu-id="52894-133">Annak a virtuális gépnek az objektumát adja meg, amelyhez ez a parancsmag hatékony útvonalakat kap.</span><span class="sxs-lookup"><span data-stu-id="52894-133">Specifies the virtual machine object for which this cmdlet gets effective routes.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52894-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52894-134">CommonParameters</span></span>
<span data-ttu-id="52894-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52894-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52894-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52894-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52894-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52894-137">INPUTS</span></span>

## <span data-ttu-id="52894-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52894-138">OUTPUTS</span></span>

### <span data-ttu-id="52894-139">System. Collections. Generic. IEnumerable<Microsoft. WindowsAzure. Management. Network. models. EffectiveRouteTable, Microsoft. WindowsAzure. Management. Network></span><span class="sxs-lookup"><span data-stu-id="52894-139">System.Collections.Generic.IEnumerable<Microsoft.WindowsAzure.Management.Network.Models.EffectiveRouteTable, Microsoft.WindowsAzure.Management.Network></span></span>

## <span data-ttu-id="52894-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52894-140">NOTES</span></span>

## <span data-ttu-id="52894-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52894-141">RELATED LINKS</span></span>

[<span data-ttu-id="52894-142">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="52894-142">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="52894-143">Új – AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="52894-143">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="52894-144">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="52894-144">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)

[<span data-ttu-id="52894-145">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="52894-145">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="52894-146">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="52894-146">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


