---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: 4b327193a8dcbfecae8f13fa234da703d1a93cfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680494"
---
# <span data-ttu-id="b909b-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b909b-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="b909b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b909b-102">SYNOPSIS</span></span>
<span data-ttu-id="b909b-103">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="b909b-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b909b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b909b-104">SYNTAX</span></span>

### <span data-ttu-id="b909b-105">ApplicationWithoutCredentialParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b909b-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b909b-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b909b-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b909b-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b909b-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b909b-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b909b-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b909b-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b909b-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b909b-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b909b-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b909b-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b909b-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b909b-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b909b-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b909b-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b909b-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b909b-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b909b-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b909b-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="b909b-115">DESCRIPTION</span></span>
<span data-ttu-id="b909b-116">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="b909b-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="b909b-117">Megjegyzés: a parancsmag emellett implicit módon létrehoz egy alkalmazást, és beállítja annak tulajdonságait (ha a ApplicationId nem található meg).</span><span class="sxs-lookup"><span data-stu-id="b909b-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="b909b-118">Az alkalmazás specifikus paramétereinek frissítéséhez használja Set-AzureRmADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b909b-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="b909b-119">Példák</span><span class="sxs-lookup"><span data-stu-id="b909b-119">EXAMPLES</span></span>

### <span data-ttu-id="b909b-120">--------------------------Példa 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b909b-120">--------------------------  Example 1  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="b909b-121">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="b909b-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="b909b-122">DisplayName típusú ObjectId</span><span class="sxs-lookup"><span data-stu-id="b909b-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="b909b-123">DemoApp ServicePrincipal f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="b909b-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="b909b-124">--------------------------Példa 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b909b-124">--------------------------  Example 2  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp
```

<span data-ttu-id="b909b-125">Új szolgáltatásnevet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b909b-125">Creates a new service principal.</span></span>
<span data-ttu-id="b909b-126">A parancsmag szintén implicit módon hoz létre egy alkalmazást, mivel az egyik nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="b909b-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="b909b-127">DisplayName típusú ObjectId</span><span class="sxs-lookup"><span data-stu-id="b909b-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="b909b-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="b909b-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="b909b-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b909b-129">PARAMETERS</span></span>

### <span data-ttu-id="b909b-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b909b-130">-ApplicationId</span></span>
<span data-ttu-id="b909b-131">Egy szolgáltató egyedi alkalmazásspecifikus azonosítója bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="b909b-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="b909b-132">Miután létrehozta ezt a tulajdonságot, nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="b909b-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="b909b-133">Ha egy alkalmazás-azonosító nincs megadva, a program létrehoz egy azonosítót.</span><span class="sxs-lookup"><span data-stu-id="b909b-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b909b-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b909b-134">-CertValue</span></span>
<span data-ttu-id="b909b-135">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="b909b-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b909b-136">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="b909b-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b909b-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b909b-137">-DisplayName</span></span>
<span data-ttu-id="b909b-138">A szolgáltatás megbízójának rövid neve.</span><span class="sxs-lookup"><span data-stu-id="b909b-138">The friendly name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b909b-139">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b909b-139">-EndDate</span></span>
<span data-ttu-id="b909b-140">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="b909b-140">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b909b-141">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="b909b-141">The default end date value is one year from today.</span></span> <span data-ttu-id="b909b-142">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="b909b-142">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b909b-143">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="b909b-143">-KeyCredentials</span></span>
<span data-ttu-id="b909b-144">A szolgáltatóhoz társított tanúsítvány-hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="b909b-144">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b909b-145">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="b909b-145">-Password</span></span>
<span data-ttu-id="b909b-146">A szolgáltatásnevet társítani kívánt jelszó.</span><span class="sxs-lookup"><span data-stu-id="b909b-146">The password to be associated with the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b909b-147">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="b909b-147">-PasswordCredentials</span></span>
<span data-ttu-id="b909b-148">A szolgáltatási megbízóhoz társított jelszós hitelesítő adatok listája.</span><span class="sxs-lookup"><span data-stu-id="b909b-148">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b909b-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b909b-149">-StartDate</span></span>
<span data-ttu-id="b909b-150">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="b909b-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b909b-151">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="b909b-151">The default start date value is today.</span></span> <span data-ttu-id="b909b-152">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="b909b-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b909b-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b909b-153">-Confirm</span></span>
<span data-ttu-id="b909b-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b909b-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b909b-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b909b-155">-WhatIf</span></span>
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

### <span data-ttu-id="b909b-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b909b-156">-DefaultProfile</span></span>
<span data-ttu-id="b909b-157">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b909b-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b909b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b909b-158">CommonParameters</span></span>
<span data-ttu-id="b909b-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b909b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b909b-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b909b-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b909b-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b909b-161">INPUTS</span></span>

## <span data-ttu-id="b909b-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b909b-162">OUTPUTS</span></span>

### <span data-ttu-id="b909b-163">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b909b-163">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="b909b-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b909b-164">NOTES</span></span>
<span data-ttu-id="b909b-165">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="b909b-165">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b909b-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b909b-166">RELATED LINKS</span></span>

[<span data-ttu-id="b909b-167">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b909b-167">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b909b-168">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b909b-168">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b909b-169">Új – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b909b-169">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="b909b-170">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b909b-170">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="b909b-171">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b909b-171">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="b909b-172">Új – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b909b-172">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="b909b-173">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b909b-173">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

