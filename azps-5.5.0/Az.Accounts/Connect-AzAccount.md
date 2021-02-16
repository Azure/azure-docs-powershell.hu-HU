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
# Connect-AzAccount

## SYNOPSIS
Csatlakozzon az Azure-hoz egy hitelesített fiókkal az Az PowerShell-modulok parancsmagjaival való használathoz.

## SZINTAXIS

### UserWithSubscriptionId (alapértelmezett)
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UserWithCredential
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS

A parancsmag egy hitelesített fiókkal csatlakozik az Azure-hoz az `Connect-AzAccount` Az PowerShell-modulok parancsmagjaival való használathoz. Ezt a hitelesített fiókot csak az Azure Resource Manager-kérésekkel használhatja. Ha hitelesített fiókot szeretne hozzáadni a Szolgáltatáskezeléshez, használja az `Add-AzureAccount` Azure PowerShell modul parancsmagját. Ha nincs kontextus az aktuális felhasználóhoz, a felhasználó környezetlistát az első 25 előfizetésük kontextusával tölti ki a rendszer.
A felhasználóhoz létrehozott környezetek listáját a futtatás után `Get-AzContext -ListAvailable` használhatja. A környezetfüggő sokaság kihagyása érdekében adja meg a **SkipContextPopulation** kapcsoló paramétert. A parancsmag végrehajtása után lecsatlakozhat egy Azure-fiókról. `Disconnect-AzAccount`

## PÉLDÁK

### 1. példa: Csatlakozás Azure-fiókhoz

Ez a példa egy Azure-fiókhoz kapcsolódik. Meg kell adnia egy Microsoft-fiókot vagy szervezeti azonosítót. Ha a hitelesítő adatokhoz engedélyezve van a többtényezős hitelesítés, akkor az interaktív lehetőséggel vagy egyszerű szolgáltatás-hitelesítéssel kell bejelentkeznie.

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 2. példa: (Csak Windows PowerShell 5.1 esetén) Csatlakozás az Azure-hoz szervezeti azonosítóval

Ez a forgatókönyv csak a Windows PowerShell 5.1-ben működik. Az első parancs kéri a felhasználói hitelesítő adatokat, és tárolja őket a `$Credential` változóban. A második parancs az Ebben tárolt hitelesítő adatokkal csatlakozik egy Azure-fiókhoz. `$Credential` Ez a fiók szervezeti azonosítóval hitelesíthető az Azure-ral.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 3. példa: Csatlakozás az Azure-hoz egyszerű szolgáltatásfiók használatával

Az első parancs kéri a szolgáltatáshoz szükséges egyszerű hitelesítő adatokat, és tárolja őket a `$Credential` változóban. Amikor a rendszer kéri, adja meg a felhasználónév és a szolgáltatás egyszerű kódjának azonosítóját jelszóként. A második parancs a megadott Azure-bérlőt a változóban tárolt egyszerű szolgáltatás hitelesítő adataival köti `$Credential` össze. A **ServicePrincipal kapcsoló** paramétere azt jelzi, hogy a fiók egyszerű szolgáltatásnévként van hitelesítve.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 4. példa: Interaktív bejelentkezés használata egy adott bérlőhöz és előfizetéshez való csatlakozáshoz

Ez a példa csatlakozik egy Azure-fiókhoz a megadott bérlői fiókkal és előfizetéssel.

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 5. példa: Csatlakozás felügyelt szolgáltatás-identitás használatával

Ez a példa a gazdakörnyezet Felügyelt szolgáltatás-identitásával (MSI) csatlakozik. Például egy olyan virtuális gépről jelentkezik be az Azure-ba, amely rendelkezik hozzárendelt MSI-vel.

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 6. példa: Csatlakozás Felügyelt szolgáltatás-identitás bejelentkezéssel és ClientId azonosítóval

Ez a példa a **myUserAssignedIdentity felügyelt szolgáltatás-identitásával kapcsolódik.** Hozzáadja a felhasználó által hozzárendelt identitást a virtuális géphez, majd a felhasználó által hozzárendelt identitás ClientId azonosítóját használva csatlakozik. További információt a felügyelt identitások konfigurálása [Azure-erőforrásokhoz Azure VM-en.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)

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

### 7. példa: Csatlakozás tanúsítványok használatával

Ez a példa tanúsítványalapú egyszerű szolgáltatás-hitelesítéssel csatlakozik egy Azure-fiókhoz.
A hitelesítéshez használt egyszerű szolgáltatásnévnek a megadott tanúsítvánnyal kell létrejönnie. Az önaírt tanúsítványok létrehozásáról és az engedélyek hozzárendelésével kapcsolatos további információkért lásd: Egyszerű szolgáltatásnév létrehozása tanúsítványsal az [Azure PowerShell használatával](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)

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

## PARAMETERS

### -AccessToken

Hozzáférési jogkivonatot ad meg.

> [!CAUTION]
> A hozzáférési jogkivonatok a hitelesítő adatok egy típusa. A bizalmas kezelés érdekében a megfelelő biztonsági óvintézkedést kell alkalmaznia. A hozzáférési jogkivonatok időtúllépést is okozhatnak, és megakadályozhatják a hosszú ideig futó feladatok elvégzését.

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

### -AccountId

A hozzáférési jogkivonat fiókazonosítója az **AccessToken** paraméterkészletében. A felügyelt szolgáltatás fiókazonosítója **a ManagedService paraméterkészletében.** Lehet felügyelt szolgáltatáserőforrás-azonosító vagy társított ügyfélazonosító.
A rendszer által hozzárendelt identitás használatához hagyja üresen ezt a mezőt.

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

### -ApplicationId

A szolgáltatásnév alkalmazásazonosítója.

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

### -CertificateThumbprint

Tanúsítvány kivonata vagy thumbprint.

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

### -ContextName

A bejelentkezés alapértelmezett Azure-környezetének neve. Az Azure környezetekkel kapcsolatos további információkért lásd az [Azure PowerShell környezetobjektumokat.](/powershell/azure/context-persistence)

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

### -Hitelesítő adatok

Egy **PSCredential objektumot** ad meg. A **PSCredential** objektumról a következőt írja be: `Get-Help Get-Credential` . A **PSCredential** objektum a szervezeti azonosítók felhasználói azonosítóját és jelszavát, illetve a szolgáltatásnévhez használt hitelesítő adatok azonosítóját és titkos azonosítóját biztosítja.

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

### -DefaultProfile

Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Környezet

Az Azure-fiókot tartalmazó környezet.

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

### -Force

A meglévő környezet felülírása ugyanazokkal a névvel, és nem kell rákérdezni.

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

### -GraphAccessToken

AccessToken for Graph Service.

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

### -Identity

Bejelentkezés felügyelt szolgáltatás-identitás használatával.

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

### -KeyVaultAccessToken

AccessToken a KeyVault szolgáltatáshoz.

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

### -ManagedServiceHostName

Elavult. Ha testre szabott MSI-végpontot használ, állítsa be a környezeti MSI_ENDPOINT, például " http://localhost:50342/oauth2/token ". A felügyelt szolgáltatás állomásneve.

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

### -ManagedServicePort

Elavult. Ha testre szabott MSI-végpontot használ, állítsa be a környezeti MSI_ENDPOINT, például " http://localhost:50342/oauth2/token ". A felügyelt szolgáltatás portszáma.

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

### -ManagedServiceSecret

Elavult. Ha testre szabott MSI-titkos halmazt használ, állítsa be a környezeti MSI_SECRET. Token a felügyelt szolgáltatásba való bejelentkezéshez.

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

### -MaxContextPopulation

Az előfizetés maximális száma a környezetek feltöltéséhez bejelentkezés után. Az alapértelmezett érték 25. Az összes előfizetés környezetbe való feltöltéséhez állítsa -1-re.

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

### -Scope

Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.

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

### -ServicePrincipal

Azt jelzi, hogy a fiók hitelesítése egyszerű szolgáltatásnévvel megadott hitelesítő adatokkal történik.

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

### -SkipContextPopulation

Kihagyja a környezet sokaságát, ha nem talál környezeteket.

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

### -SkipValidation

Hozzáférési jogkivonat érvényesítésének kihagyása.

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

### -Előfizetés

Előfizetés neve vagy azonosítója.

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

### -Tenant

Nem kötelező bérlő neve vagy azonosítója.

> [!NOTE]
> Az aktuális API korlátai miatt bérlőazonosítót kell használnia a bérlő neve helyett, amikor vállalati vállalati (B2B) fiókhoz csatlakozik.

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

### -UseDeviceAuthentication

Böngészővezérlő helyett használjon eszközkód-hitelesítést.

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

### -Confirm

A parancsmag futtatása előtt a rendszer megerősítést kér.

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

### -WhatIf

A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
