---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: 8eb01ccfa16b1d3610468f98117ee650376d4b6c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843154"
---
# <span data-ttu-id="66ec9-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="66ec9-101">Update-AzADApplication</span></span>

## <span data-ttu-id="66ec9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="66ec9-103">Frissít egy meglévő Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="66ec9-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="66ec9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66ec9-104">SYNTAX</span></span>

### <span data-ttu-id="66ec9-105">ApplicationObjectIdWithUpdateParamsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66ec9-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ec9-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="66ec9-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ec9-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="66ec9-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66ec9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="66ec9-108">DESCRIPTION</span></span>
<span data-ttu-id="66ec9-109">Frissít egy meglévő Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="66ec9-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="66ec9-110">Az alkalmazáshoz tartozó hitelesítő adatok frissítéséhez használja az New-AzADAppCredential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="66ec9-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="66ec9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="66ec9-111">EXAMPLES</span></span>

### <span data-ttu-id="66ec9-112">Példa 1 – egy alkalmazás megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="66ec9-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="66ec9-113">Frissíti a "fb7b3405-CA44-4b5b-8584-12392f5d96d7" azonosítójú alkalmazás megjelenítendő nevét a "MyNewDisplayName" értékkel.</span><span class="sxs-lookup"><span data-stu-id="66ec9-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="66ec9-114">Példa 2 – egy alkalmazás összes tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="66ec9-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="66ec9-115">Frissíti egy "fb7b3405-CA44-4b5b-8584-12392f5d96d7" azonosítójú alkalmazás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="66ec9-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="66ec9-116">3 példa – egy alkalmazás megjelenítendő nevének frissítése a csővezetékek segítségével</span><span class="sxs-lookup"><span data-stu-id="66ec9-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="66ec9-117">Az "fb7b3405-CA44-4b5b-8584-12392f5d96d7" azonosítójú azonosítójú alkalmazást kapja, az Update-AzADApplication parancsmagot tartalmazó csövekkel pedig a "MyNewDisplayName" névre frissítheti az alkalmazás megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="66ec9-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="66ec9-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66ec9-118">PARAMETERS</span></span>

### <span data-ttu-id="66ec9-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="66ec9-119">-ApplicationId</span></span>
<span data-ttu-id="66ec9-120">A frissítendő alkalmazás alkalmazás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="66ec9-120">The application id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="66ec9-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="66ec9-122">Igaz, ha az alkalmazást más bérlői fiókkal osztották meg; egyéb esetben false.</span><span class="sxs-lookup"><span data-stu-id="66ec9-122">True if the application is shared with other tenants; otherwise, false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ec9-123">-DefaultProfile</span></span>
<span data-ttu-id="66ec9-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66ec9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="66ec9-125">-DisplayName</span></span>
<span data-ttu-id="66ec9-126">A frissítendő alkalmazás megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="66ec9-126">The display name for the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-127">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="66ec9-127">-HomePage</span></span>
<span data-ttu-id="66ec9-128">Az alkalmazás kezdőlapjának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="66ec9-128">The URL to the application's homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="66ec9-129">-IdentifierUri</span></span>
<span data-ttu-id="66ec9-130">Az alkalmazást azonosító URI-k.</span><span class="sxs-lookup"><span data-stu-id="66ec9-130">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66ec9-131">-InputObject</span></span>
<span data-ttu-id="66ec9-132">A frissítendő alkalmazást jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="66ec9-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="66ec9-133">-ObjectId</span></span>
<span data-ttu-id="66ec9-134">A frissítendő alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="66ec9-134">The object id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="66ec9-135">-ReplyUrl</span></span>
<span data-ttu-id="66ec9-136">Itt adhatja meg, hogy a rendszer milyen URL-címeket küldjön a felhasználó tokeni számára a bejelentkezéshez, vagy az 2,0-ös engedélyezési kódok és hozzáférési tokenek OAuth átirányító URI-k.</span><span class="sxs-lookup"><span data-stu-id="66ec9-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="66ec9-137">-Confirm</span></span>
<span data-ttu-id="66ec9-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="66ec9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66ec9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ec9-139">-WhatIf</span></span>
<span data-ttu-id="66ec9-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="66ec9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ec9-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66ec9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66ec9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ec9-142">CommonParameters</span></span>
<span data-ttu-id="66ec9-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66ec9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ec9-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66ec9-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ec9-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66ec9-145">INPUTS</span></span>

### <span data-ttu-id="66ec9-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="66ec9-146">System.Guid</span></span>

### <span data-ttu-id="66ec9-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="66ec9-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="66ec9-148">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="66ec9-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="66ec9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="66ec9-149">System.String</span></span>

### <span data-ttu-id="66ec9-150">System. string []</span><span class="sxs-lookup"><span data-stu-id="66ec9-150">System.String[]</span></span>

### <span data-ttu-id="66ec9-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66ec9-151">System.Boolean</span></span>

## <span data-ttu-id="66ec9-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66ec9-152">OUTPUTS</span></span>

### <span data-ttu-id="66ec9-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="66ec9-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="66ec9-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66ec9-154">NOTES</span></span>

## <span data-ttu-id="66ec9-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66ec9-155">RELATED LINKS</span></span>
