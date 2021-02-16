---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167810"
---
# <span data-ttu-id="ccfc9-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ccfc9-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="ccfc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccfc9-102">SYNOPSIS</span></span>
<span data-ttu-id="ccfc9-103">Beolvassa az Azure Adatbázis-áttelepítési szolgáltatás egy példányához tartozó tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ccfc9-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="ccfc9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ccfc9-104">SYNTAX</span></span>

### <span data-ttu-id="ccfc9-105">ResourceGroupSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ccfc9-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccfc9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccfc9-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccfc9-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="ccfc9-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccfc9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ccfc9-108">DESCRIPTION</span></span>
<span data-ttu-id="ccfc9-109">A Get-AzDataMigrationService parancsmag beolvassa az Azure Database Migration Service egy példányához társított tulajdonságokat a szolgáltatás neve és az Azure Erőforráscsoport neve alapján bemeneti paraméterekként.</span><span class="sxs-lookup"><span data-stu-id="ccfc9-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="ccfc9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ccfc9-110">EXAMPLES</span></span>

### <span data-ttu-id="ccfc9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ccfc9-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="ccfc9-112">A fenti példa beolvassa a testService nevű Azure Database Migration Service példány tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="ccfc9-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="ccfc9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ccfc9-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="ccfc9-114">A fenti példa beolvassa az Azure Database Migration Services szolgáltatást a testResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="ccfc9-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="ccfc9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccfc9-115">PARAMETERS</span></span>

### <span data-ttu-id="ccfc9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccfc9-116">-DefaultProfile</span></span>
<span data-ttu-id="ccfc9-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccfc9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccfc9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ccfc9-118">-Name</span></span>
<span data-ttu-id="ccfc9-119">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="ccfc9-119">Name of Database Migration Service.</span></span>

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

### <span data-ttu-id="ccfc9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccfc9-120">-ResourceGroupName</span></span>
<span data-ttu-id="ccfc9-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ccfc9-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="ccfc9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccfc9-122">-ResourceId</span></span>
<span data-ttu-id="ccfc9-123">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="ccfc9-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="ccfc9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccfc9-124">CommonParameters</span></span>
<span data-ttu-id="ccfc9-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccfc9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccfc9-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccfc9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccfc9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccfc9-127">INPUTS</span></span>

### <span data-ttu-id="ccfc9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ccfc9-128">System.String</span></span>

## <span data-ttu-id="ccfc9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccfc9-129">OUTPUTS</span></span>

### <span data-ttu-id="ccfc9-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ccfc9-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="ccfc9-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ccfc9-131">NOTES</span></span>

## <span data-ttu-id="ccfc9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccfc9-132">RELATED LINKS</span></span>
