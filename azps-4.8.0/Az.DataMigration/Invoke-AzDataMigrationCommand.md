---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182294"
---
# <span data-ttu-id="71589-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="71589-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="71589-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71589-102">SYNOPSIS</span></span>
<span data-ttu-id="71589-103">Új parancsot hoz létre, amelyet egy meglévő DMS-feladaton kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="71589-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="71589-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71589-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="71589-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71589-105">DESCRIPTION</span></span>
<span data-ttu-id="71589-106">A Invoke-AzDataMigrationCommand parancsmag egy új, meglévő áttelepítési feladaton futtatandó parancsot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="71589-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="71589-107">Példák</span><span class="sxs-lookup"><span data-stu-id="71589-107">EXAMPLES</span></span>

### <span data-ttu-id="71589-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="71589-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="71589-109">A fenti példák az Invoke-AzDataMigrationCommand parancsmagot használják a meglévő szolgáltatásokhoz, projektekhez és feladatokhoz tartozó parancsok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="71589-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="71589-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71589-110">PARAMETERS</span></span>

### <span data-ttu-id="71589-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="71589-111">-CommandType</span></span>
<span data-ttu-id="71589-112">Parancs típusa</span><span class="sxs-lookup"><span data-stu-id="71589-112">Command Type.</span></span>

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

### <span data-ttu-id="71589-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71589-113">-DefaultProfile</span></span>
<span data-ttu-id="71589-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71589-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71589-115">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="71589-115">-ProjectName</span></span>
<span data-ttu-id="71589-116">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="71589-116">The name of the project.</span></span>

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

### <span data-ttu-id="71589-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71589-117">-ResourceGroupName</span></span>
<span data-ttu-id="71589-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71589-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="71589-119">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="71589-119">-ServiceName</span></span>
<span data-ttu-id="71589-120">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="71589-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="71589-121">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="71589-121">-TaskName</span></span>
<span data-ttu-id="71589-122">Annak a tevékenységnek a neve, amelyen a parancs fut.</span><span class="sxs-lookup"><span data-stu-id="71589-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="71589-123">-Objektumnév</span><span class="sxs-lookup"><span data-stu-id="71589-123">-ObjectName</span></span>
<span data-ttu-id="71589-124">Annak az adatbázis-objektumnak a neve, amelyet a parancs fog futni.</span><span class="sxs-lookup"><span data-stu-id="71589-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="71589-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71589-125">-Confirm</span></span>
<span data-ttu-id="71589-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71589-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71589-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71589-127">-WhatIf</span></span>
<span data-ttu-id="71589-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71589-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71589-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71589-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71589-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71589-130">CommonParameters</span></span>
<span data-ttu-id="71589-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71589-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71589-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71589-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71589-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71589-133">INPUTS</span></span>

### <span data-ttu-id="71589-134">System. String</span><span class="sxs-lookup"><span data-stu-id="71589-134">System.String</span></span>

## <span data-ttu-id="71589-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71589-135">OUTPUTS</span></span>

### <span data-ttu-id="71589-136">Microsoft. Azure. Management. DataMigration. models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="71589-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="71589-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71589-137">NOTES</span></span>

## <span data-ttu-id="71589-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71589-138">RELATED LINKS</span></span>
