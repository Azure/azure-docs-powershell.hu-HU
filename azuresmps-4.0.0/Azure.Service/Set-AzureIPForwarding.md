---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015956"
---
# <span data-ttu-id="6a5d0-101">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="6a5d0-101">Set-AzureIPForwarding</span></span>

## <span data-ttu-id="6a5d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a5d0-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5d0-103">Engedélyezi vagy tiltja az IP-továbbítást.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-103">Enables or disables IP forwarding.</span></span>

## <span data-ttu-id="6a5d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a5d0-104">SYNTAX</span></span>

### <span data-ttu-id="6a5d0-105">EnableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="6a5d0-105">EnableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6a5d0-106">DisableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="6a5d0-106">DisableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6a5d0-107">EnableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="6a5d0-107">EnableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6a5d0-108">DisableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="6a5d0-108">DisableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6a5d0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a5d0-109">DESCRIPTION</span></span>
<span data-ttu-id="6a5d0-110">A **set-AzureIPForwarding** parancsmag engedélyezi vagy letiltja az IP-továbbítást egy virtuális gépen, platformként a szolgáltatásban (Péter), illetve egy virtuális gép vagy Péter szerepkörhöz tartozó hálózati adaptert.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-110">The **Set-AzureIPForwarding** cmdlet enables or disables IP forwarding for a virtual machine, for a platform as a service (PaaS) role, or a network adapter that belongs to a virtual machine or PaaS role.</span></span>

## <span data-ttu-id="6a5d0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6a5d0-111">EXAMPLES</span></span>

### <span data-ttu-id="6a5d0-112">1. példa: az IP-továbbítás engedélyezése virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="6a5d0-112">Example 1: Enable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

<span data-ttu-id="6a5d0-113">Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-113">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="6a5d0-114">Az aktuális parancsmag engedélyezi a virtuális gép IP-továbbítását.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-114">The current cmdlet enables IP forwarding for that virtual machine.</span></span>

### <span data-ttu-id="6a5d0-115">2. példa: a virtuális gép IP-továbbításának letiltása</span><span class="sxs-lookup"><span data-stu-id="6a5d0-115">Example 2: Disable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

<span data-ttu-id="6a5d0-116">Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-116">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="6a5d0-117">Az aktuális parancsmag letiltja a virtuális gép IP-továbbítását.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-117">The current cmdlet disables IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="6a5d0-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a5d0-118">PARAMETERS</span></span>

### <span data-ttu-id="6a5d0-119">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="6a5d0-119">-Disable</span></span>
<span data-ttu-id="6a5d0-120">Jelzi, hogy ez a parancsmag letiltja az IP-továbbítást.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-120">Indicates that this cmdlet disables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5d0-121">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="6a5d0-121">-Enable</span></span>
<span data-ttu-id="6a5d0-122">Azt jelzi, hogy ez a parancsmag engedélyezi az IP-továbbítást.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-122">Indicates that this cmdlet enables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5d0-123">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="6a5d0-123">-NetworkInterfaceName</span></span>
<span data-ttu-id="6a5d0-124">Annak a hálózati adapternek a nevét adja meg, amelyen a parancsmag az IP-továbbítást állítja be.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-124">Specifies the name of the network adapter on which this cmdlet sets IP forwarding.</span></span>

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

### <span data-ttu-id="6a5d0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a5d0-125">-PassThru</span></span>
<span data-ttu-id="6a5d0-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6a5d0-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a5d0-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="6a5d0-128">-Profile</span></span>
<span data-ttu-id="6a5d0-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6a5d0-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a5d0-131">-RoleName</span><span class="sxs-lookup"><span data-stu-id="6a5d0-131">-RoleName</span></span>
<span data-ttu-id="6a5d0-132">Annak a Péter-szerepnek a nevét adja meg, amelyen a parancsmag az IP-továbbítást állítja be.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-132">Specifies the name of a PaaS role on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a5d0-133">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="6a5d0-133">-ServiceName</span></span>
<span data-ttu-id="6a5d0-134">Egy felhőalapú szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-134">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="6a5d0-135">A Péter-szerep a paraméter által megadott szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-135">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a5d0-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="6a5d0-136">-Slot</span></span>
<span data-ttu-id="6a5d0-137">A Péter-bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-137">Specifies a PaaS slot.</span></span>
<span data-ttu-id="6a5d0-138">A Péter szerepkör, amelynek a parancsmagja a továbbítást állítja be, a paraméter által megadott bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-138">The PaaS role for which this cmdlet sets forwarding has the slot that this parameter specifies.</span></span>
<span data-ttu-id="6a5d0-139">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6a5d0-139">Valid values are:</span></span>

- <span data-ttu-id="6a5d0-140">Production</span><span class="sxs-lookup"><span data-stu-id="6a5d0-140">Production</span></span>
- <span data-ttu-id="6a5d0-141">Átmeneti tárolásra szolgáló</span><span class="sxs-lookup"><span data-stu-id="6a5d0-141">Staging</span></span>

<span data-ttu-id="6a5d0-142">Az alapértelmezett érték a termelés.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-142">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5d0-143">-VM</span><span class="sxs-lookup"><span data-stu-id="6a5d0-143">-VM</span></span>
<span data-ttu-id="6a5d0-144">Annak a virtuális gépnek az objektumát adja meg, amelyen a parancsmag az IP-továbbítást állítja be.</span><span class="sxs-lookup"><span data-stu-id="6a5d0-144">Specifies the virtual machine object on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a5d0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5d0-145">CommonParameters</span></span>
<span data-ttu-id="6a5d0-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a5d0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5d0-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a5d0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5d0-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a5d0-148">INPUTS</span></span>

## <span data-ttu-id="6a5d0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a5d0-149">OUTPUTS</span></span>

### <span data-ttu-id="6a5d0-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a5d0-150">System.Boolean</span></span>

## <span data-ttu-id="6a5d0-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a5d0-151">NOTES</span></span>

## <span data-ttu-id="6a5d0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a5d0-152">RELATED LINKS</span></span>

[<span data-ttu-id="6a5d0-153">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="6a5d0-153">Get-AzureIPForwarding</span></span>](./Get-AzureIPForwarding.md)
