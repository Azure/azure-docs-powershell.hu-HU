---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: a5faa240970f29266b8abd85c3d4f70a113fa8c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838143"
---
# <span data-ttu-id="9004c-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="9004c-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="9004c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9004c-102">SYNOPSIS</span></span>
<span data-ttu-id="9004c-103">Előfizetést ad hozzá egy felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="9004c-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="9004c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9004c-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9004c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9004c-105">DESCRIPTION</span></span>
<span data-ttu-id="9004c-106">A **New-AzManagementGroupSubscription** parancsmag előfizetést ad hozzá egy felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="9004c-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="9004c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9004c-107">EXAMPLES</span></span>

### <span data-ttu-id="9004c-108">1. példa: előfizetés hozzáadása felügyeleti csoporthoz</span><span class="sxs-lookup"><span data-stu-id="9004c-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="9004c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9004c-109">PARAMETERS</span></span>

### <span data-ttu-id="9004c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9004c-110">-DefaultProfile</span></span>
<span data-ttu-id="9004c-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9004c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9004c-112">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="9004c-112">-GroupName</span></span>
<span data-ttu-id="9004c-113">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="9004c-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9004c-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9004c-114">-PassThru</span></span>
<span data-ttu-id="9004c-115">Sikeres végrehajtás visszaadása `true`</span><span class="sxs-lookup"><span data-stu-id="9004c-115">Return `true` on successful execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9004c-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9004c-116">-SubscriptionId</span></span>
<span data-ttu-id="9004c-117">A kezeléshez társított előfizetés előfizetési azonosítója</span><span class="sxs-lookup"><span data-stu-id="9004c-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9004c-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9004c-118">-Confirm</span></span>
<span data-ttu-id="9004c-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9004c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9004c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9004c-120">-WhatIf</span></span>
<span data-ttu-id="9004c-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9004c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9004c-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9004c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9004c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9004c-123">CommonParameters</span></span>
<span data-ttu-id="9004c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9004c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9004c-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9004c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9004c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9004c-126">INPUTS</span></span>

### <span data-ttu-id="9004c-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="9004c-127">None</span></span>

## <span data-ttu-id="9004c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9004c-128">OUTPUTS</span></span>

### <span data-ttu-id="9004c-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9004c-129">System.Boolean</span></span>

## <span data-ttu-id="9004c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9004c-130">NOTES</span></span>

## <span data-ttu-id="9004c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9004c-131">RELATED LINKS</span></span>
