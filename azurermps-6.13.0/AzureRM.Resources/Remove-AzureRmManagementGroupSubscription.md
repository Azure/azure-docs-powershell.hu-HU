---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: 882583c50db8a4b4473bce829aab120a68478434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492750"
---
# <span data-ttu-id="2b6d7-101">Remove-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="2b6d7-101">Remove-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="2b6d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6d7-103">Új előfizetés eltávolítása egy felügyeleti csoportból.</span><span class="sxs-lookup"><span data-stu-id="2b6d7-103">Removes a Subscription from a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b6d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b6d7-104">SYNTAX</span></span>

```
Remove-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b6d7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b6d7-105">DESCRIPTION</span></span>
<span data-ttu-id="2b6d7-106">A **Remove-AzureRmManagementGroupSubscription** parancsmag felügyeleti csoportból távolítja el az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2b6d7-106">The **Remove-AzureRmManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="2b6d7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2b6d7-107">EXAMPLES</span></span>

### <span data-ttu-id="2b6d7-108">Példa 1 – előfizetés eltávolítása egy felügyeleti csoportból</span><span class="sxs-lookup"><span data-stu-id="2b6d7-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="2b6d7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b6d7-109">PARAMETERS</span></span>

### <span data-ttu-id="2b6d7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6d7-110">-DefaultProfile</span></span>
<span data-ttu-id="2b6d7-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b6d7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6d7-112">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="2b6d7-112">-GroupName</span></span>
<span data-ttu-id="2b6d7-113">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="2b6d7-113">Management Group Id</span></span>

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

### <span data-ttu-id="2b6d7-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b6d7-114">-PassThru</span></span>
<span data-ttu-id="2b6d7-115">Sikeres végrehajtás visszaadása `true`</span><span class="sxs-lookup"><span data-stu-id="2b6d7-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="2b6d7-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b6d7-116">-SubscriptionId</span></span>
<span data-ttu-id="2b6d7-117">A kezeléshez társított előfizetéshez tartozó Witht</span><span class="sxs-lookup"><span data-stu-id="2b6d7-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="2b6d7-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b6d7-118">-Confirm</span></span>
<span data-ttu-id="2b6d7-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b6d7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b6d7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b6d7-120">-WhatIf</span></span>
<span data-ttu-id="2b6d7-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b6d7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b6d7-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b6d7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b6d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6d7-123">CommonParameters</span></span>
<span data-ttu-id="2b6d7-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b6d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6d7-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6d7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6d7-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b6d7-126">INPUTS</span></span>

### <span data-ttu-id="2b6d7-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="2b6d7-127">None</span></span>

## <span data-ttu-id="2b6d7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b6d7-128">OUTPUTS</span></span>

### <span data-ttu-id="2b6d7-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2b6d7-129">System.Boolean</span></span>

## <span data-ttu-id="2b6d7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b6d7-130">NOTES</span></span>

## <span data-ttu-id="2b6d7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b6d7-131">RELATED LINKS</span></span>
