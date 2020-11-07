---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: aaf1162cdeeb007a680a3e9de325cbd10fadef94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844745"
---
# Add-AzVMNetworkInterface

## Áttekintés
Hálózati felületet ad hozzá egy virtuális géphez.

## SZINTAXISA

### GetNicFromNicId (alapértelmezett)
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetNicFromNicObject
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Add-AzVMNetworkInterface** parancsmag hálózati felületet ad hozzá egy virtuális géphez.
Hozzáadhat egy felületet a virtuális gép létrehozásakor, vagy hozzáadhat egyet egy meglévő virtuális géphez.

## Példák

### 1. példa: hálózati felület felvétele új virtuális gépre
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.
A parancs nevet és méretet rendel a virtuális géphez.

A második parancs hozzáadja a hálózati felületet a $VirtualMachineban tárolt virtuális géphez.

### 2. példa: hálózati felület felvétele meglévő virtuális géphez
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Az első parancs a **Get-AzVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.
A parancs a virtuális gépet a $VirtualMachine változóban tárolja.

A második parancs hozzáadja a hálózati felületet a $VirtualMachineban tárolt virtuális géphez.

A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
A virtuális géphez hozzáadni kívánt hálózati interfész AZONOSÍTÓját adja meg.
A [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) parancsmaggal hálózati felületet lehet beolvasni.

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkInterface
A hálózati felületet adja meg.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Elsődleges
Jelzi, hogy ez a parancsmag hozzáadja a hálózati felületet az elsődleges felülethez.

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Annak a helyi virtuális gép-objektumnak a megadása, amelyhez hálózati felületet szeretne adni.
Virtuális gép létrehozásához használja a **New-AzVMConfig** parancsmagot.
Ha egy meglévő virtuális gépet szeretne beolvasni, használja a **Get-AzVM** parancsmagot.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Network. models. PSNetworkInterface]
A ' NetworkInterface ' paraméter a ' System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Network. models. PSNetworkInterface] ' típus értékét veszi fel a csővezetékről.

### PSVirtualMachine
A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzVMConfig](./New-AzVMConfig.md)

[Get-AzVM](./Get-AzVM.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)
