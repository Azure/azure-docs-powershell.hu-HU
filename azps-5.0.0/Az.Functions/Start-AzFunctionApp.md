---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/start-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Start-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Start-AzFunctionApp.md
ms.openlocfilehash: c5c5fd14f61be2526c62335b9f6ed33719846a12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185408"
---
# Start-AzFunctionApp

## Áttekintés
Elindítja a függvény alkalmazást.

## SZINTAXISA

### StartByName (alapértelmezett)
```
Start-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Start-AzFunctionApp -InputObject <ISite> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## Leírás
Elindítja a függvény alkalmazást.

## Példák

### Példa 1: a Function app beszerzése név alapján, és elindíthatja.
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Start-AzFunctionApp
```

Ez a parancs a függvény alkalmazását név szerint kapja meg, és elindítja.

### 2. példa: a Function app elindítása név szerint.
```powershell
PS C:\> Start-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName
```

Ezzel a paranccsal elindíthatja a függvény alkalmazását név szerint.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.

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

### -Name (név)
A függvény app neve.

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Igaz érték visszaadása, ha a parancs sikeres.

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
Parameter Sets: StartByName
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
Parameter Sets: StartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. ISite

## KIMENETEK

### System. Boolean

## MEGJEGYZI

ALIASOK

KOMPLEX PARAMÉTEREK TULAJDONSÁGAI

Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.


INPUTOBJECT <ISite> : 
  - `Location <String>`: Erőforrás helye.
  - `CloningInfoSourceWebAppId <String>`: A forrás app ARM erőforrás-azonosítója. Az App-erőforrás-azonosító a gyártási résidők és a/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} más bővítőhelyekhez való/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}.
  - `[Kind <String>]`: Az erőforrás típusa.
  - `[Tag <IResourceTags>]`: Erőforrás-címkék.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.
  - `[ClientAffinityEnabled <Boolean?>]`: az <code>true</code> ügyfél-affinitás engedélyezéséhez: a <code>false</code> munkamenet-affinitást tartalmazó cookie-k küldésének leállítása, amely az ügyfélalkalmazás ugyanazon példányra irányuló kérelme. Alapértelmezés: <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> az ügyféltanúsítvány-alapú hitelesítés engedélyezéséhez (TLS-alapú kölcsönös hitelesítés); egyéb esetben <code>false</code> . Alapértelmezés: <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: ügyféltanúsítvány-alapú hitelesítés vesszővel elválasztott kizárási útvonalak
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Az alkalmazás beállításai felülbírálják a klónozott alkalmazást. Ha meg van adva, ezek a beállítások felülbírálják a forrás alkalmazásból klónozott beállításokat. Egyéb esetben a Source App alkalmazás beállításai megőrződnek.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> Egyéni állomásnevek klónozása a Source app-ból; egyéb esetben <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> a forrás-irányítás klónozása forrás alkalmazásból; egyéb esetben <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> a forrás-és a rendeltetési app terheléselosztásának beállítása.
  - `[CloningInfoCorrelationId <String>]`: A klónozási művelet korrelációs azonosítója. Ez az azonosító több klónozási műveletet köt össze, hogy ugyanazt a pillanatképet használja.
  - `[CloningInfoHostingEnvironment <String>]`: Alkalmazás-szolgáltatási környezet.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> a cél-app felülírása; ellenkező esetben <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: A Source app: Nyugat-amerikai vagy észak-európai verzió helye
  - `[CloningInfoTrafficManagerProfileId <String>]`: A használni kívánt forgalomirányító-profil ARM erőforrás-azonosítója. A Traffic Manager erőforrás-AZONOSÍTÓja az űrlap/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: A létrehozandó Traffic Manager-profil neve. Erre csak akkor van szükség, ha a Traffic Manager profilja még nem létezik.
  - `[Config <ISiteConfig>]`: Az alkalmazás konfigurációja.
    - `IsPushEnabled <Boolean>`: Megadhatja vagy beállíthatja, hogy a leküldéses végpont engedélyezve van-e.
    - `[ActionMinProcessExecutionTime <String>]`: A folyamat végrehajtásának minimális ideje a művelet megkezdése előtt
    - `[ActionType <AutoHealActionType?>]`: Előre definiált műveletek.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> Ha a mindig engedélyezve van, egyéb esetben <code>false</code> :
    - `[ApiDefinitionUrl <String>]`: Az API-definíció URL-címe.
    - `[ApiManagementConfigId <String>]`: APIM-Api azonosító.
    - `[AppCommandLine <String>]`: Az App parancssora az indításhoz.
    - `[AppSetting <INameValuePair[]>]`: Alkalmazásbeállítások.
      - `[Name <String>]`: Páros név.
      - `[Value <String>]`: Pair érték.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> Ha az automatikus gyógyulás engedélyezve van, egyéb esetben <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Automatikus swap-tárolóhely neve.
    - `[ConnectionString <IConnStringInfo[]>]`: Kapcsolódási karakterláncok.
      - `[ConnectionString <String>]`: Kapcsolati karakterlánc értéke.
      - `[Name <String>]`: A kapcsolati karakterlánc neve.
      - `[Type <ConnectionStringType?>]`: Adatbázis típusa.
    - `[CorAllowedOrigin <String[]>]`: Beilleszti vagy beállítja az eredeti hívások (például: http://example.com:12345) . Az összes engedélyezéséhez használja a "*" billentyűt.
    - `[CorSupportCredentials <Boolean?>]`: Beolvassa vagy beállítja, hogy a hitelesítő adatokkal rendelkező CORS-kérelmek engedélyezve vannak-e. https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsTovábbi részletekért tekintse meg.
    - `[CustomActionExe <String>]`: Végrehajtható fájl futtatása.
    - `[CustomActionParameter <String>]`: A végrehajtható fájl paramétereinek paraméterei.
    - `[DefaultDocument <String[]>]`: Alapértelmezett dokumentumok.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Ha a részletes hibák naplózása engedélyezve van, egyéb esetben <code>false</code> .
    - `[DocumentRoot <String>]`: Dokumentum gyökerét.
    - `[DynamicTagsJson <String>]`: A leküldéses regisztráció végpontjában a felhasználói jogcímekről kiértékelt dinamikus címkék listáját tartalmazó JSON karakterláncot kap vagy állít be.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: A Ramp-up szabályok listája.
      - `[ActionHostName <String>]`: Annak a bővítőhelynek a neve, amelybe a forgalmat irányítja át. Pl. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Egyéni döntési algoritmust is megadhat a TiPCallback webhelyen, mely URL-címet lehet megadni. Lásd: a TiPCallback a szerelő és a szerződések számára.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: A ReroutePercentage újraértékeléséhez a percekben megadott intervallumot adja meg.
      - `[ChangeStep <Double?>]`: Az automatikus Ramp up forgatókönyvben ez a lépés a Hozzáadás/Eltávolítás, <code>ReroutePercentage</code> amíg el nem éri a \n <code>MinReroutePercentage</code> vagy a         <code>MaxReroutePercentage</code> . A webhely metrikáit a .\NCustom-döntési algoritmusban megadott minden N percben ellenőrizni <code>ChangeIntervalInMinutes</code> lehet a TiPCallback webhelyen, mely URL-címet lehet megadni <code>ChangeDecisionCallbackUrl</code> .
      - `[MaxReroutePercentage <Double?>]`: Itt adhatja meg azt a felső határt, amely alatt a ReroutePercentage marad.
      - `[MinReroutePercentage <Double?>]`: Itt adhatja meg azt az alsó határértéket, amely fölött a ReroutePercentage marad.
      - `[Name <String>]`: A műveletterv szabály neve. Az ajánlott név arra a pontra mutat, amely a kísérletben szereplő forgalmat fogja fogadni.
      - `[ReroutePercentage <Double?>]`: Az átirányítani kívánt forgalom százalékos aránya <code>ActionHostName</code> .
    - `[FtpsState <FtpsState?>]`: FTP/FTPS szolgáltatás
    - `[HandlerMapping <IHandlerMapping[]>]`: Kezelői megfeleltetések.
      - `[Argument <String>]`: A parancsfájl-feldolgozó által átadandó parancssori argumentumok.
      - `[Extension <String>]`: A kiterjesztéssel elvégezhető kérelmeket a megadott FastCGI-alkalmazás kezeli.
      - `[ScriptProcessor <String>]`: A FastCGI-alkalmazás abszolút elérési útja.
    - `[HealthCheckPath <String>]`: Állapot-ellenőrzés elérési útja
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: webhelyek beállítása, hogy az ügyfelek a http 2.0-s verziós kapcsolatot engedélyezzék
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Ha a http-naplózás engedélyezve van, egyéb esetben <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-biztonsági korlátozások a Main esetében.
      - `[Action <String>]`: Engedélyezze vagy tiltsa le az IP-címtartomány elérését.
      - `[Description <String>]`: IP-korlátozási szabály leírása.
      - `[IPAddress <String>]`: IP-cím: a biztonsági korlátozás érvényes.         Lehet egy egyszerű IPv4-cím (kötelező SubnetMask tulajdonság) vagy a CIDR-jelölés (például IPv4/Mask (vezető bit)) formájában. Az CIDR esetében a SubnetMask tulajdonság nem adható meg.
      - `[Name <String>]`: IP-korlátozási szabály neve.
      - `[Priority <Int32?>]`: Az IP-korlátozási szabály prioritása.
      - `[SubnetMask <String>]`: Alhálózati maszk az IP-címek tartományához: a korlátozás érvényes.
      - `[SubnetTrafficTag <Int32?>]`: (belső) alhálózat-forgalmi címke
      - `[Tag <IPFilterTag?>]`: Itt határozhatja meg, hogy melyik IP-szűrőt fogja használni a rendszer. Ez a szolgáltatás támogatja az IP-szűrést a proxykban.
      - `[VnetSubnetResourceId <String>]`: Virtuális hálózati erőforrás-azonosító
      - `[VnetTrafficTag <Int32?>]`: (belső) vnet forgalmi címke
    - `[JavaContainer <String>]`: Java tároló.
    - `[JavaContainerVersion <String>]`: Java tároló verziója.
    - `[JavaVersion <String>]`: Java-verzió.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Megengedett maximális lemezhasználat MEGABÁJTban.
    - `[LimitMaxMemoryInMb <Int64?>]`: Az engedélyezett memória maximális kihasználtsága MEGABÁJTban.
    - `[LimitMaxPercentageCpu <Double?>]`: Megengedett maximális CPU-használati százalék
    - `[LinuxFxVersion <String>]`: Linux app-keretrendszer és verzió
    - `[LoadBalancing <SiteLoadBalancing?>]`: A webhely terheléselosztása.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> a helyi MySQL engedélyezéséhez; egyéb esetben <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: HTTP-naplók: a könyvtár mérete korlátozva
    - `[MachineKeyDecryption <String>]`: A visszafejtéshez használt algoritmus.
    - `[MachineKeyDecryptionKey <String>]`: Visszafejtési kulcs.
    - `[MachineKeyValidation <String>]`: MachineKey érvényesítése.
    - `[MachineKeyValidationKey <String>]`: Érvényesítési kulcs.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Felügyelt csővezeték üzemmód.
    - `[ManagedServiceIdentityId <Int32?>]`: Felügyelt szolgáltatás azonosítóját azonosító
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: az SSL-kérésekhez szükséges TLS minimális verziójának beállítása
    - `[NetFrameworkVersion <String>]`: .NET-keretrendszer verziója.
    - `[NodeVersion <String>]`: Node.js verziója.
    - `[NumberOfWorker <Int32?>]`: A munkavállalók száma.
    - `[PhpVersion <String>]`: A PHP verziója.
    - `[PowerShellVersion <String>]`: A PowerShell verziója.
    - `[PreWarmedInstanceCount <Int32?>]`: Az előmelegített példányok száma.         Ez a beállítás csak a fogyasztási és a rugalmas csomagokra érvényes.
    - `[PublishingUsername <String>]`: Közzétételi Felhasználónév.
    - `[PushKind <String>]`: Az erőforrás típusa.
    - `[PythonVersion <String>]`: A Python verziója.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Ha a távoli hibakeresés engedélyezve van, egyéb esetben <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Távoli hibakeresési verzió.
    - `[RequestCount <Int32?>]`: Kérések száma.
    - `[RequestTimeInterval <String>]`: Időintervallum.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> Ha a kérés nyomkövetése engedélyezve van, egyéb esetben <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: A nyomkövetés lejárati időpontjának kérése
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-biztonsági korlátozások az SCM-hez.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Az SCM-re vonatkozó IP-biztonsági korlátozások fő.
    - `[ScmType <ScmType?>]`: SCM típus.
    - `[SlowRequestCount <Int32?>]`: Kérések száma.
    - `[SlowRequestTimeInterval <String>]`: Időintervallum.
    - `[SlowRequestTimeTaken <String>]`: Idő.
    - `[TagWhitelistJson <String>]`: A leküldéses regisztrációs végpont által használt címkék listáját tartalmazó JSON-karakterláncot kap vagy állít be.
    - `[TagsRequiringAuth <String>]`: A leküldéses regisztráció végpontján a felhasználó által használt hitelesítést igénylő kódok listáját tartalmazó, JSON-karakterláncot kap vagy állít be.         A címkék tartalmazhatnak alfanumerikus karaktereket, a következőt: "_", "@", "#", ".", ":", "-".         Az érvényesítést a PushRequestHandler kell végrehajtani.
    - `[TracingOption <String>]`: Nyomkövetési beállítások.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Privát bájton alapuló szabály.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A szabályok az állapotkódok alapján.
      - `[Count <Int32?>]`: Kérések száma.
      - `[Status <Int32?>]`: HTTP-állapotkód.
      - `[SubStatus <Int32?>]`: Alállapot kérése
      - `[TimeInterval <String>]`: Időintervallum.
      - `[Win32Status <Int32?>]`: Win32-hibakód.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32 bites munkavégző folyamat használata; egyéb esetben <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Virtuális alkalmazások.
      - `[PhysicalPath <String>]`: Fizikai elérési út.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> Ha engedélyezve van az előzetes bekapcsolás, egyéb esetben <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Virtuális könyvtárak a virtuális alkalmazáshoz.
        - `[PhysicalPath <String>]`: Fizikai elérési út.
        - `[VirtualPath <String>]`: A virtuális alkalmazás elérési útja.
      - `[VirtualPath <String>]`: Virtuális elérési út.
    - `[VnetName <String>]`: Virtuális hálózati név.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> Ha a Webszoftvercsatorna engedélyezve van, egyéb esetben <code>false</code> .
    - `[WindowsFxVersion <String>]`: Xenon alkalmazás kerete és verziója
    - `[XManagedServiceIdentityId <Int32?>]`: Explicit felügyelt szolgáltatás-azonosító
  - `[ContainerSize <Int32?>]`: A függvény tárolójának mérete.
  - `[DailyMemoryTimeQuota <Int32?>]`: Maximálisan engedélyezett napi memória-időkvóta (csak dinamikus alkalmazásokban alkalmazható).
  - `[Enabled <Boolean?>]`: <code>true</code> Ha az alkalmazás engedélyezve van, egyéb esetben <code>false</code> . Az érték hamis értékre állítása letiltja az alkalmazást (az alkalmazást kapcsolat nélkül jeleníti meg).
  - `[HostNameSslState <IHostNameSslState[]>]`: A gépnév SSL-Államok az App állomásnevek SSL-kötéseinek kezelésére szolgálnak.
    - `[HostType <HostType?>]`: Azt jelzi, hogy a gépnév normál vagy tárházas állomásnév-e.
    - `[Name <String>]`Hostname.
    - `[SslState <SslState?>]`: SSL típusa.
    - `[Thumbprint <String>]`: SSL-tanúsítvány ujjlenyomata.
    - `[ToUpdate <Boolean?>]`: A <code>true</code> meglévő állomásnév frissítésének beállítása.
    - `[VirtualIP <String>]`: A gépnévhez rendelt virtuális IP-cím, ha az IP-alapú SSL engedélyezve van.
  - `[HostNamesDisabled <Boolean?>]`: az <code>true</code> app nyilvános állomásnevek letiltása; ellenkező esetben <code>false</code> .          Ha <code>true</code> az App csak API-kezelési folyamaton keresztül érhető el.
  - `[HostingEnvironmentProfileId <String>]`: Az alkalmazás szolgáltatási környezetének erőforrás-azonosítója.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: egy webhely beállítása csak HTTPS-kérelmek elfogadásához. Http-kérelmek átirányításának problémái
  - `[HyperV <Boolean?>]`: Hyper-V homokozó.
  - `[IdentityType <ManagedServiceIdentityType?>]`: A felügyelt szolgáltatás identitásának típusa.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Az erőforráshoz társított felhasználó által kiosztott identitások listája. A felhasználó személyazonosságát ismertető szótár fő hivatkozásai az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}"-ban az űrlapon lesznek.
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.
  - `[IsXenon <Boolean?>]`: Elavult: Hyper-V homokozó.
  - `[RedundancyMode <RedundancyMode?>]`: Webhely-redundancia mód
  - `[Reserved <Boolean?>]`: <code>true</code> Ha fenn van foglalva, egyéb esetben <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: az <code>true</code> SCM-(KUDU-) webhely leállítása, ha az alkalmazás le van állítva; ellenkező esetben <code>false</code> . Az alapértelmezett érték <code>false</code> .
  - `[ServerFarmId <String>]`: A társított app Service Plan ("/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}") erőforrás-azonosítója.

## KAPCSOLÓDÓ HIVATKOZÁSOK

