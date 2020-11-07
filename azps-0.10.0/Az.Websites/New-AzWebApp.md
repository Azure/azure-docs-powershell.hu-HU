---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: ec5f9cf60025e6b35248b2e7f8058040b404ec42
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842754"
---
# <span data-ttu-id="681cf-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="681cf-101">New-AzWebApp</span></span>

## <span data-ttu-id="681cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="681cf-102">SYNOPSIS</span></span>
<span data-ttu-id="681cf-103">Azure webalkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="681cf-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="681cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="681cf-104">SYNTAX</span></span>

### <span data-ttu-id="681cf-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="681cf-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="681cf-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="681cf-106">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="681cf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="681cf-107">DESCRIPTION</span></span>
<span data-ttu-id="681cf-108">A **New-AzWebApp** parancsmag létrehoz egy Azure webalkalmazást egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="681cf-108">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="681cf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="681cf-109">EXAMPLES</span></span>

### <span data-ttu-id="681cf-110">Példa 1: Webalkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="681cf-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="681cf-111">Ez a parancs létrehoz egy ContosoSite nevű Azure webalkalmazást a meglévő erőforráscsoport alapértelmezett-web-WestUS a West US Data Center nevű adatcsoportban.</span><span class="sxs-lookup"><span data-stu-id="681cf-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="681cf-112">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="681cf-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="681cf-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="681cf-113">PARAMETERS</span></span>

### <span data-ttu-id="681cf-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="681cf-114">-AppServicePlan</span></span>
<span data-ttu-id="681cf-115">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="681cf-115">App Service Plan Name</span></span>

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

### <span data-ttu-id="681cf-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="681cf-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="681cf-117">Az app beállításai felülírják a HashTable</span><span class="sxs-lookup"><span data-stu-id="681cf-117">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="681cf-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="681cf-118">-AseName</span></span>
<span data-ttu-id="681cf-119">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="681cf-119">App Service Environment Name</span></span>

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

### <span data-ttu-id="681cf-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="681cf-120">-AseResourceGroupName</span></span>
<span data-ttu-id="681cf-121">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="681cf-121">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="681cf-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="681cf-122">-AsJob</span></span>
<span data-ttu-id="681cf-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="681cf-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="681cf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="681cf-124">-DefaultProfile</span></span>
<span data-ttu-id="681cf-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="681cf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681cf-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="681cf-126">-GitRepositoryPath</span></span>
<span data-ttu-id="681cf-127">A telepítéshez használt containign a GitHub-tárház elérési útja.</span><span class="sxs-lookup"><span data-stu-id="681cf-127">Path to the GitHub repository containign the web application to deploy.</span></span>

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

### <span data-ttu-id="681cf-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="681cf-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="681cf-129">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="681cf-129">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="681cf-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="681cf-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="681cf-131">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="681cf-131">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="681cf-132">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="681cf-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="681cf-133">A Source WebApp Slots funkció</span><span class="sxs-lookup"><span data-stu-id="681cf-133">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="681cf-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="681cf-134">-Location</span></span>
<span data-ttu-id="681cf-135">Helyre</span><span class="sxs-lookup"><span data-stu-id="681cf-135">Location</span></span>

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

### <span data-ttu-id="681cf-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="681cf-136">-Name</span></span>
<span data-ttu-id="681cf-137">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="681cf-137">WebApp Name</span></span>

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

### <span data-ttu-id="681cf-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="681cf-138">-ResourceGroupName</span></span>
<span data-ttu-id="681cf-139">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="681cf-139">Resource Group Name</span></span>

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

### <span data-ttu-id="681cf-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="681cf-140">-SourceWebApp</span></span>
<span data-ttu-id="681cf-141">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="681cf-141">Source WebApp Object</span></span>

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

### <span data-ttu-id="681cf-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="681cf-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="681cf-143">A meglévő forgalomirányítási profil erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="681cf-143">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="681cf-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="681cf-144">-Confirm</span></span>
<span data-ttu-id="681cf-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="681cf-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="681cf-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="681cf-146">-WhatIf</span></span>
<span data-ttu-id="681cf-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="681cf-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="681cf-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="681cf-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="681cf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="681cf-149">CommonParameters</span></span>
<span data-ttu-id="681cf-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="681cf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="681cf-151">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="681cf-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="681cf-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="681cf-152">INPUTS</span></span>

### <span data-ttu-id="681cf-153">Webhely</span><span class="sxs-lookup"><span data-stu-id="681cf-153">Site</span></span>
<span data-ttu-id="681cf-154">A ' SourceWebApp ' paraméter a "webhely" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="681cf-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="681cf-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="681cf-155">OUTPUTS</span></span>

### <span data-ttu-id="681cf-156">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="681cf-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="681cf-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="681cf-157">NOTES</span></span>

## <span data-ttu-id="681cf-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="681cf-158">RELATED LINKS</span></span>

[<span data-ttu-id="681cf-159">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="681cf-159">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="681cf-160">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="681cf-160">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="681cf-161">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="681cf-161">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="681cf-162">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="681cf-162">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="681cf-163">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="681cf-163">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


