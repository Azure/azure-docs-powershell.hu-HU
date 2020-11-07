---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 9d544d48a430aa671c0c18721e6dece6f1351424
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839901"
---
# <span data-ttu-id="28e73-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28e73-101">New-AzWebApp</span></span>

## <span data-ttu-id="28e73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28e73-102">SYNOPSIS</span></span>
<span data-ttu-id="28e73-103">Azure webalkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="28e73-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="28e73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28e73-104">SYNTAX</span></span>

### <span data-ttu-id="28e73-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28e73-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28e73-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="28e73-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28e73-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="28e73-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28e73-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="28e73-108">DESCRIPTION</span></span>
<span data-ttu-id="28e73-109">A **New-AzWebApp** parancsmag létrehoz egy Azure webalkalmazást egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="28e73-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="28e73-110">Példák</span><span class="sxs-lookup"><span data-stu-id="28e73-110">EXAMPLES</span></span>

### <span data-ttu-id="28e73-111">Példa 1: Webalkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="28e73-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="28e73-112">Ez a parancs létrehoz egy ContosoSite nevű Azure webalkalmazást a meglévő erőforráscsoport alapértelmezett-web-WestUS a West US Data Center nevű adatcsoportban.</span><span class="sxs-lookup"><span data-stu-id="28e73-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="28e73-113">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="28e73-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="28e73-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28e73-114">PARAMETERS</span></span>

### <span data-ttu-id="28e73-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="28e73-115">-AppServicePlan</span></span>
<span data-ttu-id="28e73-116">Alkalmazás-szolgáltatási terv neve vagy alkalmazás-szolgáltatási terv azonosítója. Ha egy WebApp-és app-szolgáltatási csomag különböző erőforráscsoport, használja az azonosítót a név helyett.</span><span class="sxs-lookup"><span data-stu-id="28e73-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="28e73-117">Az alkalmazás-szolgáltatási terv azonosítóját a következő használatával lehet beolvasni: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp. id az App Service Plan azonosítóját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="28e73-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="28e73-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="28e73-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="28e73-119">Az app beállításai felülírják a HashTable</span><span class="sxs-lookup"><span data-stu-id="28e73-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="28e73-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="28e73-120">-AseName</span></span>
<span data-ttu-id="28e73-121">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="28e73-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="28e73-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28e73-122">-AseResourceGroupName</span></span>
<span data-ttu-id="28e73-123">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="28e73-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="28e73-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28e73-124">-AsJob</span></span>
<span data-ttu-id="28e73-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="28e73-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28e73-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="28e73-126">-ContainerImageName</span></span>
<span data-ttu-id="28e73-127">Tároló képnév és választható címke (például kép: címke)</span><span class="sxs-lookup"><span data-stu-id="28e73-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="28e73-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="28e73-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="28e73-129">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="28e73-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="28e73-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="28e73-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="28e73-131">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="28e73-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="28e73-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="28e73-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="28e73-133">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="28e73-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="28e73-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e73-134">-DefaultProfile</span></span>
<span data-ttu-id="28e73-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28e73-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28e73-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="28e73-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="28e73-137">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="28e73-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="28e73-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="28e73-138">-GitRepositoryPath</span></span>
<span data-ttu-id="28e73-139">A telepítendő webalkalmazást tartalmazó GitHub-tárház elérési útja.</span><span class="sxs-lookup"><span data-stu-id="28e73-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="28e73-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="28e73-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="28e73-141">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="28e73-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="28e73-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="28e73-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="28e73-143">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="28e73-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="28e73-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="28e73-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="28e73-145">A Source WebApp Slots funkció</span><span class="sxs-lookup"><span data-stu-id="28e73-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="28e73-146">-Hely</span><span class="sxs-lookup"><span data-stu-id="28e73-146">-Location</span></span>
<span data-ttu-id="28e73-147">Helyre</span><span class="sxs-lookup"><span data-stu-id="28e73-147">Location</span></span>

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

### <span data-ttu-id="28e73-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28e73-148">-Name</span></span>
<span data-ttu-id="28e73-149">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="28e73-149">WebApp Name</span></span>

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

### <span data-ttu-id="28e73-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28e73-150">-ResourceGroupName</span></span>
<span data-ttu-id="28e73-151">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="28e73-151">Resource Group Name</span></span>

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

### <span data-ttu-id="28e73-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="28e73-152">-SourceWebApp</span></span>
<span data-ttu-id="28e73-153">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="28e73-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="28e73-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="28e73-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="28e73-155">A meglévő forgalomirányítási profil erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="28e73-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="28e73-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28e73-156">-Confirm</span></span>
<span data-ttu-id="28e73-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28e73-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28e73-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28e73-158">-WhatIf</span></span>
<span data-ttu-id="28e73-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="28e73-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28e73-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28e73-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28e73-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e73-161">CommonParameters</span></span>
<span data-ttu-id="28e73-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28e73-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e73-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28e73-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e73-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28e73-164">INPUTS</span></span>

### <span data-ttu-id="28e73-165">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="28e73-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="28e73-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28e73-166">OUTPUTS</span></span>

### <span data-ttu-id="28e73-167">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="28e73-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="28e73-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28e73-168">NOTES</span></span>

## <span data-ttu-id="28e73-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28e73-169">RELATED LINKS</span></span>

[<span data-ttu-id="28e73-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28e73-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="28e73-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28e73-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="28e73-172">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28e73-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="28e73-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28e73-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="28e73-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28e73-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


