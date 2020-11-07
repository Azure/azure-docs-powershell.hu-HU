---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 2c7162f5a93c112a3f67b308941b56b698792fa3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668147"
---
# <span data-ttu-id="6dda4-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="6dda4-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="6dda4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6dda4-102">SYNOPSIS</span></span>

<span data-ttu-id="6dda4-103">A megadott adatbázis szinkronizálása az Analysis Services-kiszolgáló meghatározott példányán az Add-AzAnalysisServicesAccount parancsban megadott, a jelenleg bejelentkezett környezetben található összes lekérdezés scaleout-példányához</span><span class="sxs-lookup"><span data-stu-id="6dda4-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="6dda4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6dda4-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6dda4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6dda4-105">DESCRIPTION</span></span>

<span data-ttu-id="6dda4-106">A Sync-AzAnalysisServicesInstance parancsmag az Analysis Services Server meghatározott példányának egy adott adatbázisát szinkronizálja az aktuálisan bejelentkezett scaleout-példányokkal az Add-AzAnalysisServicesAccount parancsban megadott módon.</span><span class="sxs-lookup"><span data-stu-id="6dda4-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="6dda4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6dda4-107">EXAMPLES</span></span>

### <span data-ttu-id="6dda4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6dda4-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="6dda4-109">Ez a parancs szinkronizálja a SalesOrders nevű adatbázist a "contoso" nevű kiszolgálón a környezet westus.asazure.windows.net, feltéve, hogy a felhasználó bejelentkezett a környezetbe Add-AzAnalysisServicesAccount parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="6dda4-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="6dda4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6dda4-110">PARAMETERS</span></span>

### <span data-ttu-id="6dda4-111">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="6dda4-111">-Database</span></span>

<span data-ttu-id="6dda4-112">A szinkronizálandó adatbázis identitása</span><span class="sxs-lookup"><span data-stu-id="6dda4-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dda4-113">-Példány</span><span class="sxs-lookup"><span data-stu-id="6dda4-113">-Instance</span></span>

<span data-ttu-id="6dda4-114">Az Analysis Services-kiszolgálópéldány újraindításának neve</span><span class="sxs-lookup"><span data-stu-id="6dda4-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="6dda4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dda4-115">-PassThru</span></span>

<span data-ttu-id="6dda4-116">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="6dda4-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6dda4-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6dda4-117">-Confirm</span></span>
<span data-ttu-id="6dda4-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6dda4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dda4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dda4-119">-WhatIf</span></span>
<span data-ttu-id="6dda4-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6dda4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dda4-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6dda4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dda4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dda4-122">CommonParameters</span></span>
<span data-ttu-id="6dda4-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6dda4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dda4-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dda4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dda4-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6dda4-125">INPUTS</span></span>

### <span data-ttu-id="6dda4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6dda4-126">System.String</span></span>

## <span data-ttu-id="6dda4-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6dda4-127">OUTPUTS</span></span>

### <span data-ttu-id="6dda4-128">Microsoft. Azure. Command. AnalysisServices. Dataplane. models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="6dda4-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="6dda4-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6dda4-129">NOTES</span></span>

<span data-ttu-id="6dda4-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="6dda4-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="6dda4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6dda4-131">RELATED LINKS</span></span>
