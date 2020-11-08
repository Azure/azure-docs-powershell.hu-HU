---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185002"
---
# <span data-ttu-id="bdee4-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="bdee4-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="bdee4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bdee4-102">SYNOPSIS</span></span>
<span data-ttu-id="bdee4-103">A Windows Virtual Desktop Application csoport regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="bdee4-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="bdee4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bdee4-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bdee4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bdee4-105">DESCRIPTION</span></span>
<span data-ttu-id="bdee4-106">A Windows Virtual Desktop Application csoport regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="bdee4-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="bdee4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bdee4-107">EXAMPLES</span></span>

### <span data-ttu-id="bdee4-108">1. példa: a Windows virtuális asztali alkalmazás csoportjának regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="bdee4-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="bdee4-109">Ez a parancs a Windows virtuálisasztal-alkalmazás csoportjának egy munkaterületre való törlésének megszüntetése.</span><span class="sxs-lookup"><span data-stu-id="bdee4-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="bdee4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bdee4-110">PARAMETERS</span></span>

### <span data-ttu-id="bdee4-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="bdee4-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="bdee4-112">ResourceGroupName elérési útja</span><span class="sxs-lookup"><span data-stu-id="bdee4-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="bdee4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdee4-113">-DefaultProfile</span></span>
<span data-ttu-id="bdee4-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdee4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdee4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdee4-115">-ResourceGroupName</span></span>
<span data-ttu-id="bdee4-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="bdee4-116">Resource Group Name</span></span>

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

### <span data-ttu-id="bdee4-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdee4-117">-SubscriptionId</span></span>
<span data-ttu-id="bdee4-118">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="bdee4-118">Subscription Id</span></span>

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

### <span data-ttu-id="bdee4-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bdee4-119">-WorkspaceName</span></span>
<span data-ttu-id="bdee4-120">Munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="bdee4-120">Workspace Name</span></span>

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

### <span data-ttu-id="bdee4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bdee4-121">-Confirm</span></span>
<span data-ttu-id="bdee4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bdee4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdee4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdee4-123">-WhatIf</span></span>
<span data-ttu-id="bdee4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bdee4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdee4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bdee4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdee4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdee4-126">CommonParameters</span></span>
<span data-ttu-id="bdee4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bdee4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdee4-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bdee4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdee4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdee4-129">INPUTS</span></span>

## <span data-ttu-id="bdee4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdee4-130">OUTPUTS</span></span>

### <span data-ttu-id="bdee4-131">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="bdee4-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="bdee4-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bdee4-132">NOTES</span></span>

<span data-ttu-id="bdee4-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bdee4-133">ALIASES</span></span>

## <span data-ttu-id="bdee4-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdee4-134">RELATED LINKS</span></span>

