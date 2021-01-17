---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: fd91ea79cbad51d03c0986ed5f55601af240de16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387307"
---
# <span data-ttu-id="13987-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="13987-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="13987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13987-102">SYNOPSIS</span></span>
<span data-ttu-id="13987-103">List start menu items in the given application group.</span><span class="sxs-lookup"><span data-stu-id="13987-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="13987-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13987-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="13987-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13987-105">DESCRIPTION</span></span>
<span data-ttu-id="13987-106">List start menu items in the given application group.</span><span class="sxs-lookup"><span data-stu-id="13987-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="13987-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13987-107">EXAMPLES</span></span>

### <span data-ttu-id="13987-108">2. példa: A Windows virtuális asztal Start menüjének elemeinek felsorolása</span><span class="sxs-lookup"><span data-stu-id="13987-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="13987-109">Ez a parancs a Windows virtuális asztal Start menüjének elemeit sorolja fel egy aplicaton csoportban.</span><span class="sxs-lookup"><span data-stu-id="13987-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="13987-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13987-110">PARAMETERS</span></span>

### <span data-ttu-id="13987-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="13987-111">-ApplicationGroupName</span></span>
<span data-ttu-id="13987-112">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="13987-112">The name of the application group</span></span>

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

### <span data-ttu-id="13987-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13987-113">-DefaultProfile</span></span>
<span data-ttu-id="13987-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13987-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13987-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13987-115">-ResourceGroupName</span></span>
<span data-ttu-id="13987-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13987-116">The name of the resource group.</span></span>
<span data-ttu-id="13987-117">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="13987-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="13987-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13987-118">-SubscriptionId</span></span>
<span data-ttu-id="13987-119">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="13987-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="13987-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13987-120">CommonParameters</span></span>
<span data-ttu-id="13987-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13987-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13987-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13987-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13987-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13987-123">INPUTS</span></span>

## <span data-ttu-id="13987-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13987-124">OUTPUTS</span></span>

### <span data-ttu-id="13987-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="13987-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="13987-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13987-126">NOTES</span></span>

<span data-ttu-id="13987-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="13987-127">ALIASES</span></span>

## <span data-ttu-id="13987-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13987-128">RELATED LINKS</span></span>

