---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: e997013eb5646ca0f22904dd6fc68cf09a3ba228
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145410"
---
# <span data-ttu-id="c07bd-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c07bd-101">Connect-AzAccount</span></span>

## <span data-ttu-id="c07bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c07bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c07bd-103">Csatlakozzon az Azure-hoz egy hitelesített fiókkal az Az PowerShell-modulok parancsmagjaival való használathoz.</span><span class="sxs-lookup"><span data-stu-id="c07bd-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="c07bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c07bd-104">SYNTAX</span></span>

### <span data-ttu-id="c07bd-105">UserWithSubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c07bd-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c07bd-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c07bd-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c07bd-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="c07bd-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c07bd-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c07bd-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c07bd-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c07bd-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c07bd-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="c07bd-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c07bd-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c07bd-111">DESCRIPTION</span></span>

<span data-ttu-id="c07bd-112">A parancsmag egy hitelesített fiókkal csatlakozik az Azure-hoz az `Connect-AzAccount` Az PowerShell-modulok parancsmagjaival való használathoz.</span><span class="sxs-lookup"><span data-stu-id="c07bd-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="c07bd-113">Ezt a hitelesített fiókot csak az Azure Resource Manager-kérésekkel használhatja.</span><span class="sxs-lookup"><span data-stu-id="c07bd-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="c07bd-114">Ha hitelesített fiókot szeretne hozzáadni a Szolgáltatáskezeléshez, használja az `Add-AzureAccount` Azure PowerShell modul parancsmagját.</span><span class="sxs-lookup"><span data-stu-id="c07bd-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="c07bd-115">Ha nincs kontextus az aktuális felhasználóhoz, a felhasználó környezetlistát az első 25 előfizetésük kontextusával tölti ki a rendszer.</span><span class="sxs-lookup"><span data-stu-id="c07bd-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="c07bd-116">A felhasználóhoz létrehozott környezetek listáját a futtatás után `Get-AzContext -ListAvailable` használhatja.</span><span class="sxs-lookup"><span data-stu-id="c07bd-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="c07bd-117">A környezetfüggő sokaság kihagyása érdekében adja meg a **SkipContextPopulation** kapcsoló paramétert.</span><span class="sxs-lookup"><span data-stu-id="c07bd-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="c07bd-118">A parancsmag végrehajtása után lecsatlakozhat egy Azure-fiókról. `Disconnect-AzAccount`</span><span class="sxs-lookup"><span data-stu-id="c07bd-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="c07bd-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c07bd-119">EXAMPLES</span></span>

### <span data-ttu-id="c07bd-120">1. példa: Csatlakozás Azure-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="c07bd-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="c07bd-121">Ez a példa egy Azure-fiókhoz kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="c07bd-121">This example connects to an Azure account.</span></span> <span data-ttu-id="c07bd-122">Meg kell adnia egy Microsoft-fiókot vagy szervezeti azonosítót.</span><span class="sxs-lookup"><span data-stu-id="c07bd-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="c07bd-123">Ha a hitelesítő adatokhoz engedélyezve van a többtényezős hitelesítés, akkor az interaktív lehetőséggel vagy egyszerű szolgáltatás-hitelesítéssel kell bejelentkeznie.</span><span class="sxs-lookup"><span data-stu-id="c07bd-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c07bd-124">2. példa: (Csak Windows PowerShell 5.1 esetén) Csatlakozás az Azure-hoz szervezeti azonosítóval</span><span class="sxs-lookup"><span data-stu-id="c07bd-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="c07bd-125">Ez a forgatókönyv csak a Windows PowerShell 5.1-ben működik.</span><span class="sxs-lookup"><span data-stu-id="c07bd-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="c07bd-126">Az első parancs kéri a felhasználói hitelesítő adatokat, és tárolja őket a `$Credential` változóban.</span><span class="sxs-lookup"><span data-stu-id="c07bd-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="c07bd-127">A második parancs az Ebben tárolt hitelesítő adatokkal csatlakozik egy Azure-fiókhoz. `$Credential`</span><span class="sxs-lookup"><span data-stu-id="c07bd-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="c07bd-128">Ez a fiók szervezeti azonosítóval hitelesíthető az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="c07bd-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c07bd-129">3. példa: Csatlakozás az Azure-hoz egyszerű szolgáltatásfiók használatával</span><span class="sxs-lookup"><span data-stu-id="c07bd-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="c07bd-130">Az első parancs kéri a szolgáltatáshoz szükséges egyszerű hitelesítő adatokat, és tárolja őket a `$Credential` változóban.</span><span class="sxs-lookup"><span data-stu-id="c07bd-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="c07bd-131">Amikor a rendszer kéri, adja meg a felhasználónév és a szolgáltatás egyszerű kódjának azonosítóját jelszóként.</span><span class="sxs-lookup"><span data-stu-id="c07bd-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="c07bd-132">A második parancs a megadott Azure-bérlőt a változóban tárolt egyszerű szolgáltatás hitelesítő adataival köti `$Credential` össze.</span><span class="sxs-lookup"><span data-stu-id="c07bd-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="c07bd-133">A **ServicePrincipal kapcsoló** paramétere azt jelzi, hogy a fiók egyszerű szolgáltatásnévként van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="c07bd-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c07bd-134">4. példa: Interaktív bejelentkezés használata egy adott bérlőhöz és előfizetéshez való csatlakozáshoz</span><span class="sxs-lookup"><span data-stu-id="c07bd-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="c07bd-135">Ez a példa csatlakozik egy Azure-fiókhoz a megadott bérlői fiókkal és előfizetéssel.</span><span class="sxs-lookup"><span data-stu-id="c07bd-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c07bd-136">5. példa: Csatlakozás felügyelt szolgáltatás-identitás használatával</span><span class="sxs-lookup"><span data-stu-id="c07bd-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="c07bd-137">Ez a példa a gazdakörnyezet Felügyelt szolgáltatás-identitásával (MSI) csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="c07bd-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="c07bd-138">Például egy olyan virtuális gépről jelentkezik be az Azure-ba, amely rendelkezik hozzárendelt MSI-vel.</span><span class="sxs-lookup"><span data-stu-id="c07bd-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c07bd-139">6. példa: Csatlakozás Felügyelt szolgáltatás-identitás bejelentkezéssel és ClientId azonosítóval</span><span class="sxs-lookup"><span data-stu-id="c07bd-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="c07bd-140">Ez a példa a **myUserAssignedIdentity felügyelt szolgáltatás-identitásával kapcsolódik.**</span><span class="sxs-lookup"><span data-stu-id="c07bd-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="c07bd-141">Hozzáadja a felhasználó által hozzárendelt identitást a virtuális géphez, majd a felhasználó által hozzárendelt identitás ClientId azonosítóját használva csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="c07bd-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="c07bd-142">További információt a felügyelt identitások konfigurálása [Azure-erőforrásokhoz Azure VM-en.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)</span><span class="sxs-lookup"><span data-stu-id="c07bd-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c07bd-143">7. példa: Csatlakozás tanúsítványok használatával</span><span class="sxs-lookup"><span data-stu-id="c07bd-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="c07bd-144">Ez a példa tanúsítványalapú egyszerű szolgáltatás-hitelesítéssel csatlakozik egy Azure-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="c07bd-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="c07bd-145">A hitelesítéshez használt egyszerű szolgáltatásnévnek a megadott tanúsítvánnyal kell létrejönnie.</span><span class="sxs-lookup"><span data-stu-id="c07bd-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="c07bd-146">Az önaírt tanúsítványok létrehozásáról és az engedélyek hozzárendelésével kapcsolatos további információkért lásd: Egyszerű szolgáltatásnév létrehozása tanúsítványsal az [Azure PowerShell használatával](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="c07bd-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## <span data-ttu-id="c07bd-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c07bd-147">PARAMETERS</span></span>

### <span data-ttu-id="c07bd-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="c07bd-148">-AccessToken</span></span>

<span data-ttu-id="c07bd-149">Hozzáférési jogkivonatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c07bd-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="c07bd-150">A hozzáférési jogkivonatok a hitelesítő adatok egy típusa.</span><span class="sxs-lookup"><span data-stu-id="c07bd-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="c07bd-151">A bizalmas kezelés érdekében a megfelelő biztonsági óvintézkedést kell alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="c07bd-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="c07bd-152">A hozzáférési jogkivonatok időtúllépést is okozhatnak, és megakadályozhatják a hosszú ideig futó feladatok elvégzését.</span><span class="sxs-lookup"><span data-stu-id="c07bd-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="c07bd-153">-AccountId</span></span>

<span data-ttu-id="c07bd-154">A hozzáférési jogkivonat fiókazonosítója az **AccessToken** paraméterkészletében.</span><span class="sxs-lookup"><span data-stu-id="c07bd-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="c07bd-155">A felügyelt szolgáltatás fiókazonosítója **a ManagedService paraméterkészletében.**</span><span class="sxs-lookup"><span data-stu-id="c07bd-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="c07bd-156">Lehet felügyelt szolgáltatáserőforrás-azonosító vagy társított ügyfélazonosító.</span><span class="sxs-lookup"><span data-stu-id="c07bd-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="c07bd-157">A rendszer által hozzárendelt identitás használatához hagyja üresen ezt a mezőt.</span><span class="sxs-lookup"><span data-stu-id="c07bd-157">To use the system assigned identity, leave this field blank.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c07bd-158">-ApplicationId</span></span>

<span data-ttu-id="c07bd-159">A szolgáltatásnév alkalmazásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="c07bd-159">Application ID of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="c07bd-160">-CertificateThumbprint</span></span>

<span data-ttu-id="c07bd-161">Tanúsítvány kivonata vagy thumbprint.</span><span class="sxs-lookup"><span data-stu-id="c07bd-161">Certificate Hash or Thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="c07bd-162">-ContextName</span></span>

<span data-ttu-id="c07bd-163">A bejelentkezés alapértelmezett Azure-környezetének neve.</span><span class="sxs-lookup"><span data-stu-id="c07bd-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="c07bd-164">Az Azure környezetekkel kapcsolatos további információkért lásd az [Azure PowerShell környezetobjektumokat.](/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="c07bd-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-165">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="c07bd-165">-Credential</span></span>

<span data-ttu-id="c07bd-166">Egy **PSCredential objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="c07bd-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="c07bd-167">A **PSCredential** objektumról a következőt írja be: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="c07bd-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="c07bd-168">A **PSCredential** objektum a szervezeti azonosítók felhasználói azonosítóját és jelszavát, illetve a szolgáltatásnévhez használt hitelesítő adatok azonosítóját és titkos azonosítóját biztosítja.</span><span class="sxs-lookup"><span data-stu-id="c07bd-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07bd-169">-DefaultProfile</span></span>

<span data-ttu-id="c07bd-170">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c07bd-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c07bd-171">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c07bd-171">-Environment</span></span>

<span data-ttu-id="c07bd-172">Az Azure-fiókot tartalmazó környezet.</span><span class="sxs-lookup"><span data-stu-id="c07bd-172">Environment containing the Azure account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-173">-Force</span><span class="sxs-lookup"><span data-stu-id="c07bd-173">-Force</span></span>

<span data-ttu-id="c07bd-174">A meglévő környezet felülírása ugyanazokkal a névvel, és nem kell rákérdezni.</span><span class="sxs-lookup"><span data-stu-id="c07bd-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="c07bd-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="c07bd-175">-GraphAccessToken</span></span>

<span data-ttu-id="c07bd-176">AccessToken for Graph Service.</span><span class="sxs-lookup"><span data-stu-id="c07bd-176">AccessToken for Graph Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-177">-Identity</span><span class="sxs-lookup"><span data-stu-id="c07bd-177">-Identity</span></span>

<span data-ttu-id="c07bd-178">Bejelentkezés felügyelt szolgáltatás-identitás használatával.</span><span class="sxs-lookup"><span data-stu-id="c07bd-178">Login using a Managed Service Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="c07bd-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="c07bd-180">AccessToken a KeyVault szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="c07bd-180">AccessToken for KeyVault Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="c07bd-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="c07bd-182">Elavult.</span><span class="sxs-lookup"><span data-stu-id="c07bd-182">Obsolete.</span></span> <span data-ttu-id="c07bd-183">Ha testre szabott MSI-végpontot használ, állítsa be a környezeti MSI_ENDPOINT, például " http://localhost:50342/oauth2/token ".</span><span class="sxs-lookup"><span data-stu-id="c07bd-183">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".</span></span> <span data-ttu-id="c07bd-184">A felügyelt szolgáltatás állomásneve.</span><span class="sxs-lookup"><span data-stu-id="c07bd-184">Host name for the managed service.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-185">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="c07bd-185">-ManagedServicePort</span></span>

<span data-ttu-id="c07bd-186">Elavult.</span><span class="sxs-lookup"><span data-stu-id="c07bd-186">Obsolete.</span></span> <span data-ttu-id="c07bd-187">Ha testre szabott MSI-végpontot használ, állítsa be a környezeti MSI_ENDPOINT, például " http://localhost:50342/oauth2/token ". A felügyelt szolgáltatás portszáma.</span><span class="sxs-lookup"><span data-stu-id="c07bd-187">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".Port number for the managed service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-188">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="c07bd-188">-ManagedServiceSecret</span></span>

<span data-ttu-id="c07bd-189">Elavult.</span><span class="sxs-lookup"><span data-stu-id="c07bd-189">Obsolete.</span></span> <span data-ttu-id="c07bd-190">Ha testre szabott MSI-titkos halmazt használ, állítsa be a környezeti MSI_SECRET.</span><span class="sxs-lookup"><span data-stu-id="c07bd-190">To use customized MSI secret, please set environment variable MSI_SECRET.</span></span> <span data-ttu-id="c07bd-191">Token a felügyelt szolgáltatásba való bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="c07bd-191">Token for the managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-192">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="c07bd-192">-MaxContextPopulation</span></span>

<span data-ttu-id="c07bd-193">Az előfizetés maximális száma a környezetek feltöltéséhez bejelentkezés után.</span><span class="sxs-lookup"><span data-stu-id="c07bd-193">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="c07bd-194">Az alapértelmezett érték 25.</span><span class="sxs-lookup"><span data-stu-id="c07bd-194">Default is 25.</span></span> <span data-ttu-id="c07bd-195">Az összes előfizetés környezetbe való feltöltéséhez állítsa -1-re.</span><span class="sxs-lookup"><span data-stu-id="c07bd-195">To populate all subscriptions to contexts, set to -1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-196">-Scope</span><span class="sxs-lookup"><span data-stu-id="c07bd-196">-Scope</span></span>

<span data-ttu-id="c07bd-197">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="c07bd-197">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-198">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c07bd-198">-ServicePrincipal</span></span>

<span data-ttu-id="c07bd-199">Azt jelzi, hogy a fiók hitelesítése egyszerű szolgáltatásnévvel megadott hitelesítő adatokkal történik.</span><span class="sxs-lookup"><span data-stu-id="c07bd-199">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-200">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="c07bd-200">-SkipContextPopulation</span></span>

<span data-ttu-id="c07bd-201">Kihagyja a környezet sokaságát, ha nem talál környezeteket.</span><span class="sxs-lookup"><span data-stu-id="c07bd-201">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="c07bd-202">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="c07bd-202">-SkipValidation</span></span>

<span data-ttu-id="c07bd-203">Hozzáférési jogkivonat érvényesítésének kihagyása.</span><span class="sxs-lookup"><span data-stu-id="c07bd-203">Skip validation for access token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-204">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="c07bd-204">-Subscription</span></span>

<span data-ttu-id="c07bd-205">Előfizetés neve vagy azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c07bd-205">Subscription Name or ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-206">-Tenant</span><span class="sxs-lookup"><span data-stu-id="c07bd-206">-Tenant</span></span>

<span data-ttu-id="c07bd-207">Nem kötelező bérlő neve vagy azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c07bd-207">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="c07bd-208">Az aktuális API korlátai miatt bérlőazonosítót kell használnia a bérlő neve helyett, amikor vállalati vállalati (B2B) fiókhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="c07bd-208">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-209">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="c07bd-209">-UseDeviceAuthentication</span></span>

<span data-ttu-id="c07bd-210">Böngészővezérlő helyett használjon eszközkód-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="c07bd-210">Use device code authentication instead of a browser control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-211">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c07bd-211">-Confirm</span></span>

<span data-ttu-id="c07bd-212">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c07bd-212">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c07bd-213">-WhatIf</span></span>

<span data-ttu-id="c07bd-214">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c07bd-214">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c07bd-215">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c07bd-215">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07bd-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07bd-216">CommonParameters</span></span>
<span data-ttu-id="c07bd-217">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c07bd-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07bd-218">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c07bd-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07bd-219">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c07bd-219">INPUTS</span></span>

### <span data-ttu-id="c07bd-220">System.String</span><span class="sxs-lookup"><span data-stu-id="c07bd-220">System.String</span></span>

## <span data-ttu-id="c07bd-221">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c07bd-221">OUTPUTS</span></span>

### <span data-ttu-id="c07bd-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="c07bd-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="c07bd-223">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c07bd-223">NOTES</span></span>

## <span data-ttu-id="c07bd-224">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c07bd-224">RELATED LINKS</span></span>
