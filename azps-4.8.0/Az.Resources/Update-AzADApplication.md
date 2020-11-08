---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: c4754ecf8cae06fd43f57bc50d3b3fbeaf1d5081
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184002"
---
# <span data-ttu-id="d7f9f-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d7f9f-101">Update-AzADApplication</span></span>

## <span data-ttu-id="d7f9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f9f-103">Frissít egy meglévő Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="d7f9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7f9f-104">SYNTAX</span></span>

### <span data-ttu-id="d7f9f-105">ApplicationObjectIdWithUpdateParamsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7f9f-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7f9f-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7f9f-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7f9f-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7f9f-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7f9f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7f9f-108">DESCRIPTION</span></span>
<span data-ttu-id="d7f9f-109">Frissít egy meglévő Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="d7f9f-110">Az alkalmazáshoz tartozó hitelesítő adatok frissítéséhez használja az New-AzADAppCredential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="d7f9f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d7f9f-111">EXAMPLES</span></span>

### <span data-ttu-id="d7f9f-112">Példa 1 – egy alkalmazás megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="d7f9f-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="d7f9f-113">Frissíti a "fb7b3405-CA44-4b5b-8584-12392f5d96d7" azonosítójú alkalmazás megjelenítendő nevét a "MyNewDisplayName" értékkel.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="d7f9f-114">Példa 2 – egy alkalmazás összes tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="d7f9f-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="d7f9f-115">Frissíti egy "fb7b3405-CA44-4b5b-8584-12392f5d96d7" azonosítójú alkalmazás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="d7f9f-116">3 példa – egy alkalmazás megjelenítendő nevének frissítése a csővezetékek segítségével</span><span class="sxs-lookup"><span data-stu-id="d7f9f-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="d7f9f-117">Az "fb7b3405-CA44-4b5b-8584-12392f5d96d7" azonosítójú azonosítójú alkalmazást kapja, az Update-AzADApplication parancsmagot tartalmazó csövekkel pedig a "MyNewDisplayName" névre frissítheti az alkalmazás megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="d7f9f-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7f9f-118">PARAMETERS</span></span>

### <span data-ttu-id="d7f9f-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d7f9f-119">-ApplicationId</span></span>
<span data-ttu-id="d7f9f-120">A frissítendő alkalmazás alkalmazás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="d7f9f-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="d7f9f-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="d7f9f-122">Igaz, ha az alkalmazást más bérlői fiókkal osztották meg; egyéb esetben false.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="d7f9f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f9f-123">-DefaultProfile</span></span>
<span data-ttu-id="d7f9f-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7f9f-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d7f9f-125">-DisplayName</span></span>
<span data-ttu-id="d7f9f-126">A frissítendő alkalmazás megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="d7f9f-127">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="d7f9f-127">-HomePage</span></span>
<span data-ttu-id="d7f9f-128">Az alkalmazás kezdőlapjának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="d7f9f-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="d7f9f-129">-IdentifierUri</span></span>
<span data-ttu-id="d7f9f-130">Az alkalmazást azonosító URI-k.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="d7f9f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7f9f-131">-InputObject</span></span>
<span data-ttu-id="d7f9f-132">A frissítendő alkalmazást jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f9f-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d7f9f-133">-ObjectId</span></span>
<span data-ttu-id="d7f9f-134">A frissítendő alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-134">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f9f-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="d7f9f-135">-ReplyUrl</span></span>
<span data-ttu-id="d7f9f-136">Itt adhatja meg, hogy a rendszer milyen URL-címeket küldjön a felhasználó tokeni számára a bejelentkezéshez, vagy az 2,0-ös engedélyezési kódok és hozzáférési tokenek OAuth átirányító URI-k.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="d7f9f-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7f9f-137">-Confirm</span></span>
<span data-ttu-id="d7f9f-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7f9f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7f9f-139">-WhatIf</span></span>
<span data-ttu-id="d7f9f-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7f9f-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7f9f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f9f-142">CommonParameters</span></span>
<span data-ttu-id="d7f9f-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7f9f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f9f-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d7f9f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f9f-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7f9f-145">INPUTS</span></span>

### <span data-ttu-id="d7f9f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d7f9f-146">System.String</span></span>

### <span data-ttu-id="d7f9f-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d7f9f-147">System.Guid</span></span>

### <span data-ttu-id="d7f9f-148">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d7f9f-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="d7f9f-149">System. string []</span><span class="sxs-lookup"><span data-stu-id="d7f9f-149">System.String[]</span></span>

### <span data-ttu-id="d7f9f-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7f9f-150">System.Boolean</span></span>

## <span data-ttu-id="d7f9f-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7f9f-151">OUTPUTS</span></span>

### <span data-ttu-id="d7f9f-152">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d7f9f-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d7f9f-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7f9f-153">NOTES</span></span>

## <span data-ttu-id="d7f9f-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7f9f-154">RELATED LINKS</span></span>
