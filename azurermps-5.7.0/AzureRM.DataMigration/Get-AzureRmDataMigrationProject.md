---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502611"
---
# <span data-ttu-id="cab9e-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="cab9e-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="cab9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cab9e-102">SYNOPSIS</span></span>
<span data-ttu-id="cab9e-103">Beolvassa az Azure adatbázis-áttelepítési projektek tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="cab9e-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cab9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cab9e-104">SYNTAX</span></span>

### <span data-ttu-id="cab9e-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cab9e-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="cab9e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cab9e-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="cab9e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cab9e-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="cab9e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cab9e-108">DESCRIPTION</span></span>
<span data-ttu-id="cab9e-109">A Get-AzureRmDataMigrationProject parancsmag beolvassa az Azure Database Migration Project tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="cab9e-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="cab9e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cab9e-110">EXAMPLES</span></span>

### <span data-ttu-id="cab9e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cab9e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="cab9e-112">A fenti példa beolvassa az Azure adatbázis-áttelepítési projektet a TestProject nevű erőforrás csoport testResourceGroup nevű erőforráscsoport nevű testService</span><span class="sxs-lookup"><span data-stu-id="cab9e-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="cab9e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="cab9e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="cab9e-114">A fenti példa beolvassa az Azure adatbázis-áttelepítési projektet a PSProject-objektum bemeneti paraméterének alapján.</span><span class="sxs-lookup"><span data-stu-id="cab9e-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 


## <span data-ttu-id="cab9e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cab9e-115">PARAMETERS</span></span>

### <span data-ttu-id="cab9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab9e-116">-DefaultProfile</span></span>
<span data-ttu-id="cab9e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cab9e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cab9e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cab9e-118">-InputObject</span></span>
<span data-ttu-id="cab9e-119">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="cab9e-119">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cab9e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cab9e-120">-Name</span></span>
<span data-ttu-id="cab9e-121">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="cab9e-121">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab9e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab9e-122">-ResourceGroupName</span></span>
<span data-ttu-id="cab9e-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cab9e-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab9e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cab9e-124">-ResourceId</span></span>
<span data-ttu-id="cab9e-125">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="cab9e-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="cab9e-126">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="cab9e-126">-ServiceName</span></span>
<span data-ttu-id="cab9e-127">Az adatáttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="cab9e-127">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="cab9e-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cab9e-128">INPUTS</span></span>

### <span data-ttu-id="cab9e-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cab9e-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="cab9e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cab9e-130">System.String</span></span>


## <span data-ttu-id="cab9e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cab9e-131">OUTPUTS</span></span>

### <span data-ttu-id="cab9e-132">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. DataMigration. models. PSProject, Microsoft. Azure. commands. DataMigration, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cab9e-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProject, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="cab9e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cab9e-133">NOTES</span></span>

## <span data-ttu-id="cab9e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cab9e-134">RELATED LINKS</span></span>

