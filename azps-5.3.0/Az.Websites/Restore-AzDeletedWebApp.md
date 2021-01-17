---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466976"
---
# <span data-ttu-id="fd43d-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="fd43d-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="fd43d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd43d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd43d-103">Törölt webalkalmazás visszaállítása új vagy meglévő webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="fd43d-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="fd43d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd43d-104">SYNTAX</span></span>

### <span data-ttu-id="fd43d-105">FromDeletedResourceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd43d-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd43d-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="fd43d-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd43d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd43d-107">DESCRIPTION</span></span>
<span data-ttu-id="fd43d-108">A **Restore-AzDeletedWebApp** parancsmag visszaállít egy törölt webappot.</span><span class="sxs-lookup"><span data-stu-id="fd43d-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="fd43d-109">A TargetResourceGroupName, a TargetName és a TargetS lesz felülírva a törölt webalkalmazás tartalmával és beállításaival.</span><span class="sxs-lookup"><span data-stu-id="fd43d-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="fd43d-110">Ha a célparaméterek nincsenek megadva, a rendszer automatikusan kitölti a törölt webalkalmazás erőforráscsoportját, nevét és tárolóhelyét.</span><span class="sxs-lookup"><span data-stu-id="fd43d-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="fd43d-111">Ha a cél webapp nem létezik, automatikusan létrejön a TargetAppServicePlanName által megadott appszolgáltatás-tervben.</span><span class="sxs-lookup"><span data-stu-id="fd43d-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="fd43d-112">A RestoreContentOnly kapcsoló paraméterrel csak a törölt app fájljai állíthatók vissza az app beállításai nélkül.</span><span class="sxs-lookup"><span data-stu-id="fd43d-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="fd43d-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd43d-113">EXAMPLES</span></span>

### <span data-ttu-id="fd43d-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="fd43d-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="fd43d-115">Visszaállít egy ContosoApp nevű törölt appot, amely a Default-Web-WestUS erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="fd43d-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="fd43d-116">A ContosoPlan nevű appszolgáltatás-tervben létrejön egy új alkalmazás, ugyanazokkal a névvel és erőforráscsoporttal, és a törölt app fájljai és beállításai visszaállítva lesznek.</span><span class="sxs-lookup"><span data-stu-id="fd43d-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="fd43d-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="fd43d-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="fd43d-118">Visszaállítja egy, a Default-Web-WestUS erőforráscsoporthoz tartozó, ContosoApp nevű törölt app átmeneti tárolóhelyét.</span><span class="sxs-lookup"><span data-stu-id="fd43d-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="fd43d-119">A Rendszer felülírja a ContosoRestore nevű webalkalmazást, amely a Default-Web-EastUS erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="fd43d-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="fd43d-120">A törölt webalkalmazás beállításai nem állíthatók vissza.</span><span class="sxs-lookup"><span data-stu-id="fd43d-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="fd43d-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="fd43d-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="fd43d-122">Ha 2 törölt app van ugyanazokkal a névvel (ContosoApp), akkor mind a webhelyek adatait meg tudjuk kapni, mind a ContosoRestore appot visszaállítjuk a választott appal, az azonosítóval való visszaállítás hívásával.</span><span class="sxs-lookup"><span data-stu-id="fd43d-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="fd43d-123">4. példa</span><span class="sxs-lookup"><span data-stu-id="fd43d-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="fd43d-124">Abban az esetben, ha 2 törölt app van ugyanazokkal a névvel (ContosoApp), akkor mind a webhelyek adatait, mind a ContosoRestore appot visszaállítjuk a választott appal az InputObject(Deletedsite) adataival való hívással.</span><span class="sxs-lookup"><span data-stu-id="fd43d-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="fd43d-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd43d-125">PARAMETERS</span></span>

### <span data-ttu-id="fd43d-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd43d-126">-AsJob</span></span>
<span data-ttu-id="fd43d-127">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fd43d-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd43d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd43d-128">-DefaultProfile</span></span>
<span data-ttu-id="fd43d-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd43d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd43d-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="fd43d-130">-DeletedId</span></span>
<span data-ttu-id="fd43d-131">A törölt Azure Web App azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd43d-131">The Id of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd43d-132">-Force</span><span class="sxs-lookup"><span data-stu-id="fd43d-132">-Force</span></span>
<span data-ttu-id="fd43d-133">A visszaállítást megerősítés kérése nélkül kell megtennie.</span><span class="sxs-lookup"><span data-stu-id="fd43d-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fd43d-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd43d-134">-InputObject</span></span>
<span data-ttu-id="fd43d-135">A törölt Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fd43d-135">The deleted Azure Web App.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd43d-136">-Location</span><span class="sxs-lookup"><span data-stu-id="fd43d-136">-Location</span></span>
<span data-ttu-id="fd43d-137">A törölt Azure Web App helye.</span><span class="sxs-lookup"><span data-stu-id="fd43d-137">The location of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd43d-138">-Name</span><span class="sxs-lookup"><span data-stu-id="fd43d-138">-Name</span></span>
<span data-ttu-id="fd43d-139">A törölt Azure Web App neve.</span><span class="sxs-lookup"><span data-stu-id="fd43d-139">The name of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd43d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd43d-140">-ResourceGroupName</span></span>
<span data-ttu-id="fd43d-141">A törölt Azure Web App erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="fd43d-141">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd43d-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="fd43d-142">-RestoreContentOnly</span></span>
<span data-ttu-id="fd43d-143">Állítsa vissza a webalkalmazás fájljait, de ne állítsa vissza a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="fd43d-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="fd43d-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="fd43d-144">-Slot</span></span>
<span data-ttu-id="fd43d-145">A törölt Azure Web App-slot.</span><span class="sxs-lookup"><span data-stu-id="fd43d-145">The deleted Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd43d-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="fd43d-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="fd43d-147">Az új Azure Web App app appszolgáltatás-csomagja.</span><span class="sxs-lookup"><span data-stu-id="fd43d-147">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd43d-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="fd43d-148">-TargetName</span></span>
<span data-ttu-id="fd43d-149">Az új Azure Web App neve.</span><span class="sxs-lookup"><span data-stu-id="fd43d-149">The name of the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd43d-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd43d-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="fd43d-151">Az új Azure Web Appot tartalmazó erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="fd43d-151">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd43d-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="fd43d-152">-TargetSlot</span></span>
<span data-ttu-id="fd43d-153">Az új Azure Web App-slot neve.</span><span class="sxs-lookup"><span data-stu-id="fd43d-153">The name of the new Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd43d-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="fd43d-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="fd43d-155">Segítségével helyreállítható egy törölt app egy offline méretarányú egységből.</span><span class="sxs-lookup"><span data-stu-id="fd43d-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="fd43d-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd43d-156">-Confirm</span></span>
<span data-ttu-id="fd43d-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fd43d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd43d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd43d-158">-WhatIf</span></span>
<span data-ttu-id="fd43d-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fd43d-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd43d-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd43d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd43d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd43d-161">CommonParameters</span></span>
<span data-ttu-id="fd43d-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd43d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd43d-163">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd43d-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd43d-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd43d-164">INPUTS</span></span>

### <span data-ttu-id="fd43d-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="fd43d-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="fd43d-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd43d-166">OUTPUTS</span></span>

### <span data-ttu-id="fd43d-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="fd43d-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fd43d-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd43d-168">NOTES</span></span>

## <span data-ttu-id="fd43d-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd43d-169">RELATED LINKS</span></span>

[<span data-ttu-id="fd43d-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="fd43d-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)