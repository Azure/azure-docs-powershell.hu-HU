---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194581"
---
# <span data-ttu-id="58c26-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="58c26-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="58c26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="58c26-102">SYNOPSIS</span></span>
<span data-ttu-id="58c26-103">Megoldást kap a projekt áttelepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="58c26-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="58c26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="58c26-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="58c26-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="58c26-105">DESCRIPTION</span></span>
<span data-ttu-id="58c26-106">Megoldást kap a projekt áttelepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="58c26-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="58c26-107">Példák</span><span class="sxs-lookup"><span data-stu-id="58c26-107">EXAMPLES</span></span>

### <span data-ttu-id="58c26-108">Példa 1: Get</span><span class="sxs-lookup"><span data-stu-id="58c26-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="58c26-109">Áttelepítheti a Project-oldatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="58c26-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="58c26-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="58c26-110">PARAMETERS</span></span>

### <span data-ttu-id="58c26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c26-111">-DefaultProfile</span></span>
<span data-ttu-id="58c26-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58c26-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c26-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="58c26-113">-MigrateProjectName</span></span>
<span data-ttu-id="58c26-114">Az Azure áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="58c26-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="58c26-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="58c26-115">-Name</span></span>
<span data-ttu-id="58c26-116">Áttelepítési megoldás egyedi neve egy áttelepítési projekten belül.</span><span class="sxs-lookup"><span data-stu-id="58c26-116">Unique name of a migration solution within a migrate project.</span></span>

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

### <span data-ttu-id="58c26-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c26-117">-ResourceGroupName</span></span>
<span data-ttu-id="58c26-118">Annak a programnak a neve, amely a projectet Áttelepítő Azure Resource Group része.</span><span class="sxs-lookup"><span data-stu-id="58c26-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="58c26-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58c26-119">-SubscriptionId</span></span>
<span data-ttu-id="58c26-120">Azure-előfizetési azonosító, amelybe a projekt-áttelepítést hozta létre.</span><span class="sxs-lookup"><span data-stu-id="58c26-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="58c26-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c26-121">CommonParameters</span></span>
<span data-ttu-id="58c26-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="58c26-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c26-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="58c26-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c26-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="58c26-124">INPUTS</span></span>

## <span data-ttu-id="58c26-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58c26-125">OUTPUTS</span></span>

### <span data-ttu-id="58c26-126">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180901Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="58c26-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="58c26-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="58c26-127">NOTES</span></span>

<span data-ttu-id="58c26-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="58c26-128">ALIASES</span></span>

## <span data-ttu-id="58c26-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58c26-129">RELATED LINKS</span></span>

