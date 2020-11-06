---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: 171f09e2d9a9e6e646731817526451b311f94482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500419"
---
# <span data-ttu-id="c65c2-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c65c2-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="c65c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c65c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c65c2-103">Új Azure Active Directory-alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c65c2-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c65c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c65c2-104">SYNTAX</span></span>

### <span data-ttu-id="c65c2-105">ApplicationWithoutCredentialParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c65c2-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65c2-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c65c2-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65c2-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c65c2-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65c2-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c65c2-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65c2-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c65c2-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c65c2-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="c65c2-110">DESCRIPTION</span></span>
<span data-ttu-id="c65c2-111">Új Azure Active Directory-alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c65c2-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="c65c2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c65c2-112">EXAMPLES</span></span>

### <span data-ttu-id="c65c2-113">Hozzon létre új AAD-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="c65c2-113">Create new AAD application.</span></span>
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="c65c2-114">Új Azure Active Directory-alkalmazást hoz létre hitelesítő adatok nélkül.</span><span class="sxs-lookup"><span data-stu-id="c65c2-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="c65c2-115">Új AAD-alkalmazás létrehozása jelszóval.</span><span class="sxs-lookup"><span data-stu-id="c65c2-115">Create new AAD application with password.</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="c65c2-116">Új Azure Active Directory-alkalmazás létrehozása és a jelszóhoz kapcsolódó hitelesítő adatok társítása.</span><span class="sxs-lookup"><span data-stu-id="c65c2-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="c65c2-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c65c2-117">PARAMETERS</span></span>

### <span data-ttu-id="c65c2-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="c65c2-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="c65c2-119">Az az érték, amely azt adja meg, hogy az alkalmazás egyetlen bérlő vagy több bérlői fiók-e.</span><span class="sxs-lookup"><span data-stu-id="c65c2-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="c65c2-120">-CertValue</span></span>
<span data-ttu-id="c65c2-121">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="c65c2-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="c65c2-122">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="c65c2-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65c2-123">-DefaultProfile</span></span>
<span data-ttu-id="c65c2-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c65c2-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c65c2-125">-DisplayName</span></span>
<span data-ttu-id="c65c2-126">Az új alkalmazás megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="c65c2-126">Display name of the new application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c65c2-127">-EndDate</span></span>
<span data-ttu-id="c65c2-128">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="c65c2-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="c65c2-129">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="c65c2-129">The default end date value is one year from today.</span></span> <span data-ttu-id="c65c2-130">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="c65c2-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-131">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="c65c2-131">-HomePage</span></span>
<span data-ttu-id="c65c2-132">Az alkalmazás kezdőlapjának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="c65c2-132">The URL to the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="c65c2-133">-IdentifierUris</span></span>
<span data-ttu-id="c65c2-134">Az alkalmazást azonosító URI-k.</span><span class="sxs-lookup"><span data-stu-id="c65c2-134">The URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-135">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="c65c2-135">-KeyCredentials</span></span>
<span data-ttu-id="c65c2-136">Az alkalmazáshoz társított tanúsítvány-hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="c65c2-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-137">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="c65c2-137">-Password</span></span>
<span data-ttu-id="c65c2-138">Az alkalmazáshoz társított jelszó.</span><span class="sxs-lookup"><span data-stu-id="c65c2-138">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="c65c2-139">-PasswordCredentials</span></span>
<span data-ttu-id="c65c2-140">Az alkalmazáshoz társított jelszós hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="c65c2-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="c65c2-141">-ReplyUrls</span></span>
<span data-ttu-id="c65c2-142">Az alkalmazás válaszának URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c65c2-142">The application reply urls.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c65c2-143">-StartDate</span></span>
<span data-ttu-id="c65c2-144">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="c65c2-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="c65c2-145">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="c65c2-145">The default start date value is today.</span></span> <span data-ttu-id="c65c2-146">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c65c2-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c65c2-147">-Confirm</span></span>
<span data-ttu-id="c65c2-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c65c2-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c65c2-149">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c65c2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65c2-150">CommonParameters</span></span>
<span data-ttu-id="c65c2-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c65c2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65c2-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65c2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65c2-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c65c2-153">INPUTS</span></span>

### <span data-ttu-id="c65c2-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="c65c2-154">None</span></span>
<span data-ttu-id="c65c2-155">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c65c2-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c65c2-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c65c2-156">OUTPUTS</span></span>

### <span data-ttu-id="c65c2-157">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c65c2-157">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c65c2-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c65c2-158">NOTES</span></span>
<span data-ttu-id="c65c2-159">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="c65c2-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c65c2-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c65c2-160">RELATED LINKS</span></span>

[<span data-ttu-id="c65c2-161">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c65c2-161">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="c65c2-162">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c65c2-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="c65c2-163">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c65c2-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="c65c2-164">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c65c2-164">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="c65c2-165">Új – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c65c2-165">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="c65c2-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c65c2-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

