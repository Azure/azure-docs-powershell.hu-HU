---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Invoke-AzureRmDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
ms.openlocfilehash: 882d7eb0b005478850addda2d066c7266e6c2ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499540"
---
# <span data-ttu-id="33cf0-101">Invoke-AzureRmDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="33cf0-101">Invoke-AzureRmDataMigrationCommand</span></span>

## <span data-ttu-id="33cf0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="33cf0-103">Új parancsot hoz létre, amelyet egy meglévő DMS-feladaton kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="33cf0-103">Creates a new command to be executed on an existing DMS task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33cf0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33cf0-104">SYNTAX</span></span>

```
Invoke-AzureRmDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33cf0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="33cf0-105">DESCRIPTION</span></span>
<span data-ttu-id="33cf0-106">A New-AzureRmDataMigrationCommand parancsmag egy új, meglévő áttelepítési feladaton futtatandó parancsot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="33cf0-106">The New-AzureRmDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="33cf0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="33cf0-107">EXAMPLES</span></span>

### <span data-ttu-id="33cf0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="33cf0-108">Example 1</span></span>
```
PS C:\> $command = New-AzureRmDmsCommand -CommandType Complete -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="33cf0-109">A fenti példák az New-AzureRmDmsCommand parancsmagot használják a meglévő szolgáltatásokhoz, projektekhez és feladatokhoz tartozó parancsok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="33cf0-109">The above examples uses the New-AzureRmDmsCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="33cf0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33cf0-110">PARAMETERS</span></span>

### <span data-ttu-id="33cf0-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="33cf0-111">-CommandType</span></span>
<span data-ttu-id="33cf0-112">Parancs típusa</span><span class="sxs-lookup"><span data-stu-id="33cf0-112">Command Type.</span></span>

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

### <span data-ttu-id="33cf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33cf0-113">-DefaultProfile</span></span>
<span data-ttu-id="33cf0-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33cf0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33cf0-115">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="33cf0-115">-ProjectName</span></span>
<span data-ttu-id="33cf0-116">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="33cf0-116">The name of the project.</span></span>

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

### <span data-ttu-id="33cf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33cf0-117">-ResourceGroupName</span></span>
<span data-ttu-id="33cf0-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="33cf0-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="33cf0-119">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="33cf0-119">-ServiceName</span></span>
<span data-ttu-id="33cf0-120">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="33cf0-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="33cf0-121">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="33cf0-121">-TaskName</span></span>
<span data-ttu-id="33cf0-122">Annak a tevékenységnek a neve, amelyen a parancs fut.</span><span class="sxs-lookup"><span data-stu-id="33cf0-122">The name of the task the command is run on.</span></span>

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

### <span data-ttu-id="33cf0-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="33cf0-123">-Confirm</span></span>
<span data-ttu-id="33cf0-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="33cf0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33cf0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33cf0-125">-WhatIf</span></span>
<span data-ttu-id="33cf0-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="33cf0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33cf0-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="33cf0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33cf0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33cf0-128">CommonParameters</span></span>
<span data-ttu-id="33cf0-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33cf0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33cf0-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33cf0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33cf0-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33cf0-131">INPUTS</span></span>

### <span data-ttu-id="33cf0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="33cf0-132">System.String</span></span>

## <span data-ttu-id="33cf0-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33cf0-133">OUTPUTS</span></span>

### <span data-ttu-id="33cf0-134">Microsoft. Azure. Management. DataMigration. models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="33cf0-134">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="33cf0-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33cf0-135">NOTES</span></span>

## <span data-ttu-id="33cf0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33cf0-136">RELATED LINKS</span></span>
