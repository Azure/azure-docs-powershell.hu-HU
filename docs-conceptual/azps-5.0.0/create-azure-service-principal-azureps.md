---
title: Azure-beli szolgáltatásnevek használata az Azure PowerShell-lel
description: Megtudhatja, hogyan hozhat létre és használhat szolgáltatásneveket az Azure PowerShell-lel.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 20a58253e3f9435a9d33c700435f77fbb42df7ea
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/05/2020
ms.locfileid: "93365143"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="b75fb-103">Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="b75fb-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="b75fb-104">Az Azure-szolgáltatásokat használó automatizált eszközöknek mindig korlátozott hozzáférésűeknek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="b75fb-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="b75fb-105">Az Azure szolgáltatásneveket használ ahelyett, hogy az alkalmazásokat teljes körű jogosultsággal rendelkező felhasználóként jelentkeztetné be.</span><span class="sxs-lookup"><span data-stu-id="b75fb-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="b75fb-106">Az Azure-beli szolgáltatásnevek olyan identitások, amelyekkel az alkalmazások, üzemeltetett szolgáltatások és automatizált eszközök hozzáférhetnek az Azure erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="b75fb-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="b75fb-107">A hozzáférést a szolgáltatásnévhez rendelt szerepkörök korlátozzák, így Ön szabhatja meg, hogy mely erőforrások, mely szinten legyenek hozzáférhetők.</span><span class="sxs-lookup"><span data-stu-id="b75fb-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="b75fb-108">Biztonsági okokból az automatizált eszközök esetében minden esetben ajánlott a szolgáltatásnevek használata a felhasználói identitással való bejelentkezés helyett.</span><span class="sxs-lookup"><span data-stu-id="b75fb-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="b75fb-109">A cikk bemutatja a szolgáltatásnevek létrehozásának, adatlekérésének és visszaállításának lépéseit az Azure PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="b75fb-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

> [!WARNING]
> <span data-ttu-id="b75fb-110">Amikor a [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) paranccsal egy szolgáltatásnevet hoz létre, a kimenetben olyan hitelesítő adatok találhatóak, amelyeket meg kell védeni.</span><span class="sxs-lookup"><span data-stu-id="b75fb-110">When you create a service principal using the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="b75fb-111">Ügyeljen arra, hogy ne adja meg ezeket a hitelesítő adatokat a kódban, és ne adja be a hitelesítő adatokat a verziókövetésbe.</span><span class="sxs-lookup"><span data-stu-id="b75fb-111">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="b75fb-112">Vagy [felügyelt identitásokat](/azure/active-directory/managed-identities-azure-resources/overview) is használhat – ebben az esetben nincs szükség hitelesítő adatokra.</span><span class="sxs-lookup"><span data-stu-id="b75fb-112">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="b75fb-113">Alapértelmezés szerint a [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) parancs hozzárendeli a [Közreműködő](/azure/role-based-access-control/built-in-roles#contributor) szerepkört a szolgáltatásnévhez az előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="b75fb-113">By default, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="b75fb-114">Annak érdekében, hogy kisebb eséllyel sérüljön a szolgáltatásnév kockázata, rendeljen hozzá egy konkrétabb szerepkört, és szűkítse a hatókört egy erőforrásra vagy erőforráscsoportra.</span><span class="sxs-lookup"><span data-stu-id="b75fb-114">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="b75fb-115">További információt a [szerepkör-hozzárendelés hozzáadásának lépéseit](/azure/role-based-access-control/role-assignments-steps) ismertető cikkben találhat.</span><span class="sxs-lookup"><span data-stu-id="b75fb-115">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="b75fb-116">Egyszerű szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="b75fb-116">Create a service principal</span></span>

<span data-ttu-id="b75fb-117">Hozzon létre egy szolgáltatásnevet a [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="b75fb-117">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="b75fb-118">A szolgáltatásnév létrehozása során Ön választhatja ki, hogy az milyen típusú bejelentkezési hitelesítést használjon.</span><span class="sxs-lookup"><span data-stu-id="b75fb-118">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="b75fb-119">Ha a fiókja nem rendelkezik engedéllyel a szolgáltatásnév létrehozásához, akkor a `New-AzADServicePrincipal` az alábbi hibaüzenetet adja vissza: „Nincs megfelelő jogosultsága a művelet elvégzéséhez”.</span><span class="sxs-lookup"><span data-stu-id="b75fb-119">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="b75fb-120">A szolgáltatásnév létrehozásához vegye fel a kapcsolatot az Azure Active Directory-rendszergazdájával.</span><span class="sxs-lookup"><span data-stu-id="b75fb-120">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="b75fb-121">A szolgáltatásnevek esetében kétféle hitelesítési típus érhető el: Jelszóalapú hitelesítés és tanúsítványalapú hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="b75fb-121">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="b75fb-122">Jelszóalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="b75fb-122">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b75fb-123">A jelszóalapú hitelesítéshez használt szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**.</span><span class="sxs-lookup"><span data-stu-id="b75fb-123">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="b75fb-124">Ez a szerepkör teljes körű engedélyekkel rendelkezik az Azure-fiókba való olvasásra, illetve írásra.</span><span class="sxs-lookup"><span data-stu-id="b75fb-124">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="b75fb-125">További információ a szerepkör-hozzárendelések kezelésével kapcsolatban: [Szolgáltatásnév-szerepkörök kezelése](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="b75fb-125">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="b75fb-126">Egyéb hitelesítési paraméter hiányában a rendszer jelszóalapú hitelesítést használ, és véletlenszerű jelszót hoz létre az Ön számára.</span><span class="sxs-lookup"><span data-stu-id="b75fb-126">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="b75fb-127">Ez az ajánlott módszer, ha jelszóalapú hitelesítést szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="b75fb-127">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="b75fb-128">A visszaadott objektum tartalmazza a `Secret` tagot, amely egy, a létrehozott jelszót tartalmazó `SecureString`.</span><span class="sxs-lookup"><span data-stu-id="b75fb-128">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="b75fb-129">Győződjön meg róla, hogy a szolgáltatásnév hitelesítéséhez használt értéket biztonságos helyen tárolja.</span><span class="sxs-lookup"><span data-stu-id="b75fb-129">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="b75fb-130">Ennek értéke _nem_ fog megjelenni a konzol kimenetén.</span><span class="sxs-lookup"><span data-stu-id="b75fb-130">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="b75fb-131">Ha elvesztette a jelszót, [állítsa vissza a szolgáltatásnév hitelesítő adatait](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="b75fb-131">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="b75fb-132">A következő kód lehetővé teszi a titkos kód exportálását:</span><span class="sxs-lookup"><span data-stu-id="b75fb-132">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="b75fb-133">Felhasználó által megadott jelszavak esetén a `-PasswordCredential` argumentumhoz `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objektumokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="b75fb-133">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="b75fb-134">Az objektumoknak érvényes `StartDate` és `EndDate` paraméterekkel kell rendelkezniük, és egyszerű szöveges `Password` értékre van szükségük.</span><span class="sxs-lookup"><span data-stu-id="b75fb-134">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="b75fb-135">A jelszó létrehozása során kövesse az [Azure Active Directory-jelszavakra vonatkozó szabályokat és korlátozásokat](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="b75fb-135">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="b75fb-136">Ne használjon gyenge vagy korábban már használt jelszót.</span><span class="sxs-lookup"><span data-stu-id="b75fb-136">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="b75fb-137">A `New-AzADServicePrincipal` által visszaadott objektum tartalmazza az `Id` és a `DisplayName` tagokat, amelyek közül bármelyik használható a szolgáltatásnévvel való bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="b75fb-137">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b75fb-138">A szolgáltatásnévvel való bejelentkezéshez szükség van a szolgáltatásnév létrehozásakor használt bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="b75fb-138">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="b75fb-139">A szolgáltatásnév létrehozása pillanatában aktív bérlő lekéréséhez futtassa a következő parancsot _rögtön_ a szolgáltatásnév létrehozása után:</span><span class="sxs-lookup"><span data-stu-id="b75fb-139">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="b75fb-140">Tanúsítványalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="b75fb-140">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b75fb-141">Tanúsítványalapú hitelesítést használó szolgáltatásnév létrehozásakor nincs alapértelmezett szerepkör hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="b75fb-141">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="b75fb-142">További információ a szerepkör-hozzárendelések kezelésével kapcsolatban: [Szolgáltatásnév-szerepkörök kezelése](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="b75fb-142">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="b75fb-143">A tanúsítványalapú hitelesítést használó szolgáltatásnevek létrehozása a `-CertValue` paraméterrel történik.</span><span class="sxs-lookup"><span data-stu-id="b75fb-143">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="b75fb-144">E paraméter esetében a nyilvános tanúsítvány base64-kódolású ASCII sztringjére van szükség.</span><span class="sxs-lookup"><span data-stu-id="b75fb-144">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="b75fb-145">Ez egy PEM-fájl vagy egy szöveges kódolású CRT- vagy CER-fájl lehet.</span><span class="sxs-lookup"><span data-stu-id="b75fb-145">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="b75fb-146">A bináris kódolású nyilvános tanúsítványok nem támogatottak.</span><span class="sxs-lookup"><span data-stu-id="b75fb-146">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="b75fb-147">Az alábbi utasítások végrehajtása során azt feltételezzük, hogy a tanúsítvány már rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="b75fb-147">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="b75fb-148">A `-KeyCredential` paraméter is használható, amelyhez `PSADKeyCredential` objektumokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="b75fb-148">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="b75fb-149">Az objektumoknak érvényes `StartDate` és `EndDate` paraméterekkel kell rendelkezniük, a `CertValue` tag esetében pedig a nyilvános tanúsítvány base64-kódolású ASCII sztringjét kell megadni.</span><span class="sxs-lookup"><span data-stu-id="b75fb-149">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="b75fb-150">A `New-AzADServicePrincipal` által visszaadott objektum tartalmazza az `Id` és a `DisplayName` tagokat, amelyek közül bármelyik használható a szolgáltatásnévvel való bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="b75fb-150">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="b75fb-151">A szolgáltatásnévvel bejelentkező ügyfeleknek hozzáféréssel kell rendelkezniük a tanúsítvány titkos kulcsához is.</span><span class="sxs-lookup"><span data-stu-id="b75fb-151">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b75fb-152">A szolgáltatásnévvel való bejelentkezéshez szükség van a szolgáltatásnév létrehozásakor használt bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="b75fb-152">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="b75fb-153">A szolgáltatásnév létrehozása pillanatában aktív bérlő lekéréséhez futtassa a következő parancsot _rögtön_ a szolgáltatásnév létrehozása után:</span><span class="sxs-lookup"><span data-stu-id="b75fb-153">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="b75fb-154">Meglévő szolgáltatásnév lekérése</span><span class="sxs-lookup"><span data-stu-id="b75fb-154">Get an existing service principal</span></span>

<span data-ttu-id="b75fb-155">Az aktív bérlő szolgáltatásneveinek listája a [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) használatával kérhető le.</span><span class="sxs-lookup"><span data-stu-id="b75fb-155">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="b75fb-156">Ez a parancs alapértelmezés szerint a bérlő _összes_ szolgáltatásnevét visszaadja.</span><span class="sxs-lookup"><span data-stu-id="b75fb-156">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="b75fb-157">Nagy szervezetek esetén az eredmények lekérése hosszabb időt vehet igénybe.</span><span class="sxs-lookup"><span data-stu-id="b75fb-157">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="b75fb-158">Ehelyett javasoljuk, hogy használja valamelyik választható kiszolgálóoldali szűrőargumentumot:</span><span class="sxs-lookup"><span data-stu-id="b75fb-158">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="b75fb-159">A `-DisplayNameBeginsWith` a megadott értékkel megegyező _előtaggal_ rendelkező szolgáltatásneveket kéri le.</span><span class="sxs-lookup"><span data-stu-id="b75fb-159">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="b75fb-160">A szolgáltatásnév megjelenített neve a `-DisplayName` létrehozáskor megadott értéke.</span><span class="sxs-lookup"><span data-stu-id="b75fb-160">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="b75fb-161">A `-DisplayName` a _pontos egyezést mutató_ szolgáltatásneveket kéri le.</span><span class="sxs-lookup"><span data-stu-id="b75fb-161">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="b75fb-162">Szolgáltatásnév-szerepkörök kezelése</span><span class="sxs-lookup"><span data-stu-id="b75fb-162">Manage service principal roles</span></span>

<span data-ttu-id="b75fb-163">Az Azure PowerShell a következő parancsmagokat biztosítja a szerepkör-hozzárendelések kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="b75fb-163">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="b75fb-164">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b75fb-164">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="b75fb-165">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b75fb-165">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="b75fb-166">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b75fb-166">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="b75fb-167">A jelszóalapú hitelesítéshez használt szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**.</span><span class="sxs-lookup"><span data-stu-id="b75fb-167">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="b75fb-168">Ez a szerepkör teljes körű engedélyekkel rendelkezik az Azure-fiókba való olvasásra, illetve írásra.</span><span class="sxs-lookup"><span data-stu-id="b75fb-168">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="b75fb-169">Az **Olvasó** szerepkör sokkal korlátozóbb, kizárólag olvasási hozzáférést biztosít.</span><span class="sxs-lookup"><span data-stu-id="b75fb-169">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="b75fb-170">További információ a szerepköralapú hozzáférés-vezérlésről (RBAC) és a szerepkörökről: [RBAC: Beépített szerepkörök](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="b75fb-170">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="b75fb-171">Példánk során az **Olvasó** szerepkört adjuk hozzá, és eltávolítjuk a **Közreműködő** szerepkört:</span><span class="sxs-lookup"><span data-stu-id="b75fb-171">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="b75fb-172">A szerepkör-hozzárendelési parancsmagok esetében nincs szükség a szolgáltatásnév objektumazonosítójára.</span><span class="sxs-lookup"><span data-stu-id="b75fb-172">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="b75fb-173">Ezek a hozzárendelt alkalmazásazonosítót használják, amelyet a rendszer a létrehozás során állít elő.</span><span class="sxs-lookup"><span data-stu-id="b75fb-173">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="b75fb-174">A szolgáltatásnév alkalmazásazonosítójának lekéréséhez használja a `Get-AzADServicePrincipal` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b75fb-174">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="b75fb-175">Ha a fiókja nem jogosult szerepkörök hozzárendelésére, akkor egy hibaüzenet jelenik meg, miszerint a fiókja nem jogosult a Microsoft.Authorization/roleAssignments/write művelet végrehajtására.</span><span class="sxs-lookup"><span data-stu-id="b75fb-175">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="b75fb-176">A szerepkörök kezeléséhez vegye fel a kapcsolatot az Azure Active Directory-rendszergazdájával.</span><span class="sxs-lookup"><span data-stu-id="b75fb-176">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="b75fb-177">A szerepkör hozzáadása _nem_ korlátozza az előzetesen hozzárendelt engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="b75fb-177">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="b75fb-178">A szolgáltatásnév engedélyeinek korlátozása során a **Közreműködő** szerepkört el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="b75fb-178">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="b75fb-179">A módosítások a hozzárendelt szerepkörök listázásával ellenőrizhetők:</span><span class="sxs-lookup"><span data-stu-id="b75fb-179">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="b75fb-180">Bejelentkezés szolgáltatásnév használatával</span><span class="sxs-lookup"><span data-stu-id="b75fb-180">Sign in using a service principal</span></span>

<span data-ttu-id="b75fb-181">Tesztelje az új szolgáltatásnév hitelesítő adatait és engedélyeit a bejelentkezéssel.</span><span class="sxs-lookup"><span data-stu-id="b75fb-181">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="b75fb-182">A szolgáltatásnévvel történő bejelentkezéshez szükség van a szolgáltatásnévhez rendelt `applicationId` értékre és a létrehozáskori bérlőre.</span><span class="sxs-lookup"><span data-stu-id="b75fb-182">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="b75fb-183">Bejelentkezés szolgáltatásnévvel, jelszó használatával:</span><span class="sxs-lookup"><span data-stu-id="b75fb-183">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="b75fb-184">A tanúsítványalapú hitelesítéshez az Azure PowerShellnek egy helyi tanúsítványtárolóból kell információkat lekérnie a tanúsítvány ujjlenyomata alapján.</span><span class="sxs-lookup"><span data-stu-id="b75fb-184">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

<span data-ttu-id="b75fb-185">A tanúsítvány PowerShell által hozzáférhető tanúsítványtárolóba való importálásával kapcsolatos utasításokért lásd: [Bejelentkezés az Azure PowerShell-lel](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="b75fb-185">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="b75fb-186">Hitelesítő adatok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="b75fb-186">Reset credentials</span></span>

<span data-ttu-id="b75fb-187">Ha elfelejtette a szolgáltatásnévhez tartozó hitelesítő adatokat, a [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) parancsmaggal adhat hozzá új hitelesítő adatokat, véletlenszerű jelszóval.</span><span class="sxs-lookup"><span data-stu-id="b75fb-187">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="b75fb-188">Ez a parancsmag nem támogatja a felhasználó által megadott hitelesítő adatokat a jelszó visszaállításakor.</span><span class="sxs-lookup"><span data-stu-id="b75fb-188">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b75fb-189">Javasoljuk, hogy az új hitelesítő adatok hozzárendelése előtt törölje a meglévő hitelesítő adatokat, nehogy azokkal jelentkezzen be.</span><span class="sxs-lookup"><span data-stu-id="b75fb-189">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="b75fb-190">Ehhez használja a [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) parancsmagot:</span><span class="sxs-lookup"><span data-stu-id="b75fb-190">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="b75fb-191">Hibaelhárítás</span><span class="sxs-lookup"><span data-stu-id="b75fb-191">Troubleshooting</span></span>

<span data-ttu-id="b75fb-192">Ha a _„New-AzADServicePrincipal: Már létezik egy másik objektum ezzel az értékkel az identifierUris tulajdonsághoz.”_ hibaüzenetet kapja, győződjön meg arról, hogy nem létezik ilyen nevű szolgáltatásnév.</span><span class="sxs-lookup"><span data-stu-id="b75fb-192">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_ , verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="b75fb-193">Ha a meglévő szolgáltatásnévre már nincs rá szükség, az alábbi példa szerint eltávolíthatja.</span><span class="sxs-lookup"><span data-stu-id="b75fb-193">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="b75fb-194">Ez a hiba akkor is jelentkezhet, ha korábban már létrehozott szolgáltatásnevet egy Azure Active Directory-alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="b75fb-194">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="b75fb-195">Ha eltávolítja a szolgáltatásnevet, az alkalmazás továbbra is elérhető marad.</span><span class="sxs-lookup"><span data-stu-id="b75fb-195">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="b75fb-196">Ez az alkalmazás segít elkerülni, hogy másik szolgáltatásnevet hozzon létre ugyanazon a néven.</span><span class="sxs-lookup"><span data-stu-id="b75fb-196">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="b75fb-197">A következő példa alkalmazásával meggyőződhet arról, nem található ugyanolyan nevű Azure Active Directory-alkalmazás:</span><span class="sxs-lookup"><span data-stu-id="b75fb-197">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="b75fb-198">Ha létezik olyan azonos nevű alkalmazás, amelyre már nincs szükség, az alábbi példa szerint eltávolíthatja.</span><span class="sxs-lookup"><span data-stu-id="b75fb-198">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="b75fb-199">Ellenkező esetben válasszon egy alternatív nevet a létrehozni kívánt új szolgáltatásnév számára.</span><span class="sxs-lookup"><span data-stu-id="b75fb-199">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>
