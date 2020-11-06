---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: b97506b8f104859c54c55ee1a937916623f4201d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492660"
---
# <span data-ttu-id="af6be-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="af6be-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="af6be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af6be-102">SYNOPSIS</span></span>
<span data-ttu-id="af6be-103">Az Azure app szolgáltatás tervének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="af6be-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af6be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af6be-104">SYNTAX</span></span>

### <span data-ttu-id="af6be-105">S1</span><span class="sxs-lookup"><span data-stu-id="af6be-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af6be-106">S2</span><span class="sxs-lookup"><span data-stu-id="af6be-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af6be-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="af6be-107">DESCRIPTION</span></span>
<span data-ttu-id="af6be-108">A **Remove-AzureRmAppServicePlan** parancsmag eltávolítja az Azure app szolgáltatási csomagját.</span><span class="sxs-lookup"><span data-stu-id="af6be-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="af6be-109">Példák</span><span class="sxs-lookup"><span data-stu-id="af6be-109">EXAMPLES</span></span>

### <span data-ttu-id="af6be-110">1. példa: alkalmazás-szolgáltatási csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="af6be-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="af6be-111">Ez a parancs eltávolítja a ContosoASP nevű Azure app Service Plant, amely a Default-Web-WestUS nevű erőforrás-csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="af6be-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="af6be-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af6be-112">PARAMETERS</span></span>

### <span data-ttu-id="af6be-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="af6be-113">-AppServicePlan</span></span>
<span data-ttu-id="af6be-114">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="af6be-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="af6be-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af6be-115">-AsJob</span></span>
<span data-ttu-id="af6be-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="af6be-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af6be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af6be-117">-DefaultProfile</span></span>
<span data-ttu-id="af6be-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af6be-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af6be-119">-Force</span><span class="sxs-lookup"><span data-stu-id="af6be-119">-Force</span></span>
<span data-ttu-id="af6be-120">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="af6be-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="af6be-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af6be-121">-Name</span></span>
<span data-ttu-id="af6be-122">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="af6be-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="af6be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af6be-123">-ResourceGroupName</span></span>
<span data-ttu-id="af6be-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="af6be-124">Resource Group Name</span></span>

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

### <span data-ttu-id="af6be-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af6be-125">-Confirm</span></span>
<span data-ttu-id="af6be-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af6be-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af6be-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af6be-127">-WhatIf</span></span>
<span data-ttu-id="af6be-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af6be-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af6be-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af6be-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af6be-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af6be-130">CommonParameters</span></span>
<span data-ttu-id="af6be-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af6be-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af6be-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af6be-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af6be-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af6be-133">INPUTS</span></span>

### <span data-ttu-id="af6be-134">Microsoft. Azure. Management. WebSites. models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="af6be-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="af6be-135">Paraméterek: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="af6be-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="af6be-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af6be-136">OUTPUTS</span></span>

### <span data-ttu-id="af6be-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="af6be-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="af6be-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af6be-138">NOTES</span></span>

## <span data-ttu-id="af6be-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af6be-139">RELATED LINKS</span></span>

[<span data-ttu-id="af6be-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="af6be-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="af6be-141">Új – AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="af6be-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="af6be-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="af6be-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


