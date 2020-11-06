---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497144"
---
# <span data-ttu-id="3881b-101">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3881b-101">Restore-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="3881b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3881b-102">SYNOPSIS</span></span>
<span data-ttu-id="3881b-103">Törölt webalkalmazás visszaállítása új vagy meglévő webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="3881b-103">Restores a deleted web app to a new or existing web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3881b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3881b-104">SYNTAX</span></span>

### <span data-ttu-id="3881b-105">FromDeletedResourceName</span><span class="sxs-lookup"><span data-stu-id="3881b-105">FromDeletedResourceName</span></span>
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3881b-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="3881b-106">FromDeletedApp</span></span>
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## <span data-ttu-id="3881b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3881b-107">DESCRIPTION</span></span>
<span data-ttu-id="3881b-108">A **Restore-AzureRmDeletedWebApp** parancsmag visszaállítja a törölt webalkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="3881b-108">The **Restore-AzureRmDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="3881b-109">A TargetResourceGroupName, az cél és a TargetSlot által megadott webappot felülírja a törölt webalkalmazás tartalma és beállításai.</span><span class="sxs-lookup"><span data-stu-id="3881b-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="3881b-110">Ha a cél paraméterei nincsenek megadva, akkor a program automatikusan kitölti őket a törölt webalkalmazás erőforráscsoport, neve és tárolóhelye között.</span><span class="sxs-lookup"><span data-stu-id="3881b-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="3881b-111">Ha a cél webalkalmazás nem létezik, akkor az automatikusan létrejön az TargetAppServicePlanName által megadott app Service csomagban.</span><span class="sxs-lookup"><span data-stu-id="3881b-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="3881b-112">A RestoreContentOnly kapcsoló paraméterrel csak a törölt alkalmazások fájljait lehet visszaállítani az app beállításai nélkül.</span><span class="sxs-lookup"><span data-stu-id="3881b-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="3881b-113">Példák</span><span class="sxs-lookup"><span data-stu-id="3881b-113">EXAMPLES</span></span>

### <span data-ttu-id="3881b-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3881b-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="3881b-115">Visszaállítja a ContosoApp nevű törölt alkalmazást, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="3881b-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="3881b-116">Ekkor létrejön egy új, azonos nevű és erőforráscsoport nevű app a ContosoPlan nevű app Service Planben, a törölt alkalmazás fájljait és beállításait pedig visszaállítja a program.</span><span class="sxs-lookup"><span data-stu-id="3881b-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="3881b-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="3881b-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="3881b-118">Visszaállítja egy ContosoApp nevű törölt App átmeneti tárolóhelyét, amely az erőforráscsoport alapértelmezett – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="3881b-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="3881b-119">A ContosoRestore nevű WebApp a default (erőforráscsoport) csoporthoz tartozik – a web-EastUS felülírja.</span><span class="sxs-lookup"><span data-stu-id="3881b-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="3881b-120">A törölt webalkalmazás beállításai nem lesznek visszaállítva.</span><span class="sxs-lookup"><span data-stu-id="3881b-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="3881b-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3881b-121">PARAMETERS</span></span>

### <span data-ttu-id="3881b-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3881b-122">-AsJob</span></span>
<span data-ttu-id="3881b-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3881b-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3881b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3881b-124">-DefaultProfile</span></span>
<span data-ttu-id="3881b-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3881b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3881b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3881b-126">-Force</span></span>
<span data-ttu-id="3881b-127">A visszaállítást a megerősítés kérése nélkül végezze el.</span><span class="sxs-lookup"><span data-stu-id="3881b-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3881b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3881b-128">-InputObject</span></span>
<span data-ttu-id="3881b-129">A törölt Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3881b-129">The deleted Azure Web App.</span></span>

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3881b-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3881b-130">-Name</span></span>
<span data-ttu-id="3881b-131">A törölt Azure Web App neve.</span><span class="sxs-lookup"><span data-stu-id="3881b-131">The name of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3881b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3881b-132">-ResourceGroupName</span></span>
<span data-ttu-id="3881b-133">A törölt Azure Web App erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="3881b-133">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3881b-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="3881b-134">-RestoreContentOnly</span></span>
<span data-ttu-id="3881b-135">Állítsa vissza a webalkalmazás fájljait, de ne állítsa vissza a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="3881b-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="3881b-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="3881b-136">-Slot</span></span>
<span data-ttu-id="3881b-137">A törölt Azure Web App tárolóhelye.</span><span class="sxs-lookup"><span data-stu-id="3881b-137">The deleted Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3881b-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="3881b-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="3881b-139">Az új Azure Web App alkalmazás-szolgáltatási terve.</span><span class="sxs-lookup"><span data-stu-id="3881b-139">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3881b-140">-Cél</span><span class="sxs-lookup"><span data-stu-id="3881b-140">-TargetName</span></span>
<span data-ttu-id="3881b-141">Az új Azure Web App neve.</span><span class="sxs-lookup"><span data-stu-id="3881b-141">The name of the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3881b-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3881b-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="3881b-143">Az új Azure Web App erőforráscsoportot tartalmazó erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="3881b-143">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3881b-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="3881b-144">-TargetSlot</span></span>
<span data-ttu-id="3881b-145">Az új Azure Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="3881b-145">The name of the new Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3881b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3881b-146">CommonParameters</span></span>
<span data-ttu-id="3881b-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3881b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3881b-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3881b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3881b-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3881b-149">INPUTS</span></span>

### <span data-ttu-id="3881b-150">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3881b-150">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="3881b-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3881b-151">OUTPUTS</span></span>

### <span data-ttu-id="3881b-152">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3881b-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3881b-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3881b-153">NOTES</span></span>

## <span data-ttu-id="3881b-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3881b-154">RELATED LINKS</span></span>

[<span data-ttu-id="3881b-155">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3881b-155">Get-AzureRmDeletedWebApp</span></span>](./Get-AzureRmDeletedWebApp.md)
