---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 2163c18fecadba069b7c3fba260ab81538ed5583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497143"
---
# <span data-ttu-id="91a33-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="91a33-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="91a33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91a33-102">SYNOPSIS</span></span>
<span data-ttu-id="91a33-103">Azure-alkalmazási szolgáltatási csomagot állít be.</span><span class="sxs-lookup"><span data-stu-id="91a33-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91a33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91a33-104">SYNTAX</span></span>

### <span data-ttu-id="91a33-105">S1</span><span class="sxs-lookup"><span data-stu-id="91a33-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91a33-106">S2</span><span class="sxs-lookup"><span data-stu-id="91a33-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91a33-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="91a33-107">DESCRIPTION</span></span>
<span data-ttu-id="91a33-108">A **set-AzureRmAppServicePlan** parancsmag az Azure app szolgáltatási csomagját állítja be.</span><span class="sxs-lookup"><span data-stu-id="91a33-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="91a33-109">Példák</span><span class="sxs-lookup"><span data-stu-id="91a33-109">EXAMPLES</span></span>

### <span data-ttu-id="91a33-110">1: alkalmazás-szolgáltatási csomag módosítása</span><span class="sxs-lookup"><span data-stu-id="91a33-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="91a33-111">Ez a parancs beállítja a PerSiteScaling beállítást az ContosoASP nevű app-szolgáltatási tervben, amely a Default-Web-WestUS nevű erőforráscsoport része.</span><span class="sxs-lookup"><span data-stu-id="91a33-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="91a33-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91a33-112">PARAMETERS</span></span>

### <span data-ttu-id="91a33-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="91a33-113">-AdminSiteName</span></span>
<span data-ttu-id="91a33-114">Rendszergazdai webhely neve</span><span class="sxs-lookup"><span data-stu-id="91a33-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a33-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="91a33-115">-AppServicePlan</span></span>
<span data-ttu-id="91a33-116">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="91a33-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91a33-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91a33-117">-AsJob</span></span>
<span data-ttu-id="91a33-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="91a33-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91a33-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a33-119">-DefaultProfile</span></span>
<span data-ttu-id="91a33-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91a33-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91a33-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91a33-121">-Name</span></span>
<span data-ttu-id="91a33-122">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="91a33-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a33-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="91a33-123">-NumberofWorkers</span></span>
<span data-ttu-id="91a33-124">Munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="91a33-124">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a33-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="91a33-125">-PerSiteScaling</span></span>
<span data-ttu-id="91a33-126">Egy webhely méretezése logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="91a33-126">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a33-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91a33-127">-ResourceGroupName</span></span>
<span data-ttu-id="91a33-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="91a33-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a33-129">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="91a33-129">-Tier</span></span>
<span data-ttu-id="91a33-130">Tier</span><span class="sxs-lookup"><span data-stu-id="91a33-130">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a33-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="91a33-131">-WorkerSize</span></span>
<span data-ttu-id="91a33-132">Munkatársi méret</span><span class="sxs-lookup"><span data-stu-id="91a33-132">Worker Size</span></span>

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

### <span data-ttu-id="91a33-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a33-133">CommonParameters</span></span>
<span data-ttu-id="91a33-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91a33-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a33-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91a33-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a33-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91a33-136">INPUTS</span></span>

### <span data-ttu-id="91a33-137">Microsoft. Azure. Management. WebSites. models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="91a33-137">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="91a33-138">Paraméterek: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="91a33-138">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="91a33-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91a33-139">OUTPUTS</span></span>

### <span data-ttu-id="91a33-140">Microsoft. Azure. Management. WebSites. models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="91a33-140">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="91a33-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91a33-141">NOTES</span></span>

## <span data-ttu-id="91a33-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91a33-142">RELATED LINKS</span></span>

[<span data-ttu-id="91a33-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91a33-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="91a33-144">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91a33-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="91a33-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91a33-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="91a33-146">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91a33-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="91a33-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91a33-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="91a33-148">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91a33-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


