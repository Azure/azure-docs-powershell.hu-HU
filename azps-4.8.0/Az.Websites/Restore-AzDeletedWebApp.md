---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182438"
---
# <span data-ttu-id="47472-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="47472-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="47472-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47472-102">SYNOPSIS</span></span>
<span data-ttu-id="47472-103">Törölt webalkalmazás visszaállítása új vagy meglévő webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="47472-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="47472-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47472-104">SYNTAX</span></span>

### <span data-ttu-id="47472-105">FromDeletedResourceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47472-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47472-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="47472-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47472-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="47472-107">DESCRIPTION</span></span>
<span data-ttu-id="47472-108">A **Restore-AzDeletedWebApp** parancsmag visszaállítja a törölt webalkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="47472-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="47472-109">A TargetResourceGroupName, az cél és a TargetSlot által megadott webappot felülírja a törölt webalkalmazás tartalma és beállításai.</span><span class="sxs-lookup"><span data-stu-id="47472-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="47472-110">Ha a cél paraméterei nincsenek megadva, akkor a program automatikusan kitölti őket a törölt webalkalmazás erőforráscsoport, neve és tárolóhelye között.</span><span class="sxs-lookup"><span data-stu-id="47472-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="47472-111">Ha a cél webalkalmazás nem létezik, akkor az automatikusan létrejön az TargetAppServicePlanName által megadott app Service csomagban.</span><span class="sxs-lookup"><span data-stu-id="47472-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="47472-112">A RestoreContentOnly kapcsoló paraméterrel csak a törölt alkalmazások fájljait lehet visszaállítani az app beállításai nélkül.</span><span class="sxs-lookup"><span data-stu-id="47472-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="47472-113">Példák</span><span class="sxs-lookup"><span data-stu-id="47472-113">EXAMPLES</span></span>

### <span data-ttu-id="47472-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="47472-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="47472-115">Visszaállítja a ContosoApp nevű törölt alkalmazást, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="47472-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="47472-116">Ekkor létrejön egy új, azonos nevű és erőforráscsoport nevű app a ContosoPlan nevű app Service Planben, a törölt alkalmazás fájljait és beállításait pedig visszaállítja a program.</span><span class="sxs-lookup"><span data-stu-id="47472-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="47472-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="47472-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="47472-118">Visszaállítja egy ContosoApp nevű törölt App átmeneti tárolóhelyét, amely az erőforráscsoport alapértelmezett – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="47472-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="47472-119">A ContosoRestore nevű WebApp a default (erőforráscsoport) csoporthoz tartozik – a web-EastUS felülírja.</span><span class="sxs-lookup"><span data-stu-id="47472-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="47472-120">A törölt webalkalmazás beállításai nem lesznek visszaállítva.</span><span class="sxs-lookup"><span data-stu-id="47472-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="47472-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="47472-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="47472-122">Abban az esetben, ha két törölt App azonos nevű (ContosoApp), akkor mi mindent megtudhat a webhelyekről, és a ContosoRestore nevű alkalmazást visszaállíthatja a választott alkalmazással, ha visszahívja az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="47472-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="47472-123">4. példa</span><span class="sxs-lookup"><span data-stu-id="47472-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="47472-124">Abban az esetben, ha két törölt App azonos nevű (ContosoApp), akkor mi mindent megtudhat a webhelyekről, és a ContosoRestore nevű alkalmazást visszaállíthatja a InputObject (Deletedsite) adatainak visszaállításával.</span><span class="sxs-lookup"><span data-stu-id="47472-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="47472-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47472-125">PARAMETERS</span></span>

### <span data-ttu-id="47472-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47472-126">-AsJob</span></span>
<span data-ttu-id="47472-127">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="47472-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47472-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47472-128">-DefaultProfile</span></span>
<span data-ttu-id="47472-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47472-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47472-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="47472-130">-DeletedId</span></span>
<span data-ttu-id="47472-131">A törölt Azure Web App azonosítója.</span><span class="sxs-lookup"><span data-stu-id="47472-131">The Id of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="47472-132">-Force</span><span class="sxs-lookup"><span data-stu-id="47472-132">-Force</span></span>
<span data-ttu-id="47472-133">A visszaállítást a megerősítés kérése nélkül végezze el.</span><span class="sxs-lookup"><span data-stu-id="47472-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="47472-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47472-134">-InputObject</span></span>
<span data-ttu-id="47472-135">A törölt Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="47472-135">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="47472-136">-Hely</span><span class="sxs-lookup"><span data-stu-id="47472-136">-Location</span></span>
<span data-ttu-id="47472-137">A törölt Azure Web App helye.</span><span class="sxs-lookup"><span data-stu-id="47472-137">The location of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="47472-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47472-138">-Name</span></span>
<span data-ttu-id="47472-139">A törölt Azure Web App neve.</span><span class="sxs-lookup"><span data-stu-id="47472-139">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="47472-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47472-140">-ResourceGroupName</span></span>
<span data-ttu-id="47472-141">A törölt Azure Web App erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="47472-141">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="47472-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="47472-142">-RestoreContentOnly</span></span>
<span data-ttu-id="47472-143">Állítsa vissza a webalkalmazás fájljait, de ne állítsa vissza a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="47472-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="47472-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="47472-144">-Slot</span></span>
<span data-ttu-id="47472-145">A törölt Azure Web App tárolóhelye.</span><span class="sxs-lookup"><span data-stu-id="47472-145">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="47472-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="47472-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="47472-147">Az új Azure Web App alkalmazás-szolgáltatási terve.</span><span class="sxs-lookup"><span data-stu-id="47472-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="47472-148">-Cél</span><span class="sxs-lookup"><span data-stu-id="47472-148">-TargetName</span></span>
<span data-ttu-id="47472-149">Az új Azure Web App neve.</span><span class="sxs-lookup"><span data-stu-id="47472-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="47472-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47472-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="47472-151">Az új Azure Web App erőforráscsoportot tartalmazó erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="47472-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="47472-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="47472-152">-TargetSlot</span></span>
<span data-ttu-id="47472-153">Az új Azure Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="47472-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="47472-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="47472-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="47472-155">A törölt alkalmazások visszaállítása egy olyan méretarányos egységről, amely nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="47472-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="47472-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47472-156">-Confirm</span></span>
<span data-ttu-id="47472-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47472-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47472-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47472-158">-WhatIf</span></span>
<span data-ttu-id="47472-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47472-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47472-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47472-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47472-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47472-161">CommonParameters</span></span>
<span data-ttu-id="47472-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47472-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47472-163">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47472-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47472-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47472-164">INPUTS</span></span>

### <span data-ttu-id="47472-165">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="47472-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="47472-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47472-166">OUTPUTS</span></span>

### <span data-ttu-id="47472-167">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="47472-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="47472-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47472-168">NOTES</span></span>

## <span data-ttu-id="47472-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47472-169">RELATED LINKS</span></span>

[<span data-ttu-id="47472-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="47472-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)