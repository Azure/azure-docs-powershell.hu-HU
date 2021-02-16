---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: f10d11dbbe98c098286a072d5882bf5d3a464d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162346"
---
# Switch-AzCloudService

## SYNOPSIS
Az IP-pontokat felcseréli két felhőszolgáltatás (kiterjesztett támogatás) terhelésegyenleg-elosztása között.

## SZINTAXIS

### CloudServiceName (alapértelmezett)
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CloudService
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## LEÍRÁS
Az IP-pontokat felcseréli két felhőszolgáltatás (kiterjesztett támogatás) terhelésegyenleg-elosztása között.

## PÉLDÁK

### 1. példa: Felhőszolgáltatás váltása név használatával
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

A fenti parancs meghívja a "BService" nevű, a felhőbeli szolgáltatáson a helyi műveletet, és végrehajtja a műveletet, amint a felhasználó megerősíti a műveletet a megerősítést kérő üzenetben.
A "BService" felcserélhető a felcserélhető felhőszolgáltatással.

### 2. példa: Felhőszolgáltatás váltása felhőalapú szolgáltatásobjektum használatával
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

A fenti parancs meghívja a "BService" nevű, a felhőbeli szolgáltatáson a helyi műveletet, és végrehajtja a műveletet, amint a felhasználó megerősíti a műveletet a megerősítést kérő üzenetben.
A "BService" felcserélhető a felcserélhető felhőszolgáltatással.

## PARAMETERS

### -AsJob
A parancs futtatása feladatként

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Async


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudService
A felhőszolgáltatás tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudServiceName


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.
Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


<CloudService>CLOUDSERVICE: 
  - `Location <String>`: Erőforrás helye.
  - `[Configuration <String>]`: A felhőszolgáltatás XML-szolgáltatáskonfigurációját (.cscfg) adja meg.
  - `[ConfigurationUrl <String>]`: Olyan URL-címet ad meg, amely a blobszolgáltatás szolgáltatás-konfigurációjának helyére hivatkozik. A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet SAS-URI.         Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: Egy felhőbeli szolgáltatásbővítmény-profilt ismertet.
    - `[Extension <IExtension[]>]`: A felhőszolgáltatás bővítményei.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: Explicit módon megadhatja, hogy a platform képes-e automatikusan frissíteni a TypeHandlerVersiont a nagyobb alverziókra, amikor elérhetővé válnak.
      - `[ForceUpdateTag <String>]`: Címkével kényszerítheti a megadott nyilvános és védett beállítások alkalmazását.         A címkeérték módosítása lehetővé teszi a bővítmény újrafuttatését a nyilvános vagy védett beállítások módosítása nélkül.         Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit a kezelő továbbra is alkalmazza.         Ha sem a forceUpdateTag, sem a nyilvános vagy védett beállítások egyike sem változik, a bővítmény a szerepkörpéldányba áramolna ugyanazokkal a sorszámmal, és a kezelő implementációja függ attól, hogy újra futtatja-e vagy sem.
      - `[Name <String>]`: A bővítmény neve.
      - `[ProtectedSetting <String>]`: A bővítmény védett beállításai, amelyek titkosítottak, mielőtt elkülde volna a szerepkörpéldánynak.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: A bővítménykezelő közzétevője neve.
      - `[RolesAppliedTo <String[]>]`: A bővítmény alkalmazásához választható szerepkörök listája. Ha a tulajdonság nincs megadva, vagy a "*" érték meg van adva, a bővítmény a felhőszolgáltatás összes szerepkörében érvényes lesz.
      - `[Setting <String>]`: A bővítmény nyilvános beállításai. JSON-bővítményekben ez a bővítmény JSON-beállításai. XML-bővítmény (például RDP) esetén ez a bővítmény XML-beállítása.
      - `[SourceVaultId <String>]`: Erőforrás-azonosító
      - `[Type <String>]`: A bővítmény típusát határozza meg.
      - `[TypeHandlerVersion <String>]`: A bővítmény verzióját adja meg. A bővítmény verzióját határozza meg. Ha ez az elem nincs megadva, vagy csillag (*) használja értékként, akkor a bővítmény legújabb verzióját használja a program. Ha az értéket egy főverzió számával, a csillagot pedig alverziószámmal (X.) adja meg, akkor a megadott főverzió legújabb alverziója van kiválasztva. Ha a főverzió és az alverzió száma meg van adva (X.Y), akkor az adott bővítményverzió van kiválasztva. Ha egy verzió meg van adva, a szerepkörpéldányon automatikus frissítés történik.
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`: A felhőszolgáltatás hálózati profilja.
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: A felhőszolgáltatás terheléselosztási konfigurációjának listája.
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: AZ IP-címek listája
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`: A felhőszolgáltatás által hivatkozott privát IP-cím.
        - `[PublicIPAddressId <String>]`: Erőforrás-azonosító
        - `[SubnetId <String>]`: Erőforrás-azonosító
      - `[Name <String>]`: Erőforrás neve
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`: Erőforrás-azonosító
  - `[OSProfile <ICloudServiceOSProfile>]`: A felhőszolgáltatás operációs rendszerprofilját ismerteti.
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: A szerepkörpéldányokra telepíthető tanúsítványok halmazát adja meg.
      - `[SourceVaultId <String>]`: Erőforrás-azonosító
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: A SourceVault kulcstár-hivatkozásai, amelyek tanúsítványokat tartalmaznak.
        - `[CertificateUrl <String>]`: Ez annak a tanúsítványnak az URL-címe, amely titkosként lett feltöltve a kulcstárolóba.
  - `[PackageUrl <String>]`: Egy URL-címet ad meg, amely a szolgáltatáscsomag helyére hivatkozik a Blob szolgáltatásban. A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet sas-uri.         Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: A felhőszolgáltatás szerepkörprofilját ismerteti.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: A felhőszolgáltatás szerepkörei.
      - `[Name <String>]`: Erőforrás neve.
      - `[SkuCapacity <Int64?>]`: A felhőszolgáltatás szerepkörpéldányainak számát adja meg.
      - `[SkuName <String>]`: A termékváltozat neve. MEGJEGYZÉS: Ha az új termékváltozat nem támogatott a felhőszolgáltatás által jelenleg használt hardveren, törölnie és újra létre kell hoznia a felhőszolgáltatást, vagy vissza kell lépnie a régi termékváltozatra.
      - `[SkuTier <String>]`: A felhőszolgáltatás rétegét adja meg. Lehetséges értékek: <br /><br /> **Normál** <br /><br /> **Alapszintű**
  - `[StartCloudService <Boolean?>]`: (Nem kötelező) Azt jelzi, hogy a felhőszolgáltatást a létrehozása után azonnal el kell-e kezdeni. Az alapértelmezett érték `true` a .         Ha hamis, a szolgáltatásmodell továbbra is telepítve van, de a kód nem fut azonnal. Ehelyett a szolgáltatás PoweredOff lesz, amíg fel nem hívja a Start menüt, és a szolgáltatás elindul. Az üzembe helyezett szolgáltatások akkor is költségeket fizetninek, ha a szolgáltatás nem működik.
  - `[Tag <ICloudServiceTags>]`: Erőforráscímkék.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: A felhőszolgáltatás frissítési módja. A szerepkörpéldányok ki vannak osztva a tartományok frissítéséhez a szolgáltatás telepítésekor. A frissítéseket manuálisan kezdeményezheti az egyes frissítési tartományokban, illetve automatikusan az összes frissítési tartományban.         Lehetséges értékek: <br /><br />**Automatikus**<br /><br />**Kézi** <br /><br />**Egyidejű**<br /><br />         Ha nincs megadva, az alapértelmezett érték az Automatikus. Ha a Kézi beállítás van beállítva, akkor a PUT UpdateDomain tartományt meg kell hívva alkalmazni a frissítést. Ha az Automatikus beállítás van beállítva, a rendszer automatikusan alkalmazza a frissítést az egyes frissítési tartományokra.

## KAPCSOLÓDÓ HIVATKOZÁSOK

