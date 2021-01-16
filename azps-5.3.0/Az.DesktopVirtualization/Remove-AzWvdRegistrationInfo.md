---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467885"
---
# <span data-ttu-id="581b0-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="581b0-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="581b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="581b0-102">SYNOPSIS</span></span>
<span data-ttu-id="581b0-103">Távolítsa el a Windows virtuális asztali regisztrációs adatait.</span><span class="sxs-lookup"><span data-stu-id="581b0-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="581b0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="581b0-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="581b0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="581b0-105">DESCRIPTION</span></span>
<span data-ttu-id="581b0-106">Távolítsa el a Windows virtuális asztali regisztrációs adatait.</span><span class="sxs-lookup"><span data-stu-id="581b0-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="581b0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="581b0-107">EXAMPLES</span></span>

### <span data-ttu-id="581b0-108">1. példa: Virtuális asztali Windows regisztrációs jogkivonat törlése</span><span class="sxs-lookup"><span data-stu-id="581b0-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="581b0-109">Ez a parancs törli a Windows virtuális asztali regisztrációs jogkivonatát egy gazdakészletben.</span><span class="sxs-lookup"><span data-stu-id="581b0-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="581b0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="581b0-110">PARAMETERS</span></span>

### <span data-ttu-id="581b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581b0-111">-DefaultProfile</span></span>
<span data-ttu-id="581b0-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="581b0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="581b0-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="581b0-113">-HostPoolName</span></span>
<span data-ttu-id="581b0-114">Állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="581b0-114">Host Pool Name</span></span>

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

### <span data-ttu-id="581b0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="581b0-115">-ResourceGroupName</span></span>
<span data-ttu-id="581b0-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="581b0-116">Resource Group Name</span></span>

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

### <span data-ttu-id="581b0-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="581b0-117">-SubscriptionId</span></span>
<span data-ttu-id="581b0-118">help foo 1</span><span class="sxs-lookup"><span data-stu-id="581b0-118">help foo 1</span></span>

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

### <span data-ttu-id="581b0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="581b0-119">-Confirm</span></span>
<span data-ttu-id="581b0-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="581b0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="581b0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="581b0-121">-WhatIf</span></span>
<span data-ttu-id="581b0-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="581b0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="581b0-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="581b0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="581b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581b0-124">CommonParameters</span></span>
<span data-ttu-id="581b0-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="581b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="581b0-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="581b0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581b0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="581b0-127">INPUTS</span></span>

## <span data-ttu-id="581b0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="581b0-128">OUTPUTS</span></span>

## <span data-ttu-id="581b0-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="581b0-129">NOTES</span></span>

<span data-ttu-id="581b0-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="581b0-130">ALIASES</span></span>

## <span data-ttu-id="581b0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="581b0-131">RELATED LINKS</span></span>

