---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 732eb92a46fa7e69ba5274398de648c16142ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492948"
---
# <span data-ttu-id="bfaad-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="bfaad-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="bfaad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bfaad-102">SYNOPSIS</span></span>

<span data-ttu-id="bfaad-103">A megadott adatbázis szinkronizálása az Analysis Services-kiszolgáló meghatározott példányán az Add-AzureAnalysisServicesAccount parancsban megadott, a jelenleg bejelentkezett környezetben található összes lekérdezés scaleout-példányához</span><span class="sxs-lookup"><span data-stu-id="bfaad-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfaad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bfaad-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bfaad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bfaad-105">DESCRIPTION</span></span>

<span data-ttu-id="bfaad-106">A Sync-AzureAnalysisServicesInstance parancsmag az Analysis Services Server meghatározott példányának egy adott adatbázisát szinkronizálja az aktuálisan bejelentkezett scaleout-példányokkal az Add-AzureAnalysisServicesAccount parancsban megadott módon.</span><span class="sxs-lookup"><span data-stu-id="bfaad-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="bfaad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bfaad-107">EXAMPLES</span></span>

### <span data-ttu-id="bfaad-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bfaad-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="bfaad-109">Ez a parancs szinkronizálja a SalesOrders nevű adatbázist a "contoso" nevű kiszolgálón a környezet westus.asazure.windows.net, feltéve, hogy a felhasználó bejelentkezett erre a környezetre Add-AzureAnalysisServicesAccount parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="bfaad-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="bfaad-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bfaad-110">PARAMETERS</span></span>

### <span data-ttu-id="bfaad-111">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="bfaad-111">-Database</span></span>

<span data-ttu-id="bfaad-112">A szinkronizálandó adatbázis identitása</span><span class="sxs-lookup"><span data-stu-id="bfaad-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="bfaad-113">-Példány</span><span class="sxs-lookup"><span data-stu-id="bfaad-113">-Instance</span></span>

<span data-ttu-id="bfaad-114">Az Analysis Services-kiszolgálópéldány újraindításának neve</span><span class="sxs-lookup"><span data-stu-id="bfaad-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="bfaad-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfaad-115">-PassThru</span></span>

<span data-ttu-id="bfaad-116">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="bfaad-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="bfaad-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bfaad-117">-Confirm</span></span>
<span data-ttu-id="bfaad-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bfaad-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfaad-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfaad-119">-WhatIf</span></span>
<span data-ttu-id="bfaad-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bfaad-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfaad-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfaad-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfaad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfaad-122">CommonParameters</span></span>
<span data-ttu-id="bfaad-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bfaad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfaad-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfaad-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfaad-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfaad-125">INPUTS</span></span>

### <span data-ttu-id="bfaad-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bfaad-126">System.String</span></span>
<span data-ttu-id="bfaad-127">Paraméterek: Database (ByValue), instance (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bfaad-127">Parameters: Database (ByValue), Instance (ByValue)</span></span>

## <span data-ttu-id="bfaad-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfaad-128">OUTPUTS</span></span>

### <span data-ttu-id="bfaad-129">Microsoft. Azure. Command. AnalysisServices. Dataplane. models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="bfaad-129">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="bfaad-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bfaad-130">NOTES</span></span>

<span data-ttu-id="bfaad-131">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="bfaad-131">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="bfaad-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfaad-132">RELATED LINKS</span></span>
