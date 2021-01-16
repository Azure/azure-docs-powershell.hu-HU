---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354977"
---
# <span data-ttu-id="131f2-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="131f2-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="131f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="131f2-102">SYNOPSIS</span></span>
<span data-ttu-id="131f2-103">Egy központi IoT-alkalmazást töröl.</span><span class="sxs-lookup"><span data-stu-id="131f2-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="131f2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="131f2-104">SYNTAX</span></span>

### <span data-ttu-id="131f2-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="131f2-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="131f2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="131f2-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="131f2-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="131f2-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="131f2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="131f2-108">DESCRIPTION</span></span>
<span data-ttu-id="131f2-109">Egy meglévő központi IoT-alkalmazást töröl.</span><span class="sxs-lookup"><span data-stu-id="131f2-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="131f2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="131f2-110">EXAMPLES</span></span>

### <span data-ttu-id="131f2-111">Example 1 Delete and IoT Central Application</span><span class="sxs-lookup"><span data-stu-id="131f2-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="131f2-112">A megadott Központi IoT-alkalmazás törlése.</span><span class="sxs-lookup"><span data-stu-id="131f2-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="131f2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="131f2-113">PARAMETERS</span></span>

### <span data-ttu-id="131f2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="131f2-114">-AsJob</span></span>
<span data-ttu-id="131f2-115">Futtassa a parancsmagot feladatként a háttérben.</span><span class="sxs-lookup"><span data-stu-id="131f2-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="131f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131f2-116">-DefaultProfile</span></span>
<span data-ttu-id="131f2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="131f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="131f2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="131f2-118">-InputObject</span></span>
<span data-ttu-id="131f2-119">Iot Central Application Input Object.</span><span class="sxs-lookup"><span data-stu-id="131f2-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="131f2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="131f2-120">-Name</span></span>
<span data-ttu-id="131f2-121">Az Iot Központi alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="131f2-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="131f2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="131f2-122">-PassThru</span></span>
<span data-ttu-id="131f2-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="131f2-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="131f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="131f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="131f2-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="131f2-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="131f2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="131f2-126">-ResourceId</span></span>
<span data-ttu-id="131f2-127">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="131f2-127">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="131f2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="131f2-128">-Confirm</span></span>
<span data-ttu-id="131f2-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="131f2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="131f2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="131f2-130">-WhatIf</span></span>
<span data-ttu-id="131f2-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="131f2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="131f2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="131f2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="131f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131f2-133">CommonParameters</span></span>
<span data-ttu-id="131f2-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="131f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131f2-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="131f2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131f2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="131f2-136">INPUTS</span></span>

### <span data-ttu-id="131f2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="131f2-137">System.String</span></span>

### <span data-ttu-id="131f2-138">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="131f2-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="131f2-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="131f2-139">OUTPUTS</span></span>

### <span data-ttu-id="131f2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="131f2-140">System.Boolean</span></span>

## <span data-ttu-id="131f2-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="131f2-141">NOTES</span></span>

## <span data-ttu-id="131f2-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="131f2-142">RELATED LINKS</span></span>
