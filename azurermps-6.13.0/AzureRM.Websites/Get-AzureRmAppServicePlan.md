---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: 9fe7d3d9580411c31fdf5ca7e21ba1c4379217a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497192"
---
# <span data-ttu-id="2b3e5-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2b3e5-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="2b3e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3e5-103">Egy Azure app-szolgáltatási csomagot kap a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b3e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b3e5-104">SYNTAX</span></span>

### <span data-ttu-id="2b3e5-105">S1</span><span class="sxs-lookup"><span data-stu-id="2b3e5-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b3e5-106">S2</span><span class="sxs-lookup"><span data-stu-id="2b3e5-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b3e5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b3e5-107">DESCRIPTION</span></span>
<span data-ttu-id="2b3e5-108">A **Get-AzureRmAppServicePlan** parancsmag egy Azure app-szolgáltatási csomagot kap a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="2b3e5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2b3e5-109">EXAMPLES</span></span>

### <span data-ttu-id="2b3e5-110">1. példa: alkalmazás-szolgáltatási terv beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="2b3e5-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="2b3e5-111">Ez a parancs beolvassa a ContosoASP nevű app-szolgáltatást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="2b3e5-112">2. példa: a minden alkalmazás-szolgáltatási csomag beszerzése egy helyre</span><span class="sxs-lookup"><span data-stu-id="2b3e5-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="2b3e5-113">Ez a parancs a "Nyugat-amerikai" régióban található összes app-szolgáltatási csomagot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="2b3e5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b3e5-114">PARAMETERS</span></span>

### <span data-ttu-id="2b3e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3e5-115">-DefaultProfile</span></span>
<span data-ttu-id="2b3e5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b3e5-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="2b3e5-117">-Location</span></span>
<span data-ttu-id="2b3e5-118">Helyre</span><span class="sxs-lookup"><span data-stu-id="2b3e5-118">Location</span></span> 

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

### <span data-ttu-id="2b3e5-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b3e5-119">-Name</span></span>
<span data-ttu-id="2b3e5-120">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="2b3e5-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="2b3e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b3e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b3e5-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2b3e5-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2b3e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3e5-123">CommonParameters</span></span>
<span data-ttu-id="2b3e5-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b3e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3e5-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b3e5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3e5-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b3e5-126">INPUTS</span></span>

### <span data-ttu-id="2b3e5-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="2b3e5-127">None</span></span>

## <span data-ttu-id="2b3e5-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b3e5-128">OUTPUTS</span></span>

### <span data-ttu-id="2b3e5-129">Microsoft. Azure. Management. WebSites. models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2b3e5-129">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="2b3e5-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b3e5-130">NOTES</span></span>

## <span data-ttu-id="2b3e5-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b3e5-131">RELATED LINKS</span></span>

[<span data-ttu-id="2b3e5-132">Új – AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2b3e5-132">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="2b3e5-133">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2b3e5-133">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="2b3e5-134">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2b3e5-134">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


