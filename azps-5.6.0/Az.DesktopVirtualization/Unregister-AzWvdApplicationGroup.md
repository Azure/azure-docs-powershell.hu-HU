---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 9d3b8c0b1c126353eeab8a2509395e25e467bf0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925610"
---
# <span data-ttu-id="e3a72-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="e3a72-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="e3a72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3a72-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a72-103">A Windows virtuális asztali alkalmazáscsoportjának regisztrációjának a regisztrációját.</span><span class="sxs-lookup"><span data-stu-id="e3a72-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="e3a72-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3a72-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e3a72-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3a72-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a72-106">A Windows virtuális asztali alkalmazáscsoportjának regisztrációjának a regisztrációját.</span><span class="sxs-lookup"><span data-stu-id="e3a72-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="e3a72-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3a72-107">EXAMPLES</span></span>

### <span data-ttu-id="e3a72-108">1. példa: Windows virtuális asztali alkalmazáscsoport regisztrációjának a regisztrációjának a</span><span class="sxs-lookup"><span data-stu-id="e3a72-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="e3a72-109">Ez a parancs a Windows virtuális asztali alkalmazáscsoport munkaterületre való regisztrációját nem regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="e3a72-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="e3a72-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3a72-110">PARAMETERS</span></span>

### <span data-ttu-id="e3a72-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="e3a72-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="e3a72-112">ResourceGroupName Elérési út</span><span class="sxs-lookup"><span data-stu-id="e3a72-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="e3a72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a72-113">-DefaultProfile</span></span>
<span data-ttu-id="e3a72-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3a72-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3a72-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a72-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3a72-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e3a72-116">Resource Group Name</span></span>

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

### <span data-ttu-id="e3a72-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3a72-117">-SubscriptionId</span></span>
<span data-ttu-id="e3a72-118">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="e3a72-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a72-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e3a72-119">-WorkspaceName</span></span>
<span data-ttu-id="e3a72-120">Munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="e3a72-120">Workspace Name</span></span>

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

### <span data-ttu-id="e3a72-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3a72-121">-Confirm</span></span>
<span data-ttu-id="e3a72-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e3a72-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a72-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a72-123">-WhatIf</span></span>
<span data-ttu-id="e3a72-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e3a72-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a72-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3a72-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a72-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a72-126">CommonParameters</span></span>
<span data-ttu-id="e3a72-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a72-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a72-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3a72-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a72-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3a72-129">INPUTS</span></span>

## <span data-ttu-id="e3a72-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3a72-130">OUTPUTS</span></span>

### <span data-ttu-id="e3a72-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="e3a72-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="e3a72-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3a72-132">NOTES</span></span>

<span data-ttu-id="e3a72-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e3a72-133">ALIASES</span></span>

## <span data-ttu-id="e3a72-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3a72-134">RELATED LINKS</span></span>

