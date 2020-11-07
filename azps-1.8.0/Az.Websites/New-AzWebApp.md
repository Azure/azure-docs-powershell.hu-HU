---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 8120b22f02d137ff261b1b4e345b917d6ae82a5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668342"
---
# <span data-ttu-id="9e450-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e450-101">New-AzWebApp</span></span>

## <span data-ttu-id="9e450-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e450-102">SYNOPSIS</span></span>
<span data-ttu-id="9e450-103">Azure webalkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9e450-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="9e450-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e450-104">SYNTAX</span></span>

### <span data-ttu-id="9e450-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e450-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e450-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="9e450-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e450-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e450-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e450-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e450-108">DESCRIPTION</span></span>
<span data-ttu-id="9e450-109">A **New-AzWebApp** parancsmag létrehoz egy Azure webalkalmazást egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="9e450-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="9e450-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9e450-110">EXAMPLES</span></span>

### <span data-ttu-id="9e450-111">Példa 1: Webalkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e450-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="9e450-112">Ez a parancs létrehoz egy ContosoSite nevű Azure webalkalmazást a meglévő erőforráscsoport alapértelmezett-web-WestUS a West US Data Center nevű adatcsoportban.</span><span class="sxs-lookup"><span data-stu-id="9e450-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="9e450-113">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="9e450-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="9e450-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e450-114">PARAMETERS</span></span>

### <span data-ttu-id="9e450-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9e450-115">-AppServicePlan</span></span>
<span data-ttu-id="9e450-116">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="9e450-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="9e450-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="9e450-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="9e450-118">Az app beállításai felülírják a HashTable</span><span class="sxs-lookup"><span data-stu-id="9e450-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="9e450-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="9e450-119">-AseName</span></span>
<span data-ttu-id="9e450-120">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="9e450-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="9e450-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e450-121">-AseResourceGroupName</span></span>
<span data-ttu-id="9e450-122">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="9e450-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="9e450-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e450-123">-AsJob</span></span>
<span data-ttu-id="9e450-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9e450-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e450-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="9e450-125">-ContainerImageName</span></span>
<span data-ttu-id="9e450-126">Tároló képnév és választható címke (például kép: címke)</span><span class="sxs-lookup"><span data-stu-id="9e450-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="9e450-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="9e450-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="9e450-128">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="9e450-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="9e450-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="9e450-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="9e450-130">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="9e450-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="9e450-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="9e450-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="9e450-132">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="9e450-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="9e450-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e450-133">-DefaultProfile</span></span>
<span data-ttu-id="9e450-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e450-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e450-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="9e450-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="9e450-136">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="9e450-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="9e450-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="9e450-137">-GitRepositoryPath</span></span>
<span data-ttu-id="9e450-138">A telepítendő webalkalmazást tartalmazó GitHub-tárház elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9e450-138">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="9e450-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="9e450-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="9e450-140">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="9e450-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="9e450-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="9e450-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="9e450-142">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="9e450-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="9e450-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="9e450-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="9e450-144">A Source WebApp Slots funkció</span><span class="sxs-lookup"><span data-stu-id="9e450-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="9e450-145">-Hely</span><span class="sxs-lookup"><span data-stu-id="9e450-145">-Location</span></span>
<span data-ttu-id="9e450-146">Helyre</span><span class="sxs-lookup"><span data-stu-id="9e450-146">Location</span></span>

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

### <span data-ttu-id="9e450-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e450-147">-Name</span></span>
<span data-ttu-id="9e450-148">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="9e450-148">WebApp Name</span></span>

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

### <span data-ttu-id="9e450-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e450-149">-ResourceGroupName</span></span>
<span data-ttu-id="9e450-150">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9e450-150">Resource Group Name</span></span>

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

### <span data-ttu-id="9e450-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="9e450-151">-SourceWebApp</span></span>
<span data-ttu-id="9e450-152">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="9e450-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="9e450-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9e450-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="9e450-154">A meglévő forgalomirányítási profil erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="9e450-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="9e450-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9e450-155">-Confirm</span></span>
<span data-ttu-id="9e450-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e450-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e450-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e450-157">-WhatIf</span></span>
<span data-ttu-id="9e450-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9e450-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e450-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e450-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e450-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e450-160">CommonParameters</span></span>
<span data-ttu-id="9e450-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e450-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e450-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e450-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e450-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e450-163">INPUTS</span></span>

### <span data-ttu-id="9e450-164">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9e450-164">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9e450-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e450-165">OUTPUTS</span></span>

### <span data-ttu-id="9e450-166">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9e450-166">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9e450-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e450-167">NOTES</span></span>

## <span data-ttu-id="9e450-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e450-168">RELATED LINKS</span></span>

[<span data-ttu-id="9e450-169">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e450-169">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="9e450-170">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e450-170">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="9e450-171">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e450-171">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="9e450-172">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e450-172">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="9e450-173">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e450-173">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


