---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186592"
---
# <span data-ttu-id="9c369-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c369-101">New-AzWebApp</span></span>

## <span data-ttu-id="9c369-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c369-102">SYNOPSIS</span></span>
<span data-ttu-id="9c369-103">Azure webalkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9c369-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="9c369-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c369-104">SYNTAX</span></span>

### <span data-ttu-id="9c369-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c369-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c369-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="9c369-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c369-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c369-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c369-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c369-108">DESCRIPTION</span></span>
<span data-ttu-id="9c369-109">A **New-AzWebApp** parancsmag létrehoz egy Azure webalkalmazást egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="9c369-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="9c369-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9c369-110">EXAMPLES</span></span>

### <span data-ttu-id="9c369-111">Példa 1: Webalkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="9c369-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="9c369-112">Ez a parancs létrehoz egy ContosoSite nevű Azure webalkalmazást a meglévő erőforráscsoport alapértelmezett-web-WestUS a West US Data Center nevű adatcsoportban.</span><span class="sxs-lookup"><span data-stu-id="9c369-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="9c369-113">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="9c369-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="9c369-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c369-114">PARAMETERS</span></span>

### <span data-ttu-id="9c369-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9c369-115">-AppServicePlan</span></span>
<span data-ttu-id="9c369-116">Alkalmazás-szolgáltatási terv neve vagy alkalmazás-szolgáltatási terv azonosítója. Ha egy WebApp-és app-szolgáltatási csomag különböző erőforráscsoport, használja az azonosítót a név helyett.</span><span class="sxs-lookup"><span data-stu-id="9c369-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="9c369-117">Az alkalmazás-szolgáltatási terv azonosítóját a következő használatával lehet beolvasni: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp. id az App Service Plan azonosítóját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="9c369-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="9c369-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="9c369-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="9c369-119">Az app beállításai felülírják a HashTable</span><span class="sxs-lookup"><span data-stu-id="9c369-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="9c369-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="9c369-120">-AseName</span></span>
<span data-ttu-id="9c369-121">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="9c369-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="9c369-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c369-122">-AseResourceGroupName</span></span>
<span data-ttu-id="9c369-123">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="9c369-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="9c369-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c369-124">-AsJob</span></span>
<span data-ttu-id="9c369-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9c369-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c369-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="9c369-126">-ContainerImageName</span></span>
<span data-ttu-id="9c369-127">Tároló képnév és választható címke (például kép: címke)</span><span class="sxs-lookup"><span data-stu-id="9c369-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="9c369-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="9c369-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="9c369-129">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="9c369-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="9c369-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="9c369-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="9c369-131">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="9c369-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="9c369-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="9c369-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="9c369-133">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="9c369-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="9c369-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c369-134">-DefaultProfile</span></span>
<span data-ttu-id="9c369-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c369-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c369-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="9c369-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="9c369-137">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="9c369-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="9c369-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="9c369-138">-GitRepositoryPath</span></span>
<span data-ttu-id="9c369-139">A telepítendő webalkalmazást tartalmazó GitHub-tárház elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9c369-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="9c369-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="9c369-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="9c369-141">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="9c369-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="9c369-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="9c369-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="9c369-143">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="9c369-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="9c369-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="9c369-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="9c369-145">A Source WebApp Slots funkció</span><span class="sxs-lookup"><span data-stu-id="9c369-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="9c369-146">-Hely</span><span class="sxs-lookup"><span data-stu-id="9c369-146">-Location</span></span>
<span data-ttu-id="9c369-147">Helyre</span><span class="sxs-lookup"><span data-stu-id="9c369-147">Location</span></span>

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

### <span data-ttu-id="9c369-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9c369-148">-Name</span></span>
<span data-ttu-id="9c369-149">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="9c369-149">WebApp Name</span></span>

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

### <span data-ttu-id="9c369-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c369-150">-ResourceGroupName</span></span>
<span data-ttu-id="9c369-151">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9c369-151">Resource Group Name</span></span>

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

### <span data-ttu-id="9c369-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="9c369-152">-SourceWebApp</span></span>
<span data-ttu-id="9c369-153">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="9c369-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="9c369-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c369-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="9c369-155">A meglévő forgalomirányítási profil erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="9c369-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="9c369-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c369-156">-Confirm</span></span>
<span data-ttu-id="9c369-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c369-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c369-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c369-158">-WhatIf</span></span>
<span data-ttu-id="9c369-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c369-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c369-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c369-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c369-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c369-161">CommonParameters</span></span>
<span data-ttu-id="9c369-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c369-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c369-163">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c369-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c369-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c369-164">INPUTS</span></span>

### <span data-ttu-id="9c369-165">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9c369-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9c369-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c369-166">OUTPUTS</span></span>

### <span data-ttu-id="9c369-167">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9c369-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9c369-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c369-168">NOTES</span></span>

## <span data-ttu-id="9c369-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c369-169">RELATED LINKS</span></span>

[<span data-ttu-id="9c369-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c369-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="9c369-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c369-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="9c369-172">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c369-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="9c369-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c369-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="9c369-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c369-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

