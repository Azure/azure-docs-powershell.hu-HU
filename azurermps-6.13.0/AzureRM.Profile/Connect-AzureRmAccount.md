---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680311"
---
# <span data-ttu-id="27395-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="27395-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="27395-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27395-102">SYNOPSIS</span></span>
<span data-ttu-id="27395-103">Csatlakozás az Azure-hoz hitelesített fiókkal az Azure Resource Manager parancsmag-kérésekkel való használathoz.</span><span class="sxs-lookup"><span data-stu-id="27395-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27395-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27395-104">SYNTAX</span></span>

### <span data-ttu-id="27395-105">UserWithSubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27395-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27395-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27395-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27395-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27395-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27395-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27395-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27395-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="27395-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27395-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="27395-110">DESCRIPTION</span></span>
<span data-ttu-id="27395-111">Az Connect-AzureRmAccount parancsmag az Azure erőforrás-kezelő parancsmag-kérésekkel használható hitelesített fiókkal csatlakozik az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="27395-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="27395-112">Ezt a hitelesített fiókot csak az Azure Resource Manager parancsmagokkal használhatja.</span><span class="sxs-lookup"><span data-stu-id="27395-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="27395-113">Ha a szolgáltatásvezérlő parancsmagokkal használható hitelesített fiókot szeretne felvenni, használja a Add-AzureAccount vagy a Import-AzurePublishSettingsFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="27395-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="27395-114">Ha az aktuális felhasználóhoz nem tartozik környezet, ez a parancs a felhasználó helyi listáját fogja kitölteni mindegyik (az első 25) előfizetése kontextusában.</span><span class="sxs-lookup"><span data-stu-id="27395-114">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="27395-115">A felhasználóhoz létrehozott környezetek listája a "Get-AzureRmContext – ListAvailable" futtatásával érhető el.</span><span class="sxs-lookup"><span data-stu-id="27395-115">The list of contexts created for the user can be found by running "Get-AzureRmContext -ListAvailable".</span></span> <span data-ttu-id="27395-116">A környezeti sokaság kihagyásához futtathatja ezt a parancsot a "-SkipContextPopulation" kapcsoló paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="27395-116">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="27395-117">A parancsmag végrehajtása után az Azure-fiókokat leválaszthatja a leválasztást a AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="27395-117">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="27395-118">Példák</span><span class="sxs-lookup"><span data-stu-id="27395-118">EXAMPLES</span></span>

### <span data-ttu-id="27395-119">1. példa: interaktív bejelentkezés használata Azure-fiókhoz való csatlakozáshoz</span><span class="sxs-lookup"><span data-stu-id="27395-119">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="27395-120">Ez a parancs Azure-fiókhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="27395-120">This command connects to an Azure account.</span></span>
<span data-ttu-id="27395-121">Ha az Azure Resource Manager-parancsmagokat ezzel a fiókkal szeretné futtatni, akkor a kérdésnél a Microsoft-fiók vagy a szervezeti azonosító hitelesítő adatait kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="27395-121">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="27395-122">Ha a többtényezős hitelesítés engedélyezve van a hitelesítő adataiban, be kell jelentkeznie az interaktív beállítással vagy a Principal Authentication szolgáltatás használatával.</span><span class="sxs-lookup"><span data-stu-id="27395-122">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="27395-123">2. példa: csatlakozás Azure-fiókhoz szervezeti azonosító hitelesítő adatokkal</span><span class="sxs-lookup"><span data-stu-id="27395-123">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="27395-124">Az első parancs kérni fogja a felhasználói hitelesítő adatok (Felhasználónév és jelszó) megadását, majd a $Credential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="27395-124">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="27395-125">A második parancs a $Credentialban tárolt hitelesítő adatok használatával csatlakozik az Azure-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="27395-125">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="27395-126">Ez a fiók az Azure Resource Manager segítségével hitelesíti a szervezeti azonosító hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="27395-126">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="27395-127">Ehhez a fiókhoz nem használható többtényezős hitelesítés vagy Microsoft-fiókhoz tartozó hitelesítő adatok az Azure Resource Manager-parancsmagok futtatásához.</span><span class="sxs-lookup"><span data-stu-id="27395-127">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="27395-128">3. példa: csatlakozás Azure-ös egyszerű szolgáltatási fiókhoz</span><span class="sxs-lookup"><span data-stu-id="27395-128">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="27395-129">Az első parancs a szolgáltatás fő hitelesítő adatait (alkalmazásspecifikus azonosítóját és a szolgáltatás fő titkát) kapja meg, majd a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="27395-129">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="27395-130">A második parancs az Azurehoz csatlakozik a megadott bérlői web$Credentialban tárolt szolgáltatás-fő hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="27395-130">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="27395-131">A ServicePrincipal kapcsoló paraméter azt jelzi, hogy a fiók a szolgáltatás-megbízóként van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="27395-131">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="27395-132">4. példa: interaktív bejelentkezés használata egy adott bérlői fiókhoz való csatlakozáshoz és előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="27395-132">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="27395-133">Ez a parancs egy Azure-fiókhoz csatlakozik, és konfigurálva van a AzureRM PowerShell a megadott bérlői fiók és az előfizetés parancsmagjának futtatásához alapértelmezés szerint.</span><span class="sxs-lookup"><span data-stu-id="27395-133">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="27395-134">5. példa: fiók felvétele a felügyelt szolgáltatás identitási bejelentkezési funkciójával</span><span class="sxs-lookup"><span data-stu-id="27395-134">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="27395-135">Ez a parancs az állomás környezetének felügyelt szolgáltatás identitásával csatlakozik hozzá (például ha a felügyelt szolgáltatás-identitással rendelkező VirtualMachine hajtja végre a kódot, így a kód bejelentkezhet a hozzárendelt identitás használatával)</span><span class="sxs-lookup"><span data-stu-id="27395-135">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="27395-136">6. példa: fiók hozzáadása tanúsítványokkal</span><span class="sxs-lookup"><span data-stu-id="27395-136">Example 6: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="27395-137">Ez a parancs egy Azure-fiókhoz, a tanúsítvány-alapú szolgáltatás egyszerű hitelesítésével csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="27395-137">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="27395-138">A hitelesítéshez használt Theservice elsődlegesnek kell lennie az adott tanúsítvánnyal.</span><span class="sxs-lookup"><span data-stu-id="27395-138">Theservice principal used for authentication should have been created with the given certificate.</span></span>

## <span data-ttu-id="27395-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27395-139">PARAMETERS</span></span>

### <span data-ttu-id="27395-140">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="27395-140">-AccessToken</span></span>
<span data-ttu-id="27395-141">Az Access-tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="27395-141">Specifies an access token.</span></span>

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

### <span data-ttu-id="27395-142">-AccountId</span><span class="sxs-lookup"><span data-stu-id="27395-142">-AccountId</span></span>
<span data-ttu-id="27395-143">A hozzáférési jogkivonat fiókneve</span><span class="sxs-lookup"><span data-stu-id="27395-143">Account Id for access token</span></span>

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

### <span data-ttu-id="27395-144">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="27395-144">-ApplicationId</span></span>
<span data-ttu-id="27395-145">SPN</span><span class="sxs-lookup"><span data-stu-id="27395-145">SPN</span></span>

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

### <span data-ttu-id="27395-146">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="27395-146">-CertificateThumbprint</span></span>
<span data-ttu-id="27395-147">Certificate hash (ujjlenyomat)</span><span class="sxs-lookup"><span data-stu-id="27395-147">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="27395-148">-ContextName</span><span class="sxs-lookup"><span data-stu-id="27395-148">-ContextName</span></span>
<span data-ttu-id="27395-149">Az alapértelmezett környezet neve ebből a bejelentkezésből.</span><span class="sxs-lookup"><span data-stu-id="27395-149">Name of the default context from this login.</span></span>  <span data-ttu-id="27395-150">A bejelentkezés után ezt a nevet fogja tudni választani.</span><span class="sxs-lookup"><span data-stu-id="27395-150">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="27395-151">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="27395-151">-Credential</span></span>
<span data-ttu-id="27395-152">Egy PSCredential-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="27395-152">Specifies a PSCredential object.</span></span>
<span data-ttu-id="27395-153">Ha további információra van kíváncsi a PSCredential objektumról, írja be Get-Help Get-hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="27395-153">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="27395-154">A PSCredential objektum a szervezeti azonosító hitelesítő adatait, illetve az alkalmazás AZONOSÍTÓját, illetve a fő hitelesítő adatok titkos azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="27395-154">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27395-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27395-155">-DefaultProfile</span></span>
<span data-ttu-id="27395-156">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27395-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27395-157">-Környezet</span><span class="sxs-lookup"><span data-stu-id="27395-157">-Environment</span></span>
<span data-ttu-id="27395-158">A fiókot tartalmazó környezet a bejelentkezéshez</span><span class="sxs-lookup"><span data-stu-id="27395-158">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="27395-159">-Force</span><span class="sxs-lookup"><span data-stu-id="27395-159">-Force</span></span>
<span data-ttu-id="27395-160">Felülírja a meglévő környezetet ugyanazzal a névvel, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="27395-160">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="27395-161">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="27395-161">-GraphAccessToken</span></span>
<span data-ttu-id="27395-162">AccessToken a Graph szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="27395-162">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="27395-163">– Identitás</span><span class="sxs-lookup"><span data-stu-id="27395-163">-Identity</span></span>
<span data-ttu-id="27395-164">Jelentkezzen be a felügyelt szolgáltatás identitása szolgáltatással az aktuális környezetben.</span><span class="sxs-lookup"><span data-stu-id="27395-164">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="27395-165">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="27395-165">-KeyVaultAccessToken</span></span>
<span data-ttu-id="27395-166">AccessToken a rendszerhez</span><span class="sxs-lookup"><span data-stu-id="27395-166">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="27395-167">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="27395-167">-ManagedServiceHostName</span></span>
<span data-ttu-id="27395-168">Host Name a felügyelt szolgáltatás bejelentkezéséhez</span><span class="sxs-lookup"><span data-stu-id="27395-168">Host name for managed service login</span></span>

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

### <span data-ttu-id="27395-169">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="27395-169">-ManagedServicePort</span></span>
<span data-ttu-id="27395-170">A felügyelt szolgáltatás bejelentkezésének portszáma</span><span class="sxs-lookup"><span data-stu-id="27395-170">Port number for managed service login</span></span>

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

### <span data-ttu-id="27395-171">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="27395-171">-ManagedServiceSecret</span></span>
<span data-ttu-id="27395-172">Titkos – bizonyos típusú felügyelt szolgáltatás-bejelentkezéshez használt.</span><span class="sxs-lookup"><span data-stu-id="27395-172">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="27395-173">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="27395-173">-Scope</span></span>
<span data-ttu-id="27395-174">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="27395-174">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="27395-175">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="27395-175">-ServicePrincipal</span></span>
<span data-ttu-id="27395-176">Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="27395-176">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="27395-177">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="27395-177">-SkipContextPopulation</span></span>
<span data-ttu-id="27395-178">A környezeti populáció kihagyása, ha nincsenek kontextusok.</span><span class="sxs-lookup"><span data-stu-id="27395-178">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="27395-179">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="27395-179">-SkipValidation</span></span>
<span data-ttu-id="27395-180">Az érvényesítés kihagyása az Access-jogkivonat esetében</span><span class="sxs-lookup"><span data-stu-id="27395-180">Skip validation for access token</span></span>

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

### <span data-ttu-id="27395-181">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="27395-181">-Subscription</span></span>
<span data-ttu-id="27395-182">Előfizetés neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="27395-182">Subscription Name or ID</span></span>

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

### <span data-ttu-id="27395-183">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="27395-183">-TenantId</span></span>
<span data-ttu-id="27395-184">Nem kötelező tartománynév vagy bérlői azonosító.</span><span class="sxs-lookup"><span data-stu-id="27395-184">Optional domain name or tenant ID.</span></span> <span data-ttu-id="27395-185">A tartománynév nem minden bejelentkezési helyzetben fog működni.</span><span class="sxs-lookup"><span data-stu-id="27395-185">Domain name will not work in all sign-in situations.</span></span> <span data-ttu-id="27395-186">A Cloud Solution Provider (CSP) bejelentkezéshez a bérlői AZONOSÍTÓra van szükség.</span><span class="sxs-lookup"><span data-stu-id="27395-186">For Cloud Solution Provider (CSP) sign-in, tenant ID is required.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27395-187">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27395-187">-Confirm</span></span>
<span data-ttu-id="27395-188">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27395-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27395-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27395-189">-WhatIf</span></span>
<span data-ttu-id="27395-190">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27395-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27395-191">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27395-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27395-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27395-192">CommonParameters</span></span>
<span data-ttu-id="27395-193">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27395-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27395-194">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27395-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27395-195">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27395-195">INPUTS</span></span>

### <span data-ttu-id="27395-196">System. String</span><span class="sxs-lookup"><span data-stu-id="27395-196">System.String</span></span>
<span data-ttu-id="27395-197">Paraméterek: előfizetés (ByValue)</span><span class="sxs-lookup"><span data-stu-id="27395-197">Parameters: Subscription (ByValue)</span></span>

## <span data-ttu-id="27395-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27395-198">OUTPUTS</span></span>

### <span data-ttu-id="27395-199">Microsoft. Azure. Command. profil. models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="27395-199">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="27395-200">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27395-200">NOTES</span></span>

## <span data-ttu-id="27395-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27395-201">RELATED LINKS</span></span>
