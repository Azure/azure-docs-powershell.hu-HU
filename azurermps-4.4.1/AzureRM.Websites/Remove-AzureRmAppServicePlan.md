---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d1d07e27a7ad6fb6059cbfc8e4c972b1cedaf7e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504667"
---
# <span data-ttu-id="ee63e-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ee63e-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="ee63e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee63e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee63e-103">Az Azure app szolgáltatás tervének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ee63e-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee63e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee63e-104">SYNTAX</span></span>

### <span data-ttu-id="ee63e-105">S1</span><span class="sxs-lookup"><span data-stu-id="ee63e-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee63e-106">S2</span><span class="sxs-lookup"><span data-stu-id="ee63e-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee63e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee63e-107">DESCRIPTION</span></span>
<span data-ttu-id="ee63e-108">A **Remove-AzureRmAppServicePlan** parancsmag eltávolítja az Azure app szolgáltatási csomagját.</span><span class="sxs-lookup"><span data-stu-id="ee63e-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="ee63e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ee63e-109">EXAMPLES</span></span>

### <span data-ttu-id="ee63e-110">1. példa: alkalmazás-szolgáltatási csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ee63e-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ee63e-111">Ez a parancs eltávolítja a ContosoASP nevű Azure app Service Plant, amely a Default-Web-WestUS nevű erőforrás-csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="ee63e-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ee63e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee63e-112">PARAMETERS</span></span>

### <span data-ttu-id="ee63e-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ee63e-113">-AppServicePlan</span></span>
<span data-ttu-id="ee63e-114">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="ee63e-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee63e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ee63e-115">-Force</span></span>
<span data-ttu-id="ee63e-116">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="ee63e-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="ee63e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee63e-117">-Name</span></span>
<span data-ttu-id="ee63e-118">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="ee63e-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="ee63e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee63e-119">-ResourceGroupName</span></span>
<span data-ttu-id="ee63e-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ee63e-120">Resource Group Name</span></span>

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

### <span data-ttu-id="ee63e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee63e-121">-Confirm</span></span>
<span data-ttu-id="ee63e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee63e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee63e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee63e-123">-WhatIf</span></span>
<span data-ttu-id="ee63e-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee63e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee63e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee63e-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee63e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee63e-126">-DefaultProfile</span></span>
<span data-ttu-id="ee63e-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee63e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee63e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee63e-128">CommonParameters</span></span>
<span data-ttu-id="ee63e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee63e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee63e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee63e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee63e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee63e-131">INPUTS</span></span>

### <span data-ttu-id="ee63e-132">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="ee63e-132">ServerFarmWithRichSku</span></span>
<span data-ttu-id="ee63e-133">A ' AppServicePlan ' paraméter az "ServerFarmWithRichSku" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ee63e-133">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="ee63e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee63e-134">OUTPUTS</span></span>

### <span data-ttu-id="ee63e-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ee63e-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ee63e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee63e-136">NOTES</span></span>

## <span data-ttu-id="ee63e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee63e-137">RELATED LINKS</span></span>

[<span data-ttu-id="ee63e-138">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ee63e-138">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="ee63e-139">Új – AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ee63e-139">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="ee63e-140">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ee63e-140">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


