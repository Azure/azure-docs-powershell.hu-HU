---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: f541ac58fe8512d67fab1755cfededc8839388e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840014"
---
# <span data-ttu-id="29522-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="29522-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="29522-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29522-102">SYNOPSIS</span></span>
<span data-ttu-id="29522-103">Az Azure app szolgáltatás tervének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="29522-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="29522-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29522-104">SYNTAX</span></span>

### <span data-ttu-id="29522-105">S1</span><span class="sxs-lookup"><span data-stu-id="29522-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29522-106">S2</span><span class="sxs-lookup"><span data-stu-id="29522-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29522-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="29522-107">DESCRIPTION</span></span>
<span data-ttu-id="29522-108">A **Remove-AzAppServicePlan** parancsmag eltávolítja az Azure app szolgáltatási csomagját.</span><span class="sxs-lookup"><span data-stu-id="29522-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="29522-109">Példák</span><span class="sxs-lookup"><span data-stu-id="29522-109">EXAMPLES</span></span>

### <span data-ttu-id="29522-110">1. példa: alkalmazás-szolgáltatási csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="29522-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="29522-111">Ez a parancs eltávolítja a ContosoASP nevű Azure app Service Plant, amely a Default-Web-WestUS nevű erőforrás-csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="29522-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="29522-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29522-112">PARAMETERS</span></span>

### <span data-ttu-id="29522-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="29522-113">-AppServicePlan</span></span>
<span data-ttu-id="29522-114">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="29522-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="29522-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29522-115">-AsJob</span></span>
<span data-ttu-id="29522-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="29522-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29522-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29522-117">-DefaultProfile</span></span>
<span data-ttu-id="29522-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29522-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29522-119">-Force</span><span class="sxs-lookup"><span data-stu-id="29522-119">-Force</span></span>
<span data-ttu-id="29522-120">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="29522-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="29522-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29522-121">-Name</span></span>
<span data-ttu-id="29522-122">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="29522-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="29522-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29522-123">-ResourceGroupName</span></span>
<span data-ttu-id="29522-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="29522-124">Resource Group Name</span></span>

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

### <span data-ttu-id="29522-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29522-125">-Confirm</span></span>
<span data-ttu-id="29522-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29522-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29522-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29522-127">-WhatIf</span></span>
<span data-ttu-id="29522-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29522-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29522-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29522-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29522-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29522-130">CommonParameters</span></span>
<span data-ttu-id="29522-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29522-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29522-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29522-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29522-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29522-133">INPUTS</span></span>

### <span data-ttu-id="29522-134">Microsoft. Azure. Command. WebApps. models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="29522-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="29522-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29522-135">OUTPUTS</span></span>

### <span data-ttu-id="29522-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="29522-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="29522-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29522-137">NOTES</span></span>

## <span data-ttu-id="29522-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29522-138">RELATED LINKS</span></span>

[<span data-ttu-id="29522-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="29522-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="29522-140">Új – AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="29522-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="29522-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="29522-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


