---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297008"
---
# <span data-ttu-id="c8d41-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c8d41-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="c8d41-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8d41-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d41-103">Regisztrálja a Windows Virtual Desktop Application Group alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="c8d41-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="c8d41-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8d41-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c8d41-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8d41-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d41-106">Regisztrálja a Windows Virtual Desktop Application Group alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="c8d41-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="c8d41-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c8d41-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d41-108">1. példa: egy Windows Virtual Desktop-alkalmazás regisztrálása</span><span class="sxs-lookup"><span data-stu-id="c8d41-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="c8d41-109">Ez a parancs egy Windows virtuális asztali alkalmazás csoportját regisztrálja egy munkaterületre.</span><span class="sxs-lookup"><span data-stu-id="c8d41-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="c8d41-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8d41-110">PARAMETERS</span></span>

### <span data-ttu-id="c8d41-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="c8d41-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="c8d41-112">ApplicationGroupPath elérési útja</span><span class="sxs-lookup"><span data-stu-id="c8d41-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="c8d41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d41-113">-DefaultProfile</span></span>
<span data-ttu-id="c8d41-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8d41-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8d41-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d41-115">-ResourceGroupName</span></span>
<span data-ttu-id="c8d41-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c8d41-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c8d41-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8d41-117">-SubscriptionId</span></span>
<span data-ttu-id="c8d41-118">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="c8d41-118">Subscription Id</span></span>

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

### <span data-ttu-id="c8d41-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c8d41-119">-WorkspaceName</span></span>
<span data-ttu-id="c8d41-120">Munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="c8d41-120">Workspace Name</span></span>

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

### <span data-ttu-id="c8d41-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8d41-121">-Confirm</span></span>
<span data-ttu-id="c8d41-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8d41-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d41-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d41-123">-WhatIf</span></span>
<span data-ttu-id="c8d41-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8d41-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8d41-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8d41-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d41-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d41-126">CommonParameters</span></span>
<span data-ttu-id="c8d41-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8d41-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d41-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c8d41-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d41-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8d41-129">INPUTS</span></span>

## <span data-ttu-id="c8d41-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8d41-130">OUTPUTS</span></span>

### <span data-ttu-id="c8d41-131">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8d41-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="c8d41-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8d41-132">NOTES</span></span>

<span data-ttu-id="c8d41-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c8d41-133">ALIASES</span></span>

## <span data-ttu-id="c8d41-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8d41-134">RELATED LINKS</span></span>

