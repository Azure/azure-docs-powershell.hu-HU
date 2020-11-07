---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 00a0e0a688f49615cadff3990071cd49d1356443
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666786"
---
# <span data-ttu-id="efa4a-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="efa4a-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="efa4a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="efa4a-102">SYNOPSIS</span></span>
<span data-ttu-id="efa4a-103">Beolvassa az Azure adatbázis-áttelepítési projektek tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="efa4a-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="efa4a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="efa4a-104">SYNTAX</span></span>

### <span data-ttu-id="efa4a-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efa4a-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efa4a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efa4a-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efa4a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efa4a-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="efa4a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="efa4a-108">DESCRIPTION</span></span>
<span data-ttu-id="efa4a-109">A Get-AzDataMigrationProject parancsmag beolvassa az Azure Database Migration Project tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="efa4a-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="efa4a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="efa4a-110">EXAMPLES</span></span>

### <span data-ttu-id="efa4a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="efa4a-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="efa4a-112">A fenti példa beolvassa az Azure adatbázis-áttelepítési projektet a TestProject nevű erőforrás csoport testResourceGroup nevű erőforráscsoport nevű testService</span><span class="sxs-lookup"><span data-stu-id="efa4a-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="efa4a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="efa4a-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="efa4a-114">A fenti példa beolvassa az Azure adatbázis-áttelepítési projektet a PSProject-objektum bemeneti paraméterének alapján.</span><span class="sxs-lookup"><span data-stu-id="efa4a-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="efa4a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="efa4a-115">PARAMETERS</span></span>

### <span data-ttu-id="efa4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa4a-116">-DefaultProfile</span></span>
<span data-ttu-id="efa4a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efa4a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efa4a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efa4a-118">-InputObject</span></span>
<span data-ttu-id="efa4a-119">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="efa4a-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efa4a-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="efa4a-120">-Name</span></span>
<span data-ttu-id="efa4a-121">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="efa4a-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa4a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa4a-122">-ResourceGroupName</span></span>
<span data-ttu-id="efa4a-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="efa4a-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa4a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efa4a-124">-ResourceId</span></span>
<span data-ttu-id="efa4a-125">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="efa4a-125">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa4a-126">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="efa4a-126">-ServiceName</span></span>
<span data-ttu-id="efa4a-127">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="efa4a-127">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa4a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa4a-128">CommonParameters</span></span>
<span data-ttu-id="efa4a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="efa4a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa4a-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efa4a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa4a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa4a-131">INPUTS</span></span>

### <span data-ttu-id="efa4a-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="efa4a-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="efa4a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="efa4a-133">System.String</span></span>

## <span data-ttu-id="efa4a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa4a-134">OUTPUTS</span></span>

### <span data-ttu-id="efa4a-135">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="efa4a-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="efa4a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="efa4a-136">NOTES</span></span>

## <span data-ttu-id="efa4a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efa4a-137">RELATED LINKS</span></span>
