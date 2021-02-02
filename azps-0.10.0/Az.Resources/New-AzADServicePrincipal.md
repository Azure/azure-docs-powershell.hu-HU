---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: cd82db28fbf9902b0dedf9415290d769db3ea231
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251591"
---
# New-AzADServicePrincipal

## SYNOPSIS
Létrehoz egy új azure Active Directory szolgáltatásnévből.

## SZINTAXIS

### SimpleParameterSet (alapértelmezett)
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordPatlanParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPmirParameterSet
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
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordPmirParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyPmirParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithoutCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordPmirParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationObjectWithKeyPmirParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Létrehoz egy új azure Active Directory szolgáltatásnévből. Az alapértelmezett paraméterkészlet alapértelmezett értékeket használ a paraméterekhez, ha a felhasználó nem biztosít számukra ilyen értéket. A használt alapértelmezett értékekről az alábbi paraméterek leírásában olvashat bővebben.
Ez a parancsmag képes szerepkört rendelni a egyszerű szolgáltatásnévhez a paraméterekkel és paraméterekkel; ha egyik paraméter sem áll rendelkezésre, a rendszer nem rendel szerepkört a `Role` `Scope` szolgáltatásnévhez. A paraméterek és a közreműködői paraméterek alapértelmezett értékei a "Közreműködő" és az aktuális előfizetés ( megjegyzés: az alapértelmezett értékeket csak akkor használja a rendszer, ha a felhasználó a két paraméter egyikének értéket ad meg, a másiknak azonban `Role` `Scope` nem).
A parancsmag ezenkívül implicit módon létrehoz egy alkalmazást, és beállítja a tulajdonságait (ha az ApplicationId nincs megtéve). Az alkalmazásspecifikus paraméterek frissítéséhez használja az Set-AzADApplication parancsmagot.

> [!WARNING]
> Amikor egyszerű szolgáltatást hoz létre a **New-AzADServicePrincipal** paranccsal, a kimenet azokat a hitelesítő adatokat tartalmazza, amelyek védelmét meg kell védenie. Másik lehetőségként fontolja meg felügyelt [identitások használatát](/azure/active-directory/managed-identities-azure-resources/overview) a hitelesítő adatok használatának elkerülése érdekében.
>
> A **New-AzADServicePrincipal** alapértelmezés szerint [](/azure/role-based-access-control/built-in-roles#contributor) hozzárendeli a közreműködői szerepkört a szolgáltatásnévhez az előfizetés hatókörében. Ha csökkenteni szeretne egy feltört szolgáltatásnév kockázatát, rendeljen hozzá egy konkrétabb szerepkört, és szűkítse a hatókört egy erőforrás- vagy erőforráscsoportra. További [információt a Lépések a szerepkör-hozzárendelés](/azure/role-based-access-control/role-assignments-steps) hozzáadásához.

## PÉLDÁK

### 1. példa – Egyszerű AD szolgáltatásnév létrehozása

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

A fenti parancs létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja. Mivel nem adott meg alkalmazásazonosítót, a rendszer létrehozott egy alkalmazást a szolgáltatásnévhez. Mivel nem adott meg értéket a szolgáltatáshoz, a létrehozott egyszerű `Role` `Scope` szolgáltatásnévnek nincs engedélye.

### 2. példa: Egyszerű AD szolgáltatásnév létrehozása megadott szerepkörrel és alapértelmezett hatókörrel

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

A fenti parancs létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja. Mivel az alkalmazásazonosítót nem biztosította, a rendszer létrehozott egy alkalmazást a szolgáltatásnévhez. A szolgáltatásnév "Olvasó" engedélyekkel lett létrehozva az aktuális előfizetés fölött (mivel a paraméterhez nem lett `Scope` megadva érték).

### 3. példa: Egyszerű AD szolgáltatásnév létrehozása meghatározott hatókörű és alapértelmezett szerepkörrel

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

A fenti parancs létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja. Mivel az alkalmazásazonosítót nem biztosította, a rendszer létrehozott egy alkalmazást a szolgáltatásnévhez. A szolgáltatásnév "Közreműködői" engedélyekkel lett létrehozva (mivel a paraméterhez nem lett megadva `Role` érték) a megadott erőforráscsoport hatóköre alapján.

### 4. példa : Egyszerű AD szolgáltatásnév létrehozása meghatározott hatókörű és szerepkörű szolgáltatásnévvel

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

A fenti parancs létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja. Mivel az alkalmazásazonosítót nem biztosította, a rendszer létrehozott egy alkalmazást a szolgáltatásnévhez. A szolgáltatásnév "Olvasó" engedélyekkel lett létrehozva a megadott erőforráscsoport hatókörében.

### 5. példa : Új AD szolgáltatásnév létrehozása szerepkör-hozzárendeléssel használt alkalmazásazonosító használatával

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

Létrehoz egy új AD-szolgáltatásnév a (34a28ad2-dec4-4a41-bc3b-d22ddf90000e) azonosítójú alkalmazáshoz. Mivel nem adott meg értéket a szolgáltatáshoz, a létrehozott egyszerű `Role` `Scope` szolgáltatásnévnek nincs engedélye.

### 6. példa: Új AD szolgáltatásnév létrehozása pipázás használatával

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

A (3ede3c26-b443-4e0b-9efc-b05e68338dc3) objektumazonosítóval és a New-AzADServicePrincipal-parancsmaghoz vezető új AD-szolgáltatásnév létrehozásához szükségescsöveket használja.

## PARAMETERS

### -ApplicationId
A bérlői webhelyen egy egyszerű szolgáltatásnév egyedi alkalmazásazonosítója.
A tulajdonság létrehozása után ezt a tulajdonságot nem lehet módosítani.
Ha nincs megadva alkalmazásazonosító, létrejön egy.

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
Az az objektum, amely azt az alkalmazást képviseli, amelyhez a szolgáltatásnév létre van hozva.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue
Az "aszimmetrikus" hitelesítőadat-típus értéke.
A 64-es alapkódolt tanúsítványt képviseli.

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
A szolgáltatásnév rövid neve. Ha nincs megjelölve megjelenítendő név, ez az érték alapértelmezés szerint az "azure-powershell-MM-dd-yyyy-HH-mm-mm-mm", ahol az utótag az alkalmazás létrehozásának ideje.

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
A hitelesítő adatok használatának tényleges záró dátuma.
Az alapértelmezett záró dátum egy év a mai naptól. Az "aszimmetrikus" típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt megelőzően kell megadni.

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

### -KeyCredential
Az alkalmazáshoz társított kulcs hitelesítő adatok gyűjteménye.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Password
A szolgáltatásnévhez társítható jelszó. Ha nem ad meg jelszót, a program létrehoz egy véletlenszerű GUID azonosítót, és jelszóként fogja használni.

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordCredential
Az alkalmazáshoz társított jelszó-hitelesítő adatok gyűjteménye.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szerepkör
Az egyszerű szolgáltatásnév szerepköre a hatókörben. Ha a megadott érték meg van jelölve, de nincs megjelölve érték, akkor alapértelmezés szerint a `Scope` `Role` `Role` "Közreműködő" szerepkört használja.

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

### -Scope
Az a tartomány, amelyhez a egyszerű szolgáltatásnév rendelkezik engedélyekkel. Ha a megadott érték meg van jelölve, de nincs megjelölve érték, akkor az alapértelmezett érték az `Role` `Scope` aktuális `Scope` előfizetés.

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
Ha be van állítva, a rendszer kihagyja az egyszerű szolgáltatásnév alapértelmezett szerepkör-hozzárendelésének létrehozását.

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
A hitelesítő adatok használatának tényleges kezdő dátuma.
A kezdő dátum alapértelmezett értéke a mai nap. Az "aszimmetrikus" típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt követően kell megadni.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.Guid

### System.String

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Paraméterek: ApplicationObject (ByValue)

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]

### System.Security.SecureString

### System.DateTime

## KIMENETEK

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper

## MEGJEGYZÉSEK
Kulcsszavak: azure, Az, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[New-AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)

