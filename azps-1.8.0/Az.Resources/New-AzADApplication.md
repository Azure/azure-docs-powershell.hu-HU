---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: fa861a7be0716ec1da1f2f2a100e7dbbdc97af51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669407"
---
# <span data-ttu-id="3dfda-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="3dfda-101">New-AzADApplication</span></span>

## <span data-ttu-id="3dfda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3dfda-102">SYNOPSIS</span></span>
<span data-ttu-id="3dfda-103">Új Azure Active Directory-alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3dfda-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="3dfda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3dfda-104">SYNTAX</span></span>

### <span data-ttu-id="3dfda-105">ApplicationWithoutCredentialParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3dfda-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dfda-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dfda-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dfda-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dfda-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dfda-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dfda-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dfda-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dfda-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dfda-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="3dfda-110">DESCRIPTION</span></span>
<span data-ttu-id="3dfda-111">Új Azure Active Directory-alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3dfda-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="3dfda-112">Példák</span><span class="sxs-lookup"><span data-stu-id="3dfda-112">EXAMPLES</span></span>

### <span data-ttu-id="3dfda-113">Példa 1 – új AAD alkalmazás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="3dfda-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="3dfda-114">Új Azure Active Directory-alkalmazást hoz létre hitelesítő adatok nélkül.</span><span class="sxs-lookup"><span data-stu-id="3dfda-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="3dfda-115">Példa 2 – új AAD-alkalmazás létrehozása jelszóval.</span><span class="sxs-lookup"><span data-stu-id="3dfda-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="3dfda-116">Új Azure Active Directory-alkalmazás létrehozása és a jelszóhoz kapcsolódó hitelesítő adatok társítása.</span><span class="sxs-lookup"><span data-stu-id="3dfda-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="3dfda-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3dfda-117">PARAMETERS</span></span>

### <span data-ttu-id="3dfda-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="3dfda-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="3dfda-119">Az az érték, amely azt adja meg, hogy az alkalmazás egyetlen bérlő vagy több bérlői fiók-e.</span><span class="sxs-lookup"><span data-stu-id="3dfda-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="3dfda-120">-CertValue</span></span>
<span data-ttu-id="3dfda-121">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="3dfda-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="3dfda-122">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="3dfda-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dfda-123">-DefaultProfile</span></span>
<span data-ttu-id="3dfda-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3dfda-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3dfda-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3dfda-125">-DisplayName</span></span>
<span data-ttu-id="3dfda-126">Az új alkalmazás megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="3dfda-126">Display name of the new application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="3dfda-127">-EndDate</span></span>
<span data-ttu-id="3dfda-128">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="3dfda-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="3dfda-129">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="3dfda-129">The default end date value is one year from today.</span></span> <span data-ttu-id="3dfda-130">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="3dfda-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-131">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="3dfda-131">-HomePage</span></span>
<span data-ttu-id="3dfda-132">Az alkalmazás kezdőlapjának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="3dfda-132">The URL to the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="3dfda-133">-IdentifierUris</span></span>
<span data-ttu-id="3dfda-134">Az alkalmazást azonosító URI-k.</span><span class="sxs-lookup"><span data-stu-id="3dfda-134">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-135">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="3dfda-135">-KeyCredentials</span></span>
<span data-ttu-id="3dfda-136">Az alkalmazáshoz társított tanúsítvány-hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="3dfda-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-137">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="3dfda-137">-Password</span></span>
<span data-ttu-id="3dfda-138">Az alkalmazáshoz társított jelszó.</span><span class="sxs-lookup"><span data-stu-id="3dfda-138">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="3dfda-139">-PasswordCredentials</span></span>
<span data-ttu-id="3dfda-140">Az alkalmazáshoz társított jelszós hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="3dfda-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="3dfda-141">-ReplyUrls</span></span>
<span data-ttu-id="3dfda-142">Az alkalmazás válaszának URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3dfda-142">The application reply urls.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="3dfda-143">-StartDate</span></span>
<span data-ttu-id="3dfda-144">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="3dfda-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="3dfda-145">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="3dfda-145">The default start date value is today.</span></span> <span data-ttu-id="3dfda-146">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="3dfda-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfda-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3dfda-147">-Confirm</span></span>
<span data-ttu-id="3dfda-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3dfda-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dfda-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dfda-149">-WhatIf</span></span>
<span data-ttu-id="3dfda-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3dfda-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dfda-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3dfda-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dfda-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dfda-152">CommonParameters</span></span>
<span data-ttu-id="3dfda-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3dfda-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dfda-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dfda-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dfda-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dfda-155">INPUTS</span></span>

### <span data-ttu-id="3dfda-156">System. String</span><span class="sxs-lookup"><span data-stu-id="3dfda-156">System.String</span></span>

### <span data-ttu-id="3dfda-157">System. string []</span><span class="sxs-lookup"><span data-stu-id="3dfda-157">System.String[]</span></span>

### <span data-ttu-id="3dfda-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3dfda-158">System.Boolean</span></span>

### <span data-ttu-id="3dfda-159">Microsoft. Azure. Command. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="3dfda-159">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="3dfda-160">Microsoft. Azure. Command. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="3dfda-160">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="3dfda-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="3dfda-161">System.Security.SecureString</span></span>

### <span data-ttu-id="3dfda-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="3dfda-162">System.DateTime</span></span>

## <span data-ttu-id="3dfda-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dfda-163">OUTPUTS</span></span>

### <span data-ttu-id="3dfda-164">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="3dfda-164">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="3dfda-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3dfda-165">NOTES</span></span>
<span data-ttu-id="3dfda-166">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="3dfda-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3dfda-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3dfda-167">RELATED LINKS</span></span>

[<span data-ttu-id="3dfda-168">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="3dfda-168">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="3dfda-169">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="3dfda-169">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="3dfda-170">Új – AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3dfda-170">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="3dfda-171">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3dfda-171">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="3dfda-172">Új – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3dfda-172">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="3dfda-173">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3dfda-173">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

