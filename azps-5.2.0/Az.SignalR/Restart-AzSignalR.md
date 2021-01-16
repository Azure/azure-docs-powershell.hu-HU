---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340434"
---
# <span data-ttu-id="d108e-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="d108e-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="d108e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d108e-102">SYNOPSIS</span></span>
<span data-ttu-id="d108e-103">Indítsa újra a SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d108e-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="d108e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d108e-104">SYNTAX</span></span>

### <span data-ttu-id="d108e-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d108e-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d108e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d108e-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d108e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d108e-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d108e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d108e-108">DESCRIPTION</span></span>
<span data-ttu-id="d108e-109">Indítsa újra a SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d108e-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="d108e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d108e-110">EXAMPLES</span></span>

### <span data-ttu-id="d108e-111">Adott SignalR-szolgáltatás újraindítása</span><span class="sxs-lookup"><span data-stu-id="d108e-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="d108e-112">Az alapértelmezett erőforráscsoportot a \` Set-AzDefault -ResourceGroupName myResourceGroup állíthatja \` be.</span><span class="sxs-lookup"><span data-stu-id="d108e-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="d108e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d108e-113">PARAMETERS</span></span>

### <span data-ttu-id="d108e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d108e-114">-AsJob</span></span>
<span data-ttu-id="d108e-115">Futtassa a parancsmagot a háttérben futó feladatban.</span><span class="sxs-lookup"><span data-stu-id="d108e-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="d108e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d108e-116">-DefaultProfile</span></span>
<span data-ttu-id="d108e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d108e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d108e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d108e-118">-InputObject</span></span>
<span data-ttu-id="d108e-119">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="d108e-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d108e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d108e-120">-Name</span></span>
<span data-ttu-id="d108e-121">A SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="d108e-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="d108e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d108e-122">-PassThru</span></span>
<span data-ttu-id="d108e-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="d108e-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d108e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d108e-124">-ResourceGroupName</span></span>
<span data-ttu-id="d108e-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d108e-125">The resource group name.</span></span>
<span data-ttu-id="d108e-126">Ha nincs megadva, a program az alapértelmezett beállítást használja.</span><span class="sxs-lookup"><span data-stu-id="d108e-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="d108e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d108e-127">-ResourceId</span></span>
<span data-ttu-id="d108e-128">A SignalR szolgáltatás erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="d108e-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d108e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d108e-129">-Confirm</span></span>
<span data-ttu-id="d108e-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d108e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d108e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d108e-131">-WhatIf</span></span>
<span data-ttu-id="d108e-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d108e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d108e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d108e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d108e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d108e-134">CommonParameters</span></span>
<span data-ttu-id="d108e-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d108e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d108e-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d108e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d108e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d108e-137">INPUTS</span></span>

### <span data-ttu-id="d108e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d108e-138">System.String</span></span>

### <span data-ttu-id="d108e-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d108e-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="d108e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d108e-140">OUTPUTS</span></span>

### <span data-ttu-id="d108e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d108e-141">System.Boolean</span></span>

## <span data-ttu-id="d108e-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d108e-142">NOTES</span></span>

## <span data-ttu-id="d108e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d108e-143">RELATED LINKS</span></span>
