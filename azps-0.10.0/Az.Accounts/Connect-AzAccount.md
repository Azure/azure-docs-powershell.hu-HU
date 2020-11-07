---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841102"
---
# <span data-ttu-id="3df88-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="3df88-101">Connect-AzAccount</span></span>

## <span data-ttu-id="3df88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3df88-102">SYNOPSIS</span></span>
<span data-ttu-id="3df88-103">Csatlakozás az Azure-hoz hitelesített fiókkal az Azure Resource Manager parancsmag-kérésekkel való használathoz.</span><span class="sxs-lookup"><span data-stu-id="3df88-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="3df88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3df88-104">SYNTAX</span></span>

### <span data-ttu-id="3df88-105">UserWithSubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3df88-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df88-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3df88-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3df88-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="3df88-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3df88-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3df88-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3df88-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3df88-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df88-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="3df88-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3df88-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="3df88-111">DESCRIPTION</span></span>
<span data-ttu-id="3df88-112">Az Connect-AzAccount parancsmag az Azure erőforrás-kezelő parancsmag-kérésekkel használható hitelesített fiókkal csatlakozik az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="3df88-112">The Connect-AzAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="3df88-113">Ezt a hitelesített fiókot csak az Azure Resource Manager parancsmagokkal használhatja.</span><span class="sxs-lookup"><span data-stu-id="3df88-113">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="3df88-114">Ha a szolgáltatásvezérlő parancsmagokkal használható hitelesített fiókot szeretne felvenni, használja a Add-AzAccount vagy a Import-AzPublishSettingsFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3df88-114">To add an authenticated account for use with Service Management cmdlets, use the Add-AzAccount or the Import-AzPublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="3df88-115">Ha az aktuális felhasználóhoz nem tartozik környezet, ez a parancs a felhasználó helyi listáját fogja kitölteni mindegyik (az első 25) előfizetése kontextusában.</span><span class="sxs-lookup"><span data-stu-id="3df88-115">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="3df88-116">A felhasználóhoz létrehozott környezetek listája a "Get-AzContext – ListAvailable" futtatásával érhető el.</span><span class="sxs-lookup"><span data-stu-id="3df88-116">The list of contexts created for the user can be found by running "Get-AzContext -ListAvailable".</span></span> <span data-ttu-id="3df88-117">A környezeti sokaság kihagyásához futtathatja ezt a parancsot a "-SkipContextPopulation" kapcsoló paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="3df88-117">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="3df88-118">A parancsmag végrehajtása után az Azure-fiókokat leválaszthatja a leválasztást a AzAccount.</span><span class="sxs-lookup"><span data-stu-id="3df88-118">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzAccount.</span></span>

## <span data-ttu-id="3df88-119">Példák</span><span class="sxs-lookup"><span data-stu-id="3df88-119">EXAMPLES</span></span>

### <span data-ttu-id="3df88-120">1. példa: interaktív bejelentkezés használata Azure-fiókhoz való csatlakozáshoz</span><span class="sxs-lookup"><span data-stu-id="3df88-120">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3df88-121">Ez a parancs Azure-fiókhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="3df88-121">This command connects to an Azure account.</span></span>
<span data-ttu-id="3df88-122">Ha az Azure Resource Manager-parancsmagokat ezzel a fiókkal szeretné futtatni, akkor a kérdésnél a Microsoft-fiók vagy a szervezeti azonosító hitelesítő adatait kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="3df88-122">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="3df88-123">Ha a többtényezős hitelesítés engedélyezve van a hitelesítő adataiban, be kell jelentkeznie az interaktív beállítással vagy a Principal Authentication szolgáltatás használatával.</span><span class="sxs-lookup"><span data-stu-id="3df88-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="3df88-124">2. példa: (csak a Windows PowerShell 5,1) csatlakozás Azure-fiókhoz szervezeti azonosító hitelesítő adataival</span><span class="sxs-lookup"><span data-stu-id="3df88-124">Example 2: (Windows PowerShell 5.1 only) Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3df88-125">Ez a forgatókönyv csak a Windows PowerShell 5,1-ban működik.</span><span class="sxs-lookup"><span data-stu-id="3df88-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="3df88-126">Az első parancs kérni fogja a felhasználói hitelesítő adatok (Felhasználónév és jelszó) megadását, majd a $Credential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="3df88-126">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="3df88-127">A második parancs a $Credentialban tárolt hitelesítő adatok használatával csatlakozik az Azure-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3df88-127">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="3df88-128">Ez a fiók az Azure Resource Manager segítségével hitelesíti a szervezeti azonosító hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="3df88-128">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="3df88-129">Ehhez a fiókhoz nem használható többtényezős hitelesítés vagy Microsoft-fiókhoz tartozó hitelesítő adatok az Azure Resource Manager-parancsmagok futtatásához.</span><span class="sxs-lookup"><span data-stu-id="3df88-129">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="3df88-130">3. példa: csatlakozás Azure-ös egyszerű szolgáltatási fiókhoz</span><span class="sxs-lookup"><span data-stu-id="3df88-130">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3df88-131">Az első parancs a szolgáltatás fő hitelesítő adatait (alkalmazásspecifikus azonosítóját és a szolgáltatás fő titkát) kapja meg, majd a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3df88-131">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="3df88-132">A második parancs az Azurehoz csatlakozik a megadott bérlői web$Credentialban tárolt szolgáltatás-fő hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="3df88-132">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="3df88-133">A ServicePrincipal kapcsoló paraméter azt jelzi, hogy a fiók a szolgáltatás-megbízóként van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="3df88-133">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="3df88-134">4. példa: interaktív bejelentkezés használata egy adott bérlői fiókhoz való csatlakozáshoz és előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="3df88-134">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3df88-135">Ez a parancs egy Azure-fiókhoz csatlakozik, és konfigurálva van a AzureRM PowerShell a megadott bérlői fiók és az előfizetés parancsmagjának futtatásához alapértelmezés szerint.</span><span class="sxs-lookup"><span data-stu-id="3df88-135">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="3df88-136">5. példa: fiók felvétele a felügyelt szolgáltatás identitási bejelentkezési funkciójával</span><span class="sxs-lookup"><span data-stu-id="3df88-136">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3df88-137">Ez a parancs az állomás környezetének felügyelt szolgáltatás identitásával csatlakozik hozzá (például ha a felügyelt szolgáltatás-identitással rendelkező VirtualMachine hajtja végre a kódot, így a kód bejelentkezhet a hozzárendelt identitás használatával)</span><span class="sxs-lookup"><span data-stu-id="3df88-137">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="3df88-138">6. példa: fiók hozzáadása a felügyelt szolgáltatás identitás-bejelentkezési és ClientId</span><span class="sxs-lookup"><span data-stu-id="3df88-138">Example 6: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3df88-139">Ez a parancs a "myUserAssignedIdentity" felügyelt szolgáltatás identitásával csatlakozik a felhasználóhoz rendelt identitás hozzáadásával a virtuális géphez, majd a felhasználó által kiosztott identitás ClientId.</span><span class="sxs-lookup"><span data-stu-id="3df88-139">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the ClientId of the User Assigned Identity.</span></span>
<span data-ttu-id="3df88-140">A felügyelt identitások konfigurálásáról további információt itt találhat: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="3df88-140">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="3df88-141">7. példa: fiók hozzáadása a felügyelt szolgáltatás identitás-bejelentkezési és ClientId</span><span class="sxs-lookup"><span data-stu-id="3df88-141">Example 7: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3df88-142">Ez a parancs a "myUserAssignedIdentity" felügyelt szolgáltatás identitásával csatlakozik a felhasználóhoz rendelt identitás hozzáadásával a virtuális géphez, majd a felhasználó által kiosztott identitás azonosítójának használatával.</span><span class="sxs-lookup"><span data-stu-id="3df88-142">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the Id of the User Assigned Identity.</span></span>
<span data-ttu-id="3df88-143">A felügyelt identitások konfigurálásáról további információt itt találhat: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="3df88-143">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="3df88-144">8. példa: fiók hozzáadása tanúsítványok használatával</span><span class="sxs-lookup"><span data-stu-id="3df88-144">Example 8: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="3df88-145">Ez a parancs egy Azure-fiókhoz, a tanúsítvány-alapú szolgáltatás egyszerű hitelesítésével csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="3df88-145">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="3df88-146">A hitelesítéshez használt szolgáltatásnevet a megadott tanúsítvánnyal kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="3df88-146">The service principal used for authentication should have been created with the given certificate.</span></span>

### <span data-ttu-id="3df88-147">Példa 9: fiók hozzáadása a AccessToken-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="3df88-147">Example 9: Add an account using AccessToken authentication</span></span>
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3df88-148">Ez a parancs a "AccountId" mezőben megadott Azure-fiókhoz csatlakozik a megadott AccessToken és KeyVaultAccessToken használatával.</span><span class="sxs-lookup"><span data-stu-id="3df88-148">This command connects to an Azure account specified in "AccountId" using the AccessToken and KeyVaultAccessToken provided.</span></span>

## <span data-ttu-id="3df88-149">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3df88-149">PARAMETERS</span></span>

### <span data-ttu-id="3df88-150">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="3df88-150">-AccessToken</span></span>
<span data-ttu-id="3df88-151">Az Access-tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="3df88-151">Specifies an access token.</span></span>

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

### <span data-ttu-id="3df88-152">-AccountId</span><span class="sxs-lookup"><span data-stu-id="3df88-152">-AccountId</span></span>
<span data-ttu-id="3df88-153">Az AccessToken paraméterben megadott hozzáférési jogkivonat fiókneve.</span><span class="sxs-lookup"><span data-stu-id="3df88-153">Account Id for access token in AccessToken parameter set.</span></span> <span data-ttu-id="3df88-154">A felügyelt szolgáltatáshoz tartozó fiókazonosító a ManagedService paraméterben.</span><span class="sxs-lookup"><span data-stu-id="3df88-154">Account Id for managed service in ManagedService parameter set.</span></span> <span data-ttu-id="3df88-155">Lehet felügyelt szolgáltatás-erőforrás azonosítója vagy a hozzá tartozó ügyfél-azonosító. A SystemAssigned identitás használatához hagyja üresen ezt a mezőt.</span><span class="sxs-lookup"><span data-stu-id="3df88-155">Can be a managed service resource Id, or the associated client id. To use the SystemAssigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="3df88-156">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3df88-156">-ApplicationId</span></span>
<span data-ttu-id="3df88-157">SPN</span><span class="sxs-lookup"><span data-stu-id="3df88-157">SPN</span></span>

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

### <span data-ttu-id="3df88-158">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="3df88-158">-CertificateThumbprint</span></span>
<span data-ttu-id="3df88-159">Certificate hash (ujjlenyomat)</span><span class="sxs-lookup"><span data-stu-id="3df88-159">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="3df88-160">-ContextName</span><span class="sxs-lookup"><span data-stu-id="3df88-160">-ContextName</span></span>
<span data-ttu-id="3df88-161">Az alapértelmezett környezet neve ebből a bejelentkezésből.</span><span class="sxs-lookup"><span data-stu-id="3df88-161">Name of the default context from this login.</span></span>  <span data-ttu-id="3df88-162">A bejelentkezés után ezt a nevet fogja tudni választani.</span><span class="sxs-lookup"><span data-stu-id="3df88-162">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="3df88-163">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="3df88-163">-Credential</span></span>
<span data-ttu-id="3df88-164">Egy PSCredential-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3df88-164">Specifies a PSCredential object.</span></span>
<span data-ttu-id="3df88-165">Ha további információra van kíváncsi a PSCredential objektumról, írja be Get-Help Get-hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="3df88-165">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="3df88-166">A PSCredential objektum a szervezeti azonosító hitelesítő adatait, illetve az alkalmazás AZONOSÍTÓját, illetve a fő hitelesítő adatok titkos azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3df88-166">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="3df88-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df88-167">-DefaultProfile</span></span>
<span data-ttu-id="3df88-168">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3df88-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3df88-169">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3df88-169">-Environment</span></span>
<span data-ttu-id="3df88-170">A fiókot tartalmazó környezet a bejelentkezéshez</span><span class="sxs-lookup"><span data-stu-id="3df88-170">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="3df88-171">-Force</span><span class="sxs-lookup"><span data-stu-id="3df88-171">-Force</span></span>
<span data-ttu-id="3df88-172">Felülírja a meglévő környezetet ugyanazzal a névvel, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="3df88-172">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="3df88-173">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="3df88-173">-GraphAccessToken</span></span>
<span data-ttu-id="3df88-174">AccessToken a Graph szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="3df88-174">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="3df88-175">– Identitás</span><span class="sxs-lookup"><span data-stu-id="3df88-175">-Identity</span></span>
<span data-ttu-id="3df88-176">Jelentkezzen be a felügyelt szolgáltatás identitása szolgáltatással az aktuális környezetben.</span><span class="sxs-lookup"><span data-stu-id="3df88-176">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="3df88-177">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="3df88-177">-KeyVaultAccessToken</span></span>
<span data-ttu-id="3df88-178">AccessToken a rendszerhez</span><span class="sxs-lookup"><span data-stu-id="3df88-178">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="3df88-179">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="3df88-179">-ManagedServiceHostName</span></span>
<span data-ttu-id="3df88-180">Host Name a felügyelt szolgáltatás bejelentkezéséhez</span><span class="sxs-lookup"><span data-stu-id="3df88-180">Host name for managed service login</span></span>

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

### <span data-ttu-id="3df88-181">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="3df88-181">-ManagedServicePort</span></span>
<span data-ttu-id="3df88-182">A felügyelt szolgáltatás bejelentkezésének portszáma</span><span class="sxs-lookup"><span data-stu-id="3df88-182">Port number for managed service login</span></span>

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

### <span data-ttu-id="3df88-183">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="3df88-183">-ManagedServiceSecret</span></span>
<span data-ttu-id="3df88-184">Titkos – bizonyos típusú felügyelt szolgáltatás-bejelentkezéshez használt.</span><span class="sxs-lookup"><span data-stu-id="3df88-184">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="3df88-185">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="3df88-185">-Scope</span></span>
<span data-ttu-id="3df88-186">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="3df88-186">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3df88-187">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3df88-187">-ServicePrincipal</span></span>
<span data-ttu-id="3df88-188">Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="3df88-188">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="3df88-189">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="3df88-189">-SkipContextPopulation</span></span>
<span data-ttu-id="3df88-190">A környezeti populáció kihagyása, ha nincsenek kontextusok.</span><span class="sxs-lookup"><span data-stu-id="3df88-190">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="3df88-191">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="3df88-191">-SkipValidation</span></span>
<span data-ttu-id="3df88-192">Az érvényesítés kihagyása az Access-jogkivonat esetében</span><span class="sxs-lookup"><span data-stu-id="3df88-192">Skip validation for access token</span></span>

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

### <span data-ttu-id="3df88-193">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="3df88-193">-Subscription</span></span>
<span data-ttu-id="3df88-194">Előfizetés neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="3df88-194">Subscription Name or ID</span></span>

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

### <span data-ttu-id="3df88-195">-Bérlő</span><span class="sxs-lookup"><span data-stu-id="3df88-195">-Tenant</span></span>
<span data-ttu-id="3df88-196">Nem kötelező bérlői név vagy azonosító</span><span class="sxs-lookup"><span data-stu-id="3df88-196">Optional tenant name or ID</span></span>

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

### <span data-ttu-id="3df88-197">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="3df88-197">-UseDeviceAuthentication</span></span>
<span data-ttu-id="3df88-198">Az áfakód-hitelesítés használata a böngésző vezérlő helyett</span><span class="sxs-lookup"><span data-stu-id="3df88-198">Use device code authentication instead of a browser control</span></span>

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

### <span data-ttu-id="3df88-199">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3df88-199">-Confirm</span></span>
<span data-ttu-id="3df88-200">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3df88-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df88-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df88-201">-WhatIf</span></span>
<span data-ttu-id="3df88-202">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3df88-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3df88-203">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3df88-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df88-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df88-204">CommonParameters</span></span>
<span data-ttu-id="3df88-205">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3df88-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df88-206">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3df88-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df88-207">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3df88-207">INPUTS</span></span>

### <span data-ttu-id="3df88-208">System. String</span><span class="sxs-lookup"><span data-stu-id="3df88-208">System.String</span></span>

## <span data-ttu-id="3df88-209">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3df88-209">OUTPUTS</span></span>

### <span data-ttu-id="3df88-210">Microsoft. Azure. Command. profil. models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="3df88-210">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="3df88-211">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3df88-211">NOTES</span></span>

## <span data-ttu-id="3df88-212">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3df88-212">RELATED LINKS</span></span>
