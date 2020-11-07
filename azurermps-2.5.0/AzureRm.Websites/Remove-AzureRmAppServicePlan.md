---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: e8ce0397a59a72e2960a8e0af978c1b5484c53af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848062"
---
# <span data-ttu-id="d1c3e-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d1c3e-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="d1c3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c3e-103">Az Azure app szolgáltatás tervének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1c3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1c3e-104">SYNTAX</span></span>

### <span data-ttu-id="d1c3e-105">S1</span><span class="sxs-lookup"><span data-stu-id="d1c3e-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1c3e-106">S2</span><span class="sxs-lookup"><span data-stu-id="d1c3e-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1c3e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1c3e-107">DESCRIPTION</span></span>
<span data-ttu-id="d1c3e-108">A **Remove-AzureRmAppServicePlan** parancsmag eltávolítja az Azure app szolgáltatási csomagját.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="d1c3e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d1c3e-109">EXAMPLES</span></span>

### <span data-ttu-id="d1c3e-110">1. példa: alkalmazás-szolgáltatási csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1c3e-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="d1c3e-111">Ez a parancs eltávolítja a ContosoASP nevű Azure app Service Plant, amely a Default-Web-WestUS nevű erőforrás-csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d1c3e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1c3e-112">PARAMETERS</span></span>

### <span data-ttu-id="d1c3e-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d1c3e-113">-AppServicePlan</span></span>
<span data-ttu-id="d1c3e-114">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="d1c3e-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c3e-115">-DefaultProfile</span></span>
<span data-ttu-id="d1c3e-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1c3e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d1c3e-117">-Force</span></span>
<span data-ttu-id="d1c3e-118">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="d1c3e-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="d1c3e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1c3e-119">-Name</span></span>
<span data-ttu-id="d1c3e-120">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="d1c3e-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c3e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c3e-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1c3e-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d1c3e-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c3e-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1c3e-123">-Confirm</span></span>
<span data-ttu-id="d1c3e-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c3e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1c3e-125">-WhatIf</span></span>
<span data-ttu-id="d1c3e-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1c3e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c3e-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1c3e-128">-AsJob</span></span>
<span data-ttu-id="d1c3e-129">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d1c3e-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1c3e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c3e-130">CommonParameters</span></span>
<span data-ttu-id="d1c3e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1c3e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c3e-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1c3e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c3e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1c3e-133">INPUTS</span></span>

### <span data-ttu-id="d1c3e-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="d1c3e-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="d1c3e-135">A ' AppServicePlan ' paraméter az "ServerFarmWithRichSku" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d1c3e-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="d1c3e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1c3e-136">OUTPUTS</span></span>

### <span data-ttu-id="d1c3e-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d1c3e-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d1c3e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1c3e-138">NOTES</span></span>

## <span data-ttu-id="d1c3e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1c3e-139">RELATED LINKS</span></span>

[<span data-ttu-id="d1c3e-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d1c3e-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="d1c3e-141">Új – AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d1c3e-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="d1c3e-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d1c3e-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


