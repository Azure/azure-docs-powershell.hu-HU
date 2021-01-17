---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: c4754ecf8cae06fd43f57bc50d3b3fbeaf1d5081
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469993"
---
# <span data-ttu-id="e190d-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e190d-101">Update-AzADApplication</span></span>

## <span data-ttu-id="e190d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e190d-102">SYNOPSIS</span></span>
<span data-ttu-id="e190d-103">Egy meglévő Azure Active Directory-alkalmazás frissítése.</span><span class="sxs-lookup"><span data-stu-id="e190d-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="e190d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e190d-104">SYNTAX</span></span>

### <span data-ttu-id="e190d-105">ApplicationObjectIdWithUpdateParamsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e190d-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e190d-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e190d-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e190d-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e190d-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e190d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e190d-108">DESCRIPTION</span></span>
<span data-ttu-id="e190d-109">Egy meglévő Azure Active Directory-alkalmazás frissítése.</span><span class="sxs-lookup"><span data-stu-id="e190d-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="e190d-110">Az alkalmazáshoz társított hitelesítő adatok frissítéséhez használja a New-AzADAppCredential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e190d-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="e190d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e190d-111">EXAMPLES</span></span>

### <span data-ttu-id="e190d-112">1. példa : Egy alkalmazás megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="e190d-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="e190d-113">Frissíti az alkalmazás megjelenítendő nevét az "fb7b3405-ca44-4b5b-8584-12392f5d96d7" azonosítóval "MyNewDisplayName" névre.</span><span class="sxs-lookup"><span data-stu-id="e190d-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="e190d-114">2. példa: Egy alkalmazás összes tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="e190d-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="e190d-115">Frissíti egy alkalmazás tulajdonságait az "fb7b3405-ca44-4b5b-8584-12392f5d96d7" objektumazonosítóval.</span><span class="sxs-lookup"><span data-stu-id="e190d-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="e190d-116">3. példa: Egy alkalmazás megjelenítendő nevének frissítése pipázással</span><span class="sxs-lookup"><span data-stu-id="e190d-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="e190d-117">Az alkalmazás az "fb7b3405-ca44-4b5b-8584-12392f5d96d7" objektumazonosítóval, valamint az Update-AzADApplication-parancsmagot a "MyNewDisplayName" névre frissítve az alkalmazás megjelenítendő nevét a "MyNewDisplayName" névre frissítve.</span><span class="sxs-lookup"><span data-stu-id="e190d-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="e190d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e190d-118">PARAMETERS</span></span>

### <span data-ttu-id="e190d-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e190d-119">-ApplicationId</span></span>
<span data-ttu-id="e190d-120">A frissíteni szükséges alkalmazás alkalmazásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="e190d-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="e190d-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="e190d-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="e190d-122">Igaz, ha az alkalmazás meg van osztva más bérlői webhelyekkel; ellenkező esetben hamis.</span><span class="sxs-lookup"><span data-stu-id="e190d-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="e190d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e190d-123">-DefaultProfile</span></span>
<span data-ttu-id="e190d-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e190d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e190d-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e190d-125">-DisplayName</span></span>
<span data-ttu-id="e190d-126">A frissítendő alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="e190d-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="e190d-127">-HomePage</span><span class="sxs-lookup"><span data-stu-id="e190d-127">-HomePage</span></span>
<span data-ttu-id="e190d-128">Az alkalmazás kezdőlapjára mutató URL-cím.</span><span class="sxs-lookup"><span data-stu-id="e190d-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="e190d-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="e190d-129">-IdentifierUri</span></span>
<span data-ttu-id="e190d-130">Az alkalmazást azonosító URI-k.</span><span class="sxs-lookup"><span data-stu-id="e190d-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="e190d-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e190d-131">-InputObject</span></span>
<span data-ttu-id="e190d-132">A frissítenie kell az alkalmazást képviselő objektumot.</span><span class="sxs-lookup"><span data-stu-id="e190d-132">The object representing the application to update.</span></span>

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

### <span data-ttu-id="e190d-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e190d-133">-ObjectId</span></span>
<span data-ttu-id="e190d-134">A frissítenie kell az alkalmazás objektumazonosítóját.</span><span class="sxs-lookup"><span data-stu-id="e190d-134">The object id of the application to update.</span></span>

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

### <span data-ttu-id="e190d-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="e190d-135">-ReplyUrl</span></span>
<span data-ttu-id="e190d-136">Megadja azokat az URL-címeket, amelyekre a rendszer a felhasználói tokeneket elküldi a bejelentkezéshez, illetve az OAuth 2.0 engedélyezési kódjait és hozzáférési jogkivonatokat átirányító URI-k.</span><span class="sxs-lookup"><span data-stu-id="e190d-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="e190d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e190d-137">-Confirm</span></span>
<span data-ttu-id="e190d-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e190d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e190d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e190d-139">-WhatIf</span></span>
<span data-ttu-id="e190d-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e190d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e190d-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e190d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e190d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e190d-142">CommonParameters</span></span>
<span data-ttu-id="e190d-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e190d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e190d-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e190d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e190d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e190d-145">INPUTS</span></span>

### <span data-ttu-id="e190d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e190d-146">System.String</span></span>

### <span data-ttu-id="e190d-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e190d-147">System.Guid</span></span>

### <span data-ttu-id="e190d-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e190d-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="e190d-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e190d-149">System.String[]</span></span>

### <span data-ttu-id="e190d-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e190d-150">System.Boolean</span></span>

## <span data-ttu-id="e190d-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e190d-151">OUTPUTS</span></span>

### <span data-ttu-id="e190d-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e190d-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e190d-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e190d-153">NOTES</span></span>

## <span data-ttu-id="e190d-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e190d-154">RELATED LINKS</span></span>
