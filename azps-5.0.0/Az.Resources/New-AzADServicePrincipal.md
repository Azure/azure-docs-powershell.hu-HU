---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/05/2020
ms.locfileid: "94303968"
---
# New-AzADServicePrincipal

## Áttekintés
Új Azure Active Directory-szolgáltató létrehozása.

## SZINTAXISA

### SimpleParameterSet (alapértelmezett)

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithoutCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DisplayNameWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás

Új Azure Active Directory-szolgáltató létrehozása. Az alapértelmezett paraméterérték a paraméterek alapértelmezett értékeit használja, ha azok nincsenek megadva. Az alapértelmezett értékekről további információt az egyes paraméterek leírása című témakörben találhat. Ezzel a parancsmaggal a **szerepkör** és a **hatókör** paraméterrel társíthat szerepkört a szolgáltatóhoz. Ha mindkettő nincs kihagyva, a közreműködői szerepkör a szolgáltatóhoz van társítva. A **szerepkör** és a **hatókör** paramétereinek alapértelmezett értékei az aktuális előfizetéshez **közreműködők** . A parancsmag létrehoz egy alkalmazást, és beállítja a tulajdonságait, ha nincs megadva ApplicationId. Az alkalmazásspecifikus paraméterek frissítéséhez használja az [Update-AzADApplication](./update-azadapplication.md) parancsmagot.

> [!WARNING]
> Ha a **New-AzADServicePrincipal** parancs segítségével hoz létre egy egyszerű szolgáltatásnevet, a kimenet tartalmazza a védelemmel ellátott hitelesítő adatokat is. Ügyeljen arra, hogy ne szerepeljenek ezek a hitelesítő adatok a kódban, vagy ellenőrizze a hitelesítő adatokat a forrás vezérlőben. A [felügyelt identitások](/azure/active-directory/managed-identities-azure-resources/overview) használata helyett érdemes lehet használni a hitelesítő adatok használatát.
>
> A **New-AzADServicePrincipal** alapértelmezés szerint a [munkatárs](/azure/role-based-access-control/built-in-roles#contributor) szerepkört rendeli hozzá az előfizetési tartományhoz. Ha csökkenteni szeretné a kiegyezéssel járó megbízó kockázatát, rendeljen hozzá egy specifikusabb szerepkört, és szűkítse a hatókört egy erőforrás vagy erőforrás csoportba. További információért tekintse át [a szerepkör-hozzárendelés hozzáadásának lépéseit](/azure/role-based-access-control/role-assignments-steps) .

## Példák

### Példa 1: Simple AD Service Principal Creation

Az alábbi példa létrehoz egy AD-szolgáltatót, amely a nem meghatározott paraméterek alapértelmezett értékeit használja. Mivel egy alkalmazás-azonosító nincs megadva, létrejön egy alkalmazás a szolgáltatási megbízó számára. Mivel a **szerepkörhöz** vagy a **hatókörhöz** nincs megadva érték, a létrehozta a szolgáltató a jelenlegi előfizetés **közreműködői** szerepkörét kapja.

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### 2. példa: egyszerű AD-szolgáltatás egyszerű létrehozása megadott szerepkörrel és alapértelmezett hatókörrel

Az alábbi példa létrehoz egy AD-szolgáltatót, amely a nem meghatározott paraméterek alapértelmezett értékeit használja. Mivel az alkalmazás-azonosító nincs megadva, létrejön egy alkalmazás a szolgáltatási megbízó számára. A Service Principal a jelenlegi előfizetéshez tartozó **olvasói** engedélyekkel jön létre, mivel a **hatókör** paraméter nem rendelkezik értékkel.

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### 3. példa: egyszerű AD-szolgáltatás – egyszerű létrehozás meghatározott hatókör és alapértelmezett szerepkörrel

Az alábbi példa létrehoz egy AD-szolgáltatót, amely a nem meghatározott paraméterek alapértelmezett értékeit használja. Mivel az alkalmazás-azonosító nincs megadva, létrejön egy alkalmazás a szolgáltatási megbízó számára. A szervizszerződés a megadott erőforráscsoport-tartomány **közreműködői** engedélyeivel jön létre, mivel a **role** paraméterhez nincs megadva érték.

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Példa 4: egyszerű AD-szolgáltatás egyszerű létrehozása megadott hatókörrel és szerepkörrel

Az alábbi példa létrehoz egy AD-szolgáltatót, amely a nem meghatározott paraméterek alapértelmezett értékeit használja. Mivel az alkalmazás-azonosító nincs megadva, létrejön egy alkalmazás a szolgáltatási megbízó számára. A Service Principal a megadott erőforráscsoport-hatókörhöz tartozó **olvasói** engedélyekkel jön létre.

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Példa 5: új AD Service-szolgáltató létrehozása alkalmazásspecifikus AZONOSÍTÓval szerepkör-hozzárendeléssel

Az alábbi példa létrehoz egy új AD-szolgáltatót az alkalmazáshoz a ' 00000000-0000-0000-0000-000000000000 ' AZONOSÍTÓJÚ alkalmazással. Mivel a **szerepkörhöz** vagy a **hatókörhöz** nincs megadva érték, a létrehozta a szolgáltató a jelenlegi előfizetés **közreműködői** szerepkörét kapja.

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### 6. példa: új AD-szolgáltató létrehozása csővezetékek használatával

Az alábbi példa beolvassa az "3ede3c26-b443-4e0b-9efc-b05e68338dc3" AZONOSÍTÓJÚ alkalmazást a [Get-AzADApplication](./get-azadapplication.md) parancsmag használatával. Az eredmény az, hogy a `New-AzADServicePrincipal` parancsmag segítségével új ad-szolgáltatót hoz létre ahhoz az alkalmazáshoz.

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### 7. példa: új AD Service Principal létrehozása a DisplayName és a jelszó hitelesítő adataival

Az alábbi példa új alkalmazást hoz létre a **ServicePrincipalName** név és a **StrongPassworld! 23** jelszóval. Ezt a szolgáltatást a létrehozta alkalmazás alapján hozza létre. A program hozzáadja a kezdési és a befejezési dátumot a jelszó-hitelesítő adatokhoz.

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### 8. példa: új AD-szolgáltató létrehozása a DisplayName és az egyszerű kulcs hitelesítő adataival

Az alábbi példa egy új alkalmazást hoz létre a name **ServicePrincipalName** és egy tanúsítvány **$CERT**. Létrehozza a szolgáltatásnevet a létrehozott alkalmazás alapján. A befejezési dátum hozzáadódik a legfontosabb hitelesítő adatokhoz.

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## PARAMÉTEREK

### -ApplicationId

Egy szolgáltató egyedi alkalmazásspecifikus azonosítója bérlői fiókban. Miután létrehozta ezt a tulajdonságot, nem módosítható. Ha egy meglévő alkalmazáshoz egy alkalmazás-azonosító nincs megadva, létrejön egy alkalmazás.

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationObject

Annak az alkalmazásnak az objektuma, amelybe a szolgáltatásnevet létrehozta.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue

Az aszimmetrikus hitelesítőadat-típus értéke. A Base64 kódolású tanúsítványt képviseli.

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile

Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName

A szolgáltatás megbízójának rövid neve. Ha a megjelenítendő név nem látható, akkor ez az érték alapértelmezés szerint az **Azure-PowerShell-hh-nn-éééé-hh-hh-hh-mm-mm** , ahol az utótag az alkalmazás létrehozásának időpontja.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate

A hitelesítő adatok használatának tényleges befejezési dátuma. Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.
Aszimmetrikus típusú hitelesítő adatok esetén ezt be kell állítani a X509 tanúsítvány érvényességi dátumának be vagy azt megelőzőre.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hitelesítő adatok

Az alkalmazáshoz társított legfontosabb hitelesítő adatok gyűjteménye.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordCredential

Az alkalmazáshoz társított jelszó-hitelesítő adatok gyűjteménye.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Role (szerepkör)

Annak a szerepkörnek a szerepe, amelyet a szolgáltató a hatókör felett tartalmaz. Ha nincs megadva érték, akkor a **szerepkör** alapértelmezés szerint a **közreműködői** szerepkört kapja.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope (hatókör)

Az a hatókör, amelyre a szolgáltatónak van engedélye. Ha nincs megadva érték, akkor az alapértelmezett hatókör az aktuális előfizetéshez **tartozik** .

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAssignment

Ha be van állítva, ugorjon az alapértelmezett szerepkör-hozzárendelés létrehozásához a szolgáltatónál.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate

A hitelesítő adatok használatának tényleges kezdési dátuma. A kezdő dátum alapértelmezett értéke ma. Aszimmetrikus típusú hitelesítő adatok esetében ezt be kell állítani a X509 tanúsítvány érvényességi dátumának be vagy mögé.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
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

Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)című témakörben talál.
## BEMENETEK

### System. GUID

### System. String

### Microsoft. Azure. Command. ActiveDirectory. PSADApplication

### Microsoft. Azure. Command. ActiveDirectory. PSADPasswordCredential []

### Microsoft. Azure. Command. ActiveDirectory. PSADKeyCredential []

### System. DateTime

## KIMENETEK

### Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal

### Microsoft. Azure. Command. Resources. modellek. Authorization. PSADServicePrincipalWrapper

## MEGJEGYZI

Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[Új – AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[Új – AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)