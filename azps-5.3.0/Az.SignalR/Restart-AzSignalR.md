---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468529"
---
# <span data-ttu-id="39401-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="39401-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="39401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39401-102">SYNOPSIS</span></span>
<span data-ttu-id="39401-103">Indítsa újra a SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="39401-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="39401-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39401-104">SYNTAX</span></span>

### <span data-ttu-id="39401-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39401-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39401-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39401-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39401-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39401-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39401-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39401-108">DESCRIPTION</span></span>
<span data-ttu-id="39401-109">Indítsa újra a SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="39401-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="39401-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39401-110">EXAMPLES</span></span>

### <span data-ttu-id="39401-111">Adott SignalR-szolgáltatás újraindítása</span><span class="sxs-lookup"><span data-stu-id="39401-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="39401-112">Az alapértelmezett erőforráscsoportot a \` Set-AzDefault -ResourceGroupName myResourceGroup állíthatja \` be.</span><span class="sxs-lookup"><span data-stu-id="39401-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="39401-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39401-113">PARAMETERS</span></span>

### <span data-ttu-id="39401-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39401-114">-AsJob</span></span>
<span data-ttu-id="39401-115">Futtassa a parancsmagot a háttérben futó feladatban.</span><span class="sxs-lookup"><span data-stu-id="39401-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="39401-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39401-116">-DefaultProfile</span></span>
<span data-ttu-id="39401-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39401-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39401-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39401-118">-InputObject</span></span>
<span data-ttu-id="39401-119">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="39401-119">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39401-120">-Name</span><span class="sxs-lookup"><span data-stu-id="39401-120">-Name</span></span>
<span data-ttu-id="39401-121">A SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="39401-121">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39401-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39401-122">-PassThru</span></span>
<span data-ttu-id="39401-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="39401-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="39401-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39401-124">-ResourceGroupName</span></span>
<span data-ttu-id="39401-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="39401-125">The resource group name.</span></span>
<span data-ttu-id="39401-126">Ha nincs megadva, a program az alapértelmezett beállítást használja.</span><span class="sxs-lookup"><span data-stu-id="39401-126">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39401-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39401-127">-ResourceId</span></span>
<span data-ttu-id="39401-128">A SignalR szolgáltatáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="39401-128">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39401-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39401-129">-Confirm</span></span>
<span data-ttu-id="39401-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="39401-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39401-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39401-131">-WhatIf</span></span>
<span data-ttu-id="39401-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="39401-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39401-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39401-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39401-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39401-134">CommonParameters</span></span>
<span data-ttu-id="39401-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39401-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39401-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39401-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39401-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39401-137">INPUTS</span></span>

### <span data-ttu-id="39401-138">System.String</span><span class="sxs-lookup"><span data-stu-id="39401-138">System.String</span></span>

### <span data-ttu-id="39401-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="39401-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="39401-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39401-140">OUTPUTS</span></span>

### <span data-ttu-id="39401-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39401-141">System.Boolean</span></span>

## <span data-ttu-id="39401-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39401-142">NOTES</span></span>

## <span data-ttu-id="39401-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39401-143">RELATED LINKS</span></span>
