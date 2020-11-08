---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186473"
---
# <span data-ttu-id="8bb63-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="8bb63-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="8bb63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8bb63-102">SYNOPSIS</span></span>

<span data-ttu-id="8bb63-103">A megadott adatbázis szinkronizálása az Analysis Services-kiszolgáló meghatározott példányán az Add-AzAnalysisServicesAccount parancsban megadott, a jelenleg bejelentkezett környezetben található összes lekérdezés scaleout-példányához</span><span class="sxs-lookup"><span data-stu-id="8bb63-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8bb63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8bb63-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bb63-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8bb63-105">DESCRIPTION</span></span>

<span data-ttu-id="8bb63-106">A Sync-AzAnalysisServicesInstance parancsmag az Analysis Services Server meghatározott példányának egy adott adatbázisát szinkronizálja az aktuálisan bejelentkezett scaleout-példányokkal az Add-AzAnalysisServicesAccount parancsban megadott módon.</span><span class="sxs-lookup"><span data-stu-id="8bb63-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8bb63-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8bb63-107">EXAMPLES</span></span>

### <span data-ttu-id="8bb63-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8bb63-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="8bb63-109">Ez a parancs szinkronizálja a SalesOrders nevű adatbázist a "contoso" nevű kiszolgálón a környezet westus.asazure.windows.net, feltéve, hogy a felhasználó bejelentkezett a környezetbe Add-AzAnalysisServicesAccount parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="8bb63-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="8bb63-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8bb63-110">PARAMETERS</span></span>

### <span data-ttu-id="8bb63-111">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="8bb63-111">-Database</span></span>

<span data-ttu-id="8bb63-112">A szinkronizálandó adatbázis identitása</span><span class="sxs-lookup"><span data-stu-id="8bb63-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="8bb63-113">-Példány</span><span class="sxs-lookup"><span data-stu-id="8bb63-113">-Instance</span></span>

<span data-ttu-id="8bb63-114">Az Analysis Services-kiszolgálópéldány újraindításának neve</span><span class="sxs-lookup"><span data-stu-id="8bb63-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="8bb63-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bb63-115">-PassThru</span></span>

<span data-ttu-id="8bb63-116">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="8bb63-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8bb63-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8bb63-117">-Confirm</span></span>
<span data-ttu-id="8bb63-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8bb63-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bb63-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bb63-119">-WhatIf</span></span>
<span data-ttu-id="8bb63-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8bb63-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8bb63-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8bb63-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bb63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb63-122">CommonParameters</span></span>
<span data-ttu-id="8bb63-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8bb63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb63-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bb63-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb63-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bb63-125">INPUTS</span></span>

### <span data-ttu-id="8bb63-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8bb63-126">System.String</span></span>

## <span data-ttu-id="8bb63-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bb63-127">OUTPUTS</span></span>

### <span data-ttu-id="8bb63-128">Microsoft. Azure. Command. AnalysisServices. Dataplane. models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="8bb63-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="8bb63-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8bb63-129">NOTES</span></span>

<span data-ttu-id="8bb63-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="8bb63-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="8bb63-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bb63-131">RELATED LINKS</span></span>