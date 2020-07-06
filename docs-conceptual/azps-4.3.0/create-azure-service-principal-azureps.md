---
title: Azure-beli szolgáltatásnevek használata az Azure PowerShell-lel
description: Megtudhatja, hogyan hozhat létre és használhat szolgáltatásneveket az Azure PowerShell-lel.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.openlocfilehash: ebdc0783c43ccecbbeb315de5b5baebc9539b40e
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85268119"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="117f5-103">Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="117f5-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="117f5-104">Az Azure-szolgáltatásokat használó automatizált eszközöknek mindig korlátozott hozzáférésűeknek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="117f5-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="117f5-105">Az Azure szolgáltatásneveket használ ahelyett, hogy az alkalmazásokat teljes körű jogosultsággal rendelkező felhasználóként jelentkeztetné be.</span><span class="sxs-lookup"><span data-stu-id="117f5-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="117f5-106">Az Azure-beli szolgáltatásnevek olyan identitások, amelyekkel az alkalmazások, üzemeltetett szolgáltatások és automatizált eszközök hozzáférhetnek az Azure erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="117f5-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="117f5-107">A hozzáférést a szolgáltatásnévhez rendelt szerepkörök korlátozzák, így Ön szabhatja meg, hogy mely erőforrások, mely szinten legyenek hozzáférhetők.</span><span class="sxs-lookup"><span data-stu-id="117f5-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="117f5-108">Biztonsági okokból az automatizált eszközök esetében minden esetben ajánlott a szolgáltatásnevek használata a felhasználói identitással való bejelentkezés helyett.</span><span class="sxs-lookup"><span data-stu-id="117f5-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="117f5-109">A cikk bemutatja a szolgáltatásnevek létrehozásának, adatlekérésének és visszaállításának lépéseit az Azure PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="117f5-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="117f5-110">Egyszerű szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="117f5-110">Create a service principal</span></span>

<span data-ttu-id="117f5-111">Hozzon létre egy szolgáltatásnevet a [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="117f5-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="117f5-112">A szolgáltatásnév létrehozása során Ön választhatja ki, hogy az milyen típusú bejelentkezési hitelesítést használjon.</span><span class="sxs-lookup"><span data-stu-id="117f5-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="117f5-113">Ha a fiókja nem rendelkezik engedéllyel a szolgáltatásnév létrehozásához, akkor a `New-AzADServicePrincipal` az alábbi hibaüzenetet adja vissza: „Nincs megfelelő jogosultsága a művelet elvégzéséhez”.</span><span class="sxs-lookup"><span data-stu-id="117f5-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="117f5-114">A szolgáltatásnév létrehozásához vegye fel a kapcsolatot az Azure Active Directory-rendszergazdájával.</span><span class="sxs-lookup"><span data-stu-id="117f5-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="117f5-115">A szolgáltatásnevek esetében kétféle hitelesítési típus érhető el: Jelszóalapú hitelesítés és tanúsítványalapú hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="117f5-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="117f5-116">Jelszóalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="117f5-116">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="117f5-117">A jelszóalapú hitelesítéshez használt szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**.</span><span class="sxs-lookup"><span data-stu-id="117f5-117">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="117f5-118">Ez a szerepkör teljes körű engedélyekkel rendelkezik az Azure-fiókba való olvasásra, illetve írásra.</span><span class="sxs-lookup"><span data-stu-id="117f5-118">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="117f5-119">További információ a szerepkör-hozzárendelések kezelésével kapcsolatban: [Szolgáltatásnév-szerepkörök kezelése](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="117f5-119">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="117f5-120">Egyéb hitelesítési paraméter hiányában a rendszer jelszóalapú hitelesítést használ, és véletlenszerű jelszót hoz létre az Ön számára.</span><span class="sxs-lookup"><span data-stu-id="117f5-120">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="117f5-121">Ez az ajánlott módszer, ha jelszóalapú hitelesítést szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="117f5-121">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="117f5-122">A visszaadott objektum tartalmazza a `Secret` tagot, amely egy, a létrehozott jelszót tartalmazó `SecureString`.</span><span class="sxs-lookup"><span data-stu-id="117f5-122">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="117f5-123">Győződjön meg róla, hogy a szolgáltatásnév hitelesítéséhez használt értéket biztonságos helyen tárolja.</span><span class="sxs-lookup"><span data-stu-id="117f5-123">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="117f5-124">Ennek értéke _nem_ fog megjelenni a konzol kimenetén.</span><span class="sxs-lookup"><span data-stu-id="117f5-124">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="117f5-125">Ha elvesztette a jelszót, [állítsa vissza a szolgáltatásnév hitelesítő adatait](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="117f5-125">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="117f5-126">A következő kód lehetővé teszi a titkos kód exportálását:</span><span class="sxs-lookup"><span data-stu-id="117f5-126">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="117f5-127">Felhasználó által megadott jelszavak esetén a `-PasswordCredential` argumentumhoz `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objektumokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="117f5-127">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="117f5-128">Az objektumoknak érvényes `StartDate` és `EndDate` paraméterekkel kell rendelkezniük, és egyszerű szöveges `Password` értékre van szükségük.</span><span class="sxs-lookup"><span data-stu-id="117f5-128">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="117f5-129">A jelszó létrehozása során kövesse az [Azure Active Directory-jelszavakra vonatkozó szabályokat és korlátozásokat](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="117f5-129">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="117f5-130">Ne használjon gyenge vagy korábban már használt jelszót.</span><span class="sxs-lookup"><span data-stu-id="117f5-130">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="117f5-131">A `New-AzADServicePrincipal` által visszaadott objektum tartalmazza az `Id` és a `DisplayName` tagokat, amelyek közül bármelyik használható a szolgáltatásnévvel való bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="117f5-131">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="117f5-132">A szolgáltatásnévvel való bejelentkezéshez szükség van a szolgáltatásnév létrehozásakor használt bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="117f5-132">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="117f5-133">A szolgáltatásnév létrehozása pillanatában aktív bérlő lekéréséhez futtassa a következő parancsot _rögtön_ a szolgáltatásnév létrehozása után:</span><span class="sxs-lookup"><span data-stu-id="117f5-133">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="117f5-134">Tanúsítványalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="117f5-134">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="117f5-135">Tanúsítványalapú hitelesítést használó szolgáltatásnév létrehozásakor nincs alapértelmezett szerepkör hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="117f5-135">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="117f5-136">További információ a szerepkör-hozzárendelések kezelésével kapcsolatban: [Szolgáltatásnév-szerepkörök kezelése](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="117f5-136">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="117f5-137">A tanúsítványalapú hitelesítést használó szolgáltatásnevek létrehozása a `-CertValue` paraméterrel történik.</span><span class="sxs-lookup"><span data-stu-id="117f5-137">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="117f5-138">E paraméter esetében a nyilvános tanúsítvány base64-kódolású ASCII sztringjére van szükség.</span><span class="sxs-lookup"><span data-stu-id="117f5-138">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="117f5-139">Ez egy PEM-fájl vagy egy szöveges kódolású CRT- vagy CER-fájl lehet.</span><span class="sxs-lookup"><span data-stu-id="117f5-139">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="117f5-140">A bináris kódolású nyilvános tanúsítványok nem támogatottak.</span><span class="sxs-lookup"><span data-stu-id="117f5-140">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="117f5-141">Az alábbi utasítások végrehajtása során azt feltételezzük, hogy a tanúsítvány már rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="117f5-141">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="117f5-142">A `-KeyCredential` paraméter is használható, amelyhez `PSADKeyCredential` objektumokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="117f5-142">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="117f5-143">Az objektumoknak érvényes `StartDate` és `EndDate` paraméterekkel kell rendelkezniük, a `CertValue` tag esetében pedig a nyilvános tanúsítvány base64-kódolású ASCII sztringjét kell megadni.</span><span class="sxs-lookup"><span data-stu-id="117f5-143">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="117f5-144">A `New-AzADServicePrincipal` által visszaadott objektum tartalmazza az `Id` és a `DisplayName` tagokat, amelyek közül bármelyik használható a szolgáltatásnévvel való bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="117f5-144">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="117f5-145">A szolgáltatásnévvel bejelentkező ügyfeleknek hozzáféréssel kell rendelkezniük a tanúsítvány titkos kulcsához is.</span><span class="sxs-lookup"><span data-stu-id="117f5-145">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="117f5-146">A szolgáltatásnévvel való bejelentkezéshez szükség van a szolgáltatásnév létrehozásakor használt bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="117f5-146">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="117f5-147">A szolgáltatásnév létrehozása pillanatában aktív bérlő lekéréséhez futtassa a következő parancsot _rögtön_ a szolgáltatásnév létrehozása után:</span><span class="sxs-lookup"><span data-stu-id="117f5-147">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="117f5-148">Meglévő szolgáltatásnév lekérése</span><span class="sxs-lookup"><span data-stu-id="117f5-148">Get an existing service principal</span></span>

<span data-ttu-id="117f5-149">Az aktív bérlő szolgáltatásneveinek listája a [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) használatával kérhető le.</span><span class="sxs-lookup"><span data-stu-id="117f5-149">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="117f5-150">Ez a parancs alapértelmezés szerint a bérlő _összes_ szolgáltatásnevét visszaadja.</span><span class="sxs-lookup"><span data-stu-id="117f5-150">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="117f5-151">Nagy szervezetek esetén az eredmények lekérése hosszabb időt vehet igénybe.</span><span class="sxs-lookup"><span data-stu-id="117f5-151">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="117f5-152">Ehelyett javasoljuk, hogy használja valamelyik választható kiszolgálóoldali szűrőargumentumot:</span><span class="sxs-lookup"><span data-stu-id="117f5-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="117f5-153">A `-DisplayNameBeginsWith` a megadott értékkel megegyező _előtaggal_ rendelkező szolgáltatásneveket kéri le.</span><span class="sxs-lookup"><span data-stu-id="117f5-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="117f5-154">A szolgáltatásnév megjelenített neve a `-DisplayName` létrehozáskor megadott értéke.</span><span class="sxs-lookup"><span data-stu-id="117f5-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="117f5-155">A `-DisplayName` a _pontos egyezést mutató_ szolgáltatásneveket kéri le.</span><span class="sxs-lookup"><span data-stu-id="117f5-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="117f5-156">Szolgáltatásnév-szerepkörök kezelése</span><span class="sxs-lookup"><span data-stu-id="117f5-156">Manage service principal roles</span></span>

<span data-ttu-id="117f5-157">Az Azure PowerShell a következő parancsmagokat biztosítja a szerepkör-hozzárendelések kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="117f5-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="117f5-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="117f5-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="117f5-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="117f5-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="117f5-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="117f5-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="117f5-161">A jelszóalapú hitelesítéshez használt szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**.</span><span class="sxs-lookup"><span data-stu-id="117f5-161">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="117f5-162">Ez a szerepkör teljes körű engedélyekkel rendelkezik az Azure-fiókba való olvasásra, illetve írásra.</span><span class="sxs-lookup"><span data-stu-id="117f5-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="117f5-163">Az **Olvasó** szerepkör sokkal korlátozóbb, kizárólag olvasási hozzáférést biztosít.</span><span class="sxs-lookup"><span data-stu-id="117f5-163">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="117f5-164">További információ a szerepköralapú hozzáférés-vezérlésről (RBAC) és a szerepkörökről: [RBAC: Beépített szerepkörök](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="117f5-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="117f5-165">Példánk során az **Olvasó** szerepkört adjuk hozzá, és eltávolítjuk a **Közreműködő** szerepkört:</span><span class="sxs-lookup"><span data-stu-id="117f5-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="117f5-166">A szerepkör-hozzárendelési parancsmagok esetében nincs szükség a szolgáltatásnév objektumazonosítójára.</span><span class="sxs-lookup"><span data-stu-id="117f5-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="117f5-167">Ezek a hozzárendelt alkalmazásazonosítót használják, amelyet a rendszer a létrehozás során állít elő.</span><span class="sxs-lookup"><span data-stu-id="117f5-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="117f5-168">A szolgáltatásnév alkalmazásazonosítójának lekéréséhez használja a `Get-AzADServicePrincipal` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="117f5-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="117f5-169">Ha a fiókja nem jogosult szerepkörök hozzárendelésére, akkor egy hibaüzenet jelenik meg, miszerint a fiókja nem jogosult a Microsoft.Authorization/roleAssignments/write művelet végrehajtására.</span><span class="sxs-lookup"><span data-stu-id="117f5-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="117f5-170">A szerepkörök kezeléséhez vegye fel a kapcsolatot az Azure Active Directory-rendszergazdájával.</span><span class="sxs-lookup"><span data-stu-id="117f5-170">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="117f5-171">A szerepkör hozzáadása _nem_ korlátozza az előzetesen hozzárendelt engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="117f5-171">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="117f5-172">A szolgáltatásnév engedélyeinek korlátozása során a **Közreműködő** szerepkört el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="117f5-172">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="117f5-173">A módosítások a hozzárendelt szerepkörök listázásával ellenőrizhetők:</span><span class="sxs-lookup"><span data-stu-id="117f5-173">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="117f5-174">Bejelentkezés szolgáltatásnév használatával</span><span class="sxs-lookup"><span data-stu-id="117f5-174">Sign in using a service principal</span></span>

<span data-ttu-id="117f5-175">Tesztelje az új szolgáltatásnév hitelesítő adatait és engedélyeit a bejelentkezéssel.</span><span class="sxs-lookup"><span data-stu-id="117f5-175">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="117f5-176">A szolgáltatásnévvel történő bejelentkezéshez szükség van a szolgáltatásnévhez rendelt `applicationId` értékre és a létrehozáskori bérlőre.</span><span class="sxs-lookup"><span data-stu-id="117f5-176">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="117f5-177">Bejelentkezés szolgáltatásnévvel, jelszó használatával:</span><span class="sxs-lookup"><span data-stu-id="117f5-177">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="117f5-178">A tanúsítványalapú hitelesítéshez az Azure PowerShellnek egy helyi tanúsítványtárolóból kell információkat lekérnie a tanúsítvány ujjlenyomata alapján.</span><span class="sxs-lookup"><span data-stu-id="117f5-178">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="117f5-179">A tanúsítvány PowerShell által hozzáférhető tanúsítványtárolóba való importálásával kapcsolatos utasításokért lásd: [Bejelentkezés az Azure PowerShell-lel](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="117f5-179">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="117f5-180">Hitelesítő adatok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="117f5-180">Reset credentials</span></span>

<span data-ttu-id="117f5-181">Ha elfelejtette a szolgáltatásnévhez tartozó hitelesítő adatokat, a [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) parancsmaggal adhat hozzá új hitelesítő adatokat, véletlenszerű jelszóval.</span><span class="sxs-lookup"><span data-stu-id="117f5-181">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="117f5-182">Ez a parancsmag nem támogatja a felhasználó által megadott hitelesítő adatokat a jelszó visszaállításakor.</span><span class="sxs-lookup"><span data-stu-id="117f5-182">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="117f5-183">Javasoljuk, hogy az új hitelesítő adatok hozzárendelése előtt törölje a meglévő hitelesítő adatokat, nehogy azokkal jelentkezzen be.</span><span class="sxs-lookup"><span data-stu-id="117f5-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="117f5-184">Ehhez használja a [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) parancsmagot:</span><span class="sxs-lookup"><span data-stu-id="117f5-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="117f5-185">Hibaelhárítás</span><span class="sxs-lookup"><span data-stu-id="117f5-185">Troubleshooting</span></span>

<span data-ttu-id="117f5-186">Ha a _„New-AzADServicePrincipal: Már létezik egy másik objektum ezzel az értékkel az identifierUris tulajdonsághoz.”_ hibaüzenetet kapja, győződjön meg arról, hogy nem létezik ilyen nevű szolgáltatásnév.</span><span class="sxs-lookup"><span data-stu-id="117f5-186">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_, verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="117f5-187">Ha a meglévő szolgáltatásnévre már nincs rá szükség, az alábbi példa szerint eltávolíthatja.</span><span class="sxs-lookup"><span data-stu-id="117f5-187">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="117f5-188">Ez a hiba akkor is jelentkezhet, ha korábban már létrehozott szolgáltatásnevet egy Azure Active Directory-alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="117f5-188">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="117f5-189">Ha eltávolítja a szolgáltatásnevet, az alkalmazás továbbra is elérhető marad.</span><span class="sxs-lookup"><span data-stu-id="117f5-189">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="117f5-190">Ez az alkalmazás segít elkerülni, hogy másik szolgáltatásnevet hozzon létre ugyanazon a néven.</span><span class="sxs-lookup"><span data-stu-id="117f5-190">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="117f5-191">A következő példa alkalmazásával meggyőződhet arról, nem található ugyanolyan nevű Azure Active Directory-alkalmazás:</span><span class="sxs-lookup"><span data-stu-id="117f5-191">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="117f5-192">Ha létezik olyan azonos nevű alkalmazás, amelyre már nincs szükség, az alábbi példa szerint eltávolíthatja.</span><span class="sxs-lookup"><span data-stu-id="117f5-192">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="117f5-193">Ellenkező esetben válasszon egy alternatív nevet a létrehozni kívánt új szolgáltatásnév számára.</span><span class="sxs-lookup"><span data-stu-id="117f5-193">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>
