---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 2dfa72867655b95ea752c23c8605f19e7544e8e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491820"
---
# <span data-ttu-id="c395f-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c395f-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="c395f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c395f-102">SYNOPSIS</span></span>
<span data-ttu-id="c395f-103">Azure webalkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c395f-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c395f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c395f-104">SYNTAX</span></span>

### <span data-ttu-id="c395f-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c395f-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c395f-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="c395f-106">PrivateRegistry</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] -ContainerImageName <String> -ContainerRegistryUrl <String>
 -ContainerRegistryUser <String> -ContainerRegistryPassword <SecureString>
 [-EnableContainerContinuousDeployment] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c395f-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="c395f-107">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>]
 [-EnableContainerContinuousDeployment] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-IncludeSourceWebAppSlots] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c395f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c395f-108">DESCRIPTION</span></span>
<span data-ttu-id="c395f-109">A **New-AzureRmWebApp** parancsmag létrehoz egy Azure webalkalmazást egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="c395f-109">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="c395f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c395f-110">EXAMPLES</span></span>

### <span data-ttu-id="c395f-111">Példa 1: Webalkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="c395f-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="c395f-112">Ez a parancs létrehoz egy ContosoSite nevű Azure webalkalmazást a meglévő erőforráscsoport alapértelmezett-web-WestUS a West US Data Center nevű adatcsoportban.</span><span class="sxs-lookup"><span data-stu-id="c395f-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="c395f-113">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="c395f-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="c395f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c395f-114">PARAMETERS</span></span>

### <span data-ttu-id="c395f-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c395f-115">-AppServicePlan</span></span>
<span data-ttu-id="c395f-116">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="c395f-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="c395f-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="c395f-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="c395f-118">Az app beállításai felülírják a HashTable</span><span class="sxs-lookup"><span data-stu-id="c395f-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="c395f-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="c395f-119">-AseName</span></span>
<span data-ttu-id="c395f-120">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="c395f-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="c395f-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c395f-121">-AseResourceGroupName</span></span>
<span data-ttu-id="c395f-122">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="c395f-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="c395f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c395f-123">-AsJob</span></span>
<span data-ttu-id="c395f-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c395f-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c395f-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c395f-125">-ContainerImageName</span></span>
<span data-ttu-id="c395f-126">Tároló képnév és választható címke (például kép: címke)</span><span class="sxs-lookup"><span data-stu-id="c395f-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="c395f-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c395f-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c395f-128">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="c395f-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="c395f-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c395f-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c395f-130">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="c395f-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="c395f-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c395f-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="c395f-132">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="c395f-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="c395f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c395f-133">-DefaultProfile</span></span>
<span data-ttu-id="c395f-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c395f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c395f-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c395f-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c395f-136">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="c395f-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="c395f-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="c395f-137">-GitRepositoryPath</span></span>
<span data-ttu-id="c395f-138">A telepítéshez használt containign a GitHub-tárház elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c395f-138">Path to the GitHub repository containign the web application to deploy.</span></span>

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

### <span data-ttu-id="c395f-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="c395f-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="c395f-140">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="c395f-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="c395f-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="c395f-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="c395f-142">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="c395f-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="c395f-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="c395f-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="c395f-144">A Source WebApp Slots funkció</span><span class="sxs-lookup"><span data-stu-id="c395f-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="c395f-145">-Hely</span><span class="sxs-lookup"><span data-stu-id="c395f-145">-Location</span></span>
<span data-ttu-id="c395f-146">Helyre</span><span class="sxs-lookup"><span data-stu-id="c395f-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c395f-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c395f-147">-Name</span></span>
<span data-ttu-id="c395f-148">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c395f-148">WebApp Name</span></span>

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

### <span data-ttu-id="c395f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c395f-149">-ResourceGroupName</span></span>
<span data-ttu-id="c395f-150">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c395f-150">Resource Group Name</span></span>

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

### <span data-ttu-id="c395f-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="c395f-151">-SourceWebApp</span></span>
<span data-ttu-id="c395f-152">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="c395f-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="c395f-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c395f-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="c395f-154">A meglévő forgalomirányítási profil erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c395f-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="c395f-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c395f-155">-Confirm</span></span>
<span data-ttu-id="c395f-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c395f-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c395f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c395f-157">-WhatIf</span></span>
<span data-ttu-id="c395f-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c395f-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c395f-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c395f-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c395f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c395f-160">CommonParameters</span></span>
<span data-ttu-id="c395f-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c395f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c395f-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c395f-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c395f-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c395f-163">INPUTS</span></span>

### <span data-ttu-id="c395f-164">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="c395f-164">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c395f-165">Paraméterek: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c395f-165">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="c395f-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c395f-166">OUTPUTS</span></span>

### <span data-ttu-id="c395f-167">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="c395f-167">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="c395f-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c395f-168">NOTES</span></span>

## <span data-ttu-id="c395f-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c395f-169">RELATED LINKS</span></span>

[<span data-ttu-id="c395f-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c395f-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="c395f-171">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c395f-171">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="c395f-172">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c395f-172">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="c395f-173">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c395f-173">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="c395f-174">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c395f-174">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


