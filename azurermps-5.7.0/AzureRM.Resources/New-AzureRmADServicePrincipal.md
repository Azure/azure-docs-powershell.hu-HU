---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: ca338fd648010b9158a6bc308bb4dcb2f1c48317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500415"
---
# <span data-ttu-id="b8967-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b8967-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="b8967-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8967-102">SYNOPSIS</span></span>
<span data-ttu-id="b8967-103">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="b8967-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8967-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8967-104">SYNTAX</span></span>

### <span data-ttu-id="b8967-105">ApplicationWithoutCredentialParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8967-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8967-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8967-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8967-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8967-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8967-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8967-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8967-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8967-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8967-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8967-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8967-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8967-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8967-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8967-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8967-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8967-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8967-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8967-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8967-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8967-115">DESCRIPTION</span></span>
<span data-ttu-id="b8967-116">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="b8967-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="b8967-117">Megjegyzés: a parancsmag emellett implicit módon létrehoz egy alkalmazást, és beállítja annak tulajdonságait (ha a ApplicationId nem található meg).</span><span class="sxs-lookup"><span data-stu-id="b8967-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="b8967-118">Az alkalmazás specifikus paramétereinek frissítéséhez használja Set-AzureRmADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b8967-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="b8967-119">Példák</span><span class="sxs-lookup"><span data-stu-id="b8967-119">EXAMPLES</span></span>

### <span data-ttu-id="b8967-120">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b8967-120">Example 1</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="b8967-121">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="b8967-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="b8967-122">DisplayName típusú ObjectId</span><span class="sxs-lookup"><span data-stu-id="b8967-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="b8967-123">DemoApp ServicePrincipal f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="b8967-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="b8967-124">2. példa</span><span class="sxs-lookup"><span data-stu-id="b8967-124">Example 2</span></span>
```
$SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp -Password $SecureStringPassword
```

<span data-ttu-id="b8967-125">Új szolgáltatásnevet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b8967-125">Creates a new service principal.</span></span>
<span data-ttu-id="b8967-126">A parancsmag szintén implicit módon hoz létre egy alkalmazást, mivel az egyik nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="b8967-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="b8967-127">DisplayName típusú ObjectId</span><span class="sxs-lookup"><span data-stu-id="b8967-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="b8967-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="b8967-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="b8967-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8967-129">PARAMETERS</span></span>

### <span data-ttu-id="b8967-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b8967-130">-ApplicationId</span></span>
<span data-ttu-id="b8967-131">Egy szolgáltató egyedi alkalmazásspecifikus azonosítója bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="b8967-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="b8967-132">Miután létrehozta ezt a tulajdonságot, nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="b8967-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="b8967-133">Ha egy alkalmazás-azonosító nincs megadva, a program létrehoz egy azonosítót.</span><span class="sxs-lookup"><span data-stu-id="b8967-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8967-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b8967-134">-CertValue</span></span>
<span data-ttu-id="b8967-135">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="b8967-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b8967-136">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="b8967-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8967-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8967-137">-DefaultProfile</span></span>
<span data-ttu-id="b8967-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b8967-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8967-139">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b8967-139">-DisplayName</span></span>
<span data-ttu-id="b8967-140">A szolgáltatás megbízójának rövid neve.</span><span class="sxs-lookup"><span data-stu-id="b8967-140">The friendly name of the service principal.</span></span>

```yaml
Type: String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8967-141">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b8967-141">-EndDate</span></span>
<span data-ttu-id="b8967-142">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="b8967-142">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b8967-143">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="b8967-143">The default end date value is one year from today.</span></span> <span data-ttu-id="b8967-144">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="b8967-144">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8967-145">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="b8967-145">-KeyCredentials</span></span>
<span data-ttu-id="b8967-146">A szolgáltatóhoz társított tanúsítvány-hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="b8967-146">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8967-147">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="b8967-147">-Password</span></span>
<span data-ttu-id="b8967-148">A szolgáltatásnevet társítani kívánt jelszó.</span><span class="sxs-lookup"><span data-stu-id="b8967-148">The password to be associated with the service principal.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8967-149">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="b8967-149">-PasswordCredentials</span></span>
<span data-ttu-id="b8967-150">A szolgáltatási megbízóhoz társított jelszós hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="b8967-150">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8967-151">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b8967-151">-StartDate</span></span>
<span data-ttu-id="b8967-152">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="b8967-152">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b8967-153">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="b8967-153">The default start date value is today.</span></span> <span data-ttu-id="b8967-154">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="b8967-154">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8967-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8967-155">-Confirm</span></span>
<span data-ttu-id="b8967-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8967-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8967-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8967-157">-WhatIf</span></span>
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

### <span data-ttu-id="b8967-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8967-158">CommonParameters</span></span>
<span data-ttu-id="b8967-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8967-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8967-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8967-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8967-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8967-161">INPUTS</span></span>

### <span data-ttu-id="b8967-162">Nincs</span><span class="sxs-lookup"><span data-stu-id="b8967-162">None</span></span>
<span data-ttu-id="b8967-163">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b8967-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8967-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8967-164">OUTPUTS</span></span>

### <span data-ttu-id="b8967-165">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b8967-165">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="b8967-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8967-166">NOTES</span></span>
<span data-ttu-id="b8967-167">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="b8967-167">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b8967-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8967-168">RELATED LINKS</span></span>

[<span data-ttu-id="b8967-169">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b8967-169">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b8967-170">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b8967-170">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b8967-171">Új – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b8967-171">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="b8967-172">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b8967-172">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="b8967-173">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b8967-173">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="b8967-174">Új – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b8967-174">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="b8967-175">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b8967-175">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

