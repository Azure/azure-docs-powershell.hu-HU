---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152307"
---
# <span data-ttu-id="6e79e-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="6e79e-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="6e79e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e79e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e79e-103">Regisztrál egy eszközt a projekt áttelepítésével.</span><span class="sxs-lookup"><span data-stu-id="6e79e-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="6e79e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e79e-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6e79e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e79e-105">DESCRIPTION</span></span>
<span data-ttu-id="6e79e-106">Regisztrál egy eszközt a projekt áttelepítésével.</span><span class="sxs-lookup"><span data-stu-id="6e79e-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="6e79e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e79e-107">EXAMPLES</span></span>

### <span data-ttu-id="6e79e-108">1. példa: REgister eszköz.</span><span class="sxs-lookup"><span data-stu-id="6e79e-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="6e79e-109">Regisztrál egy eszközt a projekt áttelepítésével.</span><span class="sxs-lookup"><span data-stu-id="6e79e-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="6e79e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e79e-110">PARAMETERS</span></span>

### <span data-ttu-id="6e79e-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="6e79e-111">-AcceptLanguage</span></span>
<span data-ttu-id="6e79e-112">Szokásos kérésfejléc.</span><span class="sxs-lookup"><span data-stu-id="6e79e-112">Standard request header.</span></span>
<span data-ttu-id="6e79e-113">A szolgáltatás arra használja, hogy a megfelelő nyelven válaszoljon az ügyfélre.</span><span class="sxs-lookup"><span data-stu-id="6e79e-113">Used by service to respond to client in appropriate language.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e79e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e79e-114">-DefaultProfile</span></span>
<span data-ttu-id="6e79e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e79e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e79e-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="6e79e-116">-MigrateProjectName</span></span>
<span data-ttu-id="6e79e-117">Az Azure-áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="6e79e-117">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e79e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e79e-118">-ResourceGroupName</span></span>
<span data-ttu-id="6e79e-119">Annak az Azure-erőforráscsoportnak a neve, amelybe a projektet át kell átcsoportosálni, annak a csoportnak a neve is része.</span><span class="sxs-lookup"><span data-stu-id="6e79e-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e79e-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e79e-120">-SubscriptionId</span></span>
<span data-ttu-id="6e79e-121">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="6e79e-121">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e79e-122">-Tool</span><span class="sxs-lookup"><span data-stu-id="6e79e-122">-Tool</span></span>
<span data-ttu-id="6e79e-123">Regisztrálja vagy beállítja az eszközt.</span><span class="sxs-lookup"><span data-stu-id="6e79e-123">Gets or sets the tool to be registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e79e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e79e-124">-Confirm</span></span>
<span data-ttu-id="6e79e-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6e79e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e79e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e79e-126">-WhatIf</span></span>
<span data-ttu-id="6e79e-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6e79e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e79e-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e79e-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e79e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e79e-129">CommonParameters</span></span>
<span data-ttu-id="6e79e-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e79e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e79e-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e79e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e79e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e79e-132">INPUTS</span></span>

## <span data-ttu-id="6e79e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e79e-133">OUTPUTS</span></span>

### <span data-ttu-id="6e79e-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e79e-134">System.Boolean</span></span>

## <span data-ttu-id="6e79e-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e79e-135">NOTES</span></span>

<span data-ttu-id="6e79e-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6e79e-136">ALIASES</span></span>

## <span data-ttu-id="6e79e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e79e-137">RELATED LINKS</span></span>

