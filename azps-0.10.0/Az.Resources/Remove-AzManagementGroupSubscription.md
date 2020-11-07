---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: fe3d020bb32e120fe103dd8f90bfbb1d83d9a21d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843261"
---
# <span data-ttu-id="ad0ce-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="ad0ce-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="ad0ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0ce-103">Új előfizetés eltávolítása egy felügyeleti csoportból.</span><span class="sxs-lookup"><span data-stu-id="ad0ce-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="ad0ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad0ce-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad0ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad0ce-105">DESCRIPTION</span></span>
<span data-ttu-id="ad0ce-106">A **Remove-AzManagementGroupSubscription** parancsmag felügyeleti csoportból távolítja el az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ad0ce-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="ad0ce-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ad0ce-107">EXAMPLES</span></span>

### <span data-ttu-id="ad0ce-108">Példa 1 – előfizetés eltávolítása egy felügyeleti csoportból</span><span class="sxs-lookup"><span data-stu-id="ad0ce-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="ad0ce-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad0ce-109">PARAMETERS</span></span>

### <span data-ttu-id="ad0ce-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0ce-110">-DefaultProfile</span></span>
<span data-ttu-id="ad0ce-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad0ce-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad0ce-112">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="ad0ce-112">-GroupName</span></span>
<span data-ttu-id="ad0ce-113">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="ad0ce-113">Management Group Id</span></span>

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

### <span data-ttu-id="ad0ce-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad0ce-114">-PassThru</span></span>
<span data-ttu-id="ad0ce-115">Sikeres végrehajtás visszaadása `true`</span><span class="sxs-lookup"><span data-stu-id="ad0ce-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="ad0ce-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad0ce-116">-SubscriptionId</span></span>
<span data-ttu-id="ad0ce-117">A kezeléshez társított előfizetéshez tartozó Witht</span><span class="sxs-lookup"><span data-stu-id="ad0ce-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="ad0ce-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad0ce-118">-Confirm</span></span>
<span data-ttu-id="ad0ce-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad0ce-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad0ce-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad0ce-120">-WhatIf</span></span>
<span data-ttu-id="ad0ce-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad0ce-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad0ce-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad0ce-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad0ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0ce-123">CommonParameters</span></span>
<span data-ttu-id="ad0ce-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad0ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0ce-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad0ce-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0ce-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad0ce-126">INPUTS</span></span>

### <span data-ttu-id="ad0ce-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="ad0ce-127">None</span></span>

## <span data-ttu-id="ad0ce-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad0ce-128">OUTPUTS</span></span>

### <span data-ttu-id="ad0ce-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad0ce-129">System.Boolean</span></span>

## <span data-ttu-id="ad0ce-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad0ce-130">NOTES</span></span>

## <span data-ttu-id="ad0ce-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad0ce-131">RELATED LINKS</span></span>
