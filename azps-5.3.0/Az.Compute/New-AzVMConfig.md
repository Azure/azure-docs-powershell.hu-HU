---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 62349410e3858978166fd9c5356a8c6b568b9600
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477713"
---
# New-AzVMConfig

## SYNOPSIS
Konfigurálható virtuális gépobjektumot hoz létre.

## SZINTAXIS

### DefaultParameterSet (alapértelmezett)
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzVMConfig** parancsmag létrehoz egy konfigurálható helyi virtuális gépobjektumot az Azure-hoz.
A virtuális gépi objektumok (például Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface és Set-AzVMOSDisk) konfigurálása más parancsmagokkal is használhatók.

## PÉLDÁK

### 1. példa: Virtuális gépi objektum létrehozása
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

Az első parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet03 nevű elérhetőségi halmazt kapja, majd az objektumot a $AvailabilitySet tárolja.
A második parancs létrehoz egy virtuális gépobjektumot, majd a $VirtualMachine tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.

## PARAMETERS

### -AvailabilitySetId
Egy rendelkezésre állási készlet azonosítóját adja meg.
Az elérhetőségi halmaz objektum beszerzéséhez használja a Get-AzAvailabilitySet parancsmagot.
Az elérhetőségi halmaz objektum egy ID tulajdonságot tartalmaz. <br>
Az ugyanazon rendelkezésre állási halmazban megadott virtuális gépek a rendelkezésre állás maximalizálása érdekében különböző csomópontokra vannak kiosztva. <br>
Az elérhetőségi készletekről további információt a virtuális gépek elérhetőségének [kezelése.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Az Azure tervezett karbantartásával kapcsolatos további információkért lásd: Tervezett karbantartás [virtuális gépekhez az Azure-ban](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Jelenleg egy virtuális gép csak a létrehozáskor megadott elérhetőségi beállításhoz vehető fel. Az elérhetőségi készletnek, amelyhez a VM-et hozzá kell adni, ugyanabban az erőforráscsoportban kell lennie, mint az elérhetőségi készlet erőforrásnak. Egy meglévő virtuális gép nem vehető fel egy rendelkezésre állási készletbe. <br>
Ez a tulajdonság nem létezhet nem null értékű properties.virtualMachineScaleSet hivatkozással együtt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUltraSSD
Lehetővé teszi, hogy egy vagy több felügyelt adatlemezzel UltraSSD_LRS tárolófióktípussal a VM-en.
A tárfiók-típussal rendelkező felügyelt UltraSSD_LRS csak akkor lehet virtuális gépre hozzáadni, ha ez a tulajdonság engedélyezve van.


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EvictionPolicy
Az Azure Spot virtuális gépre vonatkozó kilakoltatási házirend.  A támogatott értékek a "Deallocate" és a "Delete".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HostId
A host azonosítója

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityId
A virtuális gép méretkészletével társított felhasználói identitások listáját adja meg.
A felhasználói identitáshivatkozások ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityType
A virtuális gép identitása, ha be van állítva.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Egy licenctípust ad meg, amely azt jelzi, hogy a virtuális gép lemezképe vagy lemeze a helyszínen lett licenccel.
A Windows Server lehetséges értékei:
- Windows_Client
- Windows_Server Linux Server operációs rendszer lehetséges értékei: 
- RHEL_BYOS (RHEL) 
- SLES_BYOS (SUSE) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
Megadja az alacsony prioritású VM/VMSS-ek maximális árát. Ez az ár amerikai dollárban van meg. Ezt az árat összehasonlítjuk a VM-méret jelenlegi alacsony prioritású árával. Ezenkívül az alacsony prioritású VM/VMSS létrehozása/frissítése során összehasonlítja az árakat, és a művelet csak akkor lesz sikeres, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár. A maxPrice akkor is használatos az alacsony prioritású VM/VMSS kivül, ha a jelenlegi alacsony prioritású ár meghaladja a VM/VMSS létrehozását követően a maxPrice értéken. A lehetséges értékek a nullánál nagyobb decimális értékek. Példa: 0,01538.  -1 azt jelzi, hogy az alacsony prioritású VM/VMSS nem lesz kiváltva ár miatt. Az alapértelmezett maximális ár -1, ha nem Ön biztosítja.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptionAtHost
A EncryptionAtHost tulajdonságot a felhasználó használhatja a kérésben a gazdatitkosítás engedélyezéséhez vagy letiltásához a virtuális gép vagy virtuális gép méretarányának beállítására. Ez lehetővé teszi a titkosítást az összes lemezen, beleértve magában az erőforrás-/ideiglenes lemezen is. Alapértelmezett: A gazdaszámítógép titkosítása le lesz tiltva, hacsak ez a tulajdonság nincs igazra állítva az erőforráshoz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
A virtuális gép prioritása.  Csak a "Normál", a "Direkt" és a "Gyenge" érték támogatott.
A "Regular" normál virtuális géphez való.
A "Spot" a direkt virtuális gépekhez való.
A "Low" a direkt virtuális gépre is igaz, de a "Spot" (Direkt) szövegre cseréli. A "Gyenge" helyett használja a "Spot" (Direkt) használhatja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
Az ezzel a virtuális géppel használható Közelség elhelyezési csoport erőforrás-azonosítója.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címkék
Az erőforráshoz csatolt címkék.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Megadja a virtuális gép nevét.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
A virtuális gép méretét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmssId
A virtuális gép méretaránykészletének azonosítója

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
A virtuális gép elérhetőségi zónalistát adja meg. Az engedélyezett értékek a régió képességeitől függnek. Az engedélyezett értékek általában 1,2,3 lesznek.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.String[]

### System.Collections.Hashtable

### System.Management.Automation.SwitchParameter

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Update-AzVM](./Update-AzVM.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[Set-AzVMSourceImage](./Set-AzVMSourceImage.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)


