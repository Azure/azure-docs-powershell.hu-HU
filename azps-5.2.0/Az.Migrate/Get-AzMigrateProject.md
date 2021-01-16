---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340350"
---
# <span data-ttu-id="206c3-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="206c3-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="206c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="206c3-102">SYNOPSIS</span></span>
<span data-ttu-id="206c3-103">A projekt áttelepítésének módszere.</span><span class="sxs-lookup"><span data-stu-id="206c3-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="206c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="206c3-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="206c3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="206c3-105">DESCRIPTION</span></span>
<span data-ttu-id="206c3-106">A projekt áttelepítésének módszere.</span><span class="sxs-lookup"><span data-stu-id="206c3-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="206c3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="206c3-107">EXAMPLES</span></span>

### <span data-ttu-id="206c3-108">1. példa: Bejl</span><span class="sxs-lookup"><span data-stu-id="206c3-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="206c3-109">A projekt áttelepítésének módszere.</span><span class="sxs-lookup"><span data-stu-id="206c3-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="206c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="206c3-110">PARAMETERS</span></span>

### <span data-ttu-id="206c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="206c3-111">-DefaultProfile</span></span>
<span data-ttu-id="206c3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="206c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="206c3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="206c3-113">-Name</span></span>
<span data-ttu-id="206c3-114">Az Azure-áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="206c3-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="206c3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="206c3-115">-ResourceGroupName</span></span>
<span data-ttu-id="206c3-116">Annak az Azure-erőforráscsoportnak a neve, amelybe a projektet át kell átcsoportosálni, annak a csoportnak a neve is része.</span><span class="sxs-lookup"><span data-stu-id="206c3-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="206c3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="206c3-117">-SubscriptionId</span></span>
<span data-ttu-id="206c3-118">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="206c3-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="206c3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="206c3-119">CommonParameters</span></span>
<span data-ttu-id="206c3-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="206c3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="206c3-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="206c3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="206c3-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="206c3-122">INPUTS</span></span>

## <span data-ttu-id="206c3-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="206c3-123">OUTPUTS</span></span>

### <span data-ttu-id="206c3-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="206c3-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="206c3-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="206c3-125">NOTES</span></span>

<span data-ttu-id="206c3-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="206c3-126">ALIASES</span></span>

## <span data-ttu-id="206c3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="206c3-127">RELATED LINKS</span></span>

