---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: faf2c40bc43c1b42861bc93d2398d4d26731c112
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479702"
---
# <span data-ttu-id="04d37-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="04d37-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="04d37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04d37-102">SYNOPSIS</span></span>
<span data-ttu-id="04d37-103">Incidens törlése.</span><span class="sxs-lookup"><span data-stu-id="04d37-103">Delete an Incident.</span></span>

## <span data-ttu-id="04d37-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04d37-104">SYNTAX</span></span>

### <span data-ttu-id="04d37-105">IncidentId (default)</span><span class="sxs-lookup"><span data-stu-id="04d37-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04d37-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="04d37-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04d37-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04d37-107">DESCRIPTION</span></span>
<span data-ttu-id="04d37-108">A **Remove-AzSentinelIncident** parancsmag véglegesen töröl egy incidenst egy adott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="04d37-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="04d37-109">Az Incidens **objektumokat** átadhatja a folyamat műveleti jelével, vagy megadhatja a szükséges paramétereket.</span><span class="sxs-lookup"><span data-stu-id="04d37-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="04d37-110">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="04d37-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="04d37-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04d37-111">EXAMPLES</span></span>

### <span data-ttu-id="04d37-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="04d37-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="04d37-113">Ez a parancs eltávolítja az Incidenst a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="04d37-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="04d37-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04d37-114">PARAMETERS</span></span>

### <span data-ttu-id="04d37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d37-115">-DefaultProfile</span></span>
<span data-ttu-id="04d37-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04d37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04d37-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="04d37-117">-IncidentId</span></span>
<span data-ttu-id="04d37-118">Incidens azonosítója.</span><span class="sxs-lookup"><span data-stu-id="04d37-118">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04d37-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04d37-119">-InputObject</span></span>
<span data-ttu-id="04d37-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="04d37-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04d37-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04d37-121">-PassThru</span></span>
<span data-ttu-id="04d37-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="04d37-122">PassThru</span></span>

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

### <span data-ttu-id="04d37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04d37-123">-ResourceGroupName</span></span>
<span data-ttu-id="04d37-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="04d37-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04d37-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="04d37-125">-WorkspaceName</span></span>
<span data-ttu-id="04d37-126">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="04d37-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04d37-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04d37-127">-Confirm</span></span>
<span data-ttu-id="04d37-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="04d37-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04d37-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d37-129">-WhatIf</span></span>
<span data-ttu-id="04d37-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="04d37-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04d37-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04d37-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d37-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d37-132">CommonParameters</span></span>
<span data-ttu-id="04d37-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04d37-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d37-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04d37-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d37-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04d37-135">INPUTS</span></span>

### <span data-ttu-id="04d37-136">System.String</span><span class="sxs-lookup"><span data-stu-id="04d37-136">System.String</span></span>
### <span data-ttu-id="04d37-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="04d37-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="04d37-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04d37-138">OUTPUTS</span></span>

### <span data-ttu-id="04d37-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04d37-139">System.Boolean</span></span>
## <span data-ttu-id="04d37-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04d37-140">NOTES</span></span>

## <span data-ttu-id="04d37-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04d37-141">RELATED LINKS</span></span>
