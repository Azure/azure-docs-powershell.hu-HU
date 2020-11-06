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
# Add-AzureRmAccount

## Áttekintés
Az Azure Resource Manager parancsmag-kérésekhez használható hitelesített fiók hozzáadása.

## SZINTAXISA

### UserWithSubscriptionId (alapértelmezett)
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UserWithSubscriptionName
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionName
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionName
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionName
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az Add-AzureRmAcccount parancsmag az Azure Resource Manager parancsmag-kérésekhez használható hitelesített Azure-fiókot ad hozzá.

Ezt a hitelesített fiókot csak az Azure Resource Manager parancsmagokkal használhatja.
Ha a szolgáltatásvezérlő parancsmagokkal használható hitelesített fiókot szeretne felvenni, használja a Add-AzureAccount vagy a Import-AzurePublishSettingsFile parancsmagot.

## Példák

### Példa 1: interaktív bejelentkezést igénylő fiók hozzáadása
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

Ez a parancs Azure Resource Manager-fiókot ad hozzá.

Ha az Azure Resource Manager-parancsmagokat ezzel a fiókkal szeretné futtatni, akkor a kérdésnél a Microsoft-fiók vagy a szervezeti azonosító hitelesítő adatait kell megadnia.

Ha a többtényezős hitelesítés engedélyezve van a hitelesítő adataiban, be kell jelentkeznie az interaktív beállítással vagy a Principal Authentication szolgáltatás használatával.

### 2. példa: a szervezeti azonosító hitelesítő adataival hitelesítő fiók hozzáadása
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

Az első parancs megkapja a felhasználó hitelesítő adatait, majd a $Credential változóban tárolja őket.

A második parancs az Azure Resource Manager-fiókot adja hozzá az $Credential hitelesítő adataival.

Ez a fiók az Azure Resource Manager segítségével hitelesíti a szervezeti azonosító hitelesítő adatait.
Ehhez a fiókhoz nem használható többtényezős hitelesítés vagy Microsoft-fiókhoz tartozó hitelesítő adatok az Azure Resource Manager-parancsmagok futtatásához.

### 3. példa: a Service Principal hitelesítő adataival hitelesítő fiók hozzáadása
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

Az első parancs megkapja a felhasználó hitelesítő adatait, majd a $Credential változóban tárolja őket.

A második parancs egy Azure Resource Manager-fiókot ad hozzá a megadott bérlői webhelyhez $Credentialban tárolt hitelesítő adatokkal.
A ServicePrincipal kapcsoló paraméter azt jelzi, hogy a fiók a szolgáltatás-megbízóként van hitelesítve.

### 4. példa: fiók hozzáadása adott bérlőhöz és előfizetéshez
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

Ez a parancs egy Azure Resource Manager-fiókot hoz létre, amellyel alapértelmezés szerint a megadott bérlői fiókhoz és előfizetéshez parancsmagok futtathatók.

## PARAMÉTEREK

### -AccessToken
Az Access-tokent adja meg.

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

### -AccountId
A hozzáférési jogkivonat fiókneve

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

### -ApplicationId
SPN

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

### -CertificateThumbprint
Certificate hash (ujjlenyomat)

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

### -Hitelesítő adatok
Egy PSCredential-objektumot ad meg.
Ha további információra van kíváncsi a PSCredential objektumról, írja be Get-Help Get-hitelesítő adatait.

A PSCredential objektum a szervezeti azonosító hitelesítő adatait, illetve az alkalmazás AZONOSÍTÓját, illetve a fő hitelesítő adatok titkos azonosítóját adja meg.

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

### -Környezet
A fiókot tartalmazó környezet a bejelentkezéshez

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

### -ServicePrincipal
Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.

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

### -SubscriptionId
Az előfizetés AZONOSÍTÓját adja meg.
Ha nem adja meg ezt a paramétert, a program az előfizetési lista első előfizetését használja.

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

### -SubscriptionName
Előfizetés neve

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

### -Bérlői azonosító megkeresése
Nem kötelező bérlői név vagy azonosító

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### PSAzureProfile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

