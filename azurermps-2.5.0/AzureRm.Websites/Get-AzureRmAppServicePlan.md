---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: b85d22d1030eaa12e58cded1c7225231c7e8b964
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848621"
---
# <span data-ttu-id="ed3bc-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ed3bc-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="ed3bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed3bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3bc-103">Egy Azure app-szolgáltatási csomagot kap a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="ed3bc-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed3bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed3bc-104">SYNTAX</span></span>

### <span data-ttu-id="ed3bc-105">S1</span><span class="sxs-lookup"><span data-stu-id="ed3bc-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed3bc-106">S2</span><span class="sxs-lookup"><span data-stu-id="ed3bc-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed3bc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed3bc-107">DESCRIPTION</span></span>
<span data-ttu-id="ed3bc-108">A **Get-AzureRmAppServicePlan** parancsmag egy Azure app-szolgáltatási csomagot kap a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="ed3bc-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="ed3bc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ed3bc-109">EXAMPLES</span></span>

### <span data-ttu-id="ed3bc-110">1. példa: alkalmazás-szolgáltatási terv beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="ed3bc-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ed3bc-111">Ez a parancs beolvassa a ContosoASP nevű app-szolgáltatást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="ed3bc-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="ed3bc-112">2. példa: a minden alkalmazás-szolgáltatási csomag beszerzése egy helyre</span><span class="sxs-lookup"><span data-stu-id="ed3bc-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="ed3bc-113">Ez a parancs a "Nyugat-amerikai" régióban található összes app-szolgáltatási csomagot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="ed3bc-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="ed3bc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed3bc-114">PARAMETERS</span></span>

### <span data-ttu-id="ed3bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3bc-115">-DefaultProfile</span></span>
<span data-ttu-id="ed3bc-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed3bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed3bc-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="ed3bc-117">-Location</span></span>
<span data-ttu-id="ed3bc-118">Helyre</span><span class="sxs-lookup"><span data-stu-id="ed3bc-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3bc-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed3bc-119">-Name</span></span>
<span data-ttu-id="ed3bc-120">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="ed3bc-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3bc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed3bc-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed3bc-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ed3bc-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3bc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3bc-123">CommonParameters</span></span>
<span data-ttu-id="ed3bc-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed3bc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3bc-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed3bc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3bc-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed3bc-126">INPUTS</span></span>

### <span data-ttu-id="ed3bc-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="ed3bc-127">None</span></span>
<span data-ttu-id="ed3bc-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ed3bc-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed3bc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed3bc-129">OUTPUTS</span></span>

### <span data-ttu-id="ed3bc-130">Microsoft. Azure. Management. WebSites. models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="ed3bc-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="ed3bc-131">Microsoft. Azure. Management. WebSites. models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="ed3bc-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="ed3bc-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed3bc-132">NOTES</span></span>

## <span data-ttu-id="ed3bc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed3bc-133">RELATED LINKS</span></span>

[<span data-ttu-id="ed3bc-134">Új – AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ed3bc-134">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="ed3bc-135">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ed3bc-135">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="ed3bc-136">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ed3bc-136">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


