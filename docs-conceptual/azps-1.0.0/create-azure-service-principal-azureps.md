---
title: Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával
description: Megtudhatja, hogyan hozhat létre szolgáltatásneveket appjához vagy szolgáltatásához az Azure PowerShell használatával.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594955"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával

Ha az appját vagy szolgáltatását az Azure PowerShell-lel szeretné kezelni, egy Azure Active Directory (AAD) szolgáltatásnév alatt, és nem a saját hitelesítő adataival érdemes futtatnia. Ez a cikk végigvezeti a szolgáltatásnevek Azure PowerShell-lel való létrehozásának folyamatán.

## <a name="what-is-a-service-principal"></a>Mi az a szolgáltatásnév?

Az Azure-beli szolgáltatásnév egy biztonsági identitás, amellyel a felhasználó által létrehozott appok, szolgáltatások és automatizálási eszközök elérnek adott Azure-erőforrásokat. A szolgáltatásnevekhez a feladataikhoz kapcsolódó speciális engedélyek vannak rendelve, így jobban szabályozható a biztonság. Ez abban tér el az általános identitásoktól, hogy azok általában bármely módosítás elvégzésére jogosultak.

## <a name="verify-your-own-permission-level"></a>Saját jogosultsági szint ellenőrzése

Először is megfelelő jogosultságokkal kell rendelkeznie mind az Azure Active Directoryban, mind az Azure-előfizetésén. Létre kell tudnia hozni alkalmazást az Active Directoryban, és ki kell tudnia osztani szerepköröket a szolgáltatásnévnek.

A legegyszerűbben a portálon ellenőrizheti, hogy rendelkezik-e megfelelő jogosultságokkal. Lásd [Szükséges jogosultságok ellenőrzése a portálon](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Szolgáltatásnév létrehozása az app számára

Miután bejelentkezett Azure-fiókjába, létrehozhatja a szolgáltatásnevet. A következő módszerek egyikének rendelkezésre kell állnia az üzembe helyezett app azonosításához:

* Az üzembe helyezett alkalmazás egyedi neve – a következő példákban ez a MyDemoWebApp
* Az alkalmazásazonosító, az üzembe helyezett alkalmazáshoz, szolgáltatáshoz vagy objektumhoz társított egyedi GUID

### <a name="get-information-about-your-application"></a>Az alkalmazás adatainak lekérése

Az alkalmazással kapcsolatos információkat a `Get-AzADApplication` parancsmaggal kérheti le.

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>Szolgáltatásnév létrehozása az alkalmazás számára

A szolgáltatásnév a `New-AzADServicePrincipal` parancsmaggal hozható létre.

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

Itt használhatja közvetlenül a `$servicePrincipal.Secret` tulajdonságot a `Connect-AzAccount` argumentumaként (lásd a „Bejelentkezés a szolgáltatásnévvel” című részt) vagy átalakíthatja ezt a `SecureString` típusú sztringet egyszerű szöveges sztringgé:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a>Bejelentkezés a szolgáltatásnévvel

Most már bejelentkezhet az alkalmazás új szolgáltatásnevével a megadott `appId` és a létrehozott `password`  
használatával. Szüksége lesz a szolgáltatásnévhez tartozó bérlőazonosítóra is. A bérlőazonosító akkor jelenik meg, ha a saját hitelesítő adataival bejelentkezik az Azure-ba. Szolgáltatásnévvel való bejelentkezéshez használja a következő parancsokat:

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Sikeres bejelentkezés után az alábbihoz hasonló kimenet jelenik meg:

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

Gratulálunk! Ezekkel a hitelesítő adatokkal futtathatja az appját. Ezután be kell állítania a szolgáltatásnév jogosultságait.

## <a name="managing-roles"></a>Szerepkörök kezelése

> [!NOTE]
> Az Azure szerepköralapú hozzáférés-vezérlése (RBAC) a felhasználói nevek és szolgáltatásnevek szerepköreinek meghatározására és kezelésére szolgáló modell. A szerepkörökhöz jogosultságkészletek vannak társítva, amelyek meghatározzák az egyszerű entitás által olvasható, elérhető, írható és kezelhető erőforrásokat. További információ az RBAC-ról és a szerepkörökről: [RBAC: Beépített szerepkörök](/azure/active-directory/role-based-access-built-in-roles).

Az Azure PowerShell a következő parancsmagokat kínálja a szerepkör-hozzárendelések kezeléséhez:

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

A szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**. Mivel azonban ez széles körű engedélyekkel rendelkezik, nem feltétlenül ez a legjobb választás, attól függően, hogy az app milyen mértékben használja az Azure-szolgáltatásokat.
Az **Olvasó** szerepkör sokkal korlátozóbb, és jó választás lehet a csak olvasó appokhoz. A szerepkör-specifikus engedélyek részleteit megtekintheti az Azure Portalon, és létrehozhat saját szerepköröket is.

Esetünkben az **Olvasó** szerepkört adjuk hozzá a példához, és töröljük a **Közreműködő** szerepkört:

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Az aktuálisan hozzárendelt szerepkörök megtekintése:

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

Egyéb Azure PowerShell-parancsmagok a szerepkörök kezeléséhez:

* [Get-AzRoleDefinition](/powershell/module/az.resources/Get-azRoleDefinition)
* [New-AzRoleDefinition](/powershell/module/az.resources/New-azRoleDefinition)
* [Remove-AzRoleDefinition](/powershell/module/az.resources/Remove-azRoleDefinition)
* [Set-AzRoleDefinition](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Szolgáltatásnév hitelesítő adatainak módosítása

A jogosultságok rendszeres áttekintése és a jelszavak cseréje ajánlott biztonsági eljárás. Az app változása esetén is érdemes lehet módosítani a hitelesítő adatokat. A szolgáltatásnév jelszava például módosítható egy új jelszó létrehozásával és a korábbi törlésével.

### <a name="add-a-new-password-for-the-service-principal"></a>Új jelszó hozzáadása a szolgáltatásnévhez

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>A szolgáltatásnév hitelesítő adatainak listázása

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>A régi jelszó törlése a szolgáltatásnévből

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>A szolgáltatásnév hitelesítőadat-listájának ellenőrzése

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a>A szolgáltatásnév adatainak lekérése

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
