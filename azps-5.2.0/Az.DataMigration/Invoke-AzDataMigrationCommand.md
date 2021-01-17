---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327693"
---
# <span data-ttu-id="3b848-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="3b848-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="3b848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b848-102">SYNOPSIS</span></span>
<span data-ttu-id="3b848-103">Létrehoz egy új parancsot, amely egy meglévő DMS-feladaton hajtódik végre.</span><span class="sxs-lookup"><span data-stu-id="3b848-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="3b848-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3b848-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="3b848-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3b848-105">DESCRIPTION</span></span>
<span data-ttu-id="3b848-106">A Invoke-AzDataMigrationCommand parancsmag létrehoz egy új parancsfeladatot, amely egy meglévő áttelepítési feladaton fut.</span><span class="sxs-lookup"><span data-stu-id="3b848-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="3b848-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3b848-107">EXAMPLES</span></span>

### <span data-ttu-id="3b848-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3b848-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="3b848-109">A fenti példák a Invoke-AzDataMigrationCommand parancsmag használatával hoznak létre egy parancsot egy meglévő szolgáltatáshoz, projekthez és tevékenységhez.</span><span class="sxs-lookup"><span data-stu-id="3b848-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="3b848-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b848-110">PARAMETERS</span></span>

### <span data-ttu-id="3b848-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="3b848-111">-CommandType</span></span>
<span data-ttu-id="3b848-112">Parancstípus.</span><span class="sxs-lookup"><span data-stu-id="3b848-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b848-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b848-113">-DefaultProfile</span></span>
<span data-ttu-id="3b848-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b848-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b848-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="3b848-115">-ProjectName</span></span>
<span data-ttu-id="3b848-116">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="3b848-116">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b848-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b848-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b848-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3b848-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b848-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3b848-119">-ServiceName</span></span>
<span data-ttu-id="3b848-120">Adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="3b848-120">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b848-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="3b848-121">-TaskName</span></span>
<span data-ttu-id="3b848-122">A parancs által futtatott feladat neve.</span><span class="sxs-lookup"><span data-stu-id="3b848-122">The name of the task the command is run on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="3b848-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="3b848-123">-ObjectName</span></span>
<span data-ttu-id="3b848-124">A parancs által futtatandó adatbázis-objektum neve.</span><span class="sxs-lookup"><span data-stu-id="3b848-124">The name of the database object the command will run against.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b848-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b848-125">-Confirm</span></span>
<span data-ttu-id="3b848-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3b848-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b848-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b848-127">-WhatIf</span></span>
<span data-ttu-id="3b848-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3b848-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b848-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b848-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b848-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b848-130">CommonParameters</span></span>
<span data-ttu-id="3b848-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b848-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b848-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b848-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b848-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b848-133">INPUTS</span></span>

### <span data-ttu-id="3b848-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3b848-134">System.String</span></span>

## <span data-ttu-id="3b848-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b848-135">OUTPUTS</span></span>

### <span data-ttu-id="3b848-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span><span class="sxs-lookup"><span data-stu-id="3b848-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="3b848-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3b848-137">NOTES</span></span>

## <span data-ttu-id="3b848-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b848-138">RELATED LINKS</span></span>
