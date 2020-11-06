---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: 24c97e73728dab656a1d9fe3283e4eba6aae4ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492572"
---
# Add-AzureRmVMSshPublicKey

## Áttekintés
Hozzáadja az SSH-hoz szükséges nyilvános kulcsokat egy virtuális géphez.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Add-AzureRmVMSshPublicKey** parancsmag hozzáadja azokat a nyilvános kulcsokat, amelyekkel a biztonságos rendszerhéjon (SSH) keresztül csatlakozhat a virtuális géphez.

## Példák

### 1. példa: nyilvános kulcs hozzáadása virtuális géphez
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

Az első parancs a **Get-AzureRmVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.
A parancs a virtuális gépet a $VirtualMachine változóban tárolja.

A második parancs hozzáadja a nyilvános kulcsot a VirtualMachine07 azon helyéhez, amelyen a Path paraméter van meghatározva.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
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
Type: System.String
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
Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.
Virtuális gép objektum beszerzéséhez használja a [Get-AzureRmVM](./Get-AzureRmVM.md) parancsmagot.
A [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) parancsmaggal létrehozhatja a virtuális gép objektumát.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Új – AzureRmVMConfig](./New-AzureRmVMConfig.md)
