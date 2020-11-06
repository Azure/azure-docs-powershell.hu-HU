---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 4948de891815345efdc0b3f4ec39fb1874e510b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504684"
---
# <span data-ttu-id="7290c-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7290c-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="7290c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7290c-102">SYNOPSIS</span></span>
<span data-ttu-id="7290c-103">Azure webalkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7290c-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7290c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7290c-104">SYNTAX</span></span>

### <span data-ttu-id="7290c-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7290c-105">S1 (Default)</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileId] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7290c-106">S2</span><span class="sxs-lookup"><span data-stu-id="7290c-106">S2</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileName] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7290c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7290c-107">DESCRIPTION</span></span>
<span data-ttu-id="7290c-108">A **New-AzureRmWebApp** parancsmag létrehoz egy Azure webalkalmazást egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="7290c-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="7290c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7290c-109">EXAMPLES</span></span>

### <span data-ttu-id="7290c-110">Példa 1: Webalkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="7290c-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="7290c-111">Ez a parancs létrehoz egy ContosoSite nevű Azure webalkalmazást a meglévő erőforráscsoport alapértelmezett-web-WestUS a West US Data Center nevű adatcsoportban.</span><span class="sxs-lookup"><span data-stu-id="7290c-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="7290c-112">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="7290c-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="7290c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7290c-113">PARAMETERS</span></span>

### <span data-ttu-id="7290c-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7290c-114">-AppServicePlan</span></span>
<span data-ttu-id="7290c-115">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="7290c-115">App Service Plan Name</span></span>

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

### <span data-ttu-id="7290c-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="7290c-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="7290c-117">Az app beállításai felülírják a HashTable</span><span class="sxs-lookup"><span data-stu-id="7290c-117">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="7290c-118">-AseName</span></span>
<span data-ttu-id="7290c-119">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="7290c-119">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7290c-120">-AseResourceGroupName</span></span>
<span data-ttu-id="7290c-121">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="7290c-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="7290c-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="7290c-123">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="7290c-123">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="7290c-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="7290c-125">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="7290c-125">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-126">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="7290c-126">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="7290c-127">A Source WebApp Slots funkció</span><span class="sxs-lookup"><span data-stu-id="7290c-127">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="7290c-128">-Location</span></span>
<span data-ttu-id="7290c-129">Helyre</span><span class="sxs-lookup"><span data-stu-id="7290c-129">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7290c-130">-Name</span></span>
<span data-ttu-id="7290c-131">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="7290c-131">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7290c-132">-ResourceGroupName</span></span>
<span data-ttu-id="7290c-133">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="7290c-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-134">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="7290c-134">-SourceWebApp</span></span>
<span data-ttu-id="7290c-135">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="7290c-135">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-136">-TrafficManagerProfileId</span><span class="sxs-lookup"><span data-stu-id="7290c-136">-TrafficManagerProfileId</span></span>
<span data-ttu-id="7290c-137">Forgalomirányító-profil azonosítója</span><span class="sxs-lookup"><span data-stu-id="7290c-137">Traffic Manager Profile Id</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-138">-TrafficManagerProfileName</span><span class="sxs-lookup"><span data-stu-id="7290c-138">-TrafficManagerProfileName</span></span>
<span data-ttu-id="7290c-139">A forgalomirányító profiljának neve</span><span class="sxs-lookup"><span data-stu-id="7290c-139">Traffic Manager Profile Name</span></span>

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7290c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7290c-140">-DefaultProfile</span></span>
<span data-ttu-id="7290c-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7290c-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7290c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7290c-142">CommonParameters</span></span>
<span data-ttu-id="7290c-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7290c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7290c-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7290c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7290c-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7290c-145">INPUTS</span></span>

### <span data-ttu-id="7290c-146">Webhely</span><span class="sxs-lookup"><span data-stu-id="7290c-146">Site</span></span>
<span data-ttu-id="7290c-147">A ' SourceWebApp ' paraméter a "webhely" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7290c-147">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7290c-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7290c-148">OUTPUTS</span></span>

## <span data-ttu-id="7290c-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7290c-149">NOTES</span></span>

## <span data-ttu-id="7290c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7290c-150">RELATED LINKS</span></span>

[<span data-ttu-id="7290c-151">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7290c-151">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="7290c-152">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7290c-152">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="7290c-153">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7290c-153">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="7290c-154">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7290c-154">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="7290c-155">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7290c-155">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


