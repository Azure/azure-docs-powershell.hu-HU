---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491040"
---
# <span data-ttu-id="5ac18-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="5ac18-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="5ac18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ac18-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac18-103">Az Azure Resource Manager parancsmag-kérésekhez használható hitelesített fiók hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="5ac18-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="5ac18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ac18-104">SYNTAX</span></span>

### <span data-ttu-id="5ac18-105">UserWithSubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ac18-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac18-106">UserWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5ac18-106">UserWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac18-107">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ac18-107">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac18-108">ServicePrincipalWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5ac18-108">ServicePrincipalWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac18-109">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ac18-109">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac18-110">ServicePrincipalCertificateWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5ac18-110">ServicePrincipalCertificateWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac18-111">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ac18-111">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac18-112">AccessTokenWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5ac18-112">AccessTokenWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ac18-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ac18-113">DESCRIPTION</span></span>
<span data-ttu-id="5ac18-114">Az Add-AzureRmAcccount parancsmag az Azure Resource Manager parancsmag-kérésekhez használható hitelesített Azure-fiókot ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="5ac18-114">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="5ac18-115">Ezt a hitelesített fiókot csak az Azure Resource Manager parancsmagokkal használhatja.</span><span class="sxs-lookup"><span data-stu-id="5ac18-115">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="5ac18-116">Ha a szolgáltatásvezérlő parancsmagokkal használható hitelesített fiókot szeretne felvenni, használja a Add-AzureAccount vagy a Import-AzurePublishSettingsFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5ac18-116">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="5ac18-117">Példák</span><span class="sxs-lookup"><span data-stu-id="5ac18-117">EXAMPLES</span></span>

### <span data-ttu-id="5ac18-118">Példa 1: interaktív bejelentkezést igénylő fiók hozzáadása</span><span class="sxs-lookup"><span data-stu-id="5ac18-118">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="5ac18-119">Ez a parancs Azure Resource Manager-fiókot ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="5ac18-119">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="5ac18-120">Ha az Azure Resource Manager-parancsmagokat ezzel a fiókkal szeretné futtatni, akkor a kérdésnél a Microsoft-fiók vagy a szervezeti azonosító hitelesítő adatait kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="5ac18-120">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="5ac18-121">Ha a többtényezős hitelesítés engedélyezve van a hitelesítő adataiban, be kell jelentkeznie az interaktív beállítással vagy a Principal Authentication szolgáltatás használatával.</span><span class="sxs-lookup"><span data-stu-id="5ac18-121">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="5ac18-122">2. példa: a szervezeti azonosító hitelesítő adataival hitelesítő fiók hozzáadása</span><span class="sxs-lookup"><span data-stu-id="5ac18-122">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="5ac18-123">Az első parancs megkapja a felhasználó hitelesítő adatait, majd a $Credential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="5ac18-123">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="5ac18-124">A második parancs az Azure Resource Manager-fiókot adja hozzá az $Credential hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="5ac18-124">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="5ac18-125">Ez a fiók az Azure Resource Manager segítségével hitelesíti a szervezeti azonosító hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="5ac18-125">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="5ac18-126">Ehhez a fiókhoz nem használható többtényezős hitelesítés vagy Microsoft-fiókhoz tartozó hitelesítő adatok az Azure Resource Manager-parancsmagok futtatásához.</span><span class="sxs-lookup"><span data-stu-id="5ac18-126">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="5ac18-127">3. példa: a Service Principal hitelesítő adataival hitelesítő fiók hozzáadása</span><span class="sxs-lookup"><span data-stu-id="5ac18-127">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="5ac18-128">Az első parancs megkapja a felhasználó hitelesítő adatait, majd a $Credential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="5ac18-128">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="5ac18-129">A második parancs egy Azure Resource Manager-fiókot ad hozzá a megadott bérlői webhelyhez $Credentialban tárolt hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="5ac18-129">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="5ac18-130">A ServicePrincipal kapcsoló paraméter azt jelzi, hogy a fiók a szolgáltatás-megbízóként van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="5ac18-130">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="5ac18-131">4. példa: fiók hozzáadása adott bérlőhöz és előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="5ac18-131">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="5ac18-132">Ez a parancs egy Azure Resource Manager-fiókot hoz létre, amellyel alapértelmezés szerint a megadott bérlői fiókhoz és előfizetéshez parancsmagok futtathatók.</span><span class="sxs-lookup"><span data-stu-id="5ac18-132">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="5ac18-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ac18-133">PARAMETERS</span></span>

### <span data-ttu-id="5ac18-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="5ac18-134">-AccessToken</span></span>
<span data-ttu-id="5ac18-135">Az Access-tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ac18-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac18-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="5ac18-136">-AccountId</span></span>
<span data-ttu-id="5ac18-137">A hozzáférési jogkivonat fiókneve</span><span class="sxs-lookup"><span data-stu-id="5ac18-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac18-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5ac18-138">-ApplicationId</span></span>
<span data-ttu-id="5ac18-139">SPN</span><span class="sxs-lookup"><span data-stu-id="5ac18-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac18-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="5ac18-140">-CertificateThumbprint</span></span>
<span data-ttu-id="5ac18-141">Certificate hash (ujjlenyomat)</span><span class="sxs-lookup"><span data-stu-id="5ac18-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac18-142">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="5ac18-142">-Credential</span></span>
<span data-ttu-id="5ac18-143">Egy PSCredential-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5ac18-143">Specifies a PSCredential object.</span></span>
<span data-ttu-id="5ac18-144">Ha további információra van kíváncsi a PSCredential objektumról, írja be Get-Help Get-hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="5ac18-144">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="5ac18-145">A PSCredential objektum a szervezeti azonosító hitelesítő adatait, illetve az alkalmazás AZONOSÍTÓját, illetve a fő hitelesítő adatok titkos azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ac18-145">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac18-146">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5ac18-146">-Environment</span></span>
<span data-ttu-id="5ac18-147">A fiókot tartalmazó környezet a bejelentkezéshez</span><span class="sxs-lookup"><span data-stu-id="5ac18-147">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="5ac18-148">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5ac18-148">-ServicePrincipal</span></span>
<span data-ttu-id="5ac18-149">Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="5ac18-149">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac18-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ac18-150">-SubscriptionId</span></span>
<span data-ttu-id="5ac18-151">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ac18-151">Specifies the ID of the subscription.</span></span>
<span data-ttu-id="5ac18-152">Ha nem adja meg ezt a paramétert, a program az előfizetési lista első előfizetését használja.</span><span class="sxs-lookup"><span data-stu-id="5ac18-152">If you do not specify this parameter, the first subscription from the subscription list is used.</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac18-153">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5ac18-153">-SubscriptionName</span></span>
<span data-ttu-id="5ac18-154">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="5ac18-154">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac18-155">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="5ac18-155">-TenantId</span></span>
<span data-ttu-id="5ac18-156">Nem kötelező bérlői név vagy azonosító</span><span class="sxs-lookup"><span data-stu-id="5ac18-156">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac18-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ac18-157">-Confirm</span></span>
<span data-ttu-id="5ac18-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ac18-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac18-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac18-159">-WhatIf</span></span>
<span data-ttu-id="5ac18-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ac18-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ac18-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ac18-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ac18-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac18-162">CommonParameters</span></span>
<span data-ttu-id="5ac18-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ac18-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac18-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac18-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac18-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac18-165">INPUTS</span></span>

## <span data-ttu-id="5ac18-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac18-166">OUTPUTS</span></span>

### <span data-ttu-id="5ac18-167">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="5ac18-167">PSAzureProfile</span></span>

## <span data-ttu-id="5ac18-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ac18-168">NOTES</span></span>

## <span data-ttu-id="5ac18-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ac18-169">RELATED LINKS</span></span>

