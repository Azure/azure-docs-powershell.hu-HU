---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297701"
---
# <span data-ttu-id="aea41-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="aea41-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="aea41-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aea41-102">SYNOPSIS</span></span>
<span data-ttu-id="aea41-103">Beolvassa az Azure adatbázis-áttelepítési projektek tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="aea41-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="aea41-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aea41-104">SYNTAX</span></span>

### <span data-ttu-id="aea41-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aea41-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aea41-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aea41-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aea41-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aea41-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aea41-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aea41-108">DESCRIPTION</span></span>
<span data-ttu-id="aea41-109">A Get-AzDataMigrationProject parancsmag beolvassa az Azure Database Migration Project tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="aea41-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="aea41-110">Példák</span><span class="sxs-lookup"><span data-stu-id="aea41-110">EXAMPLES</span></span>

### <span data-ttu-id="aea41-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aea41-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="aea41-112">A fenti példa beolvassa az Azure adatbázis-áttelepítési projektet a TestProject nevű erőforrás csoport testResourceGroup nevű erőforráscsoport nevű testService</span><span class="sxs-lookup"><span data-stu-id="aea41-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="aea41-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="aea41-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="aea41-114">A fenti példa beolvassa az Azure adatbázis-áttelepítési projektet a PSProject-objektum bemeneti paraméterének alapján.</span><span class="sxs-lookup"><span data-stu-id="aea41-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="aea41-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aea41-115">PARAMETERS</span></span>

### <span data-ttu-id="aea41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea41-116">-DefaultProfile</span></span>
<span data-ttu-id="aea41-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aea41-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea41-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aea41-118">-InputObject</span></span>
<span data-ttu-id="aea41-119">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="aea41-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="aea41-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aea41-120">-Name</span></span>
<span data-ttu-id="aea41-121">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="aea41-121">The name of the project.</span></span>

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

### <span data-ttu-id="aea41-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea41-122">-ResourceGroupName</span></span>
<span data-ttu-id="aea41-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aea41-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="aea41-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aea41-124">-ResourceId</span></span>
<span data-ttu-id="aea41-125">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="aea41-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="aea41-126">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="aea41-126">-ServiceName</span></span>
<span data-ttu-id="aea41-127">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="aea41-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="aea41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea41-128">CommonParameters</span></span>
<span data-ttu-id="aea41-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aea41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea41-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea41-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea41-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aea41-131">INPUTS</span></span>

### <span data-ttu-id="aea41-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="aea41-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="aea41-133">System. String</span><span class="sxs-lookup"><span data-stu-id="aea41-133">System.String</span></span>

## <span data-ttu-id="aea41-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aea41-134">OUTPUTS</span></span>

### <span data-ttu-id="aea41-135">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="aea41-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="aea41-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aea41-136">NOTES</span></span>

## <span data-ttu-id="aea41-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aea41-137">RELATED LINKS</span></span>
