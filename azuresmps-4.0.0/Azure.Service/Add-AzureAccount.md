---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016396"
---
# Add-AzureAccount

## Áttekintés
Hozzáadja az Azure-fiókot a Windows PowerShellhez.

## SZINTAXISA

### Felhasználó (alapértelmezett)
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServicePrincipal
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Add-AzureAccount** parancsmag az Azure-fiókját és a hozzájuk tartozó előfizetéseket is elérhetővé teszi a Windows PowerShellben.
Ez olyan, mint az Azure-fiókjába való bejelentkezés a Windows PowerShellben.
Ha ki szeretne jelentkezni a fiókból, használja a **Remove-AzureAccount** parancsmagot.

A **AzureAccount** letölti az Azure-fiókjával kapcsolatos információkat, és egy előfizetési adatfájlba menti a központi felhasználói profilban.
Egy hozzáférési tokent is kap, amely lehetővé teszi, hogy a Windows PowerShell hozzáférhessen az Azure-fiókjához az Ön nevében.
Ha befejeződött a parancs, kezelheti az Azure-fiókját a Windows PowerShell segítségével.

Az Azure-fiók kétféle módon érhető el a Windows PowerShellben.
Használhatja az **Add-AzureAccount** parancsmagot, amely az Azure Active Directoryt (Azure ad) hitelesítő (Azure ad) hozzáférési jogkivonatokat, illetve egy felügyeleti tanúsítványt használó **import-AzurePublishSettingsFile-** ot használ.
A használati módszert a következő témakörben találhatja meg [: útmutató: csatlakozás az előfizetéshez](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .

A **AzureAccount** futtatásakor egy interaktív ablak jelenik meg, amely az Azure-fiókba való bejelentkezést kéri.
Ez a bejelentkezés addig érvényes, amíg lejár a hozzáférési jogkivonat.
Ha lejár, a fiókjához való hozzáférést igénylő parancsmagokra kéri a **AzureAccount** ismételt futtatását.

Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

## Példák

### 1. példa: fiók hozzáadása
```
PS C:\> Add-AzureAccount
```

Ez a parancs Azure-fiókot ad hozzá a Windows PowerShellhez.
Amikor futtatja a parancsot, a Windows megjelenik a fiók felhasználónevének és jelszavának megkereséséhez.

### 2. példa: alternatív előfizetési adatfájl használata
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

Ez a parancs a **SubscriptionDataFile** paramétert használva közvetlen **AzureAccount hoz létre** a fiókadatok tárolásához az alapértelmezett fájl helyett az C:\Testing\SDF.xml-fájlban.

## PARAMÉTEREK

### -Hitelesítő adatok
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Környezet
Azure-környezetet ad meg.

Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.
A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.
További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### -ServicePrincipal
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bérlő
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ehhez a parancsmaghoz nem tud bemeneti pipát

## KIMENETEK

### Nincs
Ez a parancsmag nem ad vissza semmilyen eredményt.

## MEGJEGYZI
* Az **Add-AzureAccount** (és az Azure ad Authentication Method) az **import-AzurePublishSettings** (és a kezelési tanúsítvány módszerét) veszi figyelembe. Ha a **AzureAccount** még egyszer használja a fiókjában, az Azure ad Authentication módszert használja, és a kezelési tanúsítványt figyelmen kívül hagyja. Ha el szeretné távolítani az Azure AD tokent, és vissza szeretné állítani a felügyeleti tanúsítvány módszert, használja a **Remove-AzureAccount** parancsmagot. További információért írja be a következőt: **Get-Help Remove-AzureAccount**.
* A hiba "a hitelesítő adatai lejártak". Kérjük, hogy jelentkezzen be újra a Add-AzureAccount használatával. " jelzi, hogy az Access-jogkivonat lejárt, és a Windows PowerShell nem fér hozzá az Azure-fiókjához. Ha vissza szeretné állítani a fiókjához való hozzáférést, futtassa újra a **AzureAccount** .
* Az Azure PowerShell-fiók és az előfizetés-parancsmagok az előfizetési adatfájlból jutnak hozzá az adataihoz, nem az élő Azure-fiókból. Ha a Windows PowerShellen kívüli fiókját vagy előfizetéseit (például az Azure felügyeleti portál segítségével) módosítja, az előfizetési adatfájl frissítéséhez futtassa ismét a **Add-AzureAccount** .

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Importálás – AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Get-AzureAccount](./Get-AzureAccount.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


