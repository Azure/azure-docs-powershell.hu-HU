---
title: Azure-beli szolgáltatásnevek használata az Azure PowerShell-lel
description: Megtudhatja, hogyan hozhat létre és használhat szolgáltatásneveket az Azure PowerShell-lel.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 2e4ae053df3e3a22e22ec40206cbce98ab5d6ff8
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83384946"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="90c7e-103">Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="90c7e-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="90c7e-104">Az Azure-szolgáltatásokat használó automatizált eszközöknek mindig korlátozott hozzáférésűeknek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="90c7e-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="90c7e-105">Az Azure szolgáltatásneveket használ ahelyett, hogy az alkalmazásokat teljes körű jogosultsággal rendelkező felhasználóként jelentkeztetné be.</span><span class="sxs-lookup"><span data-stu-id="90c7e-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="90c7e-106">Az Azure-beli szolgáltatásnevek olyan identitások, amelyekkel az alkalmazások, üzemeltetett szolgáltatások és automatizált eszközök hozzáférhetnek az Azure erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="90c7e-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="90c7e-107">A hozzáférést a szolgáltatásnévhez rendelt szerepkörök korlátozzák, így Ön szabhatja meg, hogy mely erőforrások, mely szinten legyenek hozzáférhetők.</span><span class="sxs-lookup"><span data-stu-id="90c7e-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="90c7e-108">Biztonsági okokból az automatizált eszközök esetében minden esetben ajánlott a szolgáltatásnevek használata a felhasználói identitással való bejelentkezés helyett.</span><span class="sxs-lookup"><span data-stu-id="90c7e-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="90c7e-109">A cikk bemutatja a szolgáltatásnevek létrehozásának, adatlekérésének és visszaállításának lépéseit az Azure PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="90c7e-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="90c7e-110">Egyszerű szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="90c7e-110">Create a service principal</span></span>

<span data-ttu-id="90c7e-111">Hozzon létre egy szolgáltatásnevet a [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="90c7e-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="90c7e-112">A szolgáltatásnév létrehozása során Ön választhatja ki, hogy az milyen típusú bejelentkezési hitelesítést használjon.</span><span class="sxs-lookup"><span data-stu-id="90c7e-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="90c7e-113">Ha a fiókja nem rendelkezik engedéllyel a szolgáltatásnév létrehozásához, akkor a `New-AzADServicePrincipal` az alábbi hibaüzenet adja vissza: „Nincs megfelelő jogosultsága a művelet elvégzéséhez”.</span><span class="sxs-lookup"><span data-stu-id="90c7e-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="90c7e-114">A szolgáltatásnév létrehozásához vegye fel a kapcsolatot az Azure Active Directory-rendszergazdájával.</span><span class="sxs-lookup"><span data-stu-id="90c7e-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="90c7e-115">A szolgáltatásnevek esetében kétféle hitelesítési típus érhető el: Jelszóalapú hitelesítés és tanúsítványalapú hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="90c7e-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="90c7e-116">Jelszóalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="90c7e-116">Password-based authentication</span></span>

<span data-ttu-id="90c7e-117">Egyéb hitelesítési paraméter hiányában a rendszer jelszóalapú hitelesítést használ, és véletlenszerű jelszót hoz létre az Ön számára.</span><span class="sxs-lookup"><span data-stu-id="90c7e-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="90c7e-118">Ez az ajánlott módszer, ha jelszóalapú hitelesítést szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="90c7e-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="90c7e-119">A visszaadott objektum tartalmazza a `Secret` tagot, amely egy, a létrehozott jelszót tartalmazó `SecureString`.</span><span class="sxs-lookup"><span data-stu-id="90c7e-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="90c7e-120">Győződjön meg róla, hogy a szolgáltatásnév hitelesítéséhez használt értéket biztonságos helyen tárolja.</span><span class="sxs-lookup"><span data-stu-id="90c7e-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="90c7e-121">Ennek értéke __nem__ fog megjelenni a konzol kimenetén.</span><span class="sxs-lookup"><span data-stu-id="90c7e-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="90c7e-122">Ha elvesztette a jelszót, [állítsa vissza a szolgáltatásnév hitelesítő adatait](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="90c7e-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="90c7e-123">A következő kód lehetővé teszi a titkos kód exportálását:</span><span class="sxs-lookup"><span data-stu-id="90c7e-123">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="90c7e-124">Felhasználó által megadott jelszavak esetén a `-PasswordCredential` argumentumhoz `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objektumokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="90c7e-124">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="90c7e-125">Az objektumoknak érvényes `StartDate` és `EndDate` paraméterekkel kell rendelkezniük, és egyszerű szöveges `Password` értékre van szükségük.</span><span class="sxs-lookup"><span data-stu-id="90c7e-125">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="90c7e-126">A jelszó létrehozása során kövesse az [Azure Active Directory-jelszavakra vonatkozó szabályokat és korlátozásokat](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="90c7e-126">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="90c7e-127">Ne használjon gyenge vagy korábban már használt jelszót.</span><span class="sxs-lookup"><span data-stu-id="90c7e-127">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="90c7e-128">A `New-AzADServicePrincipal` által visszaadott objektum tartalmazza az `Id` és a `DisplayName` tagokat, amelyek közül bármelyik használható a szolgáltatásnévvel való bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="90c7e-128">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="90c7e-129">A szolgáltatásnévvel való bejelentkezéshez szükség van a szolgáltatásnév létrehozásakor használt bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="90c7e-129">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="90c7e-130">A szolgáltatásnév létrehozása pillanatában aktív bérlő lekéréséhez futtassa a következő parancsot __rögtön__ a szolgáltatásnév létrehozása után:</span><span class="sxs-lookup"><span data-stu-id="90c7e-130">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="90c7e-131">Tanúsítványalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="90c7e-131">Certificate-based authentication</span></span>

<span data-ttu-id="90c7e-132">A tanúsítványalapú hitelesítést használó szolgáltatásnevek létrehozása a `-CertValue` paraméterrel történik.</span><span class="sxs-lookup"><span data-stu-id="90c7e-132">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="90c7e-133">E paraméter esetében a nyilvános tanúsítvány base64-kódolású ASCII sztringjére van szükség.</span><span class="sxs-lookup"><span data-stu-id="90c7e-133">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="90c7e-134">Ez egy PEM-fájl vagy egy szöveges kódolású CRT- vagy CER-fájl lehet.</span><span class="sxs-lookup"><span data-stu-id="90c7e-134">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="90c7e-135">A bináris kódolású nyilvános tanúsítványok nem támogatottak.</span><span class="sxs-lookup"><span data-stu-id="90c7e-135">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="90c7e-136">Az alábbi utasítások végrehajtása során azt feltételezzük, hogy a tanúsítvány már rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="90c7e-136">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="90c7e-137">A `-KeyCredential` paraméter is használható, amelyhez `PSADKeyCredential` objektumokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="90c7e-137">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="90c7e-138">Az objektumoknak érvényes `StartDate` és `EndDate` paraméterekkel kell rendelkezniük, a `CertValue` tag esetében pedig a nyilvános tanúsítvány base64-kódolású ASCII sztringjét kell megadni.</span><span class="sxs-lookup"><span data-stu-id="90c7e-138">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="90c7e-139">A `New-AzADServicePrincipal` által visszaadott objektum tartalmazza az `Id` és a `DisplayName` tagokat, amelyek közül bármelyik használható a szolgáltatásnévvel való bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="90c7e-139">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="90c7e-140">A szolgáltatásnévvel bejelentkező ügyfeleknek hozzáféréssel kell rendelkezniük a tanúsítvány titkos kulcsához is.</span><span class="sxs-lookup"><span data-stu-id="90c7e-140">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="90c7e-141">A szolgáltatásnévvel való bejelentkezéshez szükség van a szolgáltatásnév létrehozásakor használt bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="90c7e-141">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="90c7e-142">A szolgáltatásnév létrehozása pillanatában aktív bérlő lekéréséhez futtassa a következő parancsot __rögtön__ a szolgáltatásnév létrehozása után:</span><span class="sxs-lookup"><span data-stu-id="90c7e-142">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="90c7e-143">Meglévő szolgáltatásnév lekérése</span><span class="sxs-lookup"><span data-stu-id="90c7e-143">Get an existing service principal</span></span>

<span data-ttu-id="90c7e-144">A jelenleg aktív bérlő szolgáltatásneveinek listája a [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) használatával kérhető le.</span><span class="sxs-lookup"><span data-stu-id="90c7e-144">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="90c7e-145">Ez a parancs alapértelmezés szerint a bérlő __összes__ szolgáltatásnevét visszaadja, így nagy szervezetek esetén az eredmények lekérése hosszabb időt vehet igénybe.</span><span class="sxs-lookup"><span data-stu-id="90c7e-145">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="90c7e-146">Ehelyett javasoljuk, hogy használja valamelyik választható kiszolgálóoldali szűrőargumentumot:</span><span class="sxs-lookup"><span data-stu-id="90c7e-146">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="90c7e-147">A `-DisplayNameBeginsWith` a megadott értékkel megegyező _előtaggal_ rendelkező szolgáltatásneveket kéri le.</span><span class="sxs-lookup"><span data-stu-id="90c7e-147">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="90c7e-148">A szolgáltatásnév megjelenített neve a `-DisplayName` létrehozáskor megadott értéke.</span><span class="sxs-lookup"><span data-stu-id="90c7e-148">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="90c7e-149">A `-DisplayName` a _pontos egyezést mutató_ szolgáltatásneveket kéri le.</span><span class="sxs-lookup"><span data-stu-id="90c7e-149">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="90c7e-150">Szolgáltatásnév-szerepkörök kezelése</span><span class="sxs-lookup"><span data-stu-id="90c7e-150">Manage service principal roles</span></span>

<span data-ttu-id="90c7e-151">Az Azure PowerShell a következő parancsmagokat biztosítja a szerepkör-hozzárendelések kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="90c7e-151">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="90c7e-152">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="90c7e-152">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="90c7e-153">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="90c7e-153">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="90c7e-154">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="90c7e-154">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="90c7e-155">A szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**.</span><span class="sxs-lookup"><span data-stu-id="90c7e-155">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="90c7e-156">Ez a szerepkör teljes körű engedélyekkel rendelkezik az Azure-fiókba való olvasásra, illetve írásra.</span><span class="sxs-lookup"><span data-stu-id="90c7e-156">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="90c7e-157">Az **Olvasó** szerepkör sokkal korlátozóbb, kizárólag olvasási hozzáférést biztosít.</span><span class="sxs-lookup"><span data-stu-id="90c7e-157">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="90c7e-158">További információ a szerepköralapú hozzáférés-vezérlésről (RBAC) és a szerepkörökről: [RBAC: Beépített szerepkörök](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="90c7e-158">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="90c7e-159">Példánk során az **Olvasó** szerepkört adjuk hozzá, és eltávolítjuk a **Közreműködő** szerepkört:</span><span class="sxs-lookup"><span data-stu-id="90c7e-159">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="90c7e-160">A szerepkör-hozzárendelési parancsmagok esetében nincs szükség a szolgáltatásnév objektumazonosítójára.</span><span class="sxs-lookup"><span data-stu-id="90c7e-160">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="90c7e-161">Ezek a hozzárendelt alkalmazásazonosítót használják, amelyet a rendszer a létrehozás során állít elő.</span><span class="sxs-lookup"><span data-stu-id="90c7e-161">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="90c7e-162">A szolgáltatásnév alkalmazásazonosítójának lekéréséhez használja a `Get-AzADServicePrincipal` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="90c7e-162">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="90c7e-163">Ha a fiókja nem jogosult szerepkörök hozzárendelésére, akkor egy hibaüzenet jelenik meg, miszerint a fiókja nem jogosult a 'Microsoft.Authorization/roleAssignments/write' művelet végrehajtására. A szerepkörök kezeléséhez vegye fel a kapcsolatot az Azure Active Directory-rendszergazdájával.</span><span class="sxs-lookup"><span data-stu-id="90c7e-163">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="90c7e-164">A szerepkör hozzáadása _nem_ korlátozza az előzetesen hozzárendelt engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="90c7e-164">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="90c7e-165">A szolgáltatásnév engedélyeinek korlátozása során a __Közreműködő__ szerepkört el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="90c7e-165">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="90c7e-166">A módosítások a hozzárendelt szerepkörök listázásával ellenőrizhetők:</span><span class="sxs-lookup"><span data-stu-id="90c7e-166">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="90c7e-167">Bejelentkezés szolgáltatásnév használatával</span><span class="sxs-lookup"><span data-stu-id="90c7e-167">Sign in using a service principal</span></span>

<span data-ttu-id="90c7e-168">Tesztelje az új szolgáltatásnév hitelesítő adatait és engedélyeit a bejelentkezéssel.</span><span class="sxs-lookup"><span data-stu-id="90c7e-168">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="90c7e-169">A szolgáltatásnévvel történő bejelentkezéshez szükség van a szolgáltatásnévhez rendelt `applicationId` értékre és a létrehozáskori bérlőre.</span><span class="sxs-lookup"><span data-stu-id="90c7e-169">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="90c7e-170">Bejelentkezés szolgáltatásnévvel, jelszó használatával:</span><span class="sxs-lookup"><span data-stu-id="90c7e-170">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="90c7e-171">A tanúsítványalapú hitelesítéshez az Azure PowerShellnek egy helyi tanúsítványtárolóból kell információkat lekérnie a tanúsítvány ujjlenyomata alapján.</span><span class="sxs-lookup"><span data-stu-id="90c7e-171">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="90c7e-172">A tanúsítvány PowerShell által hozzáférhető tanúsítványtárolóba való importálásával kapcsolatos utasításokért lásd: [Bejelentkezés az Azure PowerShell-lel](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="90c7e-172">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="90c7e-173">Hitelesítő adatok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="90c7e-173">Reset credentials</span></span>

<span data-ttu-id="90c7e-174">Ha elfelejtette a szolgáltatásnévhez tartozó hitelesítő adatokat, a [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) parancsmaggal adhat hozzá új hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="90c7e-174">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="90c7e-175">E parancsmag esetében ugyanazokra a hitelesítő argumentumokra és típusokra van szükség, mint a `New-AzADServicePrincipal` esetében.</span><span class="sxs-lookup"><span data-stu-id="90c7e-175">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="90c7e-176">Ha nincs megadva hitelesítő argumentum, egy új `PasswordCredential` jön létre, véletlenszerű jelszóval.</span><span class="sxs-lookup"><span data-stu-id="90c7e-176">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90c7e-177">Javasoljuk, hogy az új hitelesítő adatok hozzárendelése előtt törölje a meglévő hitelesítő adatokat, nehogy azokkal jelentkezzen be.</span><span class="sxs-lookup"><span data-stu-id="90c7e-177">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="90c7e-178">Ehhez használja a [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) parancsmagot:</span><span class="sxs-lookup"><span data-stu-id="90c7e-178">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
