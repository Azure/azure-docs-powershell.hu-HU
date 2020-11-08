---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 32a5c4ac20d584c26d95724a3f4ab4630504fb6d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013031"
---
# <span data-ttu-id="9f67a-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="9f67a-101">Connect-AzAccount</span></span>

## <span data-ttu-id="9f67a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f67a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f67a-103">Csatlakozás az Azure-hoz hitelesített fiókkal a PowerShell-modulokból származó parancsmagokkal való használathoz.</span><span class="sxs-lookup"><span data-stu-id="9f67a-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="9f67a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f67a-104">SYNTAX</span></span>

### <span data-ttu-id="9f67a-105">UserWithSubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f67a-105">UserWithSubscriptionId (Default)</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>]
 [-ContextName <String>] [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f67a-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f67a-106">ServicePrincipalWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> -ServicePrincipal
 -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f67a-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="9f67a-107">UserWithCredential</span></span>

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f67a-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f67a-108">ServicePrincipalCertificateWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f67a-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f67a-109">AccessTokenWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f67a-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="9f67a-110">ManagedServiceLogin</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] -Identity
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>]
 [-ManagedServiceSecret <SecureString>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f67a-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f67a-111">DESCRIPTION</span></span>

<span data-ttu-id="9f67a-112">A `Connect-AzAccount` parancsmag hitelesített fiókkal csatlakozik az Azure-hoz a PowerShell modulokból származó parancsmagokkal való használatra.</span><span class="sxs-lookup"><span data-stu-id="9f67a-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="9f67a-113">Ezt a hitelesített fiókot csak az Azure Resource Manager kérelmei használhatják.</span><span class="sxs-lookup"><span data-stu-id="9f67a-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="9f67a-114">Ha egy hitelesített fiókot szeretne hozzáadni a szolgáltatás-kezeléshez, használja a `Add-AzureAccount` parancsmagot az Azure PowerShell-modulból.</span><span class="sxs-lookup"><span data-stu-id="9f67a-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="9f67a-115">Ha az aktuális felhasználóhoz nem tartozik környezet, a felhasználó helyi listája az első 25 előfizetésük mindegyikéhez környezettel van feltöltve.</span><span class="sxs-lookup"><span data-stu-id="9f67a-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="9f67a-116">A felhasználóhoz létrehozott környezetek listája a következő futtatásával érhető el `Get-AzContext -ListAvailable` .</span><span class="sxs-lookup"><span data-stu-id="9f67a-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="9f67a-117">A környezeti sokaság kihagyásához adja meg a **SkipContextPopulation** kapcsoló paramétert.</span><span class="sxs-lookup"><span data-stu-id="9f67a-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="9f67a-118">A parancsmag végrehajtása után az Azure-fiók segítségével leválaszthatja az Azure-fiókját `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="9f67a-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="9f67a-119">Példák</span><span class="sxs-lookup"><span data-stu-id="9f67a-119">EXAMPLES</span></span>

### <span data-ttu-id="9f67a-120">1. példa: csatlakozás Azure-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="9f67a-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="9f67a-121">Ez a példa egy Azure-fiókhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="9f67a-121">This example connects to an Azure account.</span></span> <span data-ttu-id="9f67a-122">Biztosítania kell a Microsoft-fiók vagy a szervezeti azonosító hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="9f67a-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="9f67a-123">Ha a többtényezős hitelesítés engedélyezve van a hitelesítő adataiban, be kell jelentkeznie az interaktív beállítással vagy a Principal Authentication szolgáltatás használatával.</span><span class="sxs-lookup"><span data-stu-id="9f67a-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="9f67a-124">2. példa: (csak a Windows PowerShell 5,1) csatlakozás az Azure-hoz szervezeti azonosító hitelesítő adatokkal</span><span class="sxs-lookup"><span data-stu-id="9f67a-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="9f67a-125">Ez a forgatókönyv csak a Windows PowerShell 5,1-ban működik.</span><span class="sxs-lookup"><span data-stu-id="9f67a-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="9f67a-126">Az első parancs a felhasználói hitelesítő adatok megadását kéri, és tárolja őket a `$Credential` változóban.</span><span class="sxs-lookup"><span data-stu-id="9f67a-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="9f67a-127">A második parancs az Azure-fiókhoz csatlakozik a tárolt hitelesítő adatok használatával `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="9f67a-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="9f67a-128">Ez a fiók a szervezeti azonosító hitelesítő adataival hitelesíti az Azure-t.</span><span class="sxs-lookup"><span data-stu-id="9f67a-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="9f67a-129">3. példa: csatlakozás az Azure-hoz egy egyszerű szolgáltatási fiók segítségével</span><span class="sxs-lookup"><span data-stu-id="9f67a-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="9f67a-130">Az első parancssori hitelesítő adatok megadását kéri a rendszer, és tárolja őket a `$Credential` változóban.</span><span class="sxs-lookup"><span data-stu-id="9f67a-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="9f67a-131">Adja meg az alkalmazás AZONOSÍTÓját a Felhasználónév és a szolgáltatás fő titka jelszavának, amikor a rendszer kéri.</span><span class="sxs-lookup"><span data-stu-id="9f67a-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="9f67a-132">A második parancs a megadott Azure-bérlőt a változóban tárolt szolgáltatás-fő hitelesítő adatokkal köti össze `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="9f67a-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="9f67a-133">A **ServicePrincipal** kapcsoló paraméter azt jelzi, hogy a fiók a szolgáltatás-megbízóként van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="9f67a-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="9f67a-134">Példa 4: interaktív bejelentkezés használata egy adott bérlőhöz vagy előfizetéshez való csatlakozáshoz</span><span class="sxs-lookup"><span data-stu-id="9f67a-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="9f67a-135">Ez a példa egy Azure-fiókhoz csatlakozik a megadott bérlői fiókkal és előfizetéssel.</span><span class="sxs-lookup"><span data-stu-id="9f67a-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="9f67a-136">5. példa: csatlakozás felügyelt szolgáltatás identitásának használatával</span><span class="sxs-lookup"><span data-stu-id="9f67a-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="9f67a-137">Ez a példa a Host-környezet felügyelt szolgáltatás identitását (MSI) használja.</span><span class="sxs-lookup"><span data-stu-id="9f67a-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="9f67a-138">Az Azure-ba például egy olyan virtuális gépet kell bejelentkeznie, amelynek van hozzárendelve MSI-je.</span><span class="sxs-lookup"><span data-stu-id="9f67a-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="9f67a-139">6. példa: a felügyelt szolgáltatás személyazonossági bejelentkezésének és ClientId csatlakoztatása</span><span class="sxs-lookup"><span data-stu-id="9f67a-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="9f67a-140">Ez a példa a **MyUserAssignedIdentity** felügyelt szolgáltatás identitását használja.</span><span class="sxs-lookup"><span data-stu-id="9f67a-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="9f67a-141">Hozzáadja a felhasználóhoz rendelt identitást a virtuális géphez, majd a felhasználó által kiosztott identitás ClientId használja.</span><span class="sxs-lookup"><span data-stu-id="9f67a-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="9f67a-142">További információt a [felügyelt identitások beállítása az Azure-erőforrásokhoz Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)-ben című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9f67a-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

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

### <span data-ttu-id="9f67a-143">7. példa: csatlakozás tanúsítványok használatával</span><span class="sxs-lookup"><span data-stu-id="9f67a-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="9f67a-144">Ez a példa egy Azure-fiókhoz, a tanúsítvány-alapú egyszerű hitelesítés segítségével csatlakozik az Azure-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="9f67a-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="9f67a-145">A hitelesítéshez használt szolgáltatásnevet a megadott tanúsítvánnyal kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="9f67a-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="9f67a-146">Ha szeretne többet megtudni az önaláírt tanúsítványok létrehozásáról és az engedélyek hozzárendeléséről, olvassa el az [Azure PowerShell használata tanúsítvány](/azure/active-directory/develop/howto-authenticate-service-principal-powershell) segítségével című témakört.</span><span class="sxs-lookup"><span data-stu-id="9f67a-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

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

## <span data-ttu-id="9f67a-147">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f67a-147">PARAMETERS</span></span>

### <span data-ttu-id="9f67a-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="9f67a-148">-AccessToken</span></span>

<span data-ttu-id="9f67a-149">Az Access-tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f67a-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="9f67a-150">A hozzáférési tokenek a hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="9f67a-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="9f67a-151">A megfelelő biztonsági óvintézkedéseket a bizalmas megőrzés érdekében kell elvégeznie.</span><span class="sxs-lookup"><span data-stu-id="9f67a-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="9f67a-152">Az Access-tokenek is időtúllépést okoznak, és megakadályozhatják a hosszú ideig futó feladatok befejezését.</span><span class="sxs-lookup"><span data-stu-id="9f67a-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="9f67a-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="9f67a-153">-AccountId</span></span>

<span data-ttu-id="9f67a-154">Az **AccessToken** paraméterben megadott hozzáférési jogkivonat fiókneve.</span><span class="sxs-lookup"><span data-stu-id="9f67a-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="9f67a-155">A felügyelt szolgáltatáshoz tartozó fiókazonosító a **ManagedService** paraméterben.</span><span class="sxs-lookup"><span data-stu-id="9f67a-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="9f67a-156">Lehet felügyelt szolgáltatás-erőforrás azonosítója vagy a hozzá tartozó ügyfél-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9f67a-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="9f67a-157">Ha a rendszerhez rendelt identitást szeretné használni, hagyja üresen ezt a mezőt.</span><span class="sxs-lookup"><span data-stu-id="9f67a-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="9f67a-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9f67a-158">-ApplicationId</span></span>

<span data-ttu-id="9f67a-159">A szolgáltatás megbízójának alkalmazásspecifikus azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9f67a-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="9f67a-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="9f67a-160">-CertificateThumbprint</span></span>

<span data-ttu-id="9f67a-161">Tanúsítvány-kivonat vagy ujjlenyomat.</span><span class="sxs-lookup"><span data-stu-id="9f67a-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="9f67a-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="9f67a-162">-ContextName</span></span>

<span data-ttu-id="9f67a-163">A bejelentkezés alapértelmezett Azure-környezetének neve.</span><span class="sxs-lookup"><span data-stu-id="9f67a-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="9f67a-164">További információt az Azure- [környezetekről az Azure PowerShell környezet-objektumai](/powershell/azure/context-persistence)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="9f67a-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="9f67a-165">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="9f67a-165">-Credential</span></span>

<span data-ttu-id="9f67a-166">Egy **PSCredential** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9f67a-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="9f67a-167">A **PSCredential** objektumról a következő témakörben olvashat bővebben `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="9f67a-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="9f67a-168">A **PSCredential** objektum a szervezeti azonosító hitelesítő adatait, illetve az alkalmazás azonosítóját, illetve a fő hitelesítő adatok titkos azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f67a-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="9f67a-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f67a-169">-DefaultProfile</span></span>

<span data-ttu-id="9f67a-170">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f67a-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f67a-171">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9f67a-171">-Environment</span></span>

<span data-ttu-id="9f67a-172">Az Azure-fiókot tartalmazó környezet.</span><span class="sxs-lookup"><span data-stu-id="9f67a-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="9f67a-173">-Force</span><span class="sxs-lookup"><span data-stu-id="9f67a-173">-Force</span></span>

<span data-ttu-id="9f67a-174">A meglévő környezet felülírása az adott névvel a kérdés nélkül.</span><span class="sxs-lookup"><span data-stu-id="9f67a-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="9f67a-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="9f67a-175">-GraphAccessToken</span></span>

<span data-ttu-id="9f67a-176">AccessToken a Graph szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="9f67a-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="9f67a-177">– Identitás</span><span class="sxs-lookup"><span data-stu-id="9f67a-177">-Identity</span></span>

<span data-ttu-id="9f67a-178">Jelentkezzen be a felügyelt szolgáltatás identitása használatával.</span><span class="sxs-lookup"><span data-stu-id="9f67a-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="9f67a-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="9f67a-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="9f67a-180">AccessToken.</span><span class="sxs-lookup"><span data-stu-id="9f67a-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="9f67a-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="9f67a-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="9f67a-182">A felügyelt szolgáltatás állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f67a-182">Host name for the managed service.</span></span>

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

### <span data-ttu-id="9f67a-183">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="9f67a-183">-ManagedServicePort</span></span>

<span data-ttu-id="9f67a-184">A felügyelt szolgáltatás portszáma.</span><span class="sxs-lookup"><span data-stu-id="9f67a-184">Port number for the managed service.</span></span>

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

### <span data-ttu-id="9f67a-185">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="9f67a-185">-ManagedServiceSecret</span></span>

<span data-ttu-id="9f67a-186">A felügyelt szolgáltatás bejelentkezési jogkivonata.</span><span class="sxs-lookup"><span data-stu-id="9f67a-186">Token for the managed service login.</span></span>

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

### <span data-ttu-id="9f67a-187">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="9f67a-187">-Scope</span></span>

<span data-ttu-id="9f67a-188">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="9f67a-188">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="9f67a-189">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9f67a-189">-ServicePrincipal</span></span>

<span data-ttu-id="9f67a-190">Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="9f67a-190">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="9f67a-191">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="9f67a-191">-SkipContextPopulation</span></span>

<span data-ttu-id="9f67a-192">A környezeti populáció kihagyása, ha nincsenek kontextusok.</span><span class="sxs-lookup"><span data-stu-id="9f67a-192">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="9f67a-193">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="9f67a-193">-SkipValidation</span></span>

<span data-ttu-id="9f67a-194">Az érvényesítés kihagyása az Access-tokenben.</span><span class="sxs-lookup"><span data-stu-id="9f67a-194">Skip validation for access token.</span></span>

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

### <span data-ttu-id="9f67a-195">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="9f67a-195">-Subscription</span></span>

<span data-ttu-id="9f67a-196">Előfizetés neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="9f67a-196">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="9f67a-197">-Bérlő</span><span class="sxs-lookup"><span data-stu-id="9f67a-197">-Tenant</span></span>

<span data-ttu-id="9f67a-198">Választható bérlői név vagy azonosító.</span><span class="sxs-lookup"><span data-stu-id="9f67a-198">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="9f67a-199">Az aktuális API korlátai miatt a bérlő neve helyett a bérlői azonosítót kell használnia a vállalatközi (VÁLLALATKÖZI) fiókkal való kapcsolatfelvételhez.</span><span class="sxs-lookup"><span data-stu-id="9f67a-199">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="9f67a-200">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="9f67a-200">-UseDeviceAuthentication</span></span>

<span data-ttu-id="9f67a-201">Az áfakód-hitelesítést használja a böngésző vezérlő helyett.</span><span class="sxs-lookup"><span data-stu-id="9f67a-201">Use device code authentication instead of a browser control.</span></span> <span data-ttu-id="9f67a-202">Ez a PowerShell 6-os vagy újabb verziójának alapértelmezett hitelesítési típusa.</span><span class="sxs-lookup"><span data-stu-id="9f67a-202">This is the default authentication type for PowerShell version 6 and higher.</span></span>

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

### <span data-ttu-id="9f67a-203">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f67a-203">-Confirm</span></span>

<span data-ttu-id="9f67a-204">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f67a-204">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f67a-205">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f67a-205">-WhatIf</span></span>

<span data-ttu-id="9f67a-206">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f67a-206">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f67a-207">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f67a-207">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f67a-208">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f67a-208">CommonParameters</span></span>

<span data-ttu-id="9f67a-209">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f67a-209">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f67a-210">További információt a [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9f67a-210">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
<span data-ttu-id="9f67a-211">(http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f67a-211">(http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f67a-212">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f67a-212">INPUTS</span></span>

### <span data-ttu-id="9f67a-213">System. String</span><span class="sxs-lookup"><span data-stu-id="9f67a-213">System.String</span></span>

## <span data-ttu-id="9f67a-214">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f67a-214">OUTPUTS</span></span>

### <span data-ttu-id="9f67a-215">Microsoft. Azure. Command. profil. models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="9f67a-215">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="9f67a-216">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f67a-216">NOTES</span></span>

## <span data-ttu-id="9f67a-217">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f67a-217">RELATED LINKS</span></span>
