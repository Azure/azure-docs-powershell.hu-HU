---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: c5ffd95cb3bd5e902e2e9edadfa9c96dd441c744
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922226"
---
# <span data-ttu-id="8e495-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="8e495-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="8e495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e495-102">SYNOPSIS</span></span>

<span data-ttu-id="8e495-103">Szinkronizál egy megadott adatbázist az Analysis Services-kiszolgáló adott példányában az aktuálisan naplózott környezet összes lekérdezési méretkorlát-példányával a Add-AzAnalysisServicesAccount parancsban megadottak szerint</span><span class="sxs-lookup"><span data-stu-id="8e495-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8e495-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e495-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e495-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e495-105">DESCRIPTION</span></span>

<span data-ttu-id="8e495-106">A Sync-AzAnalysisServicesInstance parancsmag szinkronizálja az Analysis Services-kiszolgáló adott példányában lévő megadott adatbázist az aktuálisan bejelentkezett környezet összes lekérdezési méretkorlátpéldányával, az Add-AzAnalysisServicesAccount parancsban megadottak szerint.</span><span class="sxs-lookup"><span data-stu-id="8e495-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8e495-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e495-107">EXAMPLES</span></span>

### <span data-ttu-id="8e495-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8e495-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="8e495-109">Ez a parancs szinkronizálja a "contoso" nevű kiszolgáló SalesOrders nevű adatbázisát westus.asazure.windows.net feltéve, hogy a felhasználó bejelentkezett ebbe a környezetbe egy Add-AzAnalysisServicesAccount paranccsal.</span><span class="sxs-lookup"><span data-stu-id="8e495-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="8e495-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e495-110">PARAMETERS</span></span>

### <span data-ttu-id="8e495-111">-Database</span><span class="sxs-lookup"><span data-stu-id="8e495-111">-Database</span></span>

<span data-ttu-id="8e495-112">A szinkronizálni kíván adatbázis identitása</span><span class="sxs-lookup"><span data-stu-id="8e495-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="8e495-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="8e495-113">-Instance</span></span>

<span data-ttu-id="8e495-114">Az újraindítani szükséges Analysis Services-kiszolgálói példány neve</span><span class="sxs-lookup"><span data-stu-id="8e495-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="8e495-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e495-115">-PassThru</span></span>

<span data-ttu-id="8e495-116">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="8e495-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8e495-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e495-117">-Confirm</span></span>
<span data-ttu-id="8e495-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8e495-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e495-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e495-119">-WhatIf</span></span>
<span data-ttu-id="8e495-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8e495-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e495-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e495-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e495-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e495-122">CommonParameters</span></span>
<span data-ttu-id="8e495-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e495-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e495-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e495-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e495-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e495-125">INPUTS</span></span>

### <span data-ttu-id="8e495-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8e495-126">System.String</span></span>

## <span data-ttu-id="8e495-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e495-127">OUTPUTS</span></span>

### <span data-ttu-id="8e495-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="8e495-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="8e495-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e495-129">NOTES</span></span>

<span data-ttu-id="8e495-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="8e495-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="8e495-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e495-131">RELATED LINKS</span></span>
