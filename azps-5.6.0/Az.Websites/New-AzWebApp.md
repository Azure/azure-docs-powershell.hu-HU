---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: e09c2660f37a7b737d137c0907ff74ef9e39a5ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928794"
---
# <span data-ttu-id="985ac-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="985ac-101">New-AzWebApp</span></span>

## <span data-ttu-id="985ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="985ac-102">SYNOPSIS</span></span>
<span data-ttu-id="985ac-103">Létrehoz egy Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="985ac-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="985ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="985ac-104">SYNTAX</span></span>

### <span data-ttu-id="985ac-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="985ac-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="985ac-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="985ac-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="985ac-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="985ac-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="985ac-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="985ac-108">DESCRIPTION</span></span>
<span data-ttu-id="985ac-109">A **New-AzWebApp** parancsmag létrehoz egy Azure Web Appot egy adott erőforráscsoportban, amely a megadott App Service-tervet és -adatközpontot használja.</span><span class="sxs-lookup"><span data-stu-id="985ac-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="985ac-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="985ac-110">EXAMPLES</span></span>

### <span data-ttu-id="985ac-111">1. példa: Webalkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="985ac-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="985ac-112">Ez a parancs létrehoz egy ContosoSite nevű Azure Web Appot a Default-Web-WestUS nevű meglévő erőforráscsoportban az usa-i adatközpontban.</span><span class="sxs-lookup"><span data-stu-id="985ac-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="985ac-113">A parancs egy ContosoServicePlan nevű meglévő appszolgáltatás-tervet használ.</span><span class="sxs-lookup"><span data-stu-id="985ac-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="985ac-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="985ac-114">PARAMETERS</span></span>

### <span data-ttu-id="985ac-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="985ac-115">-AppServicePlan</span></span>
<span data-ttu-id="985ac-116">App Service Plan Name or App Service Plan Id. Ha egy WebApp- és appszolgáltatás-csomag különböző erőforráscsoportokban található, a név helyett használja az azonosítót.</span><span class="sxs-lookup"><span data-stu-id="985ac-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="985ac-117">Az appszolgáltatás-azonosító a következő használatával szerezhető be: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id adja vissza az appszolgáltatás-terv azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="985ac-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="985ac-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="985ac-119">App Settings Overrides HashTable</span><span class="sxs-lookup"><span data-stu-id="985ac-119">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="985ac-120">-AseName</span></span>
<span data-ttu-id="985ac-121">Appszolgáltatás-környezet neve</span><span class="sxs-lookup"><span data-stu-id="985ac-121">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="985ac-122">-AseResourceGroupName</span></span>
<span data-ttu-id="985ac-123">App Service Environment Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="985ac-123">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="985ac-124">-AsJob</span></span>
<span data-ttu-id="985ac-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="985ac-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="985ac-126">-ContainerImageName</span></span>
<span data-ttu-id="985ac-127">Container Image Name and optional tag, például (image:tag)</span><span class="sxs-lookup"><span data-stu-id="985ac-127">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="985ac-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="985ac-129">Private Container Registry Password</span><span class="sxs-lookup"><span data-stu-id="985ac-129">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="985ac-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="985ac-131">Private Container Registry Server Url</span><span class="sxs-lookup"><span data-stu-id="985ac-131">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="985ac-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="985ac-133">Private Container Registry Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="985ac-133">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="985ac-134">-DefaultProfile</span></span>
<span data-ttu-id="985ac-135">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="985ac-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="985ac-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="985ac-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="985ac-137">Engedélyezi/letiltja a tároló folyamatos üzembe helyezését webhook</span><span class="sxs-lookup"><span data-stu-id="985ac-137">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="985ac-138">-GitRepositoryPath</span></span>
<span data-ttu-id="985ac-139">A központi telepítéshez szükséges webalkalmazást tartalmazó GitHub-tárház elérési útja.</span><span class="sxs-lookup"><span data-stu-id="985ac-139">Path to the GitHub repository containing the web application to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="985ac-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="985ac-141">Az Egyéni állomásnevek figyelmen kívül hagyása beállítás</span><span class="sxs-lookup"><span data-stu-id="985ac-141">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="985ac-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="985ac-143">A Forrásvezérlő mellőzása beállítás</span><span class="sxs-lookup"><span data-stu-id="985ac-143">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-144">-IncludeSourceWebAppSzajs</span><span class="sxs-lookup"><span data-stu-id="985ac-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="985ac-145">Include Source WebApp Slots Option</span><span class="sxs-lookup"><span data-stu-id="985ac-145">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-146">-Location</span><span class="sxs-lookup"><span data-stu-id="985ac-146">-Location</span></span>
<span data-ttu-id="985ac-147">Hely</span><span class="sxs-lookup"><span data-stu-id="985ac-147">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-148">-Name</span><span class="sxs-lookup"><span data-stu-id="985ac-148">-Name</span></span>
<span data-ttu-id="985ac-149">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="985ac-149">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="985ac-150">-ResourceGroupName</span></span>
<span data-ttu-id="985ac-151">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="985ac-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry, WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="985ac-152">-SourceWebApp</span></span>
<span data-ttu-id="985ac-153">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="985ac-153">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="985ac-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="985ac-155">A meglévő forgalomkezelői profil erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="985ac-155">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985ac-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="985ac-156">-Confirm</span></span>
<span data-ttu-id="985ac-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="985ac-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="985ac-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="985ac-158">-WhatIf</span></span>
<span data-ttu-id="985ac-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="985ac-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="985ac-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="985ac-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="985ac-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985ac-161">CommonParameters</span></span>
<span data-ttu-id="985ac-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="985ac-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985ac-163">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="985ac-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985ac-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="985ac-164">INPUTS</span></span>

### <span data-ttu-id="985ac-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="985ac-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="985ac-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="985ac-166">OUTPUTS</span></span>

### <span data-ttu-id="985ac-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="985ac-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="985ac-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="985ac-168">NOTES</span></span>

## <span data-ttu-id="985ac-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="985ac-169">RELATED LINKS</span></span>

[<span data-ttu-id="985ac-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="985ac-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="985ac-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="985ac-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="985ac-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="985ac-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="985ac-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="985ac-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="985ac-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="985ac-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


