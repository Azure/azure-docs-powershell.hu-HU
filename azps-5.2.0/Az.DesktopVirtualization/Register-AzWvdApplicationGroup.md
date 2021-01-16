---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341142"
---
# <span data-ttu-id="dda9a-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="dda9a-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="dda9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dda9a-102">SYNOPSIS</span></span>
<span data-ttu-id="dda9a-103">Regisztrálhat egy virtuális Windows-alkalmazáscsoportot.</span><span class="sxs-lookup"><span data-stu-id="dda9a-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="dda9a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dda9a-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dda9a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dda9a-105">DESCRIPTION</span></span>
<span data-ttu-id="dda9a-106">Regisztrálhat egy virtuális Windows-alkalmazáscsoportot.</span><span class="sxs-lookup"><span data-stu-id="dda9a-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="dda9a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dda9a-107">EXAMPLES</span></span>

### <span data-ttu-id="dda9a-108">1. példa: Windows virtuális asztali alkalmazáscsoport regisztrálása</span><span class="sxs-lookup"><span data-stu-id="dda9a-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="dda9a-109">Ez a parancs regisztrál egy Windows virtuális asztali alkalmazáscsoportot egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="dda9a-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="dda9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dda9a-110">PARAMETERS</span></span>

### <span data-ttu-id="dda9a-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="dda9a-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="dda9a-112">ApplicationGroupPath Elérési út</span><span class="sxs-lookup"><span data-stu-id="dda9a-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="dda9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda9a-113">-DefaultProfile</span></span>
<span data-ttu-id="dda9a-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dda9a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dda9a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda9a-115">-ResourceGroupName</span></span>
<span data-ttu-id="dda9a-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="dda9a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="dda9a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dda9a-117">-SubscriptionId</span></span>
<span data-ttu-id="dda9a-118">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="dda9a-118">Subscription Id</span></span>

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

### <span data-ttu-id="dda9a-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dda9a-119">-WorkspaceName</span></span>
<span data-ttu-id="dda9a-120">Munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="dda9a-120">Workspace Name</span></span>

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

### <span data-ttu-id="dda9a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dda9a-121">-Confirm</span></span>
<span data-ttu-id="dda9a-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dda9a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda9a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda9a-123">-WhatIf</span></span>
<span data-ttu-id="dda9a-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dda9a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dda9a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dda9a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda9a-126">CommonParameters</span></span>
<span data-ttu-id="dda9a-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda9a-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dda9a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda9a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dda9a-129">INPUTS</span></span>

## <span data-ttu-id="dda9a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dda9a-130">OUTPUTS</span></span>

### <span data-ttu-id="dda9a-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="dda9a-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="dda9a-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dda9a-132">NOTES</span></span>

<span data-ttu-id="dda9a-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dda9a-133">ALIASES</span></span>

## <span data-ttu-id="dda9a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dda9a-134">RELATED LINKS</span></span>

