---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 38952cb7c7deebb76568bef2a2062d20c3c1b497
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928945"
---
# <span data-ttu-id="b0a03-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b0a03-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="b0a03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a03-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a03-103">Hitelesítő adatokat ad hozzá egy meglévő egyszerű szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="b0a03-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="b0a03-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0a03-104">SYNTAX</span></span>

### <span data-ttu-id="b0a03-105">SpObjectIdWithPasswordParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0a03-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a03-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a03-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a03-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a03-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a03-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a03-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a03-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a03-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a03-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a03-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0a03-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0a03-111">DESCRIPTION</span></span>
<span data-ttu-id="b0a03-112">A New-AzADSpCredential parancsmag segítségével új hitelesítő adatokat adhat hozzá, vagy egy egyszerű szolgáltatásnévhez is be lehet adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b0a03-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="b0a03-113">A rendszer a egyszerű szolgáltatásnevet az objektumazonosító vagy a szolgáltatásnév megszolgáltatása alapján azonosítja.</span><span class="sxs-lookup"><span data-stu-id="b0a03-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="b0a03-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0a03-114">EXAMPLES</span></span>

### <span data-ttu-id="b0a03-115">1. példa: Új egyszerű szolgáltatás hitelesítő adatainak létrehozása létrehozott jelszóval</span><span class="sxs-lookup"><span data-stu-id="b0a03-115">Example 1: Create a new service principal credential using a generated password</span></span>

```powershell
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="b0a03-116">A rendszer új jelszó hitelesítő adatokat ad a meglévő egyszerű szolgáltatásnévhez az "1f99cf81-0146-4f4e-beae-2007d0668476" objektumazonosítóval.</span><span class="sxs-lookup"><span data-stu-id="b0a03-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="b0a03-117">2. példa: Új egyszerű szolgáltatás hitelesítő adatainak létrehozása tanúsítvány használatával</span><span class="sxs-lookup"><span data-stu-id="b0a03-117">Example 2: Create a new service principal credential using a certificate</span></span>

```powershell
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="b0a03-118">A megadott base64 kódolású nyilvános X509-tanúsítvány ("myapp.cer") a meglévő egyszerű szolgáltatásnévhez lesz hozzáadva az SPN használatával.</span><span class="sxs-lookup"><span data-stu-id="b0a03-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="b0a03-119">3. példa: Új egyszerű szolgáltatás hitelesítő adatainak létrehozása pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="b0a03-119">Example 3: Create a new service principal credential using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="b0a03-120">Az egyszerű szolgáltatásnév 1f99cf81-0146-4f4e-beae-2007d0668476" objektumazonosítójával és az New-AzADSpCredential-hoz vezető vezetékekkel, amelyek létrehoznak egy új egyszerű szolgáltatás hitelesítő adatokat a szolgáltatásnévhez egy létrehozott jelszóval.</span><span class="sxs-lookup"><span data-stu-id="b0a03-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="b0a03-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0a03-121">PARAMETERS</span></span>

### <span data-ttu-id="b0a03-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b0a03-122">-CertValue</span></span>
<span data-ttu-id="b0a03-123">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="b0a03-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b0a03-124">A 64-es alapkódolt tanúsítványt képviseli.</span><span class="sxs-lookup"><span data-stu-id="b0a03-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="b0a03-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a03-125">-DefaultProfile</span></span>
<span data-ttu-id="b0a03-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b0a03-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0a03-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b0a03-127">-EndDate</span></span>
<span data-ttu-id="b0a03-128">A hitelesítő adatok használatának tényleges záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="b0a03-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b0a03-129">Az alapértelmezett záró dátum egy év a mai naptól.</span><span class="sxs-lookup"><span data-stu-id="b0a03-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="b0a03-130">Az "aszimmetrikus" típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt megelőzően kell megadni.</span><span class="sxs-lookup"><span data-stu-id="b0a03-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="b0a03-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b0a03-131">-ObjectId</span></span>
<span data-ttu-id="b0a03-132">A szolgáltatásnév objektumazonosítója, amelybe fel kell adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b0a03-132">The object id of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="b0a03-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b0a03-133">-ServicePrincipalName</span></span>
<span data-ttu-id="b0a03-134">A szolgáltatásnév (SPN) neve, amelybe a hitelesítő adatokat fel kell adni.</span><span class="sxs-lookup"><span data-stu-id="b0a03-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="b0a03-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="b0a03-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="b0a03-136">Az egyszerű szolgáltatásobjektum, amelybe fel kell adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b0a03-136">The service principal object to add the credentials to.</span></span>

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

### <span data-ttu-id="b0a03-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b0a03-137">-StartDate</span></span>
<span data-ttu-id="b0a03-138">A hitelesítő adatok használatának tényleges kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="b0a03-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b0a03-139">Az alapértelmezett kezdő dátum a mai nap.</span><span class="sxs-lookup"><span data-stu-id="b0a03-139">The default start date value is today.</span></span>
<span data-ttu-id="b0a03-140">Az "aszimmetrikus" típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt követően kell megadni.</span><span class="sxs-lookup"><span data-stu-id="b0a03-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="b0a03-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0a03-141">-Confirm</span></span>
<span data-ttu-id="b0a03-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b0a03-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0a03-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0a03-143">-WhatIf</span></span>
<span data-ttu-id="b0a03-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b0a03-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0a03-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0a03-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0a03-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a03-146">CommonParameters</span></span>
<span data-ttu-id="b0a03-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0a03-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a03-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0a03-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a03-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0a03-149">INPUTS</span></span>

### <span data-ttu-id="b0a03-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b0a03-150">System.String</span></span>

### <span data-ttu-id="b0a03-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b0a03-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="b0a03-152">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="b0a03-152">System.DateTime</span></span>

## <span data-ttu-id="b0a03-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0a03-153">OUTPUTS</span></span>

### <span data-ttu-id="b0a03-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="b0a03-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="b0a03-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="b0a03-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="b0a03-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0a03-156">NOTES</span></span>

## <span data-ttu-id="b0a03-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0a03-157">RELATED LINKS</span></span>

[<span data-ttu-id="b0a03-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b0a03-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="b0a03-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b0a03-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="b0a03-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b0a03-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



