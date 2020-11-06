---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: 31d37f740500247fed433c3e40b9d8220a5af663
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499551"
---
# <span data-ttu-id="ab858-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="ab858-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="ab858-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab858-102">SYNOPSIS</span></span>
<span data-ttu-id="ab858-103">Beolvassa az Azure adatbázis-áttelepítési projektek tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="ab858-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab858-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab858-104">SYNTAX</span></span>

### <span data-ttu-id="ab858-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab858-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab858-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab858-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab858-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab858-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab858-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab858-108">DESCRIPTION</span></span>
<span data-ttu-id="ab858-109">A Get-AzureRmDataMigrationProject parancsmag beolvassa az Azure Database Migration Project tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="ab858-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="ab858-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ab858-110">EXAMPLES</span></span>

### <span data-ttu-id="ab858-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ab858-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="ab858-112">A fenti példa beolvassa az Azure adatbázis-áttelepítési projektet a TestProject nevű erőforrás csoport testResourceGroup nevű erőforráscsoport nevű testService</span><span class="sxs-lookup"><span data-stu-id="ab858-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="ab858-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ab858-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="ab858-114">A fenti példa beolvassa az Azure adatbázis-áttelepítési projektet a PSProject-objektum bemeneti paraméterének alapján.</span><span class="sxs-lookup"><span data-stu-id="ab858-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="ab858-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab858-115">PARAMETERS</span></span>

### <span data-ttu-id="ab858-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab858-116">-DefaultProfile</span></span>
<span data-ttu-id="ab858-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab858-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab858-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab858-118">-InputObject</span></span>
<span data-ttu-id="ab858-119">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="ab858-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="ab858-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab858-120">-Name</span></span>
<span data-ttu-id="ab858-121">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="ab858-121">The name of the project.</span></span>

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

### <span data-ttu-id="ab858-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab858-122">-ResourceGroupName</span></span>
<span data-ttu-id="ab858-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ab858-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="ab858-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab858-124">-ResourceId</span></span>
<span data-ttu-id="ab858-125">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ab858-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="ab858-126">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="ab858-126">-ServiceName</span></span>
<span data-ttu-id="ab858-127">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="ab858-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="ab858-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab858-128">CommonParameters</span></span>
<span data-ttu-id="ab858-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab858-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab858-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab858-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab858-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab858-131">INPUTS</span></span>

### <span data-ttu-id="ab858-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ab858-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="ab858-133">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab858-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ab858-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ab858-134">System.String</span></span>

## <span data-ttu-id="ab858-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab858-135">OUTPUTS</span></span>

### <span data-ttu-id="ab858-136">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="ab858-136">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="ab858-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab858-137">NOTES</span></span>

## <span data-ttu-id="ab858-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab858-138">RELATED LINKS</span></span>
