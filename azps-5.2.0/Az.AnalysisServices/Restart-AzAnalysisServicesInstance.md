---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352925"
---
# <span data-ttu-id="f3910-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="f3910-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="f3910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3910-102">SYNOPSIS</span></span>
<span data-ttu-id="f3910-103">Újraindítja az Analysis Services-kiszolgáló egy példányát az aktuálisan bejelentkezett környezetben, az Add-AzAnalysisServicesAccount parancsnak Add-AzAnalysisServicesAccount szerint</span><span class="sxs-lookup"><span data-stu-id="f3910-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="f3910-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3910-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3910-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3910-105">DESCRIPTION</span></span>
<span data-ttu-id="f3910-106">A Restart-AzAnalysisServicesInstance parancsmag újraindítja az Azure Analysis Services-kiszolgáló egy példányát</span><span class="sxs-lookup"><span data-stu-id="f3910-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="f3910-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3910-107">EXAMPLES</span></span>

### <span data-ttu-id="f3910-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f3910-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="f3910-109">Ez a parancs újraindítja a kiszolgáló "testserver" kiszolgálóját a Add-AzAnalysisServicesAccount környezetben</span><span class="sxs-lookup"><span data-stu-id="f3910-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="f3910-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3910-110">PARAMETERS</span></span>

### <span data-ttu-id="f3910-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="f3910-111">-Instance</span></span>
<span data-ttu-id="f3910-112">Az újraindítani szükséges Analysis Services-kiszolgálói példány neve</span><span class="sxs-lookup"><span data-stu-id="f3910-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="f3910-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3910-113">-PassThru</span></span>
<span data-ttu-id="f3910-114">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="f3910-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f3910-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3910-115">-Confirm</span></span>
<span data-ttu-id="f3910-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3910-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3910-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3910-117">-WhatIf</span></span>
<span data-ttu-id="f3910-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3910-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3910-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3910-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3910-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3910-120">CommonParameters</span></span>
<span data-ttu-id="f3910-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3910-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3910-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3910-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3910-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3910-123">INPUTS</span></span>

### <span data-ttu-id="f3910-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="f3910-124">None</span></span>

## <span data-ttu-id="f3910-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3910-125">OUTPUTS</span></span>

### <span data-ttu-id="f3910-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3910-126">System.Boolean</span></span>

## <span data-ttu-id="f3910-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3910-127">NOTES</span></span>
<span data-ttu-id="f3910-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="f3910-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="f3910-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3910-129">RELATED LINKS</span></span>
