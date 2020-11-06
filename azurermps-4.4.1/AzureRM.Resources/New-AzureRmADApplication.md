---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: c43bba247268d7ffcdbc2c33d7198415738c5694
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504763"
---
# <span data-ttu-id="345be-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="345be-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="345be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="345be-102">SYNOPSIS</span></span>
<span data-ttu-id="345be-103">Új Azure Active Directory-alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="345be-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="345be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="345be-104">SYNTAX</span></span>

### <span data-ttu-id="345be-105">ApplicationWithoutCredentialParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="345be-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="345be-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="345be-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="345be-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="345be-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="345be-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="345be-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="345be-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="345be-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="345be-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="345be-110">DESCRIPTION</span></span>
<span data-ttu-id="345be-111">Új Azure Active Directory-alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="345be-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="345be-112">Példák</span><span class="sxs-lookup"><span data-stu-id="345be-112">EXAMPLES</span></span>

### <span data-ttu-id="345be-113">--------------------------Hozzon létre új AAD-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="345be-113">--------------------------  Create new AAD application.</span></span>  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="345be-114">Új Azure Active Directory-alkalmazást hoz létre hitelesítő adatok nélkül.</span><span class="sxs-lookup"><span data-stu-id="345be-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="345be-115">--------------------------Új AAD-alkalmazás létrehozása jelszóval.</span><span class="sxs-lookup"><span data-stu-id="345be-115">--------------------------  Create new AAD application with password.</span></span>  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password "password"
```

<span data-ttu-id="345be-116">Új Azure Active Directory-alkalmazás létrehozása és a jelszóhoz kapcsolódó hitelesítő adatok társítása.</span><span class="sxs-lookup"><span data-stu-id="345be-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="345be-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="345be-117">PARAMETERS</span></span>

### <span data-ttu-id="345be-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="345be-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="345be-119">Az az érték, amely azt adja meg, hogy az alkalmazás egyetlen bérlő vagy több bérlői fiók-e.</span><span class="sxs-lookup"><span data-stu-id="345be-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="345be-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="345be-120">-CertValue</span></span>
<span data-ttu-id="345be-121">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="345be-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="345be-122">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="345be-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="345be-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="345be-123">-DisplayName</span></span>
<span data-ttu-id="345be-124">Az új alkalmazás megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="345be-124">Display name of the new application.</span></span>

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

### <span data-ttu-id="345be-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="345be-125">-EndDate</span></span>
<span data-ttu-id="345be-126">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="345be-126">The effective end date of the credential usage.</span></span>
<span data-ttu-id="345be-127">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="345be-127">The default end date value is one year from today.</span></span> <span data-ttu-id="345be-128">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="345be-128">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="345be-129">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="345be-129">-HomePage</span></span>
<span data-ttu-id="345be-130">Az alkalmazás kezdőlapjának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="345be-130">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="345be-131">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="345be-131">-IdentifierUris</span></span>
<span data-ttu-id="345be-132">Az alkalmazást azonosító URI-k.</span><span class="sxs-lookup"><span data-stu-id="345be-132">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="345be-133">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="345be-133">-KeyCredentials</span></span>
<span data-ttu-id="345be-134">Az alkalmazáshoz társított tanúsítvány-hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="345be-134">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="345be-135">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="345be-135">-Password</span></span>
<span data-ttu-id="345be-136">Az alkalmazáshoz társított jelszó.</span><span class="sxs-lookup"><span data-stu-id="345be-136">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="345be-137">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="345be-137">-PasswordCredentials</span></span>
<span data-ttu-id="345be-138">Az alkalmazáshoz társított jelszós hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="345be-138">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="345be-139">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="345be-139">-ReplyUrls</span></span>
<span data-ttu-id="345be-140">Az alkalmazás válaszának URL-címei.</span><span class="sxs-lookup"><span data-stu-id="345be-140">The application reply urls.</span></span>

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

### <span data-ttu-id="345be-141">-StartDate</span><span class="sxs-lookup"><span data-stu-id="345be-141">-StartDate</span></span>
<span data-ttu-id="345be-142">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="345be-142">The effective start date of the credential usage.</span></span>
<span data-ttu-id="345be-143">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="345be-143">The default start date value is today.</span></span> <span data-ttu-id="345be-144">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="345be-144">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="345be-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="345be-145">-Confirm</span></span>
<span data-ttu-id="345be-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="345be-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="345be-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="345be-147">-WhatIf</span></span>
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

### <span data-ttu-id="345be-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="345be-148">-DefaultProfile</span></span>
<span data-ttu-id="345be-149">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="345be-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345be-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="345be-150">CommonParameters</span></span>
<span data-ttu-id="345be-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="345be-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="345be-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="345be-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="345be-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="345be-153">INPUTS</span></span>

## <span data-ttu-id="345be-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="345be-154">OUTPUTS</span></span>

### <span data-ttu-id="345be-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="345be-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="345be-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="345be-156">NOTES</span></span>
<span data-ttu-id="345be-157">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="345be-157">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="345be-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="345be-158">RELATED LINKS</span></span>

[<span data-ttu-id="345be-159">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="345be-159">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="345be-160">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="345be-160">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="345be-161">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="345be-161">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="345be-162">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="345be-162">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="345be-163">Új – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="345be-163">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="345be-164">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="345be-164">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

