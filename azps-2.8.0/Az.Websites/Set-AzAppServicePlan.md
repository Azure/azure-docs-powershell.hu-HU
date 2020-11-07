---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: d27dc8ae315eb587ccb129125500a86e22429773
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839755"
---
# <span data-ttu-id="d8b47-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d8b47-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="d8b47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8b47-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b47-103">Azure-alkalmazási szolgáltatási csomagot állít be.</span><span class="sxs-lookup"><span data-stu-id="d8b47-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="d8b47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8b47-104">SYNTAX</span></span>

### <span data-ttu-id="d8b47-105">S1</span><span class="sxs-lookup"><span data-stu-id="d8b47-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8b47-106">S2</span><span class="sxs-lookup"><span data-stu-id="d8b47-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8b47-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8b47-107">DESCRIPTION</span></span>
<span data-ttu-id="d8b47-108">A **set-AzAppServicePlan** parancsmag az Azure app szolgáltatási csomagját állítja be.</span><span class="sxs-lookup"><span data-stu-id="d8b47-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="d8b47-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d8b47-109">EXAMPLES</span></span>

### <span data-ttu-id="d8b47-110">1: alkalmazás-szolgáltatási csomag módosítása</span><span class="sxs-lookup"><span data-stu-id="d8b47-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="d8b47-111">Ez a parancs beállítja a PerSiteScaling beállítást az ContosoASP nevű app-szolgáltatási tervben, amely a Default-Web-WestUS nevű erőforráscsoport része.</span><span class="sxs-lookup"><span data-stu-id="d8b47-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d8b47-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8b47-112">PARAMETERS</span></span>

### <span data-ttu-id="d8b47-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="d8b47-113">-AdminSiteName</span></span>
<span data-ttu-id="d8b47-114">Rendszergazdai webhely neve</span><span class="sxs-lookup"><span data-stu-id="d8b47-114">Admin Site Name</span></span>

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

### <span data-ttu-id="d8b47-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d8b47-115">-AppServicePlan</span></span>
<span data-ttu-id="d8b47-116">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="d8b47-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="d8b47-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8b47-117">-AsJob</span></span>
<span data-ttu-id="d8b47-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d8b47-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8b47-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b47-119">-DefaultProfile</span></span>
<span data-ttu-id="d8b47-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8b47-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8b47-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d8b47-121">-Name</span></span>
<span data-ttu-id="d8b47-122">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="d8b47-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="d8b47-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="d8b47-123">-NumberofWorkers</span></span>
<span data-ttu-id="d8b47-124">Munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="d8b47-124">Number Of Workers</span></span>

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

### <span data-ttu-id="d8b47-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="d8b47-125">-PerSiteScaling</span></span>
<span data-ttu-id="d8b47-126">Egy webhely méretezése logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="d8b47-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="d8b47-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b47-127">-ResourceGroupName</span></span>
<span data-ttu-id="d8b47-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d8b47-128">Resource Group Name</span></span>

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

### <span data-ttu-id="d8b47-129">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="d8b47-129">-Tier</span></span>
<span data-ttu-id="d8b47-130">Tier</span><span class="sxs-lookup"><span data-stu-id="d8b47-130">Tier</span></span>

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

### <span data-ttu-id="d8b47-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="d8b47-131">-WorkerSize</span></span>
<span data-ttu-id="d8b47-132">Munkatársi méret</span><span class="sxs-lookup"><span data-stu-id="d8b47-132">Worker Size</span></span>

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

### <span data-ttu-id="d8b47-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b47-133">CommonParameters</span></span>
<span data-ttu-id="d8b47-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8b47-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b47-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b47-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b47-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8b47-136">INPUTS</span></span>

### <span data-ttu-id="d8b47-137">Microsoft. Azure. Command. WebApps. models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d8b47-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="d8b47-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8b47-138">OUTPUTS</span></span>

### <span data-ttu-id="d8b47-139">Microsoft. Azure. Command. WebApps. models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d8b47-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="d8b47-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8b47-140">NOTES</span></span>

## <span data-ttu-id="d8b47-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8b47-141">RELATED LINKS</span></span>

[<span data-ttu-id="d8b47-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d8b47-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d8b47-143">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d8b47-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d8b47-144">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d8b47-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="d8b47-145">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d8b47-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d8b47-146">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d8b47-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d8b47-147">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d8b47-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


