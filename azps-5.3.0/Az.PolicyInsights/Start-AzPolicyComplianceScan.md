---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481039"
---
# <span data-ttu-id="578d7-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="578d7-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="578d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="578d7-102">SYNOPSIS</span></span>
<span data-ttu-id="578d7-103">Házirend-megfelelőségi kiértékelést indít el egy előfizetés vagy erőforráscsoport összes erőforrására.</span><span class="sxs-lookup"><span data-stu-id="578d7-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="578d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="578d7-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="578d7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="578d7-105">DESCRIPTION</span></span>
<span data-ttu-id="578d7-106">A **Start-AzPolicyComplianceScan** parancsmag elindítja egy előfizetés vagy erőforráscsoport házirendmegmegelőségi kiértékelését.</span><span class="sxs-lookup"><span data-stu-id="578d7-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="578d7-107">Az adott hatókörbe tartozó összes erőforrás megfelelőségi állapotát az összes hozzárendelt házirendhez kiértékeli a rendszer.</span><span class="sxs-lookup"><span data-stu-id="578d7-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="578d7-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="578d7-108">EXAMPLES</span></span>

### <span data-ttu-id="578d7-109">1. példa: Megfelelőségi vizsgálat kezdése az előfizetés hatókörében</span><span class="sxs-lookup"><span data-stu-id="578d7-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="578d7-110">Ez a parancs elindítja az aktív előfizetés házirend-megfelelőségi kiértékelést.</span><span class="sxs-lookup"><span data-stu-id="578d7-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="578d7-111">2. példa: Megfelelőségi vizsgálat kezdése az erőforráscsoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="578d7-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="578d7-112">Ez a parancs elindítja az aktív előfizetés "myRG" erőforráscsoportja házirend-megfelelőségi kiértékelést.</span><span class="sxs-lookup"><span data-stu-id="578d7-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="578d7-113">3. példa: Megfelelőségi vizsgálat kezdése és várakozás a háttérben való befejeződésére</span><span class="sxs-lookup"><span data-stu-id="578d7-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="578d7-114">Ez a parancs elindítja az aktív előfizetés házirend-megfelelőségi kiértékelést.</span><span class="sxs-lookup"><span data-stu-id="578d7-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="578d7-115">A vizsgálat befejeződik.</span><span class="sxs-lookup"><span data-stu-id="578d7-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="578d7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="578d7-116">PARAMETERS</span></span>

### <span data-ttu-id="578d7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="578d7-117">-AsJob</span></span>
<span data-ttu-id="578d7-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="578d7-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="578d7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578d7-119">-DefaultProfile</span></span>
<span data-ttu-id="578d7-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="578d7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="578d7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="578d7-121">-PassThru</span></span>
<span data-ttu-id="578d7-122">Igaz érték visszaadva, ha a parancs sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="578d7-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="578d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="578d7-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="578d7-124">Resource group name.</span></span>

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

### <span data-ttu-id="578d7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="578d7-125">-Confirm</span></span>
<span data-ttu-id="578d7-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="578d7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="578d7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="578d7-127">-WhatIf</span></span>
<span data-ttu-id="578d7-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="578d7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="578d7-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="578d7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="578d7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578d7-130">CommonParameters</span></span>
<span data-ttu-id="578d7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="578d7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578d7-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="578d7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578d7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="578d7-133">INPUTS</span></span>

### <span data-ttu-id="578d7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="578d7-134">System.String</span></span>

## <span data-ttu-id="578d7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="578d7-135">OUTPUTS</span></span>

### <span data-ttu-id="578d7-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="578d7-136">System.Boolean</span></span>

## <span data-ttu-id="578d7-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="578d7-137">NOTES</span></span>

## <span data-ttu-id="578d7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="578d7-138">RELATED LINKS</span></span>
