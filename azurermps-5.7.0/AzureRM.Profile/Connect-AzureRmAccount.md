---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492236"
---
# <span data-ttu-id="547e8-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="547e8-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="547e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="547e8-102">SYNOPSIS</span></span>
<span data-ttu-id="547e8-103">Csatlakozás az Azure-hoz hitelesített fiókkal az Azure Resource Manager parancsmag-kérésekkel való használathoz.</span><span class="sxs-lookup"><span data-stu-id="547e8-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="547e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="547e8-104">SYNTAX</span></span>

### <span data-ttu-id="547e8-105">UserWithSubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="547e8-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547e8-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="547e8-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="547e8-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="547e8-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="547e8-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="547e8-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547e8-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="547e8-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="547e8-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="547e8-110">DESCRIPTION</span></span>
<span data-ttu-id="547e8-111">Az Connect-AzureRmAccount parancsmag az Azure erőforrás-kezelő parancsmag-kérésekkel használható hitelesített fiókkal csatlakozik az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="547e8-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="547e8-112">Ezt a hitelesített fiókot csak az Azure Resource Manager parancsmagokkal használhatja.</span><span class="sxs-lookup"><span data-stu-id="547e8-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>

<span data-ttu-id="547e8-113">Ha a szolgáltatásvezérlő parancsmagokkal használható hitelesített fiókot szeretne felvenni, használja a Add-AzureAccount vagy a Import-AzurePublishSettingsFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="547e8-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

<span data-ttu-id="547e8-114">A parancsmag végrehajtása után az Azure-fiókokat leválaszthatja a leválasztást a AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="547e8-114">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="547e8-115">Példák</span><span class="sxs-lookup"><span data-stu-id="547e8-115">EXAMPLES</span></span>

### <span data-ttu-id="547e8-116">1. példa: interaktív bejelentkezés használata Azure-fiókhoz való csatlakozáshoz</span><span class="sxs-lookup"><span data-stu-id="547e8-116">Example 1: Use an interactive login to connect to an Azure account</span></span>
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="547e8-117">Ez a parancs Azure-fiókhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="547e8-117">This command connects to an Azure account.</span></span>

<span data-ttu-id="547e8-118">Ha az Azure Resource Manager-parancsmagokat ezzel a fiókkal szeretné futtatni, akkor a kérdésnél a Microsoft-fiók vagy a szervezeti azonosító hitelesítő adatait kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="547e8-118">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="547e8-119">Ha a többtényezős hitelesítés engedélyezve van a hitelesítő adataiban, be kell jelentkeznie az interaktív beállítással vagy a Principal Authentication szolgáltatás használatával.</span><span class="sxs-lookup"><span data-stu-id="547e8-119">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="547e8-120">2. példa: csatlakozás Azure-fiókhoz szervezeti azonosító hitelesítő adatokkal</span><span class="sxs-lookup"><span data-stu-id="547e8-120">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="547e8-121">Az első parancs megkapja a felhasználó hitelesítő adatait, majd a $Credential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="547e8-121">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="547e8-122">A második parancs a $Credentialban tárolt hitelesítő adatok használatával csatlakozik az Azure-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="547e8-122">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>

<span data-ttu-id="547e8-123">Ez a fiók az Azure Resource Manager segítségével hitelesíti a szervezeti azonosító hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="547e8-123">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>

<span data-ttu-id="547e8-124">Ehhez a fiókhoz nem használható többtényezős hitelesítés vagy Microsoft-fiókhoz tartozó hitelesítő adatok az Azure Resource Manager-parancsmagok futtatásához.</span><span class="sxs-lookup"><span data-stu-id="547e8-124">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="547e8-125">3. példa: csatlakozás Azure-ös egyszerű szolgáltatási fiókhoz</span><span class="sxs-lookup"><span data-stu-id="547e8-125">Example 3: Connect to an Azure service principal account</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="547e8-126">Az első parancs megkapja a felhasználó hitelesítő adatait, majd a $Credential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="547e8-126">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="547e8-127">A második parancs az Azurehoz csatlakozik a megadott bérlői web$Credentialban tárolt szolgáltatás-fő hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="547e8-127">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>

<span data-ttu-id="547e8-128">A ServicePrincipal kapcsoló paraméter azt jelzi, hogy a fiók a szolgáltatás-megbízóként van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="547e8-128">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="547e8-129">4. példa: interaktív bejelentkezés használata egy adott bérlői fiókhoz való csatlakozáshoz és előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="547e8-129">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="547e8-130">Ez a parancs egy Azure-fiókhoz csatlakozik, és konfigurálva van a AzureRM PowerShell a megadott bérlői fiók és az előfizetés parancsmagjának futtatásához alapértelmezés szerint.</span><span class="sxs-lookup"><span data-stu-id="547e8-130">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="547e8-131">5. példa: fiók felvétele a felügyelt szolgáltatás identitási bejelentkezési funkciójával</span><span class="sxs-lookup"><span data-stu-id="547e8-131">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="547e8-132">Ez a parancs a Host-környezet felügyelt szolgáltatás identitását használja (például ha a felügyelt szolgáltatás-identitással rendelkező VirtualMachine hajtja végre), a kódot az adott identitással való bejelentkezés engedélyezése teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="547e8-132">This command logs in using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

## <span data-ttu-id="547e8-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="547e8-133">PARAMETERS</span></span>

### <span data-ttu-id="547e8-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="547e8-134">-AccessToken</span></span>
<span data-ttu-id="547e8-135">Az Access-tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="547e8-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="547e8-136">-AccountId</span></span>
<span data-ttu-id="547e8-137">A hozzáférési jogkivonat fiókneve</span><span class="sxs-lookup"><span data-stu-id="547e8-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="547e8-138">-ApplicationId</span></span>
<span data-ttu-id="547e8-139">SPN</span><span class="sxs-lookup"><span data-stu-id="547e8-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="547e8-140">-CertificateThumbprint</span></span>
<span data-ttu-id="547e8-141">Certificate hash (ujjlenyomat)</span><span class="sxs-lookup"><span data-stu-id="547e8-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-142">-ContextName</span><span class="sxs-lookup"><span data-stu-id="547e8-142">-ContextName</span></span>
<span data-ttu-id="547e8-143">Az alapértelmezett környezet neve ebből a bejelentkezésből.</span><span class="sxs-lookup"><span data-stu-id="547e8-143">Name of the default context from this login.</span></span>  <span data-ttu-id="547e8-144">A bejelentkezés után ezt a nevet fogja tudni választani.</span><span class="sxs-lookup"><span data-stu-id="547e8-144">You will be able to select this context by this name after login.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-145">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="547e8-145">-Credential</span></span>
<span data-ttu-id="547e8-146">Egy PSCredential-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="547e8-146">Specifies a PSCredential object.</span></span>
<span data-ttu-id="547e8-147">Ha további információra van kíváncsi a PSCredential objektumról, írja be Get-Help Get-hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="547e8-147">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="547e8-148">A PSCredential objektum a szervezeti azonosító hitelesítő adatait, illetve az alkalmazás AZONOSÍTÓját, illetve a fő hitelesítő adatok titkos azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="547e8-148">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547e8-149">-DefaultProfile</span></span>
<span data-ttu-id="547e8-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="547e8-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-151">-Környezet</span><span class="sxs-lookup"><span data-stu-id="547e8-151">-Environment</span></span>
<span data-ttu-id="547e8-152">A fiókot tartalmazó környezet a bejelentkezéshez</span><span class="sxs-lookup"><span data-stu-id="547e8-152">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-153">-Force</span><span class="sxs-lookup"><span data-stu-id="547e8-153">-Force</span></span>
<span data-ttu-id="547e8-154">Felülírja a meglévő környezetet ugyanazzal a névvel, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="547e8-154">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-155">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="547e8-155">-GraphAccessToken</span></span>
<span data-ttu-id="547e8-156">AccessToken a Graph szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="547e8-156">AccessToken for Graph Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-157">– Identitás</span><span class="sxs-lookup"><span data-stu-id="547e8-157">-Identity</span></span>
<span data-ttu-id="547e8-158">Jelentkezzen be a felügyelt szolgáltatás identitása szolgáltatással az aktuális környezetben.</span><span class="sxs-lookup"><span data-stu-id="547e8-158">Login using managed service identity in the current environment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-159">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="547e8-159">-KeyVaultAccessToken</span></span>
<span data-ttu-id="547e8-160">AccessToken a rendszerhez</span><span class="sxs-lookup"><span data-stu-id="547e8-160">AccessToken for KeyVault Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-161">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="547e8-161">-ManagedServiceHostName</span></span>
<span data-ttu-id="547e8-162">Host Name a felügyelt szolgáltatás bejelentkezéséhez</span><span class="sxs-lookup"><span data-stu-id="547e8-162">Host name for managed service login</span></span>

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-163">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="547e8-163">-ManagedServicePort</span></span>
<span data-ttu-id="547e8-164">A felügyelt szolgáltatás bejelentkezésének portszáma</span><span class="sxs-lookup"><span data-stu-id="547e8-164">Port number for managed service login</span></span>

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-165">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="547e8-165">-Scope</span></span>
<span data-ttu-id="547e8-166">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="547e8-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-167">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="547e8-167">-ServicePrincipal</span></span>
<span data-ttu-id="547e8-168">Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="547e8-168">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-169">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="547e8-169">-SkipValidation</span></span>
<span data-ttu-id="547e8-170">Az érvényesítés kihagyása az Access-jogkivonat esetében</span><span class="sxs-lookup"><span data-stu-id="547e8-170">Skip validation for access token</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-171">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="547e8-171">-Subscription</span></span>
<span data-ttu-id="547e8-172">Előfizetés neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="547e8-172">Subscription Name or ID</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-173">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="547e8-173">-TenantId</span></span>
<span data-ttu-id="547e8-174">Nem kötelező bérlői név vagy azonosító</span><span class="sxs-lookup"><span data-stu-id="547e8-174">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="547e8-175">-Confirm</span></span>
<span data-ttu-id="547e8-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="547e8-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="547e8-177">-WhatIf</span></span>
<span data-ttu-id="547e8-178">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="547e8-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="547e8-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="547e8-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547e8-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547e8-180">CommonParameters</span></span>
<span data-ttu-id="547e8-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="547e8-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547e8-182">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="547e8-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547e8-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="547e8-183">INPUTS</span></span>

### <span data-ttu-id="547e8-184">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="547e8-184">String</span></span>
<span data-ttu-id="547e8-185">A ' SubscriptionId ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="547e8-185">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="547e8-186">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="547e8-186">String</span></span>
<span data-ttu-id="547e8-187">A ' SubscriptionName ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="547e8-187">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="547e8-188">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="547e8-188">OUTPUTS</span></span>

### <span data-ttu-id="547e8-189">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="547e8-189">PSAzureProfile</span></span>
<span data-ttu-id="547e8-190">A bejelentkezett felhasználó hitelesítő adatait, előfizetését, fiókját és bérlői adatait.</span><span class="sxs-lookup"><span data-stu-id="547e8-190">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="547e8-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="547e8-191">NOTES</span></span>

## <span data-ttu-id="547e8-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="547e8-192">RELATED LINKS</span></span>

