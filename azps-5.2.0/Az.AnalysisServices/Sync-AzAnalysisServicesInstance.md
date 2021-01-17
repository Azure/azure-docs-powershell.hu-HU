---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345629"
---
# <span data-ttu-id="031b6-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="031b6-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="031b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="031b6-102">SYNOPSIS</span></span>

<span data-ttu-id="031b6-103">Szinkronizál egy megadott adatbázist az Analysis Services-kiszolgáló adott példányában az aktuálisan naplózott környezet összes lekérdezési méretkorlátpéldányával a Add-AzAnalysisServicesAccount parancsban megadottak szerint</span><span class="sxs-lookup"><span data-stu-id="031b6-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="031b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="031b6-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="031b6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="031b6-105">DESCRIPTION</span></span>

<span data-ttu-id="031b6-106">A Sync-AzAnalysisServicesInstance parancsmag szinkronizálja az Analysis Services-kiszolgáló adott példányában lévő megadott adatbázist az aktuálisan bejelentkezett környezet összes lekérdezési méretkorlátpéldányával, az Add-AzAnalysisServicesAccount parancsban megadottak szerint.</span><span class="sxs-lookup"><span data-stu-id="031b6-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="031b6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="031b6-107">EXAMPLES</span></span>

### <span data-ttu-id="031b6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="031b6-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="031b6-109">Ez a parancs szinkronizálja a "contoso" nevű kiszolgáló SalesOrders nevű adatbázisát westus.asazure.windows.net feltéve, hogy a felhasználó bejelentkezett ebbe a környezetbe egy Add-AzAnalysisServicesAccount paranccsal.</span><span class="sxs-lookup"><span data-stu-id="031b6-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="031b6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="031b6-110">PARAMETERS</span></span>

### <span data-ttu-id="031b6-111">-Database</span><span class="sxs-lookup"><span data-stu-id="031b6-111">-Database</span></span>

<span data-ttu-id="031b6-112">A szinkronizálni kíván adatbázis identitása</span><span class="sxs-lookup"><span data-stu-id="031b6-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="031b6-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="031b6-113">-Instance</span></span>

<span data-ttu-id="031b6-114">Az újraindítani szükséges Analysis Services-kiszolgálói példány neve</span><span class="sxs-lookup"><span data-stu-id="031b6-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="031b6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="031b6-115">-PassThru</span></span>

<span data-ttu-id="031b6-116">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="031b6-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="031b6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="031b6-117">-Confirm</span></span>
<span data-ttu-id="031b6-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="031b6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="031b6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="031b6-119">-WhatIf</span></span>
<span data-ttu-id="031b6-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="031b6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="031b6-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="031b6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="031b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="031b6-122">CommonParameters</span></span>
<span data-ttu-id="031b6-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="031b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="031b6-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="031b6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="031b6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="031b6-125">INPUTS</span></span>

### <span data-ttu-id="031b6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="031b6-126">System.String</span></span>

## <span data-ttu-id="031b6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="031b6-127">OUTPUTS</span></span>

### <span data-ttu-id="031b6-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="031b6-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="031b6-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="031b6-129">NOTES</span></span>

<span data-ttu-id="031b6-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="031b6-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="031b6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="031b6-131">RELATED LINKS</span></span>
