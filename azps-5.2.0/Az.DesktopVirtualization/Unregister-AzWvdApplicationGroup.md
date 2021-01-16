---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341094"
---
# <span data-ttu-id="7ed22-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="7ed22-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="7ed22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ed22-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed22-103">A Windows virtuális asztali alkalmazáscsoportjának regisztrációjának a regisztrációját.</span><span class="sxs-lookup"><span data-stu-id="7ed22-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="7ed22-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ed22-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7ed22-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ed22-105">DESCRIPTION</span></span>
<span data-ttu-id="7ed22-106">A Windows virtuális asztali alkalmazáscsoportjának regisztrációjának a regisztrációját.</span><span class="sxs-lookup"><span data-stu-id="7ed22-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="7ed22-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ed22-107">EXAMPLES</span></span>

### <span data-ttu-id="7ed22-108">1. példa: Windows virtuális asztali alkalmazáscsoport regisztrációjának a regisztrációjának a</span><span class="sxs-lookup"><span data-stu-id="7ed22-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="7ed22-109">Ez a parancs a Windows virtuális asztali alkalmazáscsoport munkaterületre való regisztrációját nem regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="7ed22-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="7ed22-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ed22-110">PARAMETERS</span></span>

### <span data-ttu-id="7ed22-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="7ed22-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="7ed22-112">ResourceGroupName Elérési út</span><span class="sxs-lookup"><span data-stu-id="7ed22-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="7ed22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed22-113">-DefaultProfile</span></span>
<span data-ttu-id="7ed22-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ed22-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed22-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed22-115">-ResourceGroupName</span></span>
<span data-ttu-id="7ed22-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7ed22-116">Resource Group Name</span></span>

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

### <span data-ttu-id="7ed22-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ed22-117">-SubscriptionId</span></span>
<span data-ttu-id="7ed22-118">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="7ed22-118">Subscription Id</span></span>

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

### <span data-ttu-id="7ed22-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7ed22-119">-WorkspaceName</span></span>
<span data-ttu-id="7ed22-120">Munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="7ed22-120">Workspace Name</span></span>

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

### <span data-ttu-id="7ed22-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ed22-121">-Confirm</span></span>
<span data-ttu-id="7ed22-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7ed22-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed22-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed22-123">-WhatIf</span></span>
<span data-ttu-id="7ed22-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7ed22-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed22-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ed22-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ed22-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed22-126">CommonParameters</span></span>
<span data-ttu-id="7ed22-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed22-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed22-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ed22-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed22-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ed22-129">INPUTS</span></span>

## <span data-ttu-id="7ed22-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ed22-130">OUTPUTS</span></span>

### <span data-ttu-id="7ed22-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="7ed22-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="7ed22-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ed22-132">NOTES</span></span>

<span data-ttu-id="7ed22-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7ed22-133">ALIASES</span></span>

## <span data-ttu-id="7ed22-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ed22-134">RELATED LINKS</span></span>

