---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: ad827cece73c4ad3add34312befc2f9ae99ca984
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668168"
---
# <span data-ttu-id="c9d44-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="c9d44-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="c9d44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9d44-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d44-103">Napló exportálása az Analysis Services Server egy példányáról az aktuálisan bejelentkezett környezetben, az Add-AzAnalysisServicesAccount parancsban megadott módon</span><span class="sxs-lookup"><span data-stu-id="c9d44-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c9d44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9d44-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9d44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9d44-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d44-106">A Export-AzAnalysisServicesInstance parancsmag az Azure Analysis Services-kiszolgáló egy példányára exportálja a naplót fájlba</span><span class="sxs-lookup"><span data-stu-id="c9d44-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="c9d44-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9d44-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d44-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c9d44-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="c9d44-109">Ez a parancs az Add-AzAnalysisServicesAccount parancsban megadott környezetben a "TestServer" kiszolgálóról exportálja a naplót, és a OutputPath "C:\path\to\log\testserver.log" mezőben megadott fájlba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="c9d44-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="c9d44-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9d44-110">PARAMETERS</span></span>

### <span data-ttu-id="c9d44-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c9d44-111">-Force</span></span>
<span data-ttu-id="c9d44-112">Fájl felülírása, ha a kérés nélkül létezik</span><span class="sxs-lookup"><span data-stu-id="c9d44-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="c9d44-113">-Példány</span><span class="sxs-lookup"><span data-stu-id="c9d44-113">-Instance</span></span>
<span data-ttu-id="c9d44-114">Az Analysis Services-kiszolgálópéldány neve</span><span class="sxs-lookup"><span data-stu-id="c9d44-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="c9d44-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c9d44-115">-OutputPath</span></span>
<span data-ttu-id="c9d44-116">A naplófájl exportálására szolgáló kimeneti útvonal</span><span class="sxs-lookup"><span data-stu-id="c9d44-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="c9d44-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9d44-117">-PassThru</span></span>
<span data-ttu-id="c9d44-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c9d44-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c9d44-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9d44-119">-Confirm</span></span>
<span data-ttu-id="c9d44-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9d44-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9d44-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d44-121">-WhatIf</span></span>
<span data-ttu-id="c9d44-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9d44-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9d44-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9d44-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9d44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d44-124">CommonParameters</span></span>
<span data-ttu-id="c9d44-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9d44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d44-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d44-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d44-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9d44-127">INPUTS</span></span>

### <span data-ttu-id="c9d44-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="c9d44-128">None</span></span>

## <span data-ttu-id="c9d44-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9d44-129">OUTPUTS</span></span>

### <span data-ttu-id="c9d44-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="c9d44-130">System.Void</span></span>

## <span data-ttu-id="c9d44-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9d44-131">NOTES</span></span>
<span data-ttu-id="c9d44-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="c9d44-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="c9d44-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9d44-133">RELATED LINKS</span></span>
