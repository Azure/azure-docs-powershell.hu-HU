---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: a2db8d344628d8a421623cd5e6348db31a7321ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932897"
---
# <span data-ttu-id="631b1-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="631b1-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="631b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631b1-102">SYNOPSIS</span></span>
<span data-ttu-id="631b1-103">List start menu items in the given application group.</span><span class="sxs-lookup"><span data-stu-id="631b1-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="631b1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="631b1-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="631b1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="631b1-105">DESCRIPTION</span></span>
<span data-ttu-id="631b1-106">List start menu items in the given application group.</span><span class="sxs-lookup"><span data-stu-id="631b1-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="631b1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="631b1-107">EXAMPLES</span></span>

### <span data-ttu-id="631b1-108">2. példa: A Windows virtuális asztal Start menüjének elemeinek felsorolása</span><span class="sxs-lookup"><span data-stu-id="631b1-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="631b1-109">Ez a parancs a Windows virtuális asztal Start menüjének elemeit sorolja fel egy aplicaton csoportban.</span><span class="sxs-lookup"><span data-stu-id="631b1-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="631b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="631b1-110">PARAMETERS</span></span>

### <span data-ttu-id="631b1-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="631b1-111">-ApplicationGroupName</span></span>
<span data-ttu-id="631b1-112">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="631b1-112">The name of the application group</span></span>

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

### <span data-ttu-id="631b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631b1-113">-DefaultProfile</span></span>
<span data-ttu-id="631b1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="631b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="631b1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631b1-115">-ResourceGroupName</span></span>
<span data-ttu-id="631b1-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="631b1-116">The name of the resource group.</span></span>
<span data-ttu-id="631b1-117">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="631b1-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="631b1-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="631b1-118">-SubscriptionId</span></span>
<span data-ttu-id="631b1-119">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="631b1-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="631b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631b1-120">CommonParameters</span></span>
<span data-ttu-id="631b1-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="631b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631b1-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="631b1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631b1-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="631b1-123">INPUTS</span></span>

## <span data-ttu-id="631b1-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="631b1-124">OUTPUTS</span></span>

### <span data-ttu-id="631b1-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="631b1-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="631b1-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="631b1-126">NOTES</span></span>

<span data-ttu-id="631b1-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="631b1-127">ALIASES</span></span>

## <span data-ttu-id="631b1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="631b1-128">RELATED LINKS</span></span>

