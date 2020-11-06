---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493797"
---
# <span data-ttu-id="bd984-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="bd984-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="bd984-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd984-102">SYNOPSIS</span></span>

<span data-ttu-id="bd984-103">A megadott adatbázis szinkronizálása az Analysis Services-kiszolgáló meghatározott példányán az Add-AzureAnalysisServicesAccount parancsban megadott, a jelenleg bejelentkezett környezetben található összes lekérdezés scaleout-példányához</span><span class="sxs-lookup"><span data-stu-id="bd984-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd984-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd984-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## <span data-ttu-id="bd984-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd984-105">DESCRIPTION</span></span>

<span data-ttu-id="bd984-106">A Sync-AzureAnalysisServicesInstance parancsmag az Analysis Services Server meghatározott példányának egy adott adatbázisát szinkronizálja az aktuálisan bejelentkezett scaleout-példányokkal az Add-AzureAnalysisServicesAccount parancsban megadott módon.</span><span class="sxs-lookup"><span data-stu-id="bd984-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="bd984-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bd984-107">EXAMPLES</span></span>

### <span data-ttu-id="bd984-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bd984-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="bd984-109">Ez a parancs szinkronizálja a SalesOrders nevű adatbázist a "contoso" nevű kiszolgálón a környezet westus.asazure.windows.net, feltéve, hogy a felhasználó bejelentkezett erre a környezetre Add-AzureAnalysisServicesAccount parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="bd984-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="bd984-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd984-110">PARAMETERS</span></span>

### <span data-ttu-id="bd984-111">-Példány</span><span class="sxs-lookup"><span data-stu-id="bd984-111">-Instance</span></span>

<span data-ttu-id="bd984-112">Az Analysis Services-kiszolgálópéldány újraindításának neve</span><span class="sxs-lookup"><span data-stu-id="bd984-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd984-113">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="bd984-113">-Database</span></span>

<span data-ttu-id="bd984-114">A szinkronizálandó adatbázis identitása</span><span class="sxs-lookup"><span data-stu-id="bd984-114">Identity of the database to be synchronized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd984-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd984-115">-PassThru</span></span>

<span data-ttu-id="bd984-116">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="bd984-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="bd984-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd984-117">INPUTS</span></span>

### <span data-ttu-id="bd984-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="bd984-118">None</span></span>
<span data-ttu-id="bd984-119">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bd984-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd984-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd984-120">OUTPUTS</span></span>

### <span data-ttu-id="bd984-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd984-121">System.Boolean</span></span>

## <span data-ttu-id="bd984-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd984-122">NOTES</span></span>

<span data-ttu-id="bd984-123">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="bd984-123">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="bd984-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd984-124">RELATED LINKS</span></span>
