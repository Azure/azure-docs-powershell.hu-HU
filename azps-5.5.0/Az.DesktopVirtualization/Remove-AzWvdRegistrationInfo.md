---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163666"
---
# <span data-ttu-id="e51f7-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="e51f7-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="e51f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e51f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e51f7-103">Távolítsa el a Windows virtuális asztali regisztrációs adatait.</span><span class="sxs-lookup"><span data-stu-id="e51f7-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="e51f7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e51f7-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e51f7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e51f7-105">DESCRIPTION</span></span>
<span data-ttu-id="e51f7-106">Távolítsa el a windowsos virtuális asztali regisztrációs adatokat.</span><span class="sxs-lookup"><span data-stu-id="e51f7-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="e51f7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e51f7-107">EXAMPLES</span></span>

### <span data-ttu-id="e51f7-108">1. példa: Virtuális asztali Windows regisztrációs jogkivonat törlése</span><span class="sxs-lookup"><span data-stu-id="e51f7-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="e51f7-109">Ez a parancs törli a Windows virtuális asztali regisztrációs jogkivonatát egy gazdakészletben.</span><span class="sxs-lookup"><span data-stu-id="e51f7-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="e51f7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e51f7-110">PARAMETERS</span></span>

### <span data-ttu-id="e51f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51f7-111">-DefaultProfile</span></span>
<span data-ttu-id="e51f7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e51f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e51f7-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e51f7-113">-HostPoolName</span></span>
<span data-ttu-id="e51f7-114">Állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="e51f7-114">Host Pool Name</span></span>

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

### <span data-ttu-id="e51f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e51f7-115">-ResourceGroupName</span></span>
<span data-ttu-id="e51f7-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e51f7-116">Resource Group Name</span></span>

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

### <span data-ttu-id="e51f7-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e51f7-117">-SubscriptionId</span></span>
<span data-ttu-id="e51f7-118">help foo 1</span><span class="sxs-lookup"><span data-stu-id="e51f7-118">help foo 1</span></span>

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

### <span data-ttu-id="e51f7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e51f7-119">-Confirm</span></span>
<span data-ttu-id="e51f7-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e51f7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e51f7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e51f7-121">-WhatIf</span></span>
<span data-ttu-id="e51f7-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e51f7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e51f7-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e51f7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e51f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51f7-124">CommonParameters</span></span>
<span data-ttu-id="e51f7-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e51f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51f7-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e51f7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51f7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e51f7-127">INPUTS</span></span>

## <span data-ttu-id="e51f7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e51f7-128">OUTPUTS</span></span>

## <span data-ttu-id="e51f7-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e51f7-129">NOTES</span></span>

<span data-ttu-id="e51f7-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e51f7-130">ALIASES</span></span>

## <span data-ttu-id="e51f7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e51f7-131">RELATED LINKS</span></span>

