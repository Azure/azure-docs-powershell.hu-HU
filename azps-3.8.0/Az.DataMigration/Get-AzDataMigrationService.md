---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012570"
---
# <span data-ttu-id="0295d-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0295d-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="0295d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0295d-102">SYNOPSIS</span></span>
<span data-ttu-id="0295d-103">Beolvassa az Azure adatbázis áttelepítési szolgáltatásának példányaival társított tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0295d-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="0295d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0295d-104">SYNTAX</span></span>

### <span data-ttu-id="0295d-105">ResourceGroupSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0295d-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0295d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0295d-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0295d-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="0295d-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0295d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0295d-108">DESCRIPTION</span></span>
<span data-ttu-id="0295d-109">A Get-AzDataMigrationService parancsmag beolvassa az Azure-adatbázis áttelepítési szolgáltatásának a szolgáltatás neve és az Azure-Erőforrás csoport nevében a bemeneti paraméterek alapján társított tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="0295d-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="0295d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0295d-110">EXAMPLES</span></span>

### <span data-ttu-id="0295d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0295d-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="0295d-112">A fenti példa beolvassa az Azure adatbázis-áttelepítési szolgáltatás példányának testService nevű részét.</span><span class="sxs-lookup"><span data-stu-id="0295d-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="0295d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="0295d-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="0295d-114">A fenti példa beolvassa az Azure adatbázis-áttelepítési szolgáltatásokat a testResourceGroup nevű erőforráscsoport erőforrás csoportjában.</span><span class="sxs-lookup"><span data-stu-id="0295d-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="0295d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0295d-115">PARAMETERS</span></span>

### <span data-ttu-id="0295d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0295d-116">-DefaultProfile</span></span>
<span data-ttu-id="0295d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0295d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0295d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0295d-118">-Name</span></span>
<span data-ttu-id="0295d-119">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="0295d-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0295d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0295d-120">-ResourceGroupName</span></span>
<span data-ttu-id="0295d-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0295d-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0295d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0295d-122">-ResourceId</span></span>
<span data-ttu-id="0295d-123">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0295d-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="0295d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0295d-124">CommonParameters</span></span>
<span data-ttu-id="0295d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0295d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0295d-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0295d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0295d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0295d-127">INPUTS</span></span>

### <span data-ttu-id="0295d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0295d-128">System.String</span></span>

## <span data-ttu-id="0295d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0295d-129">OUTPUTS</span></span>

### <span data-ttu-id="0295d-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0295d-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="0295d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0295d-131">NOTES</span></span>

## <span data-ttu-id="0295d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0295d-132">RELATED LINKS</span></span>
