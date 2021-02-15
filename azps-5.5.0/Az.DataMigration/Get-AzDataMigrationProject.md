---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204335"
---
# <span data-ttu-id="fc492-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="fc492-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="fc492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc492-102">SYNOPSIS</span></span>
<span data-ttu-id="fc492-103">Beolvassa egy Azure-adatbázis-áttelepítési projekt tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="fc492-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="fc492-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc492-104">SYNTAX</span></span>

### <span data-ttu-id="fc492-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc492-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc492-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc492-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc492-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc492-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc492-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc492-108">DESCRIPTION</span></span>
<span data-ttu-id="fc492-109">A Get-AzDataMigrationProject parancsmag beolvassa egy Azure-adatbázis-áttelepítési projekt tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="fc492-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="fc492-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc492-110">EXAMPLES</span></span>

### <span data-ttu-id="fc492-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fc492-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="fc492-112">A fenti példa beolvassa a TestProject nevű Azure-adatbázis-áttelepítési projektet a testResourceGroup nevű erőforráscsoportban és a testService nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="fc492-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="fc492-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fc492-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="fc492-114">A fenti példa beolvassa az Azure Database Migration projektet a átadott PSProject objektum bemeneti paramétere alapján.</span><span class="sxs-lookup"><span data-stu-id="fc492-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="fc492-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc492-115">PARAMETERS</span></span>

### <span data-ttu-id="fc492-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc492-116">-DefaultProfile</span></span>
<span data-ttu-id="fc492-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc492-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc492-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc492-118">-InputObject</span></span>
<span data-ttu-id="fc492-119">PSDataMigrationService objektum.</span><span class="sxs-lookup"><span data-stu-id="fc492-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="fc492-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fc492-120">-Name</span></span>
<span data-ttu-id="fc492-121">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="fc492-121">The name of the project.</span></span>

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

### <span data-ttu-id="fc492-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc492-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc492-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fc492-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="fc492-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc492-124">-ResourceId</span></span>
<span data-ttu-id="fc492-125">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="fc492-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="fc492-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fc492-126">-ServiceName</span></span>
<span data-ttu-id="fc492-127">Adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="fc492-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="fc492-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc492-128">CommonParameters</span></span>
<span data-ttu-id="fc492-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc492-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc492-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc492-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc492-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc492-131">INPUTS</span></span>

### <span data-ttu-id="fc492-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="fc492-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="fc492-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fc492-133">System.String</span></span>

## <span data-ttu-id="fc492-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc492-134">OUTPUTS</span></span>

### <span data-ttu-id="fc492-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="fc492-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="fc492-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc492-136">NOTES</span></span>

## <span data-ttu-id="fc492-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc492-137">RELATED LINKS</span></span>
