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
# Connect-AzAccount

## Áttekintés
Csatlakozás az Azure-hoz hitelesített fiókkal az Azure Resource Manager parancsmag-kérésekkel való használathoz.

## SZINTAXISA

### UserWithSubscriptionId (alapértelmezett)
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UserWithCredential
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
Az Connect-AzAccount parancsmag az Azure erőforrás-kezelő parancsmag-kérésekkel használható hitelesített fiókkal csatlakozik az Azure-hoz.
Ezt a hitelesített fiókot csak az Azure Resource Manager parancsmagokkal használhatja.
Ha a szolgáltatásvezérlő parancsmagokkal használható hitelesített fiókot szeretne felvenni, használja a Add-AzAccount vagy a Import-AzPublishSettingsFile parancsmagot.
Ha az aktuális felhasználóhoz nem tartozik környezet, ez a parancs a felhasználó helyi listáját fogja kitölteni mindegyik (az első 25) előfizetése kontextusában. A felhasználóhoz létrehozott környezetek listája a "Get-AzContext – ListAvailable" futtatásával érhető el. A környezeti sokaság kihagyásához futtathatja ezt a parancsot a "-SkipContextPopulation" kapcsoló paraméterrel.
A parancsmag végrehajtása után az Azure-fiókokat leválaszthatja a leválasztást a AzAccount.

## Példák

### 1. példa: interaktív bejelentkezés használata Azure-fiókhoz való csatlakozáshoz
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Ez a parancs Azure-fiókhoz csatlakozik.
Ha az Azure Resource Manager-parancsmagokat ezzel a fiókkal szeretné futtatni, akkor a kérdésnél a Microsoft-fiók vagy a szervezeti azonosító hitelesítő adatait kell megadnia.
Ha a többtényezős hitelesítés engedélyezve van a hitelesítő adataiban, be kell jelentkeznie az interaktív beállítással vagy a Principal Authentication szolgáltatás használatával.

### 2. példa: (csak a Windows PowerShell 5,1) csatlakozás Azure-fiókhoz szervezeti azonosító hitelesítő adataival
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Ez a forgatókönyv csak a Windows PowerShell 5,1-ban működik. Az első parancs kérni fogja a felhasználói hitelesítő adatok (Felhasználónév és jelszó) megadását, majd a $Credential változóban tárolja őket.
A második parancs a $Credentialban tárolt hitelesítő adatok használatával csatlakozik az Azure-fiókhoz.
Ez a fiók az Azure Resource Manager segítségével hitelesíti a szervezeti azonosító hitelesítő adatait.
Ehhez a fiókhoz nem használható többtényezős hitelesítés vagy Microsoft-fiókhoz tartozó hitelesítő adatok az Azure Resource Manager-parancsmagok futtatásához.

### 3. példa: csatlakozás Azure-ös egyszerű szolgáltatási fiókhoz
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Az első parancs a szolgáltatás fő hitelesítő adatait (alkalmazásspecifikus azonosítóját és a szolgáltatás fő titkát) kapja meg, majd a $Credential változóban tárolja.
A második parancs az Azurehoz csatlakozik a megadott bérlői web$Credentialban tárolt szolgáltatás-fő hitelesítő adatokkal.
A ServicePrincipal kapcsoló paraméter azt jelzi, hogy a fiók a szolgáltatás-megbízóként van hitelesítve.

### 4. példa: interaktív bejelentkezés használata egy adott bérlői fiókhoz való csatlakozáshoz és előfizetéshez
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Ez a parancs egy Azure-fiókhoz csatlakozik, és konfigurálva van a AzureRM PowerShell a megadott bérlői fiók és az előfizetés parancsmagjának futtatásához alapértelmezés szerint.

### 5. példa: fiók felvétele a felügyelt szolgáltatás identitási bejelentkezési funkciójával
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Ez a parancs az állomás környezetének felügyelt szolgáltatás identitásával csatlakozik hozzá (például ha a felügyelt szolgáltatás-identitással rendelkező VirtualMachine hajtja végre a kódot, így a kód bejelentkezhet a hozzárendelt identitás használatával)

### 6. példa: fiók hozzáadása a felügyelt szolgáltatás identitás-bejelentkezési és ClientId
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Ez a parancs a "myUserAssignedIdentity" felügyelt szolgáltatás identitásával csatlakozik a felhasználóhoz rendelt identitás hozzáadásával a virtuális géphez, majd a felhasználó által kiosztott identitás ClientId.
A felügyelt identitások konfigurálásáról további információt itt találhat: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .

### 7. példa: fiók hozzáadása a felügyelt szolgáltatás identitás-bejelentkezési és ClientId
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Ez a parancs a "myUserAssignedIdentity" felügyelt szolgáltatás identitásával csatlakozik a felhasználóhoz rendelt identitás hozzáadásával a virtuális géphez, majd a felhasználó által kiosztott identitás azonosítójának használatával.
A felügyelt identitások konfigurálásáról további információt itt találhat: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .

### 8. példa: fiók hozzáadása tanúsítványok használatával
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

Ez a parancs egy Azure-fiókhoz, a tanúsítvány-alapú szolgáltatás egyszerű hitelesítésével csatlakozik. A hitelesítéshez használt szolgáltatásnevet a megadott tanúsítvánnyal kell létrehozni.

### Példa 9: fiók hozzáadása a AccessToken-hitelesítéssel
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

Ez a parancs a "AccountId" mezőben megadott Azure-fiókhoz csatlakozik a megadott AccessToken és KeyVaultAccessToken használatával.

## PARAMÉTEREK

### -AccessToken
Az Access-tokent adja meg.

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
Az AccessToken paraméterben megadott hozzáférési jogkivonat fiókneve. A felügyelt szolgáltatáshoz tartozó fiókazonosító a ManagedService paraméterben. Lehet felügyelt szolgáltatás-erőforrás azonosítója vagy a hozzá tartozó ügyfél-azonosító. A SystemAssigned identitás használatához hagyja üresen ezt a mezőt.

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
SPN

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
Certificate hash (ujjlenyomat)

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
Az alapértelmezett környezet neve ebből a bejelentkezésből.  A bejelentkezés után ezt a nevet fogja tudni választani.

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
Egy PSCredential-objektumot ad meg.
Ha további információra van kíváncsi a PSCredential objektumról, írja be Get-Help Get-hitelesítő adatait.
A PSCredential objektum a szervezeti azonosító hitelesítő adatait, illetve az alkalmazás AZONOSÍTÓját, illetve a fő hitelesítő adatok titkos azonosítóját adja meg.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
A fiókot tartalmazó környezet a bejelentkezéshez

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
Felülírja a meglévő környezetet ugyanazzal a névvel, ha van ilyen.

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
AccessToken a Graph szolgáltatáshoz

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

### – Identitás
Jelentkezzen be a felügyelt szolgáltatás identitása szolgáltatással az aktuális környezetben.

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
AccessToken a rendszerhez

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
Host Name a felügyelt szolgáltatás bejelentkezéséhez

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
A felügyelt szolgáltatás bejelentkezésének portszáma

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
Titkos – bizonyos típusú felügyelt szolgáltatás-bejelentkezéshez használt.

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

### -Scope (hatókör)
Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.

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
Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.

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
A környezeti populáció kihagyása, ha nincsenek kontextusok.

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
Az érvényesítés kihagyása az Access-jogkivonat esetében

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
Előfizetés neve vagy azonosítója

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

### -Bérlő
Nem kötelező bérlői név vagy azonosító

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
Az áfakód-hitelesítés használata a böngésző vezérlő helyett

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. profil. models. Core. PSAzureProfile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
