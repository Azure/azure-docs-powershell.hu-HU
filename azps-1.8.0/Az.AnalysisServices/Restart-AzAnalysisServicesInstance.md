---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 623b7c84b29e5e64a47beeff6c9f7dba88edf32b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665726"
---
# <span data-ttu-id="402ac-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="402ac-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="402ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="402ac-102">SYNOPSIS</span></span>
<span data-ttu-id="402ac-103">Az Analysis Services Server példányának újraindítása az aktuálisan bejelentkezett környezetben, az Add-AzAnalysisServicesAccount parancsban megadott módon</span><span class="sxs-lookup"><span data-stu-id="402ac-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="402ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="402ac-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="402ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="402ac-105">DESCRIPTION</span></span>
<span data-ttu-id="402ac-106">Az Restart-AzAnalysisServicesInstance parancsmag az Azure Analysis Services-kiszolgáló egy példányát indítja el újra</span><span class="sxs-lookup"><span data-stu-id="402ac-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="402ac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="402ac-107">EXAMPLES</span></span>

### <span data-ttu-id="402ac-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="402ac-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="402ac-109">Ez a parancs elindítja a "TestServer" szervert a Add-AzAnalysisServicesAccount parancsban megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="402ac-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="402ac-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="402ac-110">PARAMETERS</span></span>

### <span data-ttu-id="402ac-111">-Példány</span><span class="sxs-lookup"><span data-stu-id="402ac-111">-Instance</span></span>
<span data-ttu-id="402ac-112">Az Analysis Services-kiszolgálópéldány újraindításának neve</span><span class="sxs-lookup"><span data-stu-id="402ac-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="402ac-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="402ac-113">-PassThru</span></span>
<span data-ttu-id="402ac-114">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="402ac-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="402ac-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="402ac-115">-Confirm</span></span>
<span data-ttu-id="402ac-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="402ac-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="402ac-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="402ac-117">-WhatIf</span></span>
<span data-ttu-id="402ac-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="402ac-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="402ac-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="402ac-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="402ac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402ac-120">CommonParameters</span></span>
<span data-ttu-id="402ac-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="402ac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="402ac-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="402ac-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402ac-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="402ac-123">INPUTS</span></span>

### <span data-ttu-id="402ac-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="402ac-124">None</span></span>

## <span data-ttu-id="402ac-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="402ac-125">OUTPUTS</span></span>

### <span data-ttu-id="402ac-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="402ac-126">System.Boolean</span></span>

## <span data-ttu-id="402ac-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="402ac-127">NOTES</span></span>
<span data-ttu-id="402ac-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="402ac-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="402ac-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="402ac-129">RELATED LINKS</span></span>
