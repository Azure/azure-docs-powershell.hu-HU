---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498964"
---
# <span data-ttu-id="17066-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="17066-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="17066-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17066-102">SYNOPSIS</span></span>
<span data-ttu-id="17066-103">Beolvassa az Azure adatbázis áttelepítési szolgáltatásának példányaival társított tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="17066-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17066-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17066-104">SYNTAX</span></span>

### <span data-ttu-id="17066-105">ResourceGroupSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="17066-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="17066-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17066-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="17066-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="17066-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## <span data-ttu-id="17066-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="17066-108">DESCRIPTION</span></span>
<span data-ttu-id="17066-109">A Get-AzureRmDataMigrationService parancsmag beolvassa az Azure-adatbázis áttelepítési szolgáltatásának a szolgáltatás neve és az Azure-Erőforrás csoport nevében a bemeneti paraméterek alapján társított tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="17066-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="17066-110">Példák</span><span class="sxs-lookup"><span data-stu-id="17066-110">EXAMPLES</span></span>

### <span data-ttu-id="17066-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="17066-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="17066-112">A fenti példa beolvassa az Azure adatbázis-áttelepítési szolgáltatás példányának testService nevű részét.</span><span class="sxs-lookup"><span data-stu-id="17066-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="17066-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="17066-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

<span data-ttu-id="17066-114">A fenti példa beolvassa az Azure adatbázis-áttelepítési szolgáltatásokat a testResourceGroup nevű erőforráscsoport erőforrás csoportjában.</span><span class="sxs-lookup"><span data-stu-id="17066-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="17066-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17066-115">PARAMETERS</span></span>

### <span data-ttu-id="17066-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17066-116">-DefaultProfile</span></span>
<span data-ttu-id="17066-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17066-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17066-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17066-118">-Name</span></span>
<span data-ttu-id="17066-119">Az áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="17066-119">Name of Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17066-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17066-120">-ResourceGroupName</span></span>
<span data-ttu-id="17066-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="17066-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17066-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17066-122">-ResourceId</span></span>
<span data-ttu-id="17066-123">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="17066-123">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="17066-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17066-124">INPUTS</span></span>

### <span data-ttu-id="17066-125">System. String</span><span class="sxs-lookup"><span data-stu-id="17066-125">System.String</span></span>


## <span data-ttu-id="17066-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17066-126">OUTPUTS</span></span>

### <span data-ttu-id="17066-127">System. Collections. Generic. IList ' 1 [[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft. Azure. commands. DataMigration, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="17066-127">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="17066-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17066-128">NOTES</span></span>

## <span data-ttu-id="17066-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17066-129">RELATED LINKS</span></span>





