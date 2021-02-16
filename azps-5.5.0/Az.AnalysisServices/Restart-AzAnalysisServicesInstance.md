---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149634"
---
# <span data-ttu-id="b846b-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="b846b-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="b846b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b846b-102">SYNOPSIS</span></span>
<span data-ttu-id="b846b-103">Újraindítja az Analysis Services-kiszolgáló egy példányát az aktuálisan bejelentkezett környezetben, az Add-AzAnalysisServicesAccount parancsnak Add-AzAnalysisServicesAccount szerint</span><span class="sxs-lookup"><span data-stu-id="b846b-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="b846b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b846b-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b846b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b846b-105">DESCRIPTION</span></span>
<span data-ttu-id="b846b-106">A Restart-AzAnalysisServicesInstance parancsmag újraindítja az Azure Analysis Services-kiszolgáló egy példányát</span><span class="sxs-lookup"><span data-stu-id="b846b-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="b846b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b846b-107">EXAMPLES</span></span>

### <span data-ttu-id="b846b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b846b-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="b846b-109">Ez a parancs újraindítja a kiszolgáló "testserver" kiszolgálóját a Add-AzAnalysisServicesAccount környezetben</span><span class="sxs-lookup"><span data-stu-id="b846b-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="b846b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b846b-110">PARAMETERS</span></span>

### <span data-ttu-id="b846b-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="b846b-111">-Instance</span></span>
<span data-ttu-id="b846b-112">Az újraindítani szükséges Analysis Services-kiszolgálói példány neve</span><span class="sxs-lookup"><span data-stu-id="b846b-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="b846b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b846b-113">-PassThru</span></span>
<span data-ttu-id="b846b-114">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="b846b-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b846b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b846b-115">-Confirm</span></span>
<span data-ttu-id="b846b-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b846b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b846b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b846b-117">-WhatIf</span></span>
<span data-ttu-id="b846b-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b846b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b846b-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b846b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b846b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b846b-120">CommonParameters</span></span>
<span data-ttu-id="b846b-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b846b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b846b-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b846b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b846b-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b846b-123">INPUTS</span></span>

### <span data-ttu-id="b846b-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="b846b-124">None</span></span>

## <span data-ttu-id="b846b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b846b-125">OUTPUTS</span></span>

### <span data-ttu-id="b846b-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b846b-126">System.Boolean</span></span>

## <span data-ttu-id="b846b-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b846b-127">NOTES</span></span>
<span data-ttu-id="b846b-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="b846b-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="b846b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b846b-129">RELATED LINKS</span></span>
