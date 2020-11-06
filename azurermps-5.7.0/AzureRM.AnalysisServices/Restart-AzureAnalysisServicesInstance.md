---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 0a89ee592e6f6f6d4d9e56df6d7e4df32b010524
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496692"
---
# <span data-ttu-id="66950-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="66950-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="66950-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66950-102">SYNOPSIS</span></span>
<span data-ttu-id="66950-103">Az Analysis Services Server példányának újraindítása az aktuálisan bejelentkezett környezetben, az Add-AzureAnalysisServicesAccount parancsban megadott módon</span><span class="sxs-lookup"><span data-stu-id="66950-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66950-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66950-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="66950-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66950-105">DESCRIPTION</span></span>
<span data-ttu-id="66950-106">Az Restart-AzureAnalysisServicesInstance parancsmag az Azure Analysis Services-kiszolgáló egy példányát indítja el újra</span><span class="sxs-lookup"><span data-stu-id="66950-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="66950-107">Példák</span><span class="sxs-lookup"><span data-stu-id="66950-107">EXAMPLES</span></span>

### <span data-ttu-id="66950-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="66950-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="66950-109">Ez a parancs elindítja a "TestServer" szervert a Add-AzureAnalysisServicesAccount parancsban megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="66950-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="66950-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66950-110">PARAMETERS</span></span>

### <span data-ttu-id="66950-111">-Példány</span><span class="sxs-lookup"><span data-stu-id="66950-111">-Instance</span></span>
<span data-ttu-id="66950-112">Az Analysis Services-kiszolgálópéldány újraindításának neve</span><span class="sxs-lookup"><span data-stu-id="66950-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="66950-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66950-113">-PassThru</span></span>
<span data-ttu-id="66950-114">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="66950-114">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66950-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="66950-115">-Confirm</span></span>
<span data-ttu-id="66950-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="66950-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66950-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66950-117">-WhatIf</span></span>
<span data-ttu-id="66950-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="66950-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66950-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66950-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="66950-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66950-120">INPUTS</span></span>

### <span data-ttu-id="66950-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="66950-121">None</span></span>
<span data-ttu-id="66950-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="66950-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66950-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66950-123">OUTPUTS</span></span>

### <span data-ttu-id="66950-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66950-124">System.Boolean</span></span>

## <span data-ttu-id="66950-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66950-125">NOTES</span></span>
<span data-ttu-id="66950-126">Alias: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="66950-126">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="66950-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66950-127">RELATED LINKS</span></span>

