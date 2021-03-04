---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 4c6d2b3376bb5e92d048db61d68c7cfb1b94ee01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933170"
---
# Add-AzVMSshPublicKey

## SYNOPSIS
Hozzáadja az SSH nyilvános kulcsait egy virtuális géphez, amikor csak a VM-et létrehozza.

## SZINTAXIS

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzVMSshPublicKey** parancsmag hozzáadja a Linux virtuális géphez a Secure Shell (SSH) rendszeren keresztüli csatlakozáshoz használható nyilvános kulcsokat. Ez nem használható a VM létrehozása után, ha azt követően próbálja használni ezt a hibát, hogy a VM update-AzVM nélküli létrehozása után nem történik hiba, ha az Update-AzVM paranccsal használja a parancsot, a parancs hibaüzenetet kap.

## PÉLDÁK

### 1. példa: Nyilvános kulcs hozzáadása virtuális géphez
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

Az első parancs a VirtualMachine07 nevű virtuális gépet kapja meg **a Get-AzVM parancsmag** használatával.
A parancs a virtuális gépet a $VirtualMachine tárolja.
A második parancs hozzáadja a nyilvános kulcsot a VirtualMachine07 azon helyhez, ahol az Elérési út paraméter van megadva.

## PARAMETERS

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

### -KeyData
Egy nyilvános kulcs 64-es alapkódolását adja meg.
Linuxos virtuális géphez csatlakozhat az SSH használatával vagy a paraméter által megadott kulcs használatával.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Megadja egy fájl teljes elérési útját azon a virtuális gépen, ahol ez a parancsmag tárolja az SSH nyilvános kulcsot.
Ha a fájl már létezik, ez a parancsmag hozzáfűzi a kulcsot a fájlhoz.

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

### -VM
Azt a virtuális gépobjektumot adja meg, amit ez a parancsmag módosít.
Virtuális gépi objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.
A [New-AzVMConfig](./New-AzVMConfig.md) parancsmaggal virtuális gépi objektumot hozhat létre.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
