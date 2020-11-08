---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016582"
---
# <span data-ttu-id="fa581-101">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="fa581-101">Get-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="fa581-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa581-102">SYNOPSIS</span></span>
<span data-ttu-id="fa581-103">Egy virtuális gép, hálózati adapter vagy Péter szerepkör hálózati biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="fa581-103">Gets a network security group for a virtual machine, network adapter, or PaaS role.</span></span>

## <span data-ttu-id="fa581-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa581-104">SYNTAX</span></span>

### <span data-ttu-id="fa581-105">GetNetworkSecurityGroupAssociationForSubnet</span><span class="sxs-lookup"><span data-stu-id="fa581-105">GetNetworkSecurityGroupAssociationForSubnet</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fa581-106">GetNetworkSecurityGroupAssociationForIaaSRole</span><span class="sxs-lookup"><span data-stu-id="fa581-106">GetNetworkSecurityGroupAssociationForIaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fa581-107">GetNetworkSecurityGroupAssociationForPaaSRole</span><span class="sxs-lookup"><span data-stu-id="fa581-107">GetNetworkSecurityGroupAssociationForPaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fa581-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa581-108">DESCRIPTION</span></span>
<span data-ttu-id="fa581-109">A **Get-AzureNetworkSecurityGroupAssociation** parancsmag a virtuális gép, hálózati adapter vagy platform hálózati biztonsági csoportjának szolgáltatás (Pásti) szerepkörét kapja.</span><span class="sxs-lookup"><span data-stu-id="fa581-109">The **Get-AzureNetworkSecurityGroupAssociation** cmdlet gets the network security group for a virtual machine, network adapter, or platform as a service (PaaS) role.</span></span>

## <span data-ttu-id="fa581-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fa581-110">EXAMPLES</span></span>

### <span data-ttu-id="fa581-111">Példa 1: a virtuális gép hálózati biztonsági csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="fa581-111">Example 1: Get the network security group for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

<span data-ttu-id="fa581-112">Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="fa581-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="fa581-113">Az aktuális parancsmag a virtuális géphez társított hálózati biztonsági csoportot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fa581-113">The current cmdlet gets the network security group associated to that virtual machine.</span></span>

## <span data-ttu-id="fa581-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa581-114">PARAMETERS</span></span>

### <span data-ttu-id="fa581-115">– Részletes</span><span class="sxs-lookup"><span data-stu-id="fa581-115">-Detailed</span></span>
<span data-ttu-id="fa581-116">Azt jelzi, hogy ez a parancsmag a virtuális géphez társított hálózati biztonsági csoport adatait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fa581-116">Indicates that this cmdlet returns details of the network security group that is associated to the virtual machine.</span></span>
<span data-ttu-id="fa581-117">Ezek a részletek a hely és a szabályok között is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="fa581-117">These details include location and rules.</span></span>

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

### <span data-ttu-id="fa581-118">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="fa581-118">-NetworkInterfaceName</span></span>
<span data-ttu-id="fa581-119">Annak a hálózati adapternek a neve, amelyhez a parancsmag a hálózat biztonsági csoportját kapja.</span><span class="sxs-lookup"><span data-stu-id="fa581-119">Specifies the name of the network adapter for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa581-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="fa581-120">-Profile</span></span>
<span data-ttu-id="fa581-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="fa581-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="fa581-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="fa581-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa581-123">-RoleName</span><span class="sxs-lookup"><span data-stu-id="fa581-123">-RoleName</span></span>
<span data-ttu-id="fa581-124">Annak a Péter-szerepnek a nevét adja meg, amelyhez ez a parancsmag a hálózat biztonsági csoportját kapja.</span><span class="sxs-lookup"><span data-stu-id="fa581-124">Specifies the name of a PaaS role for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa581-125">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="fa581-125">-ServiceName</span></span>
<span data-ttu-id="fa581-126">Egy felhőalapú szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa581-126">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="fa581-127">A Péter-szerep a paraméter által megadott szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="fa581-127">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa581-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="fa581-128">-Slot</span></span>
<span data-ttu-id="fa581-129">A Péter-bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa581-129">Specifies a PaaS slot.</span></span>
<span data-ttu-id="fa581-130">A Pásti szerepkör, amelyhez a parancsmag a hálózati biztonsági csoportot kapja, a megfelelő bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa581-130">The PaaS role for which this cmdlet gets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="fa581-131">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="fa581-131">Valid values are:</span></span> 

- <span data-ttu-id="fa581-132">Production</span><span class="sxs-lookup"><span data-stu-id="fa581-132">Production</span></span>
- <span data-ttu-id="fa581-133">Átmeneti tárolásra szolgáló</span><span class="sxs-lookup"><span data-stu-id="fa581-133">Staging</span></span> 

<span data-ttu-id="fa581-134">Az alapértelmezett érték a termelés.</span><span class="sxs-lookup"><span data-stu-id="fa581-134">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa581-135">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="fa581-135">-SubnetName</span></span>
<span data-ttu-id="fa581-136">Annak az alhálózatnak a neve, amelyhez a parancsmag a hálózat biztonsági csoportját kapja.</span><span class="sxs-lookup"><span data-stu-id="fa581-136">Specifies the name of a subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa581-137">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fa581-137">-VirtualNetworkName</span></span>
<span data-ttu-id="fa581-138">Megadja annak a virtuális hálózatnak a nevét, amely tartalmazza azt az alhálózatot, amelynek a parancsmagja a hálózat biztonsági csoportját kapja.</span><span class="sxs-lookup"><span data-stu-id="fa581-138">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa581-139">-VM</span><span class="sxs-lookup"><span data-stu-id="fa581-139">-VM</span></span>
<span data-ttu-id="fa581-140">Azt a virtuális gépet adja meg, amelyre a parancsmag a hálózat biztonsági csoportját alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="fa581-140">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa581-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa581-141">CommonParameters</span></span>
<span data-ttu-id="fa581-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa581-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa581-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa581-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa581-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa581-144">INPUTS</span></span>

## <span data-ttu-id="fa581-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa581-145">OUTPUTS</span></span>

### <span data-ttu-id="fa581-146">Microsoft. WindowsAzure. Command. ServiceManagement. Network. NetworkSecurityGroup. Model. INetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fa581-146">Microsoft.WindowsAzure.Commands.ServiceManagement.Network.NetworkSecurityGroup.Model.INetworkSecurityGroup</span></span>

## <span data-ttu-id="fa581-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa581-147">NOTES</span></span>

## <span data-ttu-id="fa581-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa581-148">RELATED LINKS</span></span>

[<span data-ttu-id="fa581-149">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="fa581-149">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="fa581-150">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="fa581-150">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)


