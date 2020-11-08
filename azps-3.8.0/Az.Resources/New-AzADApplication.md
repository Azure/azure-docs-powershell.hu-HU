---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: a60e2b873803c8ad3acfdc08c645cf419cf8689f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014460"
---
# <span data-ttu-id="bd9af-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bd9af-101">New-AzADApplication</span></span>

## <span data-ttu-id="bd9af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd9af-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9af-103">Új Azure Active Directory-alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bd9af-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="bd9af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd9af-104">SYNTAX</span></span>

### <span data-ttu-id="bd9af-105">ApplicationWithoutCredentialParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd9af-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd9af-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd9af-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd9af-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd9af-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd9af-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd9af-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd9af-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd9af-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd9af-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd9af-110">DESCRIPTION</span></span>
<span data-ttu-id="bd9af-111">Új Azure Active Directory-alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bd9af-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="bd9af-112">Az alábbi engedélyek szükségesek az alkalmazás létrehozásához:</span><span class="sxs-lookup"><span data-stu-id="bd9af-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="bd9af-113">Azure Active Directory-diagram</span><span class="sxs-lookup"><span data-stu-id="bd9af-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="bd9af-114">Application. ReadWrite. OwnedBy</span><span class="sxs-lookup"><span data-stu-id="bd9af-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="bd9af-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="bd9af-115">Microsoft Graph</span></span>
  - <span data-ttu-id="bd9af-116">Directory. AccessAsUser. All</span><span class="sxs-lookup"><span data-stu-id="bd9af-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="bd9af-117">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="bd9af-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="bd9af-118">Példák</span><span class="sxs-lookup"><span data-stu-id="bd9af-118">EXAMPLES</span></span>

### <span data-ttu-id="bd9af-119">Példa 1 – új AAD alkalmazás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="bd9af-119">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="bd9af-120">Új Azure Active Directory-alkalmazást hoz létre hitelesítő adatok nélkül.</span><span class="sxs-lookup"><span data-stu-id="bd9af-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="bd9af-121">Példa 2 – új AAD-alkalmazás létrehozása jelszóval.</span><span class="sxs-lookup"><span data-stu-id="bd9af-121">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="bd9af-122">Új Azure Active Directory-alkalmazás létrehozása és a jelszóhoz kapcsolódó hitelesítő adatok társítása.</span><span class="sxs-lookup"><span data-stu-id="bd9af-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="bd9af-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd9af-123">PARAMETERS</span></span>

### <span data-ttu-id="bd9af-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="bd9af-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="bd9af-125">Az az érték, amely azt adja meg, hogy az alkalmazás egyetlen bérlő vagy több bérlői fiók-e.</span><span class="sxs-lookup"><span data-stu-id="bd9af-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="bd9af-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="bd9af-126">-CertValue</span></span>
<span data-ttu-id="bd9af-127">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="bd9af-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="bd9af-128">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="bd9af-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="bd9af-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9af-129">-DefaultProfile</span></span>
<span data-ttu-id="bd9af-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bd9af-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd9af-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bd9af-131">-DisplayName</span></span>
<span data-ttu-id="bd9af-132">Az új alkalmazás megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="bd9af-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="bd9af-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="bd9af-133">-EndDate</span></span>
<span data-ttu-id="bd9af-134">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="bd9af-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="bd9af-135">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="bd9af-135">The default end date value is one year from today.</span></span> <span data-ttu-id="bd9af-136">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="bd9af-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="bd9af-137">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="bd9af-137">-HomePage</span></span>
<span data-ttu-id="bd9af-138">Az alkalmazás kezdőlapjának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="bd9af-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="bd9af-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="bd9af-139">-IdentifierUris</span></span>
<span data-ttu-id="bd9af-140">Az alkalmazást azonosító URI-k.</span><span class="sxs-lookup"><span data-stu-id="bd9af-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="bd9af-141">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="bd9af-141">-KeyCredentials</span></span>
<span data-ttu-id="bd9af-142">Az alkalmazáshoz társított tanúsítvány-hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="bd9af-142">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="bd9af-143">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="bd9af-143">-Password</span></span>
<span data-ttu-id="bd9af-144">Az alkalmazáshoz társított jelszó.</span><span class="sxs-lookup"><span data-stu-id="bd9af-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="bd9af-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="bd9af-145">-PasswordCredentials</span></span>
<span data-ttu-id="bd9af-146">Az alkalmazáshoz társított jelszós hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="bd9af-146">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="bd9af-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="bd9af-147">-ReplyUrls</span></span>
<span data-ttu-id="bd9af-148">Az alkalmazás válaszának URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bd9af-148">The application reply urls.</span></span>

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

### <span data-ttu-id="bd9af-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="bd9af-149">-StartDate</span></span>
<span data-ttu-id="bd9af-150">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="bd9af-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="bd9af-151">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="bd9af-151">The default start date value is today.</span></span> <span data-ttu-id="bd9af-152">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="bd9af-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="bd9af-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bd9af-153">-Confirm</span></span>
<span data-ttu-id="bd9af-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd9af-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd9af-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd9af-155">-WhatIf</span></span>
<span data-ttu-id="bd9af-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bd9af-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd9af-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd9af-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd9af-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9af-158">CommonParameters</span></span>
<span data-ttu-id="bd9af-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd9af-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9af-160">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bd9af-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9af-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd9af-161">INPUTS</span></span>

### <span data-ttu-id="bd9af-162">System. String</span><span class="sxs-lookup"><span data-stu-id="bd9af-162">System.String</span></span>

### <span data-ttu-id="bd9af-163">System. string []</span><span class="sxs-lookup"><span data-stu-id="bd9af-163">System.String[]</span></span>

### <span data-ttu-id="bd9af-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd9af-164">System.Boolean</span></span>

### <span data-ttu-id="bd9af-165">Microsoft. Azure. Command. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="bd9af-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="bd9af-166">Microsoft. Azure. Command. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="bd9af-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="bd9af-167">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="bd9af-167">System.Security.SecureString</span></span>

### <span data-ttu-id="bd9af-168">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bd9af-168">System.DateTime</span></span>

## <span data-ttu-id="bd9af-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd9af-169">OUTPUTS</span></span>

### <span data-ttu-id="bd9af-170">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="bd9af-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="bd9af-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd9af-171">NOTES</span></span>
<span data-ttu-id="bd9af-172">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="bd9af-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="bd9af-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd9af-173">RELATED LINKS</span></span>

[<span data-ttu-id="bd9af-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bd9af-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="bd9af-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bd9af-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="bd9af-176">Új – AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bd9af-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="bd9af-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bd9af-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="bd9af-178">Új – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bd9af-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="bd9af-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bd9af-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

