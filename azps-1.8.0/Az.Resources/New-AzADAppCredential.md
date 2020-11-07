---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 9305dc27f6c6486f34d1b5b9fb68844f967e3989
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669408"
---
# <span data-ttu-id="1d97a-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1d97a-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="1d97a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d97a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d97a-103">Hitelesítő adatok hozzáadása egy meglévő alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="1d97a-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="1d97a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d97a-104">SYNTAX</span></span>

### <span data-ttu-id="1d97a-105">ApplicationObjectIdWithPasswordParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d97a-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d97a-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d97a-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d97a-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d97a-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d97a-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d97a-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d97a-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d97a-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d97a-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d97a-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d97a-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d97a-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d97a-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d97a-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d97a-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d97a-113">DESCRIPTION</span></span>
<span data-ttu-id="1d97a-114">Az New-AzADAppCredential parancsmag használatával új hitelesítő adatokat vehet fel, illetve hitelesítő adatokat adhat meg az alkalmazásokhoz.</span><span class="sxs-lookup"><span data-stu-id="1d97a-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="1d97a-115">Az alkalmazás azonosítása az alkalmazásobjektum-azonosító vagy az alkalmazás azonosítójának megadásával történik.</span><span class="sxs-lookup"><span data-stu-id="1d97a-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="1d97a-116">Példák</span><span class="sxs-lookup"><span data-stu-id="1d97a-116">EXAMPLES</span></span>

### <span data-ttu-id="1d97a-117">Példa 1 – új alkalmazás hitelesítő adatainak létrehozása jelszó használatával</span><span class="sxs-lookup"><span data-stu-id="1d97a-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="1d97a-118">Az új jelszó-hitelesítő adatok hozzáadódnak a meglévő Appplication a ' 1f89cf81-0146-4f4e-beae-2007d0668416 ' azonosítójú azonosítójú objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="1d97a-118">A new password credential is added to the existing appplication with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="1d97a-119">2 példa – új alkalmazásspecifikus hitelesítő adatok létrehozása tanúsítvány használatával</span><span class="sxs-lookup"><span data-stu-id="1d97a-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="1d97a-120">A megadott Base64 kódolt nyilvános X509-tanúsítvány ("SajátPr. cer") hozzáadódik a meglévő, a "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58" azonosítójú alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="1d97a-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="1d97a-121">3 Példa – új alkalmazásspecifikus hitelesítő adatok létrehozása a csővezetékekkel</span><span class="sxs-lookup"><span data-stu-id="1d97a-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="1d97a-122">Beilleszti az "1f89cf81-0146-4f4e-beae-2007d0668416" azonosítójú alkalmazást, és a New-AzADAppCredential csöveket, amelyekkel új alkalmazás hitelesítő adatait létrehozhatja az adott alkalmazáshoz a megadott jelszóval.</span><span class="sxs-lookup"><span data-stu-id="1d97a-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="1d97a-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d97a-123">PARAMETERS</span></span>

### <span data-ttu-id="1d97a-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1d97a-124">-ApplicationId</span></span>
<span data-ttu-id="1d97a-125">Az alkalmazás azonosítóját adja hozzá a hitelesítő adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="1d97a-125">The application id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="1d97a-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="1d97a-126">-ApplicationObject</span></span>
<span data-ttu-id="1d97a-127">Az Application objektum a hitelesítő adatok hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="1d97a-127">The application object to add the credentials to.</span></span>

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

### <span data-ttu-id="1d97a-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="1d97a-128">-CertValue</span></span>
<span data-ttu-id="1d97a-129">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="1d97a-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="1d97a-130">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="1d97a-130">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="1d97a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d97a-131">-DefaultProfile</span></span>
<span data-ttu-id="1d97a-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1d97a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d97a-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1d97a-133">-DisplayName</span></span>
<span data-ttu-id="1d97a-134">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="1d97a-134">The display name of the application.</span></span>

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

### <span data-ttu-id="1d97a-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="1d97a-135">-EndDate</span></span>
<span data-ttu-id="1d97a-136">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="1d97a-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="1d97a-137">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="1d97a-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="1d97a-138">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="1d97a-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="1d97a-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1d97a-139">-ObjectId</span></span>
<span data-ttu-id="1d97a-140">Annak az objektumnak az azonosítója, amelyhez hozzá szeretné adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="1d97a-140">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="1d97a-141">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="1d97a-141">-Password</span></span>
<span data-ttu-id="1d97a-142">Az alkalmazáshoz társított jelszó.</span><span class="sxs-lookup"><span data-stu-id="1d97a-142">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="1d97a-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="1d97a-143">-StartDate</span></span>
<span data-ttu-id="1d97a-144">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="1d97a-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="1d97a-145">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="1d97a-145">The default start date value is today.</span></span> <span data-ttu-id="1d97a-146">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="1d97a-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="1d97a-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d97a-147">-Confirm</span></span>
<span data-ttu-id="1d97a-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d97a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d97a-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d97a-149">-WhatIf</span></span>
<span data-ttu-id="1d97a-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d97a-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d97a-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d97a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d97a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d97a-152">CommonParameters</span></span>
<span data-ttu-id="1d97a-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d97a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d97a-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d97a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d97a-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d97a-155">INPUTS</span></span>

### <span data-ttu-id="1d97a-156">System. String</span><span class="sxs-lookup"><span data-stu-id="1d97a-156">System.String</span></span>

### <span data-ttu-id="1d97a-157">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1d97a-157">System.Guid</span></span>

### <span data-ttu-id="1d97a-158">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1d97a-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="1d97a-159">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1d97a-159">System.Security.SecureString</span></span>

### <span data-ttu-id="1d97a-160">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="1d97a-160">System.DateTime</span></span>

## <span data-ttu-id="1d97a-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d97a-161">OUTPUTS</span></span>

### <span data-ttu-id="1d97a-162">Microsoft. Azure. Command. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="1d97a-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="1d97a-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d97a-163">NOTES</span></span>

## <span data-ttu-id="1d97a-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d97a-164">RELATED LINKS</span></span>

[<span data-ttu-id="1d97a-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1d97a-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="1d97a-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1d97a-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="1d97a-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1d97a-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

