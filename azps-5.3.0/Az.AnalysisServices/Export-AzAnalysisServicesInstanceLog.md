---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479093"
---
# <span data-ttu-id="e7fa4-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="e7fa4-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="e7fa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fa4-103">Napló exportálása az Analysis Services-kiszolgáló egy példányából az aktuálisan naplózott környezetben a Add-AzAnalysisServicesAccount szerint</span><span class="sxs-lookup"><span data-stu-id="e7fa4-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="e7fa4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7fa4-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7fa4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7fa4-105">DESCRIPTION</span></span>
<span data-ttu-id="e7fa4-106">A Export-AzAnalysisServicesInstance parancsmag exportálja a naplót az Azure Analysis Services-kiszolgáló egy példányából a fájlba</span><span class="sxs-lookup"><span data-stu-id="e7fa4-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="e7fa4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7fa4-107">EXAMPLES</span></span>

### <span data-ttu-id="e7fa4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e7fa4-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="e7fa4-109">Ez a parancs exportálja a naplót a kiszolgáló "testserver" kiszolgálóról a Add-AzAnalysisServicesAccount-parancsban megadott környezetből, és menti az OutputPath 'C:\path\to\log\testserver.log' mappában megadott fájlba.</span><span class="sxs-lookup"><span data-stu-id="e7fa4-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="e7fa4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7fa4-110">PARAMETERS</span></span>

### <span data-ttu-id="e7fa4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e7fa4-111">-Force</span></span>
<span data-ttu-id="e7fa4-112">Fájl felülírása, ha van rá kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="e7fa4-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="e7fa4-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="e7fa4-113">-Instance</span></span>
<span data-ttu-id="e7fa4-114">Az Analysis Services kiszolgálói példányának neve</span><span class="sxs-lookup"><span data-stu-id="e7fa4-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7fa4-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e7fa4-115">-OutputPath</span></span>
<span data-ttu-id="e7fa4-116">Az exportálni kívánt fájl kimeneti útvonala</span><span class="sxs-lookup"><span data-stu-id="e7fa4-116">Output path to file to export log</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7fa4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7fa4-117">-PassThru</span></span>
<span data-ttu-id="e7fa4-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e7fa4-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e7fa4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7fa4-119">-Confirm</span></span>
<span data-ttu-id="e7fa4-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e7fa4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7fa4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7fa4-121">-WhatIf</span></span>
<span data-ttu-id="e7fa4-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e7fa4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7fa4-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7fa4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7fa4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fa4-124">CommonParameters</span></span>
<span data-ttu-id="e7fa4-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7fa4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fa4-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7fa4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fa4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7fa4-127">INPUTS</span></span>

### <span data-ttu-id="e7fa4-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="e7fa4-128">None</span></span>

## <span data-ttu-id="e7fa4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7fa4-129">OUTPUTS</span></span>

### <span data-ttu-id="e7fa4-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="e7fa4-130">System.Void</span></span>

## <span data-ttu-id="e7fa4-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7fa4-131">NOTES</span></span>
<span data-ttu-id="e7fa4-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="e7fa4-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="e7fa4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7fa4-133">RELATED LINKS</span></span>
