---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: f00c1499e7f7e8a5a6d6b14bcbd8289b35ae2ced
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666780"
---
# <span data-ttu-id="cc9ef-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="cc9ef-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="cc9ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="cc9ef-103">Új parancsot hoz létre, amelyet egy meglévő DMS-feladaton kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="cc9ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc9ef-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="cc9ef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc9ef-105">DESCRIPTION</span></span>
<span data-ttu-id="cc9ef-106">A Invoke-AzDataMigrationCommand parancsmag egy új, meglévő áttelepítési feladaton futtatandó parancsot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="cc9ef-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cc9ef-107">EXAMPLES</span></span>

### <span data-ttu-id="cc9ef-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cc9ef-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="cc9ef-109">A fenti példák az Invoke-AzDataMigrationCommand parancsmagot használják a meglévő szolgáltatásokhoz, projektekhez és feladatokhoz tartozó parancsok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="cc9ef-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc9ef-110">PARAMETERS</span></span>

### <span data-ttu-id="cc9ef-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="cc9ef-111">-CommandType</span></span>
<span data-ttu-id="cc9ef-112">Parancs típusa</span><span class="sxs-lookup"><span data-stu-id="cc9ef-112">Command Type.</span></span>

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

### <span data-ttu-id="cc9ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc9ef-113">-DefaultProfile</span></span>
<span data-ttu-id="cc9ef-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc9ef-115">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="cc9ef-115">-ProjectName</span></span>
<span data-ttu-id="cc9ef-116">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-116">The name of the project.</span></span>

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

### <span data-ttu-id="cc9ef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc9ef-117">-ResourceGroupName</span></span>
<span data-ttu-id="cc9ef-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cc9ef-119">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="cc9ef-119">-ServiceName</span></span>
<span data-ttu-id="cc9ef-120">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="cc9ef-121">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="cc9ef-121">-TaskName</span></span>
<span data-ttu-id="cc9ef-122">Annak a tevékenységnek a neve, amelyen a parancs fut.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="cc9ef-123">-Objektumnév</span><span class="sxs-lookup"><span data-stu-id="cc9ef-123">-ObjectName</span></span>
<span data-ttu-id="cc9ef-124">Annak az adatbázis-objektumnak a neve, amelyet a parancs fog futni.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="cc9ef-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc9ef-125">-Confirm</span></span>
<span data-ttu-id="cc9ef-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc9ef-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc9ef-127">-WhatIf</span></span>
<span data-ttu-id="cc9ef-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc9ef-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc9ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc9ef-130">CommonParameters</span></span>
<span data-ttu-id="cc9ef-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc9ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc9ef-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc9ef-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc9ef-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc9ef-133">INPUTS</span></span>

### <span data-ttu-id="cc9ef-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cc9ef-134">System.String</span></span>

## <span data-ttu-id="cc9ef-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc9ef-135">OUTPUTS</span></span>

### <span data-ttu-id="cc9ef-136">Microsoft. Azure. Management. DataMigration. models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="cc9ef-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="cc9ef-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc9ef-137">NOTES</span></span>

## <span data-ttu-id="cc9ef-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc9ef-138">RELATED LINKS</span></span>
