---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: da98138060b0c06e09a56b375c64f530ea8e51f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934658"
---
# <span data-ttu-id="13dd1-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="13dd1-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="13dd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="13dd1-103">IoT-biztonsági megoldás törlése</span><span class="sxs-lookup"><span data-stu-id="13dd1-103">Delete IoT security solution</span></span>

## <span data-ttu-id="13dd1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13dd1-104">SYNTAX</span></span>

### <span data-ttu-id="13dd1-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13dd1-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13dd1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="13dd1-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13dd1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="13dd1-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13dd1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13dd1-108">DESCRIPTION</span></span>
<span data-ttu-id="13dd1-109">A Remove-AzIotSecuritySolution parancsmag töröl egy adott iot biztonsági megoldást.</span><span class="sxs-lookup"><span data-stu-id="13dd1-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="13dd1-110">Az IoT biztonsági megoldás biztonsági adatokat és eseményeket gyűjt az iot-eszközökről és az iOT-központban a veszélyforrások megelőzése és észlelése érdekében.</span><span class="sxs-lookup"><span data-stu-id="13dd1-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="13dd1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13dd1-111">EXAMPLES</span></span>

### <span data-ttu-id="13dd1-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="13dd1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="13dd1-113">A "MySample" IoT biztonsági megoldás törlése a "MyResourceGroup" erőforráscsoporttal</span><span class="sxs-lookup"><span data-stu-id="13dd1-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="13dd1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13dd1-114">PARAMETERS</span></span>

### <span data-ttu-id="13dd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13dd1-115">-DefaultProfile</span></span>
<span data-ttu-id="13dd1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13dd1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13dd1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13dd1-117">-InputObject</span></span>
<span data-ttu-id="13dd1-118">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="13dd1-118">Input Object.</span></span>

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

### <span data-ttu-id="13dd1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="13dd1-119">-Name</span></span>
<span data-ttu-id="13dd1-120">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="13dd1-120">Resource name.</span></span>

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

### <span data-ttu-id="13dd1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13dd1-121">-PassThru</span></span>
<span data-ttu-id="13dd1-122">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="13dd1-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="13dd1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13dd1-123">-ResourceGroupName</span></span>
<span data-ttu-id="13dd1-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13dd1-124">Resource group name.</span></span>

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

### <span data-ttu-id="13dd1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13dd1-125">-ResourceId</span></span>
<span data-ttu-id="13dd1-126">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="13dd1-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="13dd1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13dd1-127">-Confirm</span></span>
<span data-ttu-id="13dd1-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13dd1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13dd1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13dd1-129">-WhatIf</span></span>
<span data-ttu-id="13dd1-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13dd1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13dd1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13dd1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13dd1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13dd1-132">CommonParameters</span></span>
<span data-ttu-id="13dd1-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13dd1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13dd1-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13dd1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13dd1-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13dd1-135">INPUTS</span></span>

### <span data-ttu-id="13dd1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="13dd1-136">System.String</span></span>

### <span data-ttu-id="13dd1-137">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="13dd1-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="13dd1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13dd1-138">OUTPUTS</span></span>

### <span data-ttu-id="13dd1-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="13dd1-139">System.Boolean</span></span>

## <span data-ttu-id="13dd1-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13dd1-140">NOTES</span></span>

## <span data-ttu-id="13dd1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13dd1-141">RELATED LINKS</span></span>
