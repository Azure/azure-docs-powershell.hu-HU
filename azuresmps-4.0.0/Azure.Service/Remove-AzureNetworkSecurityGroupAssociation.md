---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E3E0237-8E2D-4B3A-AD0C-2121DDE1AAB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28259b97f382092f5e6293048c040688011cfe92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016152"
---
# <span data-ttu-id="3cacc-101">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="3cacc-101">Remove-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="3cacc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3cacc-102">SYNOPSIS</span></span>
<span data-ttu-id="3cacc-103">Egy hálózati biztonsági csoport eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3cacc-103">Removes a network security group.</span></span>

## <span data-ttu-id="3cacc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3cacc-104">SYNTAX</span></span>

### <span data-ttu-id="3cacc-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span><span class="sxs-lookup"><span data-stu-id="3cacc-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3cacc-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span><span class="sxs-lookup"><span data-stu-id="3cacc-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3cacc-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span><span class="sxs-lookup"><span data-stu-id="3cacc-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> [-Slot <String>] -RoleName <String>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cacc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3cacc-108">DESCRIPTION</span></span>
<span data-ttu-id="3cacc-109">A **Remove-AzureNetworkSecurityGroupAssociation** parancsmag egy virtuális gépről eltávolítja a hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="3cacc-109">The **Remove-AzureNetworkSecurityGroupAssociation** cmdlet removes a network security group from a virtual machine.</span></span>

## <span data-ttu-id="3cacc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3cacc-110">EXAMPLES</span></span>

### <span data-ttu-id="3cacc-111">Példa 1: virtuális gép eltávolítása hálózati biztonsági csoportba</span><span class="sxs-lookup"><span data-stu-id="3cacc-111">Example 1: Remove a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Remove-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="3cacc-112">Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="3cacc-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="3cacc-113">Az aktuális parancsmag eltávolítja a ContosoNetworkSecurityGroup nevű hálózati biztonsági csoportot a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3cacc-113">The current cmdlet removes the network security group named ContosoNetworkSecurityGroup from that virtual machine.</span></span>

## <span data-ttu-id="3cacc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3cacc-114">PARAMETERS</span></span>

### <span data-ttu-id="3cacc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3cacc-115">-Force</span></span>
<span data-ttu-id="3cacc-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3cacc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3cacc-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3cacc-117">-Name</span></span>
<span data-ttu-id="3cacc-118">A parancsmag által eltávolított hálózati biztonsági csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cacc-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3cacc-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="3cacc-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="3cacc-120">Annak a hálózati adapternek a neve, amelyből a parancsmag eltávolítja a hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="3cacc-120">Specifies the name of the network adapter from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cacc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cacc-121">-PassThru</span></span>
<span data-ttu-id="3cacc-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3cacc-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3cacc-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3cacc-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3cacc-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="3cacc-124">-Profile</span></span>
<span data-ttu-id="3cacc-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3cacc-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3cacc-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3cacc-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3cacc-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="3cacc-127">-RoleName</span></span>
<span data-ttu-id="3cacc-128">Azt a nevet adja meg, ahol a parancsmag a hálózati biztonsági csoportot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="3cacc-128">Specifies the name of a PaaS role from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cacc-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="3cacc-129">-ServiceName</span></span>
<span data-ttu-id="3cacc-130">Egy felhőalapú szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cacc-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="3cacc-131">Az a Pásti szerepkör, amelyből a parancsmag eltávolítja a hálózat biztonsági csoportját, a paraméter által megadott szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="3cacc-131">The PaaS role from which this cmdlet removes a network security group belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cacc-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="3cacc-132">-Slot</span></span>
<span data-ttu-id="3cacc-133">A Péter-bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cacc-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="3cacc-134">Az a Pásti szerepkör, amelyből a parancsmag eltávolítja a hálózat biztonsági csoportját, a megfelelő bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cacc-134">The PaaS role from which this cmdlet removes a network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="3cacc-135">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="3cacc-135">Valid values are:</span></span>

- <span data-ttu-id="3cacc-136">Production</span><span class="sxs-lookup"><span data-stu-id="3cacc-136">Production</span></span>
- <span data-ttu-id="3cacc-137">Átmeneti tárolásra szolgáló</span><span class="sxs-lookup"><span data-stu-id="3cacc-137">Staging</span></span>

<span data-ttu-id="3cacc-138">Az alapértelmezett érték a termelés.</span><span class="sxs-lookup"><span data-stu-id="3cacc-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cacc-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3cacc-139">-SubnetName</span></span>
<span data-ttu-id="3cacc-140">Annak az alhálózatnak a neve, amelyből a parancsmag eltávolítja a hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="3cacc-140">Specifies the name of a subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cacc-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3cacc-141">-VirtualNetworkName</span></span>
<span data-ttu-id="3cacc-142">Annak az alhálózatnak a neve, amelyből a parancsmag eltávolítja a hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="3cacc-142">Specifies the name of a virtual network that contains the subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cacc-143">-VM</span><span class="sxs-lookup"><span data-stu-id="3cacc-143">-VM</span></span>
<span data-ttu-id="3cacc-144">Azt a virtuális gépet adja meg, amelyre a parancsmag a hálózat biztonsági csoportját alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="3cacc-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cacc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cacc-145">CommonParameters</span></span>
<span data-ttu-id="3cacc-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3cacc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cacc-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cacc-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cacc-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cacc-148">INPUTS</span></span>

## <span data-ttu-id="3cacc-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cacc-149">OUTPUTS</span></span>

### <span data-ttu-id="3cacc-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3cacc-150">System.Boolean</span></span>

## <span data-ttu-id="3cacc-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3cacc-151">NOTES</span></span>

## <span data-ttu-id="3cacc-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cacc-152">RELATED LINKS</span></span>

[<span data-ttu-id="3cacc-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="3cacc-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="3cacc-154">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="3cacc-154">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)
