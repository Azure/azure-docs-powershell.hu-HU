---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: db51cfdf499fcf3d6c81f47d977978a6ff4bf8cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937489"
---
# <span data-ttu-id="00e8c-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="00e8c-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="00e8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="00e8c-103">Házirend-megfelelőség felmérését indítja el egy előfizetés vagy erőforráscsoport összes erőforrására.</span><span class="sxs-lookup"><span data-stu-id="00e8c-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="00e8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00e8c-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00e8c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="00e8c-106">A **Start-AzPolicyComplianceScan** parancsmag elindítja egy előfizetés vagy erőforráscsoport házirendmegmegelőségi kiértékelését.</span><span class="sxs-lookup"><span data-stu-id="00e8c-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="00e8c-107">Az adott hatókörbe tartozó összes erőforrás megfelelőségi állapotát az összes hozzárendelt házirendhez kiértékeli a rendszer.</span><span class="sxs-lookup"><span data-stu-id="00e8c-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="00e8c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00e8c-108">EXAMPLES</span></span>

### <span data-ttu-id="00e8c-109">1. példa: Megfelelőségi vizsgálat kezdése az előfizetés hatókörében</span><span class="sxs-lookup"><span data-stu-id="00e8c-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="00e8c-110">Ez a parancs elindítja az aktív előfizetés házirend-megfelelőségértékelését.</span><span class="sxs-lookup"><span data-stu-id="00e8c-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="00e8c-111">2. példa: Megfelelőségi vizsgálat kezdése az erőforráscsoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="00e8c-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="00e8c-112">Ez a parancs elindítja az aktív előfizetés "myRG" erőforráscsoportja házirend-megfelelőségi kiértékelést.</span><span class="sxs-lookup"><span data-stu-id="00e8c-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="00e8c-113">3. példa: Megfelelőségi vizsgálat kezdése és várakozás a háttérben való befejeződésére</span><span class="sxs-lookup"><span data-stu-id="00e8c-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="00e8c-114">Ez a parancs elindítja az aktív előfizetés házirend-megfelelőségértékelését.</span><span class="sxs-lookup"><span data-stu-id="00e8c-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="00e8c-115">A vizsgálat befejeződik.</span><span class="sxs-lookup"><span data-stu-id="00e8c-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="00e8c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00e8c-116">PARAMETERS</span></span>

### <span data-ttu-id="00e8c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00e8c-117">-AsJob</span></span>
<span data-ttu-id="00e8c-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="00e8c-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="00e8c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e8c-119">-DefaultProfile</span></span>
<span data-ttu-id="00e8c-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00e8c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00e8c-121">-PassThru</span></span>
<span data-ttu-id="00e8c-122">Igaz érték visszaadva, ha a parancs sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="00e8c-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="00e8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00e8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="00e8c-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="00e8c-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00e8c-125">-Confirm</span></span>
<span data-ttu-id="00e8c-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="00e8c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00e8c-127">-WhatIf</span></span>
<span data-ttu-id="00e8c-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="00e8c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00e8c-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00e8c-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e8c-130">CommonParameters</span></span>
<span data-ttu-id="00e8c-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00e8c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e8c-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00e8c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e8c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00e8c-133">INPUTS</span></span>

### <span data-ttu-id="00e8c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="00e8c-134">System.String</span></span>

## <span data-ttu-id="00e8c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00e8c-135">OUTPUTS</span></span>

### <span data-ttu-id="00e8c-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00e8c-136">System.Boolean</span></span>

## <span data-ttu-id="00e8c-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00e8c-137">NOTES</span></span>

## <span data-ttu-id="00e8c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00e8c-138">RELATED LINKS</span></span>
