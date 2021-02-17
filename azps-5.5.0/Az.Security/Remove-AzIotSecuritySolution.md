---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208303"
---
# <span data-ttu-id="92d70-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="92d70-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="92d70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92d70-102">SYNOPSIS</span></span>
<span data-ttu-id="92d70-103">IoT-biztonsági megoldás törlése</span><span class="sxs-lookup"><span data-stu-id="92d70-103">Delete IoT security solution</span></span>

## <span data-ttu-id="92d70-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92d70-104">SYNTAX</span></span>

### <span data-ttu-id="92d70-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92d70-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92d70-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="92d70-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92d70-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="92d70-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92d70-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92d70-108">DESCRIPTION</span></span>
<span data-ttu-id="92d70-109">A Remove-AzIotSecuritySolution parancsmag töröl egy adott iot biztonsági megoldást.</span><span class="sxs-lookup"><span data-stu-id="92d70-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="92d70-110">Az IoT biztonsági megoldás biztonsági adatokat és eseményeket gyűjt az iot-eszközökről és az iOT-központban a veszélyforrások megelőzése és észlelése érdekében.</span><span class="sxs-lookup"><span data-stu-id="92d70-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="92d70-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92d70-111">EXAMPLES</span></span>

### <span data-ttu-id="92d70-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="92d70-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="92d70-113">A "MySample" IoT biztonsági megoldás törlése a "MyResourceGroup" erőforráscsoporttal</span><span class="sxs-lookup"><span data-stu-id="92d70-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="92d70-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92d70-114">PARAMETERS</span></span>

### <span data-ttu-id="92d70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d70-115">-DefaultProfile</span></span>
<span data-ttu-id="92d70-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92d70-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d70-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92d70-117">-InputObject</span></span>
<span data-ttu-id="92d70-118">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="92d70-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92d70-119">-Name</span><span class="sxs-lookup"><span data-stu-id="92d70-119">-Name</span></span>
<span data-ttu-id="92d70-120">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="92d70-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d70-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92d70-121">-PassThru</span></span>
<span data-ttu-id="92d70-122">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="92d70-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="92d70-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92d70-123">-ResourceGroupName</span></span>
<span data-ttu-id="92d70-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92d70-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d70-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92d70-125">-ResourceId</span></span>
<span data-ttu-id="92d70-126">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="92d70-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92d70-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92d70-127">-Confirm</span></span>
<span data-ttu-id="92d70-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="92d70-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92d70-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92d70-129">-WhatIf</span></span>
<span data-ttu-id="92d70-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="92d70-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92d70-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92d70-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92d70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d70-132">CommonParameters</span></span>
<span data-ttu-id="92d70-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92d70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d70-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92d70-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d70-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92d70-135">INPUTS</span></span>

### <span data-ttu-id="92d70-136">System.String</span><span class="sxs-lookup"><span data-stu-id="92d70-136">System.String</span></span>

### <span data-ttu-id="92d70-137">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="92d70-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="92d70-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92d70-138">OUTPUTS</span></span>

### <span data-ttu-id="92d70-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92d70-139">System.Boolean</span></span>

## <span data-ttu-id="92d70-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92d70-140">NOTES</span></span>

## <span data-ttu-id="92d70-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92d70-141">RELATED LINKS</span></span>
