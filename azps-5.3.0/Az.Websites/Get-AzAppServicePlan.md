---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380797"
---
# <span data-ttu-id="458af-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="458af-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="458af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="458af-102">SYNOPSIS</span></span>
<span data-ttu-id="458af-103">Egy Azure App Service-tervet kap a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="458af-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="458af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="458af-104">SYNTAX</span></span>

### <span data-ttu-id="458af-105">S1</span><span class="sxs-lookup"><span data-stu-id="458af-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="458af-106">S2</span><span class="sxs-lookup"><span data-stu-id="458af-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="458af-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="458af-107">DESCRIPTION</span></span>
<span data-ttu-id="458af-108">A **Get-AzAppServicePlan** parancsmag egy Azure App Service-tervet kap a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="458af-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="458af-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="458af-109">EXAMPLES</span></span>

### <span data-ttu-id="458af-110">1. példa: Appszolgáltatás-csomag lekérte egy erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="458af-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="458af-111">Ez a parancs a ContosoASP nevű appszolgáltatás-tervet kapja meg, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="458af-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="458af-112">2. példa: Az összes appszolgáltatás-csomag lekérte egy helyre</span><span class="sxs-lookup"><span data-stu-id="458af-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="458af-113">Ez a parancs a "Nyugat-Egyesült Államok" régió összes appszolgáltatás-csomagját beveszi.</span><span class="sxs-lookup"><span data-stu-id="458af-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="458af-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="458af-114">PARAMETERS</span></span>

### <span data-ttu-id="458af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="458af-115">-DefaultProfile</span></span>
<span data-ttu-id="458af-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="458af-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="458af-117">-Location</span><span class="sxs-lookup"><span data-stu-id="458af-117">-Location</span></span>
<span data-ttu-id="458af-118">Hely</span><span class="sxs-lookup"><span data-stu-id="458af-118">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458af-119">-Name</span><span class="sxs-lookup"><span data-stu-id="458af-119">-Name</span></span>
<span data-ttu-id="458af-120">Appszolgáltatás-terv neve</span><span class="sxs-lookup"><span data-stu-id="458af-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458af-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="458af-121">-ResourceGroupName</span></span>
<span data-ttu-id="458af-122">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="458af-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458af-123">CommonParameters</span></span>
<span data-ttu-id="458af-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="458af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458af-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="458af-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458af-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="458af-126">INPUTS</span></span>

### <span data-ttu-id="458af-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="458af-127">None</span></span>

## <span data-ttu-id="458af-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="458af-128">OUTPUTS</span></span>

### <span data-ttu-id="458af-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="458af-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="458af-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="458af-130">NOTES</span></span>

## <span data-ttu-id="458af-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="458af-131">RELATED LINKS</span></span>

[<span data-ttu-id="458af-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="458af-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="458af-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="458af-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="458af-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="458af-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


