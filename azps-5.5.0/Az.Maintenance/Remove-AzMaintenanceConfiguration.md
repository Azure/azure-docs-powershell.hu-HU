---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152370"
---
# <span data-ttu-id="3eb90-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3eb90-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="3eb90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb90-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb90-103">Konfigurációs rekord törlése</span><span class="sxs-lookup"><span data-stu-id="3eb90-103">Delete Configuration record</span></span>

## <span data-ttu-id="3eb90-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3eb90-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb90-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3eb90-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb90-106">Delete Maintenance Configuration record</span><span class="sxs-lookup"><span data-stu-id="3eb90-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="3eb90-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3eb90-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb90-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3eb90-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="3eb90-109">Delete Maintenance Configuration record</span><span class="sxs-lookup"><span data-stu-id="3eb90-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="3eb90-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3eb90-110">PARAMETERS</span></span>

### <span data-ttu-id="3eb90-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eb90-111">-AsJob</span></span>
<span data-ttu-id="3eb90-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3eb90-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3eb90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb90-113">-DefaultProfile</span></span>
<span data-ttu-id="3eb90-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3eb90-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb90-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3eb90-115">-Force</span></span>
<span data-ttu-id="3eb90-116">Eltávolítás kényszerítés megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="3eb90-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="3eb90-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3eb90-117">-Name</span></span>
<span data-ttu-id="3eb90-118">A karbantartási konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="3eb90-118">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb90-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3eb90-119">-PassThru</span></span>
<span data-ttu-id="3eb90-120">Az Eltávolítás művelet állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3eb90-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="3eb90-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3eb90-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3eb90-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb90-122">-ResourceGroupName</span></span>
<span data-ttu-id="3eb90-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3eb90-123">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb90-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3eb90-124">-Confirm</span></span>
<span data-ttu-id="3eb90-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3eb90-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb90-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb90-126">-WhatIf</span></span>
<span data-ttu-id="3eb90-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3eb90-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eb90-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3eb90-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb90-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb90-129">CommonParameters</span></span>
<span data-ttu-id="3eb90-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb90-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb90-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3eb90-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb90-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3eb90-132">INPUTS</span></span>

### <span data-ttu-id="3eb90-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3eb90-133">System.String</span></span>

## <span data-ttu-id="3eb90-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eb90-134">OUTPUTS</span></span>

### <span data-ttu-id="3eb90-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3eb90-135">System.Boolean</span></span>

## <span data-ttu-id="3eb90-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3eb90-136">NOTES</span></span>

## <span data-ttu-id="3eb90-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3eb90-137">RELATED LINKS</span></span>
