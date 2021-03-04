---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: d875ad9af0ebe864f9d396fed44961a5d48f38c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930586"
---
# Get-AzCloudServicePublicIPAddress

## SYNOPSIS
Szerezze be egy felhőszolgáltatás nyilvános IP-címét.

## SZINTAXIS

### CloudServiceName (alapértelmezett)
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### CloudService
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## LEÍRÁS
Szerezze be egy felhőszolgáltatás nyilvános IP-címét.

## PÉLDÁK

### 1. példa: Példányszintű nyilvános IP-címek lekérte egy adott felhőbeli szolgáltatásnévhez.
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

Egy adott felhőszolgáltatás nevének példányszintű nyilvános IP-címét kapja meg.

### 2. példa: Példányszintű nyilvános IP-címek lekérte egy adott felhőszolgáltatás-objektumhoz.
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

Egy adott felhőszolgáltatás-objektum példányszintű nyilvános IP-címeit kapja meg.

## PARAMETERS

### -CloudService
CloudService-példány.
A felhőszolgáltatás tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK című szakaszban található.

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
CloudServiceName.

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

### -ResourceGroupName
ResourceGroupName.

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
Előfizetés.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


<CloudService>CLOUDSERVICE: CloudService instance.
  - `Location <String>`: Erőforrás helye.
  - `[Configuration <String>]`: A felhőszolgáltatás XML-szolgáltatáskonfigurációját (.cscfg) adja meg.
  - `[ConfigurationUrl <String>]`: Olyan URL-címet ad meg, amely a blobszolgáltatás szolgáltatás-konfigurációjának helyére hivatkozik. A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet sas-uri.         Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: Egy felhőbeli szolgáltatásbővítmény-profilt ismertet.
    - `[Extension <IExtension[]>]`: A felhőszolgáltatás bővítményei.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: Kifejezetten meg kell adnia, hogy a platform képes-e automatikusan frissíteni a TypeHandlerVersiont a nagyobb alverziókra, amikor elérhetővé válnak.
      - `[ForceUpdateTag <String>]`: Címkével kényszerítheti a megadott nyilvános és védett beállítások alkalmazását.         A címkeérték módosítása lehetővé teszi a bővítmény újrafuttatését a nyilvános vagy védett beállítások módosítása nélkül.         Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit a kezelő továbbra is alkalmazza.         Ha sem a forceUpdateTag, sem a nyilvános vagy védett beállítások egyike sem változik, a bővítmény a szerepkörpéldányba áramolna ugyanazokkal a sorszámmal, és a kezelő implementációja függ attól, hogy újra futtatja-e vagy sem.
      - `[Name <String>]`: A bővítmény neve.
      - `[ProtectedSetting <String>]`: A bővítmény védett beállításai, amelyek titkosítottak, mielőtt elkülde volna a szerepkörpéldánynak.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: A bővítménykezelő közzétevője neve.
      - `[RolesAppliedTo <String[]>]`: A bővítmény alkalmazásához választható szerepkörök listája. Ha a tulajdonság nincs megadva vagy a "*" érték meg van adva, a bővítmény a felhőszolgáltatás összes szerepkörében érvényes lesz.
      - `[Setting <String>]`: A bővítmény nyilvános beállításai. JSON-bővítményekben ez a bővítmény JSON-beállításai. XML-bővítmény (például RDP) esetén ez a bővítmény XML-beállítása.
      - `[SourceVaultId <String>]`: Erőforrás-azonosító
      - `[Type <String>]`: A bővítmény típusát határozza meg.
      - `[TypeHandlerVersion <String>]`: A bővítmény verzióját adja meg. A bővítmény verzióját határozza meg. Ha ez az elem nincs megadva, vagy csillag (*) használja értékként, akkor a bővítmény legújabb verzióját használja a program. Ha az értéket egy főverzió számával, a csillagot pedig alverziószámmal (X.) adja meg, akkor a megadott főverzió legújabb alverziója van kiválasztva. Ha főverziószámot és alverziószámot ad meg (X.Y), az adott bővítményverzió van kiválasztva. Ha egy verzió meg van adva, a szerepkörpéldányon automatikus frissítés történik.
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
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: Megadja a szerepkörpéldányokra telepíthető tanúsítványok készletét.
      - `[SourceVaultId <String>]`: Erőforrás-azonosító
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: A SourceVault kulcstár-hivatkozásai, amelyek tanúsítványokat tartalmaznak.
        - `[CertificateUrl <String>]`: Ez annak a tanúsítványnak az URL-címe, amely titkosként lett feltöltve a kulcstárolóba.
  - `[PackageUrl <String>]`: Egy URL-címet ad meg, amely a szolgáltatáscsomag blobszolgáltatásban való helyére hivatkozik. A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet sas-uri.         Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: A felhőszolgáltatás szerepkörprofilját ismerteti.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: A felhőszolgáltatás szerepkörei.
      - `[Name <String>]`: Erőforrás neve.
      - `[SkuCapacity <Int64?>]`: A felhőszolgáltatás szerepkör-példányainak számát adja meg.
      - `[SkuName <String>]`: A termékváltozat neve. MEGJEGYZÉS: Ha az új termékváltozat nem támogatott a felhőszolgáltatás által jelenleg használt hardveren, törölnie és újra létre kell hoznia a felhőszolgáltatást, vagy vissza kell lépnie a régi termékváltozatra.
      - `[SkuTier <String>]`: A felhőszolgáltatás rétegét adja meg. Lehetséges értékek: <br /><br /> **Normál** <br /><br /> **Alapszintű**
  - `[StartCloudService <Boolean?>]`: (Nem kötelező) Azt jelzi, hogy a felhőszolgáltatást a létrehozása után azonnal el kell-e kezdeni. Az alapértelmezett érték `true` a .         Ha hamis, a szolgáltatásmodell továbbra is telepítve van, de a kód nem fut azonnal. Ehelyett a szolgáltatás PoweredOff lesz, amíg fel nem hívja a Start menüt, és a szolgáltatás elindul. A telepített szolgáltatások még akkor is költségeket is fizetninek, ha a szolgáltatás nem működik.
  - `[Tag <ICloudServiceTags>]`: Erőforráscímkék.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: A felhőszolgáltatás frissítési módja. A szerepkörpéldányok ki vannak osztva a tartományok frissítéséhez a szolgáltatás telepítésekor. A frissítéseket manuálisan kezdeményezheti az egyes frissítési tartományokban, illetve automatikusan az összes frissítési tartományban.         Lehetséges értékek: <br /><br />**Automatikus**<br /><br />**Kézi** <br /><br />**Egyidejű**<br /><br />         Ha nincs megadva, az alapértelmezett érték az Automatikus. Ha a Kézi beállítás van beállítva, akkor a PUT UpdateDomain tartományt meg kell hívva alkalmazni a frissítést. Ha az Automatikus beállítás van beállítva, a rendszer automatikusan alkalmazza a frissítést az egyes frissítési tartományokra.

## KAPCSOLÓDÓ HIVATKOZÁSOK

