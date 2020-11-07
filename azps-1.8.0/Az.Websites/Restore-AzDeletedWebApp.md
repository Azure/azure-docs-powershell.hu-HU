---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a90a56417ab8b1b08d72cb9d00ebe7411a6f075c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668304"
---
# <span data-ttu-id="c5edc-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c5edc-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="c5edc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5edc-102">SYNOPSIS</span></span>
<span data-ttu-id="c5edc-103">Törölt webalkalmazás visszaállítása új vagy meglévő webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="c5edc-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="c5edc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5edc-104">SYNTAX</span></span>

### <span data-ttu-id="c5edc-105">FromDeletedResourceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5edc-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5edc-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="c5edc-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5edc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5edc-107">DESCRIPTION</span></span>
<span data-ttu-id="c5edc-108">A **Restore-AzDeletedWebApp** parancsmag visszaállítja a törölt webalkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="c5edc-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="c5edc-109">A TargetResourceGroupName, az cél és a TargetSlot által megadott webappot felülírja a törölt webalkalmazás tartalma és beállításai.</span><span class="sxs-lookup"><span data-stu-id="c5edc-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="c5edc-110">Ha a cél paraméterei nincsenek megadva, akkor a program automatikusan kitölti őket a törölt webalkalmazás erőforráscsoport, neve és tárolóhelye között.</span><span class="sxs-lookup"><span data-stu-id="c5edc-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="c5edc-111">Ha a cél webalkalmazás nem létezik, akkor az automatikusan létrejön az TargetAppServicePlanName által megadott app Service csomagban.</span><span class="sxs-lookup"><span data-stu-id="c5edc-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="c5edc-112">A RestoreContentOnly kapcsoló paraméterrel csak a törölt alkalmazások fájljait lehet visszaállítani az app beállításai nélkül.</span><span class="sxs-lookup"><span data-stu-id="c5edc-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="c5edc-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c5edc-113">EXAMPLES</span></span>

### <span data-ttu-id="c5edc-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c5edc-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="c5edc-115">Visszaállítja a ContosoApp nevű törölt alkalmazást, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="c5edc-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c5edc-116">Ekkor létrejön egy új, azonos nevű és erőforráscsoport nevű app a ContosoPlan nevű app Service Planben, a törölt alkalmazás fájljait és beállításait pedig visszaállítja a program.</span><span class="sxs-lookup"><span data-stu-id="c5edc-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="c5edc-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="c5edc-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="c5edc-118">Visszaállítja egy ContosoApp nevű törölt App átmeneti tárolóhelyét, amely az erőforráscsoport alapértelmezett – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c5edc-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c5edc-119">A ContosoRestore nevű WebApp a default (erőforráscsoport) csoporthoz tartozik – a web-EastUS felülírja.</span><span class="sxs-lookup"><span data-stu-id="c5edc-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="c5edc-120">A törölt webalkalmazás beállításai nem lesznek visszaállítva.</span><span class="sxs-lookup"><span data-stu-id="c5edc-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="c5edc-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5edc-121">PARAMETERS</span></span>

### <span data-ttu-id="c5edc-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5edc-122">-AsJob</span></span>
<span data-ttu-id="c5edc-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c5edc-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5edc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5edc-124">-DefaultProfile</span></span>
<span data-ttu-id="c5edc-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5edc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5edc-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c5edc-126">-Force</span></span>
<span data-ttu-id="c5edc-127">A visszaállítást a megerősítés kérése nélkül végezze el.</span><span class="sxs-lookup"><span data-stu-id="c5edc-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c5edc-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5edc-128">-InputObject</span></span>
<span data-ttu-id="c5edc-129">A törölt Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c5edc-129">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="c5edc-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5edc-130">-Name</span></span>
<span data-ttu-id="c5edc-131">A törölt Azure Web App neve.</span><span class="sxs-lookup"><span data-stu-id="c5edc-131">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="c5edc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5edc-132">-ResourceGroupName</span></span>
<span data-ttu-id="c5edc-133">A törölt Azure Web App erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="c5edc-133">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="c5edc-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="c5edc-134">-RestoreContentOnly</span></span>
<span data-ttu-id="c5edc-135">Állítsa vissza a webalkalmazás fájljait, de ne állítsa vissza a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="c5edc-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="c5edc-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="c5edc-136">-Slot</span></span>
<span data-ttu-id="c5edc-137">A törölt Azure Web App tárolóhelye.</span><span class="sxs-lookup"><span data-stu-id="c5edc-137">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="c5edc-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="c5edc-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="c5edc-139">Az új Azure Web App alkalmazás-szolgáltatási terve.</span><span class="sxs-lookup"><span data-stu-id="c5edc-139">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="c5edc-140">-Cél</span><span class="sxs-lookup"><span data-stu-id="c5edc-140">-TargetName</span></span>
<span data-ttu-id="c5edc-141">Az új Azure Web App neve.</span><span class="sxs-lookup"><span data-stu-id="c5edc-141">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="c5edc-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5edc-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="c5edc-143">Az új Azure Web App erőforráscsoportot tartalmazó erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="c5edc-143">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="c5edc-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="c5edc-144">-TargetSlot</span></span>
<span data-ttu-id="c5edc-145">Az új Azure Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="c5edc-145">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="c5edc-146">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="c5edc-146">-UseDisasterRecovery</span></span>
<span data-ttu-id="c5edc-147">A törölt alkalmazások visszaállítása egy olyan méretarányos egységről, amely nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="c5edc-147">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="c5edc-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5edc-148">-Confirm</span></span>
<span data-ttu-id="c5edc-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5edc-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5edc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5edc-150">-WhatIf</span></span>
<span data-ttu-id="c5edc-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5edc-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5edc-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5edc-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5edc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5edc-153">CommonParameters</span></span>
<span data-ttu-id="c5edc-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5edc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5edc-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5edc-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5edc-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5edc-156">INPUTS</span></span>

### <span data-ttu-id="c5edc-157">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c5edc-157">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="c5edc-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5edc-158">OUTPUTS</span></span>

### <span data-ttu-id="c5edc-159">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c5edc-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c5edc-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5edc-160">NOTES</span></span>

## <span data-ttu-id="c5edc-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5edc-161">RELATED LINKS</span></span>

[<span data-ttu-id="c5edc-162">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c5edc-162">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)