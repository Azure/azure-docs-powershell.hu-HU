---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367063"
---
# <span data-ttu-id="09571-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09571-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="09571-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09571-102">SYNOPSIS</span></span>
<span data-ttu-id="09571-103">Eltávolít egy Azure App Service-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="09571-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="09571-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09571-104">SYNTAX</span></span>

### <span data-ttu-id="09571-105">S1</span><span class="sxs-lookup"><span data-stu-id="09571-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09571-106">S2</span><span class="sxs-lookup"><span data-stu-id="09571-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09571-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09571-107">DESCRIPTION</span></span>
<span data-ttu-id="09571-108">A **Remove-AzAppServicePlan** parancsmag eltávolítja az Azure App Service-csomagokat.</span><span class="sxs-lookup"><span data-stu-id="09571-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="09571-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09571-109">EXAMPLES</span></span>

### <span data-ttu-id="09571-110">1. példa: Appszolgáltatás-csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="09571-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="09571-111">Ez a parancs eltávolítja a ContosoASP nevű Azure App Service-tervet, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="09571-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="09571-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09571-112">PARAMETERS</span></span>

### <span data-ttu-id="09571-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09571-113">-AppServicePlan</span></span>
<span data-ttu-id="09571-114">App Service Plan objektum</span><span class="sxs-lookup"><span data-stu-id="09571-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="09571-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09571-115">-AsJob</span></span>
<span data-ttu-id="09571-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="09571-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09571-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09571-117">-DefaultProfile</span></span>
<span data-ttu-id="09571-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09571-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09571-119">-Force</span><span class="sxs-lookup"><span data-stu-id="09571-119">-Force</span></span>
<span data-ttu-id="09571-120">Forcefully Remove Option</span><span class="sxs-lookup"><span data-stu-id="09571-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="09571-121">-Name</span><span class="sxs-lookup"><span data-stu-id="09571-121">-Name</span></span>
<span data-ttu-id="09571-122">Appszolgáltatás-terv neve</span><span class="sxs-lookup"><span data-stu-id="09571-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="09571-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09571-123">-ResourceGroupName</span></span>
<span data-ttu-id="09571-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="09571-124">Resource Group Name</span></span>

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

### <span data-ttu-id="09571-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09571-125">-Confirm</span></span>
<span data-ttu-id="09571-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="09571-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09571-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09571-127">-WhatIf</span></span>
<span data-ttu-id="09571-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="09571-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09571-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09571-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09571-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09571-130">CommonParameters</span></span>
<span data-ttu-id="09571-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09571-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09571-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09571-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09571-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09571-133">INPUTS</span></span>

### <span data-ttu-id="09571-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09571-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="09571-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09571-135">OUTPUTS</span></span>

### <span data-ttu-id="09571-136">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="09571-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="09571-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09571-137">NOTES</span></span>

## <span data-ttu-id="09571-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09571-138">RELATED LINKS</span></span>

[<span data-ttu-id="09571-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09571-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="09571-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09571-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="09571-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09571-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


