---
title: Azure-beli szolgáltatásnevek használata az Azure PowerShell-lel
description: Megtudhatja, hogyan hozhat létre és használhat szolgáltatásneveket az Azure PowerShell-lel.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8969828fdaf249cae2fefa2a419962770bf1e84c
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/05/2020
ms.locfileid: "93365160"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával

Az Azure-szolgáltatásokat használó automatizált eszközöknek mindig korlátozott hozzáférésűeknek kell lenniük. Az Azure szolgáltatásneveket használ ahelyett, hogy az alkalmazásokat teljes körű jogosultsággal rendelkező felhasználóként jelentkeztetné be.

Az Azure-beli szolgáltatásnevek olyan identitások, amelyekkel az alkalmazások, üzemeltetett szolgáltatások és automatizált eszközök hozzáférhetnek az Azure erőforrásaihoz. A hozzáférést a szolgáltatásnévhez rendelt szerepkörök korlátozzák, így Ön szabhatja meg, hogy mely erőforrások, mely szinten legyenek hozzáférhetők. Biztonsági okokból az automatizált eszközök esetében minden esetben ajánlott a szolgáltatásnevek használata a felhasználói identitással való bejelentkezés helyett.

A cikk bemutatja a szolgáltatásnevek létrehozásának, adatlekérésének és visszaállításának lépéseit az Azure PowerShellben.

> [!WARNING]
> Amikor a [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) paranccsal egy szolgáltatásnevet hoz létre, a kimenetben olyan hitelesítő adatok találhatóak, amelyeket meg kell védeni. Ügyeljen arra, hogy ne adja meg ezeket a hitelesítő adatokat a kódban, és ne adja be a hitelesítő adatokat a verziókövetésbe. Vagy [felügyelt identitásokat](/azure/active-directory/managed-identities-azure-resources/overview) is használhat – ebben az esetben nincs szükség hitelesítő adatokra.
>
> Alapértelmezés szerint a [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) parancs hozzárendeli a [Közreműködő](/azure/role-based-access-control/built-in-roles#contributor) szerepkört a szolgáltatásnévhez az előfizetési hatókörben. Annak érdekében, hogy kisebb eséllyel sérüljön a szolgáltatásnév kockázata, rendeljen hozzá egy konkrétabb szerepkört, és szűkítse a hatókört egy erőforrásra vagy erőforráscsoportra. További információt a [szerepkör-hozzárendelés hozzáadásának lépéseit](/azure/role-based-access-control/role-assignments-steps) ismertető cikkben találhat.

## <a name="create-a-service-principal"></a>Egyszerű szolgáltatás létrehozása

Hozzon létre egy szolgáltatásnevet a [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) parancsmaggal. A szolgáltatásnév létrehozása során Ön választhatja ki, hogy az milyen típusú bejelentkezési hitelesítést használjon.

> [!NOTE]
> Ha a fiókja nem rendelkezik engedéllyel a szolgáltatásnév létrehozásához, akkor a `New-AzADServicePrincipal` az alábbi hibaüzenetet adja vissza: „Nincs megfelelő jogosultsága a művelet elvégzéséhez”.
> A szolgáltatásnév létrehozásához vegye fel a kapcsolatot az Azure Active Directory-rendszergazdájával.

A szolgáltatásnevek esetében kétféle hitelesítési típus érhető el: Jelszóalapú hitelesítés és tanúsítványalapú hitelesítés.

### <a name="password-based-authentication"></a>Jelszóalapú hitelesítés

> [!IMPORTANT]
> A jelszóalapú hitelesítéshez használt szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**. Ez a szerepkör teljes körű engedélyekkel rendelkezik az Azure-fiókba való olvasásra, illetve írásra. További információ a szerepkör-hozzárendelések kezelésével kapcsolatban: [Szolgáltatásnév-szerepkörök kezelése](#manage-service-principal-roles).

Egyéb hitelesítési paraméter hiányában a rendszer jelszóalapú hitelesítést használ, és véletlenszerű jelszót hoz létre az Ön számára. Ez az ajánlott módszer, ha jelszóalapú hitelesítést szeretne használni.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

A visszaadott objektum tartalmazza a `Secret` tagot, amely egy, a létrehozott jelszót tartalmazó `SecureString`. Győződjön meg róla, hogy a szolgáltatásnév hitelesítéséhez használt értéket biztonságos helyen tárolja. Ennek értéke _nem_ fog megjelenni a konzol kimenetén. Ha elvesztette a jelszót, [állítsa vissza a szolgáltatásnév hitelesítő adatait](#reset-credentials).

A következő kód lehetővé teszi a titkos kód exportálását:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

Felhasználó által megadott jelszavak esetén a `-PasswordCredential` argumentumhoz `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objektumokra van szükség. Az objektumoknak érvényes `StartDate` és `EndDate` paraméterekkel kell rendelkezniük, és egyszerű szöveges `Password` értékre van szükségük. A jelszó létrehozása során kövesse az [Azure Active Directory-jelszavakra vonatkozó szabályokat és korlátozásokat](/azure/active-directory/active-directory-passwords-policy).
Ne használjon gyenge vagy korábban már használt jelszót.

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

A `New-AzADServicePrincipal` által visszaadott objektum tartalmazza az `Id` és a `DisplayName` tagokat, amelyek közül bármelyik használható a szolgáltatásnévvel való bejelentkezéshez.

> [!IMPORTANT]
> A szolgáltatásnévvel való bejelentkezéshez szükség van a szolgáltatásnév létrehozásakor használt bérlőazonosítóra. A szolgáltatásnév létrehozása pillanatában aktív bérlő lekéréséhez futtassa a következő parancsot _rögtön_ a szolgáltatásnév létrehozása után:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a>Tanúsítványalapú hitelesítés

> [!IMPORTANT]
> Tanúsítványalapú hitelesítést használó szolgáltatásnév létrehozásakor nincs alapértelmezett szerepkör hozzárendelve. További információ a szerepkör-hozzárendelések kezelésével kapcsolatban: [Szolgáltatásnév-szerepkörök kezelése](#manage-service-principal-roles).

A tanúsítványalapú hitelesítést használó szolgáltatásnevek létrehozása a `-CertValue` paraméterrel történik. E paraméter esetében a nyilvános tanúsítvány base64-kódolású ASCII sztringjére van szükség. Ez egy PEM-fájl vagy egy szöveges kódolású CRT- vagy CER-fájl lehet. A bináris kódolású nyilvános tanúsítványok nem támogatottak. Az alábbi utasítások végrehajtása során azt feltételezzük, hogy a tanúsítvány már rendelkezésre áll.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

A `-KeyCredential` paraméter is használható, amelyhez `PSADKeyCredential` objektumokra van szükség. Az objektumoknak érvényes `StartDate` és `EndDate` paraméterekkel kell rendelkezniük, a `CertValue` tag esetében pedig a nyilvános tanúsítvány base64-kódolású ASCII sztringjét kell megadni.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

A `New-AzADServicePrincipal` által visszaadott objektum tartalmazza az `Id` és a `DisplayName` tagokat, amelyek közül bármelyik használható a szolgáltatásnévvel való bejelentkezéshez. A szolgáltatásnévvel bejelentkező ügyfeleknek hozzáféréssel kell rendelkezniük a tanúsítvány titkos kulcsához is.

> [!IMPORTANT]
> A szolgáltatásnévvel való bejelentkezéshez szükség van a szolgáltatásnév létrehozásakor használt bérlőazonosítóra. A szolgáltatásnév létrehozása pillanatában aktív bérlő lekéréséhez futtassa a következő parancsot _rögtön_ a szolgáltatásnév létrehozása után:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a>Meglévő szolgáltatásnév lekérése

Az aktív bérlő szolgáltatásneveinek listája a [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) használatával kérhető le. Ez a parancs alapértelmezés szerint a bérlő _összes_ szolgáltatásnevét visszaadja. Nagy szervezetek esetén az eredmények lekérése hosszabb időt vehet igénybe. Ehelyett javasoljuk, hogy használja valamelyik választható kiszolgálóoldali szűrőargumentumot:

- A `-DisplayNameBeginsWith` a megadott értékkel megegyező _előtaggal_ rendelkező szolgáltatásneveket kéri le. A szolgáltatásnév megjelenített neve a `-DisplayName` létrehozáskor megadott értéke.
- A `-DisplayName` a _pontos egyezést mutató_ szolgáltatásneveket kéri le.

## <a name="manage-service-principal-roles"></a>Szolgáltatásnév-szerepkörök kezelése

Az Azure PowerShell a következő parancsmagokat biztosítja a szerepkör-hozzárendelések kezeléséhez:

- [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
- [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
- [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

A jelszóalapú hitelesítéshez használt szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**. Ez a szerepkör teljes körű engedélyekkel rendelkezik az Azure-fiókba való olvasásra, illetve írásra. Az **Olvasó** szerepkör sokkal korlátozóbb, kizárólag olvasási hozzáférést biztosít. További információ a szerepköralapú hozzáférés-vezérlésről (RBAC) és a szerepkörökről: [RBAC: Beépített szerepkörök](/azure/active-directory/role-based-access-built-in-roles).

Példánk során az **Olvasó** szerepkört adjuk hozzá, és eltávolítjuk a **Közreműködő** szerepkört:

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> A szerepkör-hozzárendelési parancsmagok esetében nincs szükség a szolgáltatásnév objektumazonosítójára. Ezek a hozzárendelt alkalmazásazonosítót használják, amelyet a rendszer a létrehozás során állít elő. A szolgáltatásnév alkalmazásazonosítójának lekéréséhez használja a `Get-AzADServicePrincipal` parancsmagot.

> [!NOTE]
> Ha a fiókja nem jogosult szerepkörök hozzárendelésére, akkor egy hibaüzenet jelenik meg, miszerint a fiókja nem jogosult a Microsoft.Authorization/roleAssignments/write művelet végrehajtására. A szerepkörök kezeléséhez vegye fel a kapcsolatot az Azure Active Directory-rendszergazdájával.

A szerepkör hozzáadása _nem_ korlátozza az előzetesen hozzárendelt engedélyeket. A szolgáltatásnév engedélyeinek korlátozása során a **Közreműködő** szerepkört el kell távolítani.

A módosítások a hozzárendelt szerepkörök listázásával ellenőrizhetők:

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>Bejelentkezés szolgáltatásnév használatával

Tesztelje az új szolgáltatásnév hitelesítő adatait és engedélyeit a bejelentkezéssel. A szolgáltatásnévvel történő bejelentkezéshez szükség van a szolgáltatásnévhez rendelt `applicationId` értékre és a létrehozáskori bérlőre.

Bejelentkezés szolgáltatásnévvel, jelszó használatával:

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

A tanúsítványalapú hitelesítéshez az Azure PowerShellnek egy helyi tanúsítványtárolóból kell információkat lekérnie a tanúsítvány ujjlenyomata alapján.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

A tanúsítvány PowerShell által hozzáférhető tanúsítványtárolóba való importálásával kapcsolatos utasításokért lásd: [Bejelentkezés az Azure PowerShell-lel](authenticate-azureps.md#sp-signin)

## <a name="reset-credentials"></a>Hitelesítő adatok visszaállítása

Ha elfelejtette a szolgáltatásnévhez tartozó hitelesítő adatokat, a [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) parancsmaggal adhat hozzá új hitelesítő adatokat, véletlenszerű jelszóval. Ez a parancsmag nem támogatja a felhasználó által megadott hitelesítő adatokat a jelszó visszaállításakor.

> [!IMPORTANT]
> Javasoljuk, hogy az új hitelesítő adatok hozzárendelése előtt törölje a meglévő hitelesítő adatokat, nehogy azokkal jelentkezzen be. Ehhez használja a [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) parancsmagot:

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a>Hibaelhárítás

Ha a _„New-AzADServicePrincipal: Már létezik egy másik objektum ezzel az értékkel az identifierUris tulajdonsághoz.”_ hibaüzenetet kapja, győződjön meg arról, hogy nem létezik ilyen nevű szolgáltatásnév.

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Ha a meglévő szolgáltatásnévre már nincs rá szükség, az alábbi példa szerint eltávolíthatja.

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Ez a hiba akkor is jelentkezhet, ha korábban már létrehozott szolgáltatásnevet egy Azure Active Directory-alkalmazásban. Ha eltávolítja a szolgáltatásnevet, az alkalmazás továbbra is elérhető marad. Ez az alkalmazás segít elkerülni, hogy másik szolgáltatásnevet hozzon létre ugyanazon a néven.

A következő példa alkalmazásával meggyőződhet arról, nem található ugyanolyan nevű Azure Active Directory-alkalmazás:

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

Ha létezik olyan azonos nevű alkalmazás, amelyre már nincs szükség, az alábbi példa szerint eltávolíthatja.

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

Ellenkező esetben válasszon egy alternatív nevet a létrehozni kívánt új szolgáltatásnév számára.
