---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 64639A35-0573-48C8-AB21-19FEB09537BA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b1b251a5fef3ad91f830e18714796421d2abca7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015758"
---
# <span data-ttu-id="b9896-101">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b9896-101">Set-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="b9896-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9896-102">SYNOPSIS</span></span>
<span data-ttu-id="b9896-103">Hálózati biztonsági csoportot társít egy virtuális géphez, Péterhez vagy hálózati adapterhez.</span><span class="sxs-lookup"><span data-stu-id="b9896-103">Associates a network security group to a virtual machine, PaaS role, or network adapter.</span></span>

## <span data-ttu-id="b9896-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9896-104">SYNTAX</span></span>

### <span data-ttu-id="b9896-105">AddNetworkSecurityGroupAssociationToSubnet</span><span class="sxs-lookup"><span data-stu-id="b9896-105">AddNetworkSecurityGroupAssociationToSubnet</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VirtualNetworkName <String>
 -SubnetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b9896-106">AddNetworkSecurityGroupAssociationToIaaSRole</span><span class="sxs-lookup"><span data-stu-id="b9896-106">AddNetworkSecurityGroupAssociationToIaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VM <PersistentVMRoleContext>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b9896-107">AddNetworkSecurityGroupAssociationToPaaSRole</span><span class="sxs-lookup"><span data-stu-id="b9896-107">AddNetworkSecurityGroupAssociationToPaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] [-Slot <String>]
 -RoleName <String> -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9896-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9896-108">DESCRIPTION</span></span>
<span data-ttu-id="b9896-109">A **set-AzureNetworkSecurityGroupAssociation** parancsmag egy virtuális gépre, platformra (Péter) vagy hálózati adapterre társít egy hálózati biztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="b9896-109">The **Set-AzureNetworkSecurityGroupAssociation** cmdlet associates a network security group to a virtual machine, platform as a service (PaaS) role, or network adapter.</span></span>

## <span data-ttu-id="b9896-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b9896-110">EXAMPLES</span></span>

### <span data-ttu-id="b9896-111">Példa 1: virtuális gép hozzárendelése hálózati biztonsági csoporthoz</span><span class="sxs-lookup"><span data-stu-id="b9896-111">Example 1: Assign a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="b9896-112">Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b9896-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="b9896-113">Az aktuális parancsmag a ContosoNetworkSecurityGroup nevű hálózati biztonsági csoportot rendeli hozzá a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b9896-113">The current cmdlet assigns the network security group named ContosoNetworkSecurityGroup to that virtual machine.</span></span>

## <span data-ttu-id="b9896-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9896-114">PARAMETERS</span></span>

### <span data-ttu-id="b9896-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b9896-115">-Force</span></span>
<span data-ttu-id="b9896-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b9896-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9896-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9896-117">-Name</span></span>
<span data-ttu-id="b9896-118">A parancsmag által beállított hálózati biztonsági csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9896-118">Specifies the name of the network security group that this cmdlet sets.</span></span>

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

### <span data-ttu-id="b9896-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="b9896-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="b9896-120">Annak a hálózati adapternek a nevét adja meg, amelyre a parancsmag a hálózat biztonsági csoportját alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="b9896-120">Specifies the name of the network adapter to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9896-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9896-121">-PassThru</span></span>
<span data-ttu-id="b9896-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b9896-122">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b9896-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b9896-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b9896-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="b9896-124">-Profile</span></span>
<span data-ttu-id="b9896-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b9896-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b9896-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b9896-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b9896-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="b9896-127">-RoleName</span></span>
<span data-ttu-id="b9896-128">Annak a Péter-szerepnek a nevét adja meg, amelyre a parancsmag a hálózat biztonsági csoportját alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="b9896-128">Specifies the name of a PaaS role to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9896-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="b9896-129">-ServiceName</span></span>
<span data-ttu-id="b9896-130">Egy felhőalapú szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9896-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="b9896-131">A Péter-szerep a paraméter által megadott szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="b9896-131">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9896-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="b9896-132">-Slot</span></span>
<span data-ttu-id="b9896-133">A Péter-bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9896-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="b9896-134">A Pásti szerepkör, amelyre a parancsmag a hálózat biztonsági csoportját állítja be, a paraméter által megadott bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9896-134">The PaaS role for which this cmdlet sets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="b9896-135">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b9896-135">Valid values are:</span></span> 

- <span data-ttu-id="b9896-136">Production</span><span class="sxs-lookup"><span data-stu-id="b9896-136">Production</span></span>
- <span data-ttu-id="b9896-137">Átmeneti tárolásra szolgáló</span><span class="sxs-lookup"><span data-stu-id="b9896-137">Staging</span></span> 

<span data-ttu-id="b9896-138">Az alapértelmezett érték a termelés.</span><span class="sxs-lookup"><span data-stu-id="b9896-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9896-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b9896-139">-SubnetName</span></span>
<span data-ttu-id="b9896-140">Annak az alhálózatnak a neve, amelyhez ez a parancsmag a hálózat biztonsági csoportját társítja.</span><span class="sxs-lookup"><span data-stu-id="b9896-140">Specifies the name of a subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9896-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b9896-141">-VirtualNetworkName</span></span>
<span data-ttu-id="b9896-142">Megadja annak a virtuális hálózatnak a nevét, amely tartalmazza azt az alhálózatot, amelyhez ez a parancsmag a hálózat biztonsági csoportját társítja.</span><span class="sxs-lookup"><span data-stu-id="b9896-142">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9896-143">-VM</span><span class="sxs-lookup"><span data-stu-id="b9896-143">-VM</span></span>
<span data-ttu-id="b9896-144">Azt a virtuális gépet adja meg, amelyre a parancsmag a hálózat biztonsági csoportját alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="b9896-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9896-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9896-145">CommonParameters</span></span>
<span data-ttu-id="b9896-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9896-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9896-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9896-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9896-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9896-148">INPUTS</span></span>

## <span data-ttu-id="b9896-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9896-149">OUTPUTS</span></span>

### <span data-ttu-id="b9896-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9896-150">System.Boolean</span></span>

## <span data-ttu-id="b9896-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9896-151">NOTES</span></span>

## <span data-ttu-id="b9896-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9896-152">RELATED LINKS</span></span>

[<span data-ttu-id="b9896-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b9896-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="b9896-154">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b9896-154">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)


