---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182260"
---
# <span data-ttu-id="b07be-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="b07be-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="b07be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b07be-102">SYNOPSIS</span></span>
<span data-ttu-id="b07be-103">Távolítsa el a Windows virtuális asztali regisztrációs adatait.</span><span class="sxs-lookup"><span data-stu-id="b07be-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="b07be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b07be-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b07be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b07be-105">DESCRIPTION</span></span>
<span data-ttu-id="b07be-106">Távolítsa el a Windows virtuális asztali regisztrációs adatait.</span><span class="sxs-lookup"><span data-stu-id="b07be-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="b07be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b07be-107">EXAMPLES</span></span>

### <span data-ttu-id="b07be-108">Példa 1: a Windows virtuális asztali regisztrációs jogkivonat törlése</span><span class="sxs-lookup"><span data-stu-id="b07be-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="b07be-109">Ez a parancs törli a Windows virtuális asztali regisztrációs tokent egy állomás-készletben.</span><span class="sxs-lookup"><span data-stu-id="b07be-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="b07be-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b07be-110">PARAMETERS</span></span>

### <span data-ttu-id="b07be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07be-111">-DefaultProfile</span></span>
<span data-ttu-id="b07be-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b07be-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b07be-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b07be-113">-HostPoolName</span></span>
<span data-ttu-id="b07be-114">Állomáslista neve</span><span class="sxs-lookup"><span data-stu-id="b07be-114">Host Pool Name</span></span>

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

### <span data-ttu-id="b07be-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07be-115">-ResourceGroupName</span></span>
<span data-ttu-id="b07be-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b07be-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b07be-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b07be-117">-SubscriptionId</span></span>
<span data-ttu-id="b07be-118">Súgó a foo 1 készülékhez</span><span class="sxs-lookup"><span data-stu-id="b07be-118">help foo 1</span></span>

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

### <span data-ttu-id="b07be-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b07be-119">-Confirm</span></span>
<span data-ttu-id="b07be-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b07be-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b07be-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b07be-121">-WhatIf</span></span>
<span data-ttu-id="b07be-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b07be-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b07be-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b07be-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b07be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07be-124">CommonParameters</span></span>
<span data-ttu-id="b07be-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b07be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07be-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b07be-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07be-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b07be-127">INPUTS</span></span>

## <span data-ttu-id="b07be-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b07be-128">OUTPUTS</span></span>

## <span data-ttu-id="b07be-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b07be-129">NOTES</span></span>

<span data-ttu-id="b07be-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b07be-130">ALIASES</span></span>

## <span data-ttu-id="b07be-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b07be-131">RELATED LINKS</span></span>

