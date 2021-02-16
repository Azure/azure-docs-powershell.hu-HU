---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 8290ad3779c91565509833bbf41d7f9b37b07635
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153682"
---
# <span data-ttu-id="5e40a-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5e40a-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="5e40a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e40a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e40a-103">Hitelesítő adatokat ad hozzá egy meglévő alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="5e40a-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="5e40a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e40a-104">SYNTAX</span></span>

### <span data-ttu-id="5e40a-105">ApplicationObjectIdWithPasswordParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e40a-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e40a-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e40a-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e40a-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e40a-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e40a-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e40a-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e40a-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e40a-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e40a-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e40a-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e40a-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e40a-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e40a-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e40a-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e40a-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e40a-113">DESCRIPTION</span></span>
<span data-ttu-id="5e40a-114">A New-AzADAppCredential parancsmagot használhatja új hitelesítő adatok hozzáadásához vagy egy alkalmazás hitelesítő adatainak hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="5e40a-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="5e40a-115">Az alkalmazást az alkalmazásobjektum-azonosító vagy az alkalmazásazonosító megszolgáltatásával azonosítjuk.</span><span class="sxs-lookup"><span data-stu-id="5e40a-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="5e40a-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e40a-116">EXAMPLES</span></span>

### <span data-ttu-id="5e40a-117">1. példa: Új alkalmazás hitelesítő adatainak létrehozása jelszóval</span><span class="sxs-lookup"><span data-stu-id="5e40a-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="5e40a-118">A meglévő alkalmazáshoz 1f89cf81-0146-4f4e-beae-2007d0668416" objektumazonosítóval új jelszó lesz hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="5e40a-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="5e40a-119">2. példa: Új alkalmazás hitelesítő adatainak létrehozása tanúsítvány használatával</span><span class="sxs-lookup"><span data-stu-id="5e40a-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="5e40a-120">A megadott base64 kódolású nyilvános X509-tanúsítvány ("myapp.cer") hozzáadódik a meglévő alkalmazáshoz a (4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58) alkalmazásazonosítóval.</span><span class="sxs-lookup"><span data-stu-id="5e40a-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="5e40a-121">3. példa: Új alkalmazás hitelesítő adatainak létrehozása a pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="5e40a-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="5e40a-122">Az alkalmazás az "1f89cf81-0146-4f4e-beae-2007d0668416" objektumazonosítóval és az New-AzADAppCredential-hoz szükséges új alkalmazás hitelesítő adatok létrehozásához a megadott jelszóval.</span><span class="sxs-lookup"><span data-stu-id="5e40a-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="5e40a-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e40a-123">PARAMETERS</span></span>

### <span data-ttu-id="5e40a-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5e40a-124">-ApplicationId</span></span>
<span data-ttu-id="5e40a-125">Annak az alkalmazásnak az alkalmazásazonosítója, amelybe a hitelesítő adatokat fel kell adni.</span><span class="sxs-lookup"><span data-stu-id="5e40a-125">The application id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e40a-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="5e40a-126">-ApplicationObject</span></span>
<span data-ttu-id="5e40a-127">Az az alkalmazásobjektum, amelybe fel kell adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="5e40a-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e40a-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="5e40a-128">-CertValue</span></span>
<span data-ttu-id="5e40a-129">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="5e40a-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="5e40a-130">A 64-es alapkódolt tanúsítványt képviseli.</span><span class="sxs-lookup"><span data-stu-id="5e40a-130">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithCertValueParameterSet, ApplicationObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e40a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e40a-131">-DefaultProfile</span></span>
<span data-ttu-id="5e40a-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5e40a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e40a-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5e40a-133">-DisplayName</span></span>
<span data-ttu-id="5e40a-134">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="5e40a-134">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithPasswordParameterSet, DisplayNameWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e40a-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="5e40a-135">-EndDate</span></span>
<span data-ttu-id="5e40a-136">A hitelesítő adatok használatának tényleges záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="5e40a-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="5e40a-137">Az alapértelmezett záró dátum egy év a mai naptól.</span><span class="sxs-lookup"><span data-stu-id="5e40a-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="5e40a-138">Az "aszimmetrikus" típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt megelőzően kell megadni.</span><span class="sxs-lookup"><span data-stu-id="5e40a-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="5e40a-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5e40a-139">-ObjectId</span></span>
<span data-ttu-id="5e40a-140">Annak az alkalmazásnak az objektumazonosítója, amelybe a hitelesítő adatokat fel kell adni.</span><span class="sxs-lookup"><span data-stu-id="5e40a-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e40a-141">-Password</span><span class="sxs-lookup"><span data-stu-id="5e40a-141">-Password</span></span>
<span data-ttu-id="5e40a-142">Az alkalmazáshoz társítható jelszó.</span><span class="sxs-lookup"><span data-stu-id="5e40a-142">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: DisplayNameWithPasswordParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e40a-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="5e40a-143">-StartDate</span></span>
<span data-ttu-id="5e40a-144">A hitelesítő adatok használatának tényleges kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="5e40a-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="5e40a-145">A kezdő dátum alapértelmezett értéke a mai nap.</span><span class="sxs-lookup"><span data-stu-id="5e40a-145">The default start date value is today.</span></span> <span data-ttu-id="5e40a-146">Az "aszimmetrikus" típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt követően kell megadni.</span><span class="sxs-lookup"><span data-stu-id="5e40a-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="5e40a-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e40a-147">-Confirm</span></span>
<span data-ttu-id="5e40a-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5e40a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e40a-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e40a-149">-WhatIf</span></span>
<span data-ttu-id="5e40a-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5e40a-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e40a-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e40a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e40a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e40a-152">CommonParameters</span></span>
<span data-ttu-id="5e40a-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e40a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e40a-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e40a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e40a-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e40a-155">INPUTS</span></span>

### <span data-ttu-id="5e40a-156">System.String</span><span class="sxs-lookup"><span data-stu-id="5e40a-156">System.String</span></span>

### <span data-ttu-id="5e40a-157">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5e40a-157">System.Guid</span></span>

### <span data-ttu-id="5e40a-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="5e40a-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="5e40a-159">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="5e40a-159">System.Security.SecureString</span></span>

### <span data-ttu-id="5e40a-160">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="5e40a-160">System.DateTime</span></span>

## <span data-ttu-id="5e40a-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e40a-161">OUTPUTS</span></span>

### <span data-ttu-id="5e40a-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="5e40a-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="5e40a-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e40a-163">NOTES</span></span>

## <span data-ttu-id="5e40a-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e40a-164">RELATED LINKS</span></span>

[<span data-ttu-id="5e40a-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5e40a-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="5e40a-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5e40a-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="5e40a-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5e40a-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

