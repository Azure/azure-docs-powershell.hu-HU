---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 46977fe6b2e6cf3c3811c7d9bbd49262b06cec54
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208479"
---
# <span data-ttu-id="b8637-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b8637-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="b8637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8637-102">SYNOPSIS</span></span>
<span data-ttu-id="b8637-103">Hitelesítő adatokat ad hozzá egy meglévő egyszerű szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="b8637-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="b8637-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8637-104">SYNTAX</span></span>

### <span data-ttu-id="b8637-105">SpObjectIdWithPasswordParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8637-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8637-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8637-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8637-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8637-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8637-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8637-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8637-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8637-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8637-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8637-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8637-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8637-111">DESCRIPTION</span></span>
<span data-ttu-id="b8637-112">A New-AzADSpCredential parancsmag segítségével új hitelesítő adatokat adhat hozzá, vagy egy egyszerű szolgáltatásnévhez adhat hozzá hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b8637-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="b8637-113">A rendszer a egyszerű szolgáltatásnevet az objektumazonosító vagy a szolgáltatásnév megszolgáltatása alapján azonosítja.</span><span class="sxs-lookup"><span data-stu-id="b8637-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="b8637-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8637-114">EXAMPLES</span></span>

### <span data-ttu-id="b8637-115">1. példa: Új egyszerű szolgáltatás hitelesítő adatainak létrehozása létrehozott jelszóval</span><span class="sxs-lookup"><span data-stu-id="b8637-115">Example 1: Create a new service principal credential using a generated password</span></span>

```powershell
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="b8637-116">A rendszer új jelszót ad hozzá a meglévő egyszerű szolgáltatásnévhez az "1f99cf81-0146-4f4e-beae-2007d0668476" objektumazonosítóval.</span><span class="sxs-lookup"><span data-stu-id="b8637-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="b8637-117">2. példa: Új egyszerű szolgáltatás hitelesítő adatainak létrehozása tanúsítvány használatával</span><span class="sxs-lookup"><span data-stu-id="b8637-117">Example 2: Create a new service principal credential using a certificate</span></span>

```powershell
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="b8637-118">A megadott base64 kódolású nyilvános X509-tanúsítvány ("myapp.cer") a meglévő egyszerű szolgáltatásnévhez lesz hozzáadva az SPN használatával.</span><span class="sxs-lookup"><span data-stu-id="b8637-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="b8637-119">3. példa: Új egyszerű szolgáltatás hitelesítő adatainak létrehozása a pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="b8637-119">Example 3: Create a new service principal credential using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="b8637-120">Az egyszerű szolgáltatásnév 1f99cf81-0146-4f4e-beae-2007d0668476" objektumazonosítójával és az New-AzADSpCredential-hoz vezető vezetékekkel, amelyek létrehoznak egy új egyszerű szolgáltatás hitelesítő adatokat a szolgáltatásnévhez egy létrehozott jelszóval.</span><span class="sxs-lookup"><span data-stu-id="b8637-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="b8637-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8637-121">PARAMETERS</span></span>

### <span data-ttu-id="b8637-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b8637-122">-CertValue</span></span>
<span data-ttu-id="b8637-123">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="b8637-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b8637-124">A 64-es alapkódolt tanúsítványt képviseli.</span><span class="sxs-lookup"><span data-stu-id="b8637-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8637-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8637-125">-DefaultProfile</span></span>
<span data-ttu-id="b8637-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b8637-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8637-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b8637-127">-EndDate</span></span>
<span data-ttu-id="b8637-128">A hitelesítő adatok használatának tényleges záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="b8637-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b8637-129">Az alapértelmezett záró dátum egy év a mai naptól.</span><span class="sxs-lookup"><span data-stu-id="b8637-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="b8637-130">Az "aszimmetrikus" típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt megelőzően kell megadni.</span><span class="sxs-lookup"><span data-stu-id="b8637-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8637-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b8637-131">-ObjectId</span></span>
<span data-ttu-id="b8637-132">A szolgáltatásnév objektumazonosítója, amelybe fel kell adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b8637-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8637-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b8637-133">-ServicePrincipalName</span></span>
<span data-ttu-id="b8637-134">A szolgáltatásnév (SPN) neve, amelybe fel kell adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b8637-134">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8637-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="b8637-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="b8637-136">Az egyszerű szolgáltatásobjektum, amelybe fel kell adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b8637-136">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8637-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b8637-137">-StartDate</span></span>
<span data-ttu-id="b8637-138">A hitelesítő adatok használatának tényleges kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="b8637-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b8637-139">A kezdő dátum alapértelmezett értéke a mai nap.</span><span class="sxs-lookup"><span data-stu-id="b8637-139">The default start date value is today.</span></span>
<span data-ttu-id="b8637-140">Az "aszimmetrikus" típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt követően kell megadni.</span><span class="sxs-lookup"><span data-stu-id="b8637-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8637-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8637-141">-Confirm</span></span>
<span data-ttu-id="b8637-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b8637-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8637-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8637-143">-WhatIf</span></span>
<span data-ttu-id="b8637-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b8637-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8637-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8637-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8637-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8637-146">CommonParameters</span></span>
<span data-ttu-id="b8637-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8637-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8637-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8637-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8637-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8637-149">INPUTS</span></span>

### <span data-ttu-id="b8637-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b8637-150">System.String</span></span>

### <span data-ttu-id="b8637-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b8637-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="b8637-152">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="b8637-152">System.DateTime</span></span>

## <span data-ttu-id="b8637-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8637-153">OUTPUTS</span></span>

### <span data-ttu-id="b8637-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="b8637-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="b8637-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="b8637-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="b8637-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8637-156">NOTES</span></span>

## <span data-ttu-id="b8637-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8637-157">RELATED LINKS</span></span>

[<span data-ttu-id="b8637-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b8637-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="b8637-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b8637-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="b8637-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b8637-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



