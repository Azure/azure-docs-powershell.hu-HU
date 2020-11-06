---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
ms.openlocfilehash: 11303438a50839bbe05139888cc665198ed09810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504016"
---
# <span data-ttu-id="de5c1-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="de5c1-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="de5c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="de5c1-103">Az Azure Resource Manager parancsmag-kérésekhez használható hitelesített fiók hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="de5c1-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de5c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de5c1-104">SYNTAX</span></span>

### <span data-ttu-id="de5c1-105">UserWithSubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de5c1-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de5c1-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de5c1-106">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de5c1-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de5c1-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de5c1-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de5c1-108">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de5c1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="de5c1-109">DESCRIPTION</span></span>
<span data-ttu-id="de5c1-110">Az Add-AzureRmAcccount parancsmag az Azure Resource Manager parancsmag-kérésekhez használható hitelesített Azure-fiókot ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="de5c1-110">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="de5c1-111">Ezt a hitelesített fiókot csak az Azure Resource Manager parancsmagokkal használhatja.</span><span class="sxs-lookup"><span data-stu-id="de5c1-111">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="de5c1-112">Ha a szolgáltatásvezérlő parancsmagokkal használható hitelesített fiókot szeretne felvenni, használja a Add-AzureAccount vagy a Import-AzurePublishSettingsFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="de5c1-112">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="de5c1-113">Példák</span><span class="sxs-lookup"><span data-stu-id="de5c1-113">EXAMPLES</span></span>

### <span data-ttu-id="de5c1-114">Példa 1: interaktív bejelentkezést igénylő fiók hozzáadása</span><span class="sxs-lookup"><span data-stu-id="de5c1-114">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="de5c1-115">Ez a parancs Azure Resource Manager-fiókot ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="de5c1-115">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="de5c1-116">Ha az Azure Resource Manager-parancsmagokat ezzel a fiókkal szeretné futtatni, akkor a kérdésnél a Microsoft-fiók vagy a szervezeti azonosító hitelesítő adatait kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="de5c1-116">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="de5c1-117">Ha a többtényezős hitelesítés engedélyezve van a hitelesítő adataiban, be kell jelentkeznie az interaktív beállítással vagy a Principal Authentication szolgáltatás használatával.</span><span class="sxs-lookup"><span data-stu-id="de5c1-117">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="de5c1-118">2. példa: a szervezeti azonosító hitelesítő adataival hitelesítő fiók hozzáadása</span><span class="sxs-lookup"><span data-stu-id="de5c1-118">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="de5c1-119">Az első parancs megkapja a felhasználó hitelesítő adatait, majd a $Credential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="de5c1-119">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="de5c1-120">A második parancs az Azure Resource Manager-fiókot adja hozzá az $Credential hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="de5c1-120">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="de5c1-121">Ez a fiók az Azure Resource Manager segítségével hitelesíti a szervezeti azonosító hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="de5c1-121">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="de5c1-122">Ehhez a fiókhoz nem használható többtényezős hitelesítés vagy Microsoft-fiókhoz tartozó hitelesítő adatok az Azure Resource Manager-parancsmagok futtatásához.</span><span class="sxs-lookup"><span data-stu-id="de5c1-122">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="de5c1-123">3. példa: a Service Principal hitelesítő adataival hitelesítő fiók hozzáadása</span><span class="sxs-lookup"><span data-stu-id="de5c1-123">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="de5c1-124">Az első parancs megkapja a felhasználó hitelesítő adatait, majd a $Credential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="de5c1-124">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="de5c1-125">A második parancs egy Azure Resource Manager-fiókot ad hozzá a megadott bérlői webhelyhez $Credentialban tárolt hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="de5c1-125">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="de5c1-126">A ServicePrincipal kapcsoló paraméter azt jelzi, hogy a fiók a szolgáltatás-megbízóként van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="de5c1-126">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="de5c1-127">4. példa: fiók hozzáadása adott bérlőhöz és előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="de5c1-127">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="de5c1-128">Ez a parancs egy Azure Resource Manager-fiókot hoz létre, amellyel alapértelmezés szerint a megadott bérlői fiókhoz és előfizetéshez parancsmagok futtathatók.</span><span class="sxs-lookup"><span data-stu-id="de5c1-128">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="de5c1-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de5c1-129">PARAMETERS</span></span>

### <span data-ttu-id="de5c1-130">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="de5c1-130">-AccessToken</span></span>
<span data-ttu-id="de5c1-131">Az Access-tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="de5c1-131">Specifies an access token.</span></span>

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

### <span data-ttu-id="de5c1-132">-AccountId</span><span class="sxs-lookup"><span data-stu-id="de5c1-132">-AccountId</span></span>
<span data-ttu-id="de5c1-133">A hozzáférési jogkivonat fiókneve</span><span class="sxs-lookup"><span data-stu-id="de5c1-133">Account Id for access token</span></span>

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

### <span data-ttu-id="de5c1-134">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="de5c1-134">-ApplicationId</span></span>
<span data-ttu-id="de5c1-135">SPN</span><span class="sxs-lookup"><span data-stu-id="de5c1-135">SPN</span></span>

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

### <span data-ttu-id="de5c1-136">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="de5c1-136">-CertificateThumbprint</span></span>
<span data-ttu-id="de5c1-137">Certificate hash (ujjlenyomat)</span><span class="sxs-lookup"><span data-stu-id="de5c1-137">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="de5c1-138">-ContextName</span><span class="sxs-lookup"><span data-stu-id="de5c1-138">-ContextName</span></span>
<span data-ttu-id="de5c1-139">Az alapértelmezett környezet neve ebből a bejelentkezésből.</span><span class="sxs-lookup"><span data-stu-id="de5c1-139">Name of the default context from this login.</span></span>  <span data-ttu-id="de5c1-140">A bejelentkezés után ezt a nevet fogja tudni választani.</span><span class="sxs-lookup"><span data-stu-id="de5c1-140">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="de5c1-141">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="de5c1-141">-Credential</span></span>
<span data-ttu-id="de5c1-142">Egy PSCredential-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="de5c1-142">Specifies a PSCredential object.</span></span>
<span data-ttu-id="de5c1-143">Ha további információra van kíváncsi a PSCredential objektumról, írja be Get-Help Get-hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="de5c1-143">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="de5c1-144">A PSCredential objektum a szervezeti azonosító hitelesítő adatait, illetve az alkalmazás AZONOSÍTÓját, illetve a fő hitelesítő adatok titkos azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="de5c1-144">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="de5c1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5c1-145">-DefaultProfile</span></span>
<span data-ttu-id="de5c1-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de5c1-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de5c1-147">-Környezet</span><span class="sxs-lookup"><span data-stu-id="de5c1-147">-Environment</span></span>
<span data-ttu-id="de5c1-148">A fiókot tartalmazó környezet a bejelentkezéshez</span><span class="sxs-lookup"><span data-stu-id="de5c1-148">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="de5c1-149">-Force</span><span class="sxs-lookup"><span data-stu-id="de5c1-149">-Force</span></span>
<span data-ttu-id="de5c1-150">Felülírja a meglévő környezetet ugyanazzal a névvel, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="de5c1-150">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="de5c1-151">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="de5c1-151">-GraphAccessToken</span></span>
<span data-ttu-id="de5c1-152">AccessToken a Graph szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="de5c1-152">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="de5c1-153">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="de5c1-153">-KeyVaultAccessToken</span></span>
<span data-ttu-id="de5c1-154">AccessToken a rendszerhez</span><span class="sxs-lookup"><span data-stu-id="de5c1-154">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="de5c1-155">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="de5c1-155">-Scope</span></span>
<span data-ttu-id="de5c1-156">A környezeti változások hatókörét határozza meg, például a wheher módosítása csak a cusrrent folyamatra, illetve a felhasználó által indított összes munkamenetre érvényes.</span><span class="sxs-lookup"><span data-stu-id="de5c1-156">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="de5c1-157">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="de5c1-157">-ServicePrincipal</span></span>
<span data-ttu-id="de5c1-158">Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="de5c1-158">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de5c1-159">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="de5c1-159">-Subscription</span></span>
<span data-ttu-id="de5c1-160">Előfizetés neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="de5c1-160">Subscription Name or ID</span></span>

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

### <span data-ttu-id="de5c1-161">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="de5c1-161">-TenantId</span></span>
<span data-ttu-id="de5c1-162">Nem kötelező bérlői név vagy azonosító</span><span class="sxs-lookup"><span data-stu-id="de5c1-162">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId
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

### <span data-ttu-id="de5c1-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de5c1-163">-Confirm</span></span>
<span data-ttu-id="de5c1-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de5c1-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de5c1-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de5c1-165">-WhatIf</span></span>
<span data-ttu-id="de5c1-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de5c1-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de5c1-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de5c1-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de5c1-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5c1-168">CommonParameters</span></span>
<span data-ttu-id="de5c1-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de5c1-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5c1-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de5c1-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5c1-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de5c1-171">INPUTS</span></span>

### <span data-ttu-id="de5c1-172">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="de5c1-172">String</span></span>
<span data-ttu-id="de5c1-173">A ' SubscriptionId ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="de5c1-173">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="de5c1-174">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="de5c1-174">String</span></span>
<span data-ttu-id="de5c1-175">A ' SubscriptionName ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="de5c1-175">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="de5c1-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de5c1-176">OUTPUTS</span></span>

### <span data-ttu-id="de5c1-177">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="de5c1-177">PSAzureProfile</span></span>
<span data-ttu-id="de5c1-178">A bejelentkezett felhasználó hitelesítő adatait, előfizetését, fiókját és bérlői adatait.</span><span class="sxs-lookup"><span data-stu-id="de5c1-178">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="de5c1-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de5c1-179">NOTES</span></span>

## <span data-ttu-id="de5c1-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de5c1-180">RELATED LINKS</span></span>

