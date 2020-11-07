---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 141c601b5a903462b15bbeb45d410db24608323f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666106"
---
# <span data-ttu-id="df75b-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="df75b-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="df75b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df75b-102">SYNOPSIS</span></span>
<span data-ttu-id="df75b-103">Egy meglévő Kusto-adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="df75b-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="df75b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df75b-104">SYNTAX</span></span>

### <span data-ttu-id="df75b-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df75b-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df75b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df75b-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df75b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="df75b-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df75b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="df75b-108">DESCRIPTION</span></span>
<span data-ttu-id="df75b-109">Egy meglévő Kusto-adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="df75b-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="df75b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="df75b-110">EXAMPLES</span></span>

### <span data-ttu-id="df75b-111">Példa 1 – meglévő Kusto-adatbázis törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="df75b-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="df75b-112">A fenti parancs törli a "mykustodatabase" nevű Kusto-adatbázist a "mykustocluster" nevű "testrg" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="df75b-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="df75b-113">2. példa – meglévő Kusto-adatbázis törlése csővezetékről</span><span class="sxs-lookup"><span data-stu-id="df75b-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="df75b-114">A fenti parancs a "mykustodatabase" nevű "" nevű Kusto-adatbázist kapja a parancsmagot használó "testrg" erőforráscsoport "" nevű mykustocluster, majd az `Get-AzKustoDatabase` eredmény törléséhez a csöveket fogja használni `Remove-AzKustoDatabase` .</span><span class="sxs-lookup"><span data-stu-id="df75b-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="df75b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df75b-115">PARAMETERS</span></span>

### <span data-ttu-id="df75b-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="df75b-116">-ClusterName</span></span>
<span data-ttu-id="df75b-117">Annak a fürtnek a neve, amelyben az adatbázis létezik.</span><span class="sxs-lookup"><span data-stu-id="df75b-117">Name of the cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df75b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df75b-118">-DefaultProfile</span></span>
<span data-ttu-id="df75b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df75b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df75b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df75b-120">-InputObject</span></span>
<span data-ttu-id="df75b-121">Kusto adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="df75b-121">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df75b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df75b-122">-Name</span></span>
<span data-ttu-id="df75b-123">Eltávolítandó adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="df75b-123">Name of database to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df75b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df75b-124">-PassThru</span></span>
<span data-ttu-id="df75b-125">Adja meg, hogy a megadott adatbázis sikeresen fel lett-e függesztve.</span><span class="sxs-lookup"><span data-stu-id="df75b-125">Return whether the specified database was successfully suspended or not.</span></span>

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

### <span data-ttu-id="df75b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df75b-126">-ResourceGroupName</span></span>
<span data-ttu-id="df75b-127">Annak az erőforráscsoport-csoportnak a neve, amelyben a fürt létezik.</span><span class="sxs-lookup"><span data-stu-id="df75b-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df75b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df75b-128">-ResourceId</span></span>
<span data-ttu-id="df75b-129">Kusto adatbázis-ResourceID.</span><span class="sxs-lookup"><span data-stu-id="df75b-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df75b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df75b-130">-Confirm</span></span>
<span data-ttu-id="df75b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df75b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df75b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df75b-132">-WhatIf</span></span>
<span data-ttu-id="df75b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df75b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df75b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df75b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df75b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df75b-135">CommonParameters</span></span>
<span data-ttu-id="df75b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df75b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df75b-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df75b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df75b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df75b-138">INPUTS</span></span>

### <span data-ttu-id="df75b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="df75b-139">System.String</span></span>

### <span data-ttu-id="df75b-140">Microsoft. Azure. Command. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="df75b-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="df75b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df75b-141">OUTPUTS</span></span>

### <span data-ttu-id="df75b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df75b-142">System.Boolean</span></span>

## <span data-ttu-id="df75b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df75b-143">NOTES</span></span>

## <span data-ttu-id="df75b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df75b-144">RELATED LINKS</span></span>
