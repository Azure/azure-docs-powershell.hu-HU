---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: a75ae79722fed99ce96b0a082f4f56ace998354e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493593"
---
# <span data-ttu-id="59fcc-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="59fcc-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="59fcc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="59fcc-103">A megadott adatbázis szinkronizálása az Analysis Services-kiszolgáló meghatározott példányán az Add-AzureAnalysisServicesAccount parancsban megadott, a jelenleg bejelentkezett környezetben található összes lekérdezés scaleout-példányához</span><span class="sxs-lookup"><span data-stu-id="59fcc-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59fcc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59fcc-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59fcc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59fcc-105">DESCRIPTION</span></span>
<span data-ttu-id="59fcc-106">A Sync-AzureAnalysisServicesInstance parancsmag az Analysis Services Server meghatározott példányának egy adott adatbázisát szinkronizálja az aktuálisan bejelentkezett scaleout-példányokkal az Add-AzureAnalysisServicesAccount parancsban megadott módon.</span><span class="sxs-lookup"><span data-stu-id="59fcc-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="59fcc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59fcc-107">EXAMPLES</span></span>

### <span data-ttu-id="59fcc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="59fcc-108">Example 1</span></span>
```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="59fcc-109">Ez a parancs szinkronizálja a SalesOrders nevű adatbázist a "contoso" nevű kiszolgálón a környezet westus.asazure.windows.net, feltéve, hogy a felhasználó bejelentkezett erre a környezetre Add-AzureAnalysisServicesAccount parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="59fcc-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="59fcc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59fcc-110">PARAMETERS</span></span>

### <span data-ttu-id="59fcc-111">-Példány</span><span class="sxs-lookup"><span data-stu-id="59fcc-111">-Instance</span></span>
<span data-ttu-id="59fcc-112">Az Analysis Services-kiszolgálópéldány újraindításának neve</span><span class="sxs-lookup"><span data-stu-id="59fcc-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="59fcc-113">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="59fcc-113">-Database</span></span>
<span data-ttu-id="59fcc-114">A szinkronizálandó adatbázis identitása</span><span class="sxs-lookup"><span data-stu-id="59fcc-114">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="59fcc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59fcc-115">-PassThru</span></span>
<span data-ttu-id="59fcc-116">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="59fcc-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="59fcc-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59fcc-117">-Confirm</span></span>
<span data-ttu-id="59fcc-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59fcc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59fcc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59fcc-119">-WhatIf</span></span>
<span data-ttu-id="59fcc-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59fcc-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59fcc-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59fcc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59fcc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fcc-122">CommonParameters</span></span>
<span data-ttu-id="59fcc-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59fcc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fcc-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fcc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fcc-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59fcc-125">INPUTS</span></span>

## <span data-ttu-id="59fcc-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59fcc-126">OUTPUTS</span></span>

### <span data-ttu-id="59fcc-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59fcc-127">System.Boolean</span></span>

## <span data-ttu-id="59fcc-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59fcc-128">NOTES</span></span>
<span data-ttu-id="59fcc-129">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="59fcc-129">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="59fcc-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59fcc-130">RELATED LINKS</span></span>

