---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186733"
---
# <span data-ttu-id="0e003-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0e003-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="0e003-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e003-102">SYNOPSIS</span></span>
<span data-ttu-id="0e003-103">IoT biztonsági megoldás törlése</span><span class="sxs-lookup"><span data-stu-id="0e003-103">Delete IoT security solution</span></span>

## <span data-ttu-id="0e003-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e003-104">SYNTAX</span></span>

### <span data-ttu-id="0e003-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e003-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e003-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e003-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e003-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0e003-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e003-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e003-108">DESCRIPTION</span></span>
<span data-ttu-id="0e003-109">A Remove-AzIotSecuritySolution parancsmag egy bizonyos IOT biztonsági megoldást töröl.</span><span class="sxs-lookup"><span data-stu-id="0e003-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="0e003-110">A IoT biztonsági megoldás biztonsági adatokat és eseményeket gyűjt a IoT-eszközökről és a IoT hub-ról a fenyegetések megelőzése és észlelése érdekében.</span><span class="sxs-lookup"><span data-stu-id="0e003-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="0e003-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0e003-111">EXAMPLES</span></span>

### <span data-ttu-id="0e003-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0e003-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="0e003-113">A "MySample" IoT biztonsági megoldás törlése a "MyResourceGroup" erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="0e003-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="0e003-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e003-114">PARAMETERS</span></span>

### <span data-ttu-id="0e003-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e003-115">-DefaultProfile</span></span>
<span data-ttu-id="0e003-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e003-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e003-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e003-117">-InputObject</span></span>
<span data-ttu-id="0e003-118">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="0e003-118">Input Object.</span></span>

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

### <span data-ttu-id="0e003-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0e003-119">-Name</span></span>
<span data-ttu-id="0e003-120">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="0e003-120">Resource name.</span></span>

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

### <span data-ttu-id="0e003-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e003-121">-PassThru</span></span>
<span data-ttu-id="0e003-122">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="0e003-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="0e003-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e003-123">-ResourceGroupName</span></span>
<span data-ttu-id="0e003-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="0e003-124">Resource group name.</span></span>

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

### <span data-ttu-id="0e003-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e003-125">-ResourceId</span></span>
<span data-ttu-id="0e003-126">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="0e003-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="0e003-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e003-127">-Confirm</span></span>
<span data-ttu-id="0e003-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e003-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e003-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e003-129">-WhatIf</span></span>
<span data-ttu-id="0e003-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e003-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e003-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e003-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e003-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e003-132">CommonParameters</span></span>
<span data-ttu-id="0e003-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e003-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e003-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0e003-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e003-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e003-135">INPUTS</span></span>

### <span data-ttu-id="0e003-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0e003-136">System.String</span></span>

### <span data-ttu-id="0e003-137">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0e003-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="0e003-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e003-138">OUTPUTS</span></span>

### <span data-ttu-id="0e003-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e003-139">System.Boolean</span></span>

## <span data-ttu-id="0e003-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e003-140">NOTES</span></span>

## <span data-ttu-id="0e003-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e003-141">RELATED LINKS</span></span>