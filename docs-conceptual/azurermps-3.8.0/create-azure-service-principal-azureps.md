---
title: Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával
description: Megtudhatja, hogyan hozhat létre szolgáltatásneveket appjához vagy szolgáltatásához az Azure PowerShell használatával.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: dd2e50a4fe5ee9061403e2b61ace74213b5c858e
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/23/2018
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával

Ha az appját vagy szolgáltatását az Azure PowerShell-lel szeretné kezelni, egy Azure Active Directory (AAD) szolgáltatásnév alatt, és nem a saját hitelesítő adataival érdemes futtatnia. Ez a témakör végigvezeti a szolgáltatásnevek Azure PowerShell-lel való létrehozásának folyamatán.

> [!NOTE]
> Az Azure Portalon is létrehozhat szolgáltatásneveket. További részletekért lásd: [Active Directory-alkalmazás és -szolgáltatásnév létrehozása a portálon erőforrások eléréséhez](/azure/azure-resource-manager/resource-group-create-service-principal-portal).

## <a name="what-is-a-service-principal"></a>Mi az a szolgáltatásnév?

Az Azure-beli szolgáltatásnév egy biztonsági identitás, amellyel a felhasználó által létrehozott appok, szolgáltatások és automatizálási eszközök elérnek adott Azure-erőforrásokat. Képzelje el úgy, mint egy „felhasználói identitást” (felhasználónév és jelszó vagy tanúsítvány) egy adott szerepkörrel és szigorúan szabályozott engedélyekkel. Az általános identitásoktól eltérően ez csak konkrét feladatok végrehajtására szolgál. Csak akkor javítja a biztonságot, ha csak a felügyeleti feladataihoz szükséges minimális engedélyeket osztja ki neki.

## <a name="verify-your-own-permission-level"></a>Saját jogosultsági szint ellenőrzése

Először is megfelelő jogosultságokkal kell rendelkeznie mind az Azure Active Directoryban, mind az Azure-előfizetésén. Pontosabban, létre kell tudnia hozni appot az Active Directoryban, és ki kell tudnia osztani szerepköröket a szolgáltatásnévnek.

A legegyszerűbben a portálon ellenőrizheti, hogy rendelkezik-e megfelelő jogosultságokkal. Lásd [Szükséges jogosultságok ellenőrzése a portálon](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Szolgáltatásnév létrehozása az app számára

Miután bejelentkezett Azure-fiókjába, létrehozhatja a szolgáltatásnevet. A következő módszerek egyikének rendelkezésre kell állnia az üzembe helyezett app azonosításához:

* Az üzembe helyezett app egyedi neve (a következő példákban ez a „MyDemoWebApp”), vagy
* az alkalmazásazonosító, az üzembe helyezett alkalmazással, szolgáltatással vagy objektummal társított egyedi GUID

### <a name="get-information-about-your-application"></a>Az alkalmazás adatainak lekérése

Az alkalmazással kapcsolatos információkat a `Get-AzureRmADApplication` parancsmaggal derítheti fel.

```powershell
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```
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

A szolgáltatásnév a `New-AzureRmADServicePrincipal` parancsmaggal hozható létre.

```powershell
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $password
```

```
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>A szolgáltatásnév adatainak lekérése

```powershell
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>Bejelentkezés a szolgáltatásnévvel

Most már bejelentkezhet az app új szolgáltatásnevével a megadott *appId* és *jelszó* használatával. Meg kell adnia fiókja bérlőazonosítóját. A bérlőazonosító akkor jelenik meg, ha a saját hitelesítő adataival bejelentkezik az Azure-ba.

```powershell
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Login-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Futtassa ezt a parancsot egy új PowerShell-munkamenetből. Sikeres bejelentkezés után az alábbihoz hasonló kimenet jelenik meg:

```
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
> Az Azure szerepköralapú hozzáférés-vezérlése (RBAC) a felhasználói nevek és szolgáltatásnevek szerepköreinek meghatározására és kezelésére szolgáló modell. A szerepkörökhöz jogosultságkészletek vannak társítva, amelyek meghatározzák az egyszerű entitás által olvasható, elérhető, írható és kezelhető erőforrásokat. További információkért az RBAC-ról és a szerepkörökről: [RBAC: Beépített szerepkörök](/azure/active-directory/role-based-access-built-in-roles).

Az Azure PowerShell a következő parancsmagokat kínálja a szerepkör-hozzárendelések kezeléséhez:

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

A szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**. Mivel azonban ez széles körű engedélyekkel rendelkezik, nem feltétlenül ez a legjobb választás, attól függően, hogy az app milyen mértékben használja az Azure-szolgáltatásokat.
Az **Olvasó** szerepkör sokkal korlátozóbb, és jó választás lehet a csak olvasó appokhoz. A szerepkör-specifikus engedélyek részleteit megtekintheti az Azure Portalon, és létrehozhat saját szerepköröket is.

Esetünkben az **Olvasó** szerepkört adjuk hozzá a példához, és töröljük a **Közreműködő** szerepkört:

```powershell
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```powershell
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Az aktuálisan hozzárendelt szerepkörök megtekintése:

```powershell
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```
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

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Szolgáltatásnév hitelesítő adatainak módosítása

A jogosultságok rendszeres áttekintése és a jelszavak cseréje ajánlott biztonsági eljárás. Az app változása esetén is érdemes lehet módosítani a hitelesítő adatokat. A szolgáltatásnév jelszava például módosítható egy új jelszó létrehozásával és a korábbi törlésével.

### <a name="add-a-new-password-for-the-service-principal"></a>Új jelszó hozzáadása a szolgáltatásnévhez

```powershell
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>A szolgáltatásnév hitelesítő adatainak listázása

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>A régi jelszó törlése a szolgáltatásnévből

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>A szolgáltatásnév hitelesítőadat-listájának ellenőrzése

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
