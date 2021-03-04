---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 4176b07f8a19538a05899b526d21f21cfcc20c9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934089"
---
# <span data-ttu-id="dde49-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="dde49-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="dde49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dde49-102">SYNOPSIS</span></span>
<span data-ttu-id="dde49-103">A projekt áttelepítésének módszere.</span><span class="sxs-lookup"><span data-stu-id="dde49-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="dde49-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dde49-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dde49-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dde49-105">DESCRIPTION</span></span>
<span data-ttu-id="dde49-106">A projekt áttelepítésének módszere.</span><span class="sxs-lookup"><span data-stu-id="dde49-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="dde49-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dde49-107">EXAMPLES</span></span>

### <span data-ttu-id="dde49-108">1. példa: Bejl</span><span class="sxs-lookup"><span data-stu-id="dde49-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="dde49-109">A projekt áttelepítésének módszere.</span><span class="sxs-lookup"><span data-stu-id="dde49-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="dde49-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dde49-110">PARAMETERS</span></span>

### <span data-ttu-id="dde49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde49-111">-DefaultProfile</span></span>
<span data-ttu-id="dde49-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dde49-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dde49-113">-Name</span><span class="sxs-lookup"><span data-stu-id="dde49-113">-Name</span></span>
<span data-ttu-id="dde49-114">Az Azure-áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="dde49-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde49-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde49-115">-ResourceGroupName</span></span>
<span data-ttu-id="dde49-116">Annak az Azure-erőforráscsoportnak a neve, amelybe a projektet át kell átcsoportosálni, annak a csoportnak a neve is része.</span><span class="sxs-lookup"><span data-stu-id="dde49-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="dde49-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dde49-117">-SubscriptionId</span></span>
<span data-ttu-id="dde49-118">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="dde49-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="dde49-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde49-119">CommonParameters</span></span>
<span data-ttu-id="dde49-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde49-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde49-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dde49-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde49-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dde49-122">INPUTS</span></span>

## <span data-ttu-id="dde49-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dde49-123">OUTPUTS</span></span>

### <span data-ttu-id="dde49-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="dde49-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="dde49-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dde49-125">NOTES</span></span>

<span data-ttu-id="dde49-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dde49-126">ALIASES</span></span>

## <span data-ttu-id="dde49-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dde49-127">RELATED LINKS</span></span>

