---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015996"
---
# New-AzureRemoteAppCollection

## Áttekintés
Azure RemoteApp-gyűjteményt hoz létre.

## SZINTAXISA

### AllParameterSets (alapértelmezett)
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AzureVNet
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureRemoteAppCollection** parancsmag létrehoz egy Azure RemoteApp-gyűjteményt.

## Példák

### Példa 1: gyűjtemény létrehozása
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

A parancs Azure RemoteApp-gyűjteményt hoz létre.

### 2. példa: gyűjtemény létrehozása hitelesítő adatokkal
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

A parancs a **Get-hitelesítőadat** parancsmag hitelesítő adataival hoz létre Azure RemoteApp-gyűjteményt.

## PARAMÉTEREK

### -CollectionName
Az Azure RemoteApp-gyűjtemény nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hitelesítő adatok
Megadja egy olyan szolgáltatásfiók hitelesítő adatait, amely engedéllyel rendelkezik az Azure RemoteApp kiszolgálókhoz való csatlakozáshoz a tartományához.
Ha **PSCredential** objektumot szeretne beolvasni, használja a **Get-hitelesítőadat** parancsmagot.

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomRdpProperty
Az egyéni RDP-tulajdonságokat adja meg, amelyek a meghajtó-átirányítás és az egyéb beállítások konfigurálására használhatók.
További információt az [RDP-beállítások a Windows Server Remote Desktop Services szolgáltatáshoz](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) című témakörben talál `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  

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

### -Leírás
Az objektum rövid leírását adja meg.

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

### -DnsServers
A DNS-kiszolgálók IPv4-címeinek pontosvesszővel elválasztott listáját adja meg.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tartomány
Annak az Active Directory tartományi szolgáltatások tartománynak a neve, amelyhez csatlakozni szeretne a távoli asztali munkamenetgazda-kiszolgálókhoz.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageName
Az Azure RemoteApp-sablon képének nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
A gyűjtemény Azure-régióját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrganizationalUnit
Annak a szervezeti egységnek (OU) a nevét adja meg, amelyhez csatlakozni szeretne a TERMINÁLKISZOLGÁLÓhoz, például OU = MyOu, DC = MyDomain, DC = ParentDomain, DC = com.
Az OU-és egyenáramú attribútumoknak nagybetűs kell lenniük.
A program a gyűjtemény létrehozása után nem módosíthatja a szervezeti egységet.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Terv
Az Azure RemoteApp-gyűjtemény csomagját adja meg, amely meghatározhatja a használati korlátozásokat.
Az elérhető csomagok megtekintéséhez használja a **Get-AzureRemoteAppPlan** .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
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

### -ResourceType
A gyűjtemény erőforrás-típusát adja meg.
A paraméter elfogadható értékei a következők: app vagy asztali.

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetName
Megadja annak a virtuális hálózatnak a nevét, amellyel az Azure RemoteApp gyűjteményt létre szeretné hozni.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNetName
Egy Azure RemoteApp virtuális hálózat nevét adja meg.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppPlan](./Get-AzureRemoteAppPlan.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


