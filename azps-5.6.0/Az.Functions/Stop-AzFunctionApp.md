---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/stop-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Stop-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Stop-AzFunctionApp.md
ms.openlocfilehash: 2b8717c3387bd8e8ac6cd0fe1cdd37f957c176ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929034"
---
# Stop-AzFunctionApp

## SYNOPSIS
Leállít egy függvényalkalmazást.

## SZINTAXIS

### StopByName (alapértelmezett)
```
Stop-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Stop-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## LEÍRÁS
Leállít egy függvényalkalmazást.

## PÉLDÁK

### 1. példa: Függvényalkalmazás leállítása név szerint.
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Stop-AzFunctionApp -Force
```

Ez a parancs név szerint leállítja a függvényalkalmazást.

### 2. példa: Függvényalkalmazás leállítása név szerint.
```powershell
PS C:\> Stop-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Ez a parancs név szerint leállítja a függvényalkalmazásokat.

## PARAMETERS

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

### -Force
Kényszeríti a parancsmagot a függvényalkalmazás leállításának kényszerítésére megerősítés kérése nélkül.

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

### -InputObject
Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A függvényalkalmazás neve.

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Eredménye igaz, ha a parancs sikeres.

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

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az Azure-előfizetés azonosítója.

```yaml
Type: System.String
Parameter Sets: StopByName
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

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <ISite> 
  - `Location <String>`: Erőforrás helye.
  - `CloningInfoSourceWebAppId <String>`: ARM forrásalkalmazás erőforrás-azonosítóját. Az alkalmazáserőforrás-azonosító a következő űrlapból áll: /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}, production slots and /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}.
  - `[Kind <String>]`: Az erőforrás fajtája.
  - `[Tag <IResourceTags>]`: Erőforráscímkék.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.
  - `[ClientAffinityEnabled <Boolean?>]`: <code>true</code> az ügyfélkapcsolat engedélyezéséhez; a munkamenet-affinitás cookie-k küldésének megállítása, amelyek az ügyfélalkalmazások kérését ugyanannak a munkamenetnek a példányára <code>false</code> irányítják. Az alapértelmezett érték <code>true</code> a .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> az ügyfél tanúsítvány-hitelesítésének (TLS közös hitelesítés) engedélyezéséhez; ellenkező esetben <code>false</code> . Az alapértelmezett érték <code>false</code> a .
  - `[ClientCertExclusionPath <String>]`: Ügyfél tanúsítványának hitelesítése vesszővel elválasztott kivétel elérési útjai
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Az alkalmazásbeállítási felülbírálások a klónozott appok esetén. Ha meg van adva, ezek a beállítások felülbírálják a forrásalkalmazásból klónozott beállításokat. Ellenkező esetben a forrásalkalmazás alkalmazásbeállítása megmarad.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> az egyéni állomásnevek klónozása a forrásalkalmazásból, ellenkező esetben <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> a forrásalkalmazásból a forrásvezérlők klónozása; egyéb esetben <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> konfigurálhatja a terheléselosztást a forrás- és célalkalmazáshoz.
  - `[CloningInfoCorrelationId <String>]`: A cloning művelet korrelációs azonosítója. Ez az azonosító több cloning műveletet hoz létre ugyanannak a pillanatfelvételnek a végrehajtásához.
  - `[CloningInfoHostingEnvironment <String>]`: App szolgáltatási környezet.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> a célalkalmazás felülírása; egyéb esetben <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: A forrásalkalmazás helye, pl. Nyugat-Usa vagy Észak-Európa
  - `[CloningInfoTrafficManagerProfileId <String>]`: ARM a Traffic Manager-profil erőforrás-azonosítóját, ha létezik ilyen. A Traffic Manager erőforrás-azonosítója a következő űrlapból áll: /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: A létrehozni szükséges Traffic Manager-profil neve. Erre csak akkor van szükség, ha a Traffic Manager-profil még nem létezik.
  - `[Config <ISiteConfig>]`: Az app konfigurációja.
    - `IsPushEnabled <Boolean>`: Jelölőt kap vagy állít be, amely jelzi, hogy a leküldéses végpont engedélyezve van-e.
    - `[ActionMinProcessExecutionTime <String>]`: A művelet végrehajtása előtt a folyamat minimálisan szükséges ideje
    - `[ActionType <AutoHealActionType?>]`: Előre meghatározott teendő.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> ha a Mindig be van kapcsolva, egyébként <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: Az API-definíció URL-címe.
    - `[ApiManagementConfigId <String>]`: APIM-Api azonosító.
    - `[AppCommandLine <String>]`: Elindítandó alkalmazás parancssora.
    - `[AppSetting <INameValuePair[]>]`: Alkalmazásbeállítások.
      - `[Name <String>]`: Párnév.
      - `[Value <String>]`: Érték párosítása.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> ha az Automatikus lejátszás funkció be van kapcsolva; ellenkező esetben <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Az automatikus cserehely neve.
    - `[ConnectionString <IConnStringInfo[]>]`: Kapcsolati karakterláncok.
      - `[ConnectionString <String>]`: Kapcsolati karakterlánc értéke.
      - `[Name <String>]`: A kapcsolati karakterlánc neve.
      - `[Type <ConnectionStringType?>]`: Az adatbázis típusa.
    - `[CorAllowedOrigin <String[]>]`: Beállítja vagy beállítja azon forráslistát, amely lehetővé teszi a több forrásból való hívásokat (például: http://example.com:12345) . Az összes engedélyezése a "*" szóra van állítva.
    - `[CorSupportCredentials <Boolean?>]`: Beállítja vagy beállítja, hogy engedélyezettek-e a hitelesítő adatokkal megadott CORS-kérések. További         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         részleteket itt talál.
    - `[CustomActionExe <String>]`: Futtatható végrehajtható fájl.
    - `[CustomActionParameter <String>]`: A végrehajtható fájl paraméterei.
    - `[DefaultDocument <String[]>]`: Alapértelmezett dokumentumok.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> ha a részletes hibanaplózás engedélyezve van; ellenkező esetben <code>false</code> .
    - `[DocumentRoot <String>]`: Dokumentumgyök.
    - `[DynamicTagsJson <String>]`: Olyan JSON-karakterláncot kap vagy állít be, amely a leküldéses regisztrációs végponton található felhasználói igények alapján kiértékelésre kerül a dinamikus címkék listáját tartalmazza.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: A felfutási szabályok listája.
      - `[ActionHostName <String>]`: Annak a tárolóhelynek a állomásneve, amelybe a forgalmat átirányítja a rendszer, ha úgy dönt. Például: myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Egyéni döntési algoritmus is meg lehet adni a TiPCallback webhelybővítményben, amely URL-címet is meg lehet adni. Lásd a TiPCallback webhelybővítményét az állványhoz és a szerződésekhez.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Az ReroutePercentage átértékelhető intervallumát adja meg percben.
      - `[ChangeStep <Double?>]`: Automatikus felfutási helyzetben ez a lépés a hozzáadás/eltávolítás, amíg el nem éri a <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> vagy         <code>MaxReroutePercentage</code> . A webhely metrikákat a .\nCustom döntési algoritmusban megadott N percenként ellenőrzi a <code>ChangeIntervalInMinutes</code> TiPCallback webhelybővítmény, amely az URL-címet meg lehet <code>ChangeDecisionCallbackUrl</code> adni.
      - `[MaxReroutePercentage <Double?>]`: Azt a felső határot adja meg, amely alatt a ReroutePercentage meg fog maradni.
      - `[MinReroutePercentage <Double?>]`: Azt az alsó határértéket adja meg, amely fölött az ReroutePercentage meg fog maradni.
      - `[Name <String>]`: Az útválasztási szabály neve. Az ajánlott név a kísérlet során a forgalmat tároló tárolóhelyre mutat.
      - `[ReroutePercentage <Double?>]`: Azon forgalom százalékos aránya, amelyre a rendszer átirányítja <code>ActionHostName</code> a forgalmat.
    - `[FtpsState <FtpsState?>]`: FTP/FTPS szolgáltatás állapota
    - `[HandlerMapping <IHandlerMapping[]>]`: Kezelői leképezések.
      - `[Argument <String>]`: A parancsprogram-processzornak át kell adandó parancssori argumentumokat.
      - `[Extension <String>]`: Az ilyen kiterjesztésű kérelmeket a megadott FastCGI alkalmazással kezeljük.
      - `[ScriptProcessor <String>]`: A FastCGI alkalmazás abszolút elérési útja.
    - `[HealthCheckPath <String>]`: Állapot-ellenőrzés útvonala
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: Konfigurál egy webhelyet, amely engedélyezi az ügyfeleknek a http2.0-s kapcsolaton keresztüli csatlakozást
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> ha a HTTP-naplózás engedélyezve van; egyébként <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: A fő IP-biztonsági korlátozásai.
      - `[Action <String>]`: Hozzáférés engedélyezése vagy elutasítása ehhez az IP-tartományhoz.
      - `[Description <String>]`: IP-korlátozási szabály leírása.
      - `[IPAddress <String>]`: Az IP-cím, amelyre a biztonsági korlátozás érvényes.         Ez lehet csak ipv4-cím (kötelező AlhálózatiMaszk tulajdonság) vagy CIDR-cím, például ipv4/mask (leading bit match). CIDR esetén az Alhálózatimaszk tulajdonságot nem kell megadni.
      - `[Name <String>]`: IP-korlátozási szabály neve.
      - `[Priority <Int32?>]`: Az IP-korlátozási szabály prioritása.
      - `[SubnetMask <String>]`: Az IP-címek tartományának alhálózati maszkja, amelyekre a korlátozás érvényes.
      - `[SubnetTrafficTag <Int32?>]`: (belső) Alhálózati adatforgalom címkéje
      - `[Tag <IPFilterTag?>]`: Meghatározza, hogy mire fogja használni ezt az IP-szűrőt. Ez a proxyk IP-szűrésének támogatását támogatja.
      - `[VnetSubnetResourceId <String>]`: Virtuális hálózati erőforrás-azonosító
      - `[VnetTrafficTag <Int32?>]`: (belső) Vnet-adatforgalom címkéje
    - `[JavaContainer <String>]`: Java tároló.
    - `[JavaContainerVersion <String>]`: Java-tároló verziója.
    - `[JavaVersion <String>]`: Java verzió.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Maximális lemezméret-használat MB-ban.
    - `[LimitMaxMemoryInMb <Int64?>]`: Maximális memóriahasználat MB-ban.
    - `[LimitMaxPercentageCpu <Double?>]`: Maximális engedélyezett processzorhasználati százalékérték.
    - `[LinuxFxVersion <String>]`: Linux app keretrendszer és verzió
    - `[LoadBalancing <SiteLoadBalancing?>]`: Webhely terheléselosztása.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> a helyi MySQL engedélyezéséhez; egyéb esetben <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: HTTP-naplók címtárméretkorlátja.
    - `[MachineKeyDecryption <String>]`: A visszafejtési algoritmus.
    - `[MachineKeyDecryptionKey <String>]`: Visszafejtési kulcs.
    - `[MachineKeyValidation <String>]`: Gépkulcs érvényesítése.
    - `[MachineKeyValidationKey <String>]`: Érvényesítési kulcs.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Felügyelt folyamat mód.
    - `[ManagedServiceIdentityId <Int32?>]`: Felügyelt szolgáltatás identitásazonosítója
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Az SSL-kérelmekhez minimálisan szükséges TLS-verzió konfigurálása
    - `[NetFrameworkVersion <String>]`: .NET-keretrendszer verziója.
    - `[NodeVersion <String>]`: A Node.js.
    - `[NumberOfWorker <Int32?>]`: Dolgozók száma.
    - `[PhpVersion <String>]`: A PHP verziója.
    - `[PowerShellVersion <String>]`: A PowerShell verziója.
    - `[PreWarmedInstanceCount <Int32?>]`: Awarmed példányok száma.         Ez a beállítás csak a fogyasztási és rugalmas csomagokra vonatkozik
    - `[PublishingUsername <String>]`: Közzétételi felhasználónév.
    - `[PushKind <String>]`: Az erőforrás fajtája.
    - `[PythonVersion <String>]`: A Python verziója.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> ha a távoli hibakeresés engedélyezve van; egyéb esetben <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Távoli hibakeresési verzió.
    - `[RequestCount <Int32?>]`: Kérések száma.
    - `[RequestTimeInterval <String>]`: Időintervallum.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> ha a kéréskövetés engedélyezve van; ellenkező esetben <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: A lejárati idő nyomon követésének kérése.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: AZ SCM IP-biztonsági korlátozásai.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-biztonsági korlátozások az scm fő használatára.
    - `[ScmType <ScmType?>]`: SCM típus.
    - `[SlowRequestCount <Int32?>]`: Kérések száma.
    - `[SlowRequestTimeInterval <String>]`: Időintervallum.
    - `[SlowRequestTimeTaken <String>]`: A szükséges idő.
    - `[TagWhitelistJson <String>]`: A leküldéses regisztrációs végpont által használható címkék listáját tartalmazó JSON-karakterláncot állít be vagy állít be.
    - `[TagsRequiringAuth <String>]`: A leküldéses regisztrációs végponton felhasználói hitelesítést igénylő címkék listáját tartalmazó JSON-karakterláncot kap vagy állít be.         A címkék alfanumerikus karakterekből állhatnak, és a következő karakterekből állhatnak: '_', '@', '#', '.', ':', '-'.         Az érvényesítést a PushRequestHandlerben kell elvégezni.
    - `[TracingOption <String>]`: Nyomkövetési beállítások.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Egy magánjellegű bájton alapuló szabály.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Egy állapotkódon alapuló szabály.
      - `[Count <Int32?>]`: Kérések száma.
      - `[Status <Int32?>]`: HTTP-állapotkód.
      - `[SubStatus <Int32?>]`: Alállapot kérése.
      - `[TimeInterval <String>]`: Időintervallum.
      - `[Win32Status <Int32?>]`: Win32 hibakód.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> a 32 bites munkavégző folyamathoz; ellenkező esetben <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Virtuális alkalmazások.
      - `[PhysicalPath <String>]`: Fizikai elérési út.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> ha az előbetöltés engedélyezve van; ellenkező esetben <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Virtuális könyvtárak virtuális alkalmazáshoz.
        - `[PhysicalPath <String>]`: Fizikai elérési út.
        - `[VirtualPath <String>]`: Virtuális alkalmazás elérési útja.
      - `[VirtualPath <String>]`: Virtuális elérési út.
    - `[VnetName <String>]`: Virtuális hálózat neve.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> ha a WebSocket engedélyezve van, egyébként <code>false</code> .
    - `[WindowsFxVersion <String>]`: Xenon app keretrendszer és verzió
    - `[XManagedServiceIdentityId <Int32?>]`: Explicit felügyelt szolgáltatás identitásazonosítója
  - `[ContainerSize <Int32?>]`: A függvénytároló mérete.
  - `[DailyMemoryTimeQuota <Int32?>]`: Maximális napi memóriaidő-kvóta (csak dinamikus alkalmazások esetén alkalmazható).
  - `[Enabled <Boolean?>]`: <code>true</code> ha az alkalmazás engedélyezve van; ellenkező esetben <code>false</code> . Ennek az értéknek a hamis értékre állításával letiltja az appot (offline állapotba vált).
  - `[HostNameSslState <IHostNameSslState[]>]`: Az SSL-állomásnevek SSL-államai az alkalmazás állomásnevéhez szükséges SSL-kötések kezelésére használhatók.
    - `[HostType <HostType?>]`: Azt jelzi, hogy az állomásnév normál vagy tárházi állomásnév-e.
    - `[Name <String>]`: Állomásnév.
    - `[SslState <SslState?>]`: SSL-típus.
    - `[Thumbprint <String>]`: SSL-tanúsítvány thumbprint.
    - `[ToUpdate <Boolean?>]`: A meglévő <code>true</code> állomásnév frissítésére van beállítva.
    - `[VirtualIP <String>]`: Az IP-alapú SSL engedélyezése esetén az állomásnévhez hozzárendelt virtuális IP-cím.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> az app nyilvános állomásnevének letiltásához; ellenkező esetben <code>false</code> .          Ha <code>true</code> az app csak API-kezelési folyamaton keresztül érhető el.
  - `[HostingEnvironmentProfileId <String>]`: Az app szolgáltatási környezetének erőforrás-azonosítója.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: úgy konfigurál egy webhelyet, hogy csak a https-kérelmeket fogadja el. A http-kérelmek problémáinak átirányítása
  - `[HyperV <Boolean?>]`: Hyper-V védőfal.
  - `[IdentityType <ManagedServiceIdentityType?>]`: A felügyelt szolgáltatás identitásának típusa.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Az erőforráshoz társított felhasználó által hozzárendelt identitások listája. A felhasználói identitásszótár kulcshivatkozásai ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.
  - `[IsXenon <Boolean?>]`: Elavult: Hyper-V védőfal.
  - `[RedundancyMode <RedundancyMode?>]`: Webhely redundancia üzemmódja
  - `[Reserved <Boolean?>]`: <code>true</code> ha foglalt; egyéb esetben <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> leállítja az SCM (KUDU) webhelyet az alkalmazás leállításakor; ellenkező esetben <code>false</code> . Az alapértelmezett érték <code>false</code> a .
  - `[ServerFarmId <String>]`: A társított App Service-csomag erőforrás-azonosítója, formátuma: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## KAPCSOLÓDÓ HIVATKOZÁSOK

