---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371039"
---
# <span data-ttu-id="1950c-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="1950c-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="1950c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1950c-102">SYNOPSIS</span></span>
<span data-ttu-id="1950c-103">Megoldást kap a projekt áttelepítésére.</span><span class="sxs-lookup"><span data-stu-id="1950c-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="1950c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1950c-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1950c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1950c-105">DESCRIPTION</span></span>
<span data-ttu-id="1950c-106">Megoldást kap a projekt áttelepítésére.</span><span class="sxs-lookup"><span data-stu-id="1950c-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="1950c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1950c-107">EXAMPLES</span></span>

### <span data-ttu-id="1950c-108">1. példa: Get</span><span class="sxs-lookup"><span data-stu-id="1950c-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="1950c-109">Projektmegoldás áttelepítése név szerint.</span><span class="sxs-lookup"><span data-stu-id="1950c-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="1950c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1950c-110">PARAMETERS</span></span>

### <span data-ttu-id="1950c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1950c-111">-DefaultProfile</span></span>
<span data-ttu-id="1950c-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1950c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1950c-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="1950c-113">-MigrateProjectName</span></span>
<span data-ttu-id="1950c-114">Az Azure-áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="1950c-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="1950c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1950c-115">-Name</span></span>
<span data-ttu-id="1950c-116">Egy áttelepítési megoldás egyedi neve egy áttelepítési projekten belül.</span><span class="sxs-lookup"><span data-stu-id="1950c-116">Unique name of a migration solution within a migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1950c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1950c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1950c-118">Annak az Azure Erőforráscsoportnak a neve, amelybe a projektet át kell átcsoportosálni, annak a neve is része.</span><span class="sxs-lookup"><span data-stu-id="1950c-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="1950c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1950c-119">-SubscriptionId</span></span>
<span data-ttu-id="1950c-120">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="1950c-120">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1950c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1950c-121">CommonParameters</span></span>
<span data-ttu-id="1950c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1950c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1950c-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1950c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1950c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1950c-124">INPUTS</span></span>

## <span data-ttu-id="1950c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1950c-125">OUTPUTS</span></span>

### <span data-ttu-id="1950c-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="1950c-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="1950c-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1950c-127">NOTES</span></span>

<span data-ttu-id="1950c-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1950c-128">ALIASES</span></span>

## <span data-ttu-id="1950c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1950c-129">RELATED LINKS</span></span>

