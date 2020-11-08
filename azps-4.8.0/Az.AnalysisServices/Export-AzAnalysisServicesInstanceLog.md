---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018023"
---
# <span data-ttu-id="a8d22-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="a8d22-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="a8d22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8d22-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d22-103">Napló exportálása az Analysis Services Server egy példányáról az aktuálisan bejelentkezett környezetben, az Add-AzAnalysisServicesAccount parancsban megadott módon</span><span class="sxs-lookup"><span data-stu-id="a8d22-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="a8d22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8d22-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8d22-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8d22-105">DESCRIPTION</span></span>
<span data-ttu-id="a8d22-106">A Export-AzAnalysisServicesInstance parancsmag az Azure Analysis Services-kiszolgáló egy példányára exportálja a naplót fájlba</span><span class="sxs-lookup"><span data-stu-id="a8d22-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="a8d22-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8d22-107">EXAMPLES</span></span>

### <span data-ttu-id="a8d22-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a8d22-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="a8d22-109">Ez a parancs az Add-AzAnalysisServicesAccount parancsban megadott környezetben a "TestServer" kiszolgálóról exportálja a naplót, és a OutputPath "C:\path\to\log\testserver.log" mezőben megadott fájlba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="a8d22-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="a8d22-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8d22-110">PARAMETERS</span></span>

### <span data-ttu-id="a8d22-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a8d22-111">-Force</span></span>
<span data-ttu-id="a8d22-112">Fájl felülírása, ha a kérés nélkül létezik</span><span class="sxs-lookup"><span data-stu-id="a8d22-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="a8d22-113">-Példány</span><span class="sxs-lookup"><span data-stu-id="a8d22-113">-Instance</span></span>
<span data-ttu-id="a8d22-114">Az Analysis Services-kiszolgálópéldány neve</span><span class="sxs-lookup"><span data-stu-id="a8d22-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="a8d22-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="a8d22-115">-OutputPath</span></span>
<span data-ttu-id="a8d22-116">A naplófájl exportálására szolgáló kimeneti útvonal</span><span class="sxs-lookup"><span data-stu-id="a8d22-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="a8d22-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8d22-117">-PassThru</span></span>
<span data-ttu-id="a8d22-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a8d22-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a8d22-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8d22-119">-Confirm</span></span>
<span data-ttu-id="a8d22-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8d22-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8d22-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8d22-121">-WhatIf</span></span>
<span data-ttu-id="a8d22-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8d22-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8d22-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8d22-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8d22-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d22-124">CommonParameters</span></span>
<span data-ttu-id="a8d22-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8d22-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d22-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8d22-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d22-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8d22-127">INPUTS</span></span>

### <span data-ttu-id="a8d22-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="a8d22-128">None</span></span>

## <span data-ttu-id="a8d22-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8d22-129">OUTPUTS</span></span>

### <span data-ttu-id="a8d22-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="a8d22-130">System.Void</span></span>

## <span data-ttu-id="a8d22-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8d22-131">NOTES</span></span>
<span data-ttu-id="a8d22-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="a8d22-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="a8d22-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8d22-133">RELATED LINKS</span></span>
