---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015844"
---
# Update-AzureApplicationGateway

## Áttekintés
Az alkalmazás-átjáró frissítése

## SZINTAXISA

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az **Update-AzureApplicationGateway** parancsmag egy meglévő alkalmazás-átjárót frissít.

## Példák

### 1. példa: az alkalmazás átjárójának módosítása a neve alapján
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

Az első parancs leállítja a ApplicationGateway06 nevű alkalmazás-átjárót.
A virtuális hálózat vagy alhálózatok módosítása előtt le kell állítani egy alkalmazás-átjárót.

A második parancs módosítja a ApplicationGateway06 nevű alkalmazás-átjáró virtuális alhálózatát és alhálózatait.

### 2. példa: az alkalmazás-átjáró további tulajdonságainak módosítása
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

Ez a parancs módosítja a ApplicationGateway06 nevű alkalmazás-átjáró példányának számát, az átjáró méretét és leírását.
Ez a parancs nem módosítja az Application Gateway virtuális hálózatát vagy alhálózatait.
Ezért a parancs futtatása előtt nem kell leállítania az Application Gatewayt.

### 3. példa: az alkalmazás-átjárók módosítása a csővezeték használatával
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

Az első parancs a **Get-AzureApplicationGateway** parancsmag használatával kapja meg a ApplicationGateway06 nevű alkalmazás-átjárót.
A parancs a $ApplicationGateway változóban tárolja.

A második parancs a **GatewaySize** tulajdonságot a Medium értékre osztja.

A végleges parancs átadja a frissített $ApplicationGateway az aktuális parancsmagnak.

## PARAMÉTEREK

### -Leírás
Azt a leírást adja meg, amelyet a parancsmag az alkalmazás-átjáróhoz rendel.

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

### -GatewaySize
Azt adja meg, hogy a parancsmag milyen méretet rendel az alkalmazás-átjáróhoz.
Az érvényes értékek a következők:

- Kisvállalati
- Közepes
- Nagy

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

### -InstanceCount
Azt adja meg, hogy a parancsmag hány példányt rendel az alkalmazás-átjáróhoz.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Annak az alkalmazási átjárónak a nevét adja meg, amely a parancsmag által frissült.

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

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### -Alhálózatok
Itt adhatja meg azt az alhálózatokat, amelyben ez a parancsmag telepíti az alkalmazás-átjárót.

Nem frissíthetők az alhálózatok, miközben az alkalmazás-átjáró fut.
Az alkalmazás-átjáró leállításához használja az Stop-AzureApplicationGateway parancsmagot.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VnetName
Annak a virtuális hálózatnak a meghatározása, amelyben ez a parancsmag telepíti az alkalmazás-átjárót.

A virtuális hálózatokat nem frissítheti, miközben az alkalmazás-átjáró fut.
Az alkalmazás-átjáró leállításához használja a **stop-AzureApplicationGateway**.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[Új – AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Start-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Stop-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)
