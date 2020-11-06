---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 05ee02fcb1a1f03c2a9b349754009a178a1668b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500335"
---
# <span data-ttu-id="f6fc3-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f6fc3-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="f6fc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f6fc3-103">Azure webalkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6fc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6fc3-104">SYNTAX</span></span>

### <span data-ttu-id="f6fc3-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6fc3-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6fc3-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6fc3-106">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6fc3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6fc3-107">DESCRIPTION</span></span>
<span data-ttu-id="f6fc3-108">A **New-AzureRmWebApp** parancsmag létrehoz egy Azure webalkalmazást egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="f6fc3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f6fc3-109">EXAMPLES</span></span>

### <span data-ttu-id="f6fc3-110">Példa 1: Webalkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="f6fc3-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="f6fc3-111">Ez a parancs létrehoz egy ContosoSite nevű Azure webalkalmazást a meglévő erőforráscsoport alapértelmezett-web-WestUS a West US Data Center nevű adatcsoportban.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="f6fc3-112">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="f6fc3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6fc3-113">PARAMETERS</span></span>

### <span data-ttu-id="f6fc3-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f6fc3-114">-AppServicePlan</span></span>
<span data-ttu-id="f6fc3-115">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="f6fc3-115">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="f6fc3-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="f6fc3-117">Az app beállításai felülírják a HashTable</span><span class="sxs-lookup"><span data-stu-id="f6fc3-117">App Settings Overrides HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="f6fc3-118">-AseName</span></span>
<span data-ttu-id="f6fc3-119">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="f6fc3-119">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6fc3-120">-AseResourceGroupName</span></span>
<span data-ttu-id="f6fc3-121">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="f6fc3-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6fc3-122">-AsJob</span></span>
<span data-ttu-id="f6fc3-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f6fc3-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6fc3-124">-DefaultProfile</span></span>
<span data-ttu-id="f6fc3-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6fc3-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="f6fc3-126">-GitRepositoryPath</span></span>
<span data-ttu-id="f6fc3-127">A telepítéshez használt containign a GitHub-tárház elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-127">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="f6fc3-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="f6fc3-129">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="f6fc3-129">Ignore Custom Host Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="f6fc3-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="f6fc3-131">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="f6fc3-131">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-132">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="f6fc3-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="f6fc3-133">A Source WebApp Slots funkció</span><span class="sxs-lookup"><span data-stu-id="f6fc3-133">Include Source WebApp Slots Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="f6fc3-134">-Location</span></span>
<span data-ttu-id="f6fc3-135">Helyre</span><span class="sxs-lookup"><span data-stu-id="f6fc3-135">Location</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6fc3-136">-Name</span></span>
<span data-ttu-id="f6fc3-137">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f6fc3-137">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6fc3-138">-ResourceGroupName</span></span>
<span data-ttu-id="f6fc3-139">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f6fc3-139">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="f6fc3-140">-SourceWebApp</span></span>
<span data-ttu-id="f6fc3-141">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="f6fc3-141">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6fc3-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="f6fc3-143">A meglévő forgalomirányítási profil erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f6fc3-143">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc3-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6fc3-144">-Confirm</span></span>
<span data-ttu-id="f6fc3-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6fc3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6fc3-146">-WhatIf</span></span>
<span data-ttu-id="f6fc3-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6fc3-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6fc3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fc3-149">CommonParameters</span></span>
<span data-ttu-id="f6fc3-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6fc3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fc3-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6fc3-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fc3-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6fc3-152">INPUTS</span></span>

### <span data-ttu-id="f6fc3-153">Webhely</span><span class="sxs-lookup"><span data-stu-id="f6fc3-153">Site</span></span>
<span data-ttu-id="f6fc3-154">A ' SourceWebApp ' paraméter a "webhely" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f6fc3-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f6fc3-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6fc3-155">OUTPUTS</span></span>

### <span data-ttu-id="f6fc3-156">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="f6fc3-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="f6fc3-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6fc3-157">NOTES</span></span>

## <span data-ttu-id="f6fc3-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6fc3-158">RELATED LINKS</span></span>

[<span data-ttu-id="f6fc3-159">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f6fc3-159">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f6fc3-160">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f6fc3-160">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="f6fc3-161">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f6fc3-161">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="f6fc3-162">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f6fc3-162">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="f6fc3-163">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f6fc3-163">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


