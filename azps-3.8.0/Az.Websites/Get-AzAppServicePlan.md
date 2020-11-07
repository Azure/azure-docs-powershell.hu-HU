---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845774"
---
# <span data-ttu-id="2d6ab-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d6ab-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="2d6ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="2d6ab-103">Egy Azure app-szolgáltatási csomagot kap a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="2d6ab-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="2d6ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d6ab-104">SYNTAX</span></span>

### <span data-ttu-id="2d6ab-105">S1</span><span class="sxs-lookup"><span data-stu-id="2d6ab-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d6ab-106">S2</span><span class="sxs-lookup"><span data-stu-id="2d6ab-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d6ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d6ab-107">DESCRIPTION</span></span>
<span data-ttu-id="2d6ab-108">A **Get-AzAppServicePlan** parancsmag egy Azure app-szolgáltatási csomagot kap a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="2d6ab-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="2d6ab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2d6ab-109">EXAMPLES</span></span>

### <span data-ttu-id="2d6ab-110">1. példa: alkalmazás-szolgáltatási terv beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="2d6ab-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="2d6ab-111">Ez a parancs beolvassa a ContosoASP nevű app-szolgáltatást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="2d6ab-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="2d6ab-112">2. példa: a minden alkalmazás-szolgáltatási csomag beszerzése egy helyre</span><span class="sxs-lookup"><span data-stu-id="2d6ab-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="2d6ab-113">Ez a parancs a "Nyugat-amerikai" régióban található összes app-szolgáltatási csomagot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="2d6ab-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="2d6ab-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d6ab-114">PARAMETERS</span></span>

### <span data-ttu-id="2d6ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d6ab-115">-DefaultProfile</span></span>
<span data-ttu-id="2d6ab-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d6ab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d6ab-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="2d6ab-117">-Location</span></span>
<span data-ttu-id="2d6ab-118">Helyre</span><span class="sxs-lookup"><span data-stu-id="2d6ab-118">Location</span></span> 

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

### <span data-ttu-id="2d6ab-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d6ab-119">-Name</span></span>
<span data-ttu-id="2d6ab-120">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="2d6ab-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="2d6ab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d6ab-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d6ab-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2d6ab-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2d6ab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d6ab-123">CommonParameters</span></span>
<span data-ttu-id="2d6ab-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d6ab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d6ab-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d6ab-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d6ab-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d6ab-126">INPUTS</span></span>

### <span data-ttu-id="2d6ab-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="2d6ab-127">None</span></span>

## <span data-ttu-id="2d6ab-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d6ab-128">OUTPUTS</span></span>

### <span data-ttu-id="2d6ab-129">Microsoft. Azure. Command. WebApps. models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d6ab-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="2d6ab-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d6ab-130">NOTES</span></span>

## <span data-ttu-id="2d6ab-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d6ab-131">RELATED LINKS</span></span>

[<span data-ttu-id="2d6ab-132">Új – AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d6ab-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="2d6ab-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d6ab-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="2d6ab-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d6ab-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


