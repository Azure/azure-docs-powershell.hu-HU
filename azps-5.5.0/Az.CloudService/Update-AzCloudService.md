---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: e0f9ad794f1631c5c8615480c6074f040f7fe749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145042"
---
# Update-AzCloudService

## SYNOPSIS
Felhőszolgáltatás létrehozása vagy frissítése.
Felhívjuk a figyelmét arra, hogy egyes tulajdonságokat csak a felhőbeli szolgáltatások létrehozásakor lehet beállítani.

## SZINTAXIS

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## LEÍRÁS
Felhőszolgáltatás létrehozása vagy frissítése.
Felhívjuk a figyelmét arra, hogy egyes tulajdonságokat csak a felhőbeli szolgáltatások létrehozásakor lehet beállítani.

## PÉLDÁK

### 1. példa: RDP-bővítmény hozzáadása meglévő felhőszolgáltatáshoz
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

A fenti parancskészlet hozzáad egy RDP-bővítményt a Már meglévő, ContosoCS nevű felhőszolgáltatáshoz, amely a ContosOrg nevű erőforráscsoporthoz tartozik.

### 2. példa: Az összes bővítmény eltávolítása a felhőszolgáltatásból
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

A fenti parancskészlet eltávolítja a ContosoCS nevű meglévő felhőszolgáltatás összes bővítményét, amely a ContosOrg nevű erőforráscsoporthoz tartozik.

### 3. példa: RDP-bővítmény eltávolítása a felhőszolgáltatásból
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

A fenti parancskészlet eltávolítja az RDP-bővítményt a ContosOrg nevű erőforráscsoporthoz tartozó, ContosoCS nevű meglévő felhőszolgáltatásból.

### 4. példa: Scale-Out/Scale-In szerepkörpéldányok
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

A fenti parancsok azt mutatják be, hogy miként méretarányos és méretarányos szerepkörpéldányok száma a ContosOrg nevű erőforráscsoporthoz tartozó ContosoCS nevű felhőszolgáltatásban.

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

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
A parancs futtatása aszinkron módon

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

### -Parameter
A felhőszolgáltatást ismerteti.
A konstrukcióhoz a NOTES (JEGYZETEK) szakaszban láthatja a PARAMETER tulajdonságokat, és létrehozhat egy kivonattáblát.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: A szerepkörpéldány neve.
  - `[RoleName <String>]`: A szerepkör neve.
  - `[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést. Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.
  - `[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész számértéket ad meg. A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.

PARAMÉTER: <ICloudService> A felhőszolgáltatást ismerteti.
  - `Location <String>`: Erőforrás helye.
  - `[Configuration <String>]`: A felhőszolgáltatás XML-szolgáltatáskonfigurációját (.cscfg) adja meg.
  - `[ConfigurationUrl <String>]`: Egy URL-címet ad meg, amely a blobszolgáltatás szolgáltatás-konfigurációjának helyére hivatkozik. A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet SAS-URI.         Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.
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
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: Megadja a szerepkörpéldányokra telepíthető tanúsítványok készletét.
      - `[SourceVaultId <String>]`: Erőforrás-azonosító
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: A SourceVault kulcstár-hivatkozásai, amelyek tanúsítványokat tartalmaznak.
        - `[CertificateUrl <String>]`: Ez annak a tanúsítványnak az URL-címe, amely titkosként lett feltöltve a kulcstárolóba.
  - `[PackageUrl <String>]`: Egy URL-címet ad meg, amely a szolgáltatáscsomag blobszolgáltatásban való helyére hivatkozik. A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet SAS-URI.         Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: A felhőszolgáltatás szerepkörprofilját ismerteti.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: A felhőszolgáltatás szerepkörei.
      - `[Name <String>]`: Erőforrás neve.
      - `[SkuCapacity <Int64?>]`: A felhőszolgáltatás szerepkör-példányainak számát adja meg.
      - `[SkuName <String>]`: A termékváltozat neve. MEGJEGYZÉS: Ha az új termékváltozat nem támogatott a felhőszolgáltatás által jelenleg használt hardveren, törölnie és újra létre kell hoznia a felhőszolgáltatást, vagy vissza kell lépnie a régi termékváltozatra.
      - `[SkuTier <String>]`: A felhőszolgáltatás rétegét adja meg. Lehetséges értékek: <br /><br /> **Normál** <br /><br /> **Alapszintű**
  - `[StartCloudService <Boolean?>]`: (Nem kötelező) Azt jelzi, hogy a felhőszolgáltatást közvetlenül a létrehozása után indítja-e el. Az alapértelmezett érték `true` a .         Ha hamis, a szolgáltatásmodell továbbra is telepítve van, de a kód nem fut azonnal. Ehelyett a szolgáltatás PoweredOff lesz, amíg fel nem hívja a Start menüt, és a szolgáltatás elindul. A telepített szolgáltatások még akkor is költségeket is fizetninek, ha a szolgáltatás nem működik.
  - `[Tag <ICloudServiceTags>]`: Erőforráscímkék.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: A felhőszolgáltatás frissítési módja. A szerepkörpéldányok ki vannak osztva a tartományok frissítéséhez a szolgáltatás telepítésekor. A frissítéseket manuálisan kezdeményezheti az egyes frissítési tartományokban, illetve automatikusan az összes frissítési tartományban.         Lehetséges értékek: <br /><br />**Automatikus**<br /><br />**Kézi** <br /><br />**Egyidejű**<br /><br />         Ha nincs megadva, az alapértelmezett érték az Automatikus. Ha a Kézi beállítás van beállítva, akkor a PUT UpdateDomain tartományt meg kell hívva alkalmazni a frissítést. Ha az Automatikus beállítás van beállítva, a rendszer automatikusan alkalmazza a frissítést az egyes frissítési tartományokra.

## KAPCSOLÓDÓ HIVATKOZÁSOK

