---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e3f246a77d4adb489f660a56d3843520d3a327ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844738"
---
# Add-AzVMSshPublicKey

## Áttekintés
Hozzáadja az SSH-hoz szükséges nyilvános kulcsokat egy virtuális géphez.

## SZINTAXISA

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Add-AzVMSshPublicKey** parancsmag hozzáadja azokat a nyilvános kulcsokat, amelyekkel a biztonságos rendszerhéjon (SSH) keresztül csatlakozhat a virtuális géphez.

## Példák

### 1. példa: nyilvános kulcs hozzáadása virtuális géphez
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

Az első parancs a **Get-AzVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.
A parancs a virtuális gépet a $VirtualMachine változóban tárolja.

A második parancs hozzáadja a nyilvános kulcsot a VirtualMachine07 azon helyéhez, amelyen a Path paraméter van meghatározva.

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

### -Adatforrások
A nyilvános kulcs 64-kódolását adja meg.
A virtuális gépeket az SSH segítségével vagy a paraméter által megadott kulcs használatával is elérheti.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path (elérési út)
A fájl teljes elérési útját adja meg a virtuális gépen, ahol ez a parancsmag az SSH-s nyilvános kulcsot tárolja.
Ha a fájl már létezik, ez a parancsmag hozzáfűzi a kulcsot a fájlhoz.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.
Virtuális gép objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.
A [New-AzVMConfig](./New-AzVMConfig.md) parancsmaggal létrehozhatja a virtuális gép objektumát.

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

### PSVirtualMachine
A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Új – AzVMConfig](./New-AzVMConfig.md)
