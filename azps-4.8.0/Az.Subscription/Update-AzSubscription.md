---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: b83d186089558b18cbd511cdc5d0b407a997f635
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181242"
---
# <span data-ttu-id="ad30e-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="ad30e-101">Update-AzSubscription</span></span>

## <span data-ttu-id="ad30e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad30e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad30e-103">Azure-előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="ad30e-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="ad30e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad30e-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad30e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad30e-105">DESCRIPTION</span></span>
<span data-ttu-id="ad30e-106">Az **Update-AzSubscription** parancsmag Azure-előfizetést frissít</span><span class="sxs-lookup"><span data-stu-id="ad30e-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="ad30e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ad30e-107">EXAMPLES</span></span>

### <span data-ttu-id="ad30e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad30e-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled

```
<span data-ttu-id="ad30e-109">Az előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="ad30e-109">Updates the subscription</span></span>

## <span data-ttu-id="ad30e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad30e-110">PARAMETERS</span></span>

### <span data-ttu-id="ad30e-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="ad30e-111">-Action</span></span>
<span data-ttu-id="ad30e-112">Az előfizetésben végrehajtandó művelet</span><span class="sxs-lookup"><span data-stu-id="ad30e-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="ad30e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad30e-113">-AsJob</span></span>
<span data-ttu-id="ad30e-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ad30e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad30e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad30e-115">-DefaultProfile</span></span>
<span data-ttu-id="ad30e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad30e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad30e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad30e-117">-Name</span></span>
<span data-ttu-id="ad30e-118">Az előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="ad30e-118">Name of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad30e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad30e-119">-SubscriptionId</span></span>
<span data-ttu-id="ad30e-120">Frissítendő előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="ad30e-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="ad30e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad30e-121">-Confirm</span></span>
<span data-ttu-id="ad30e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad30e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad30e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad30e-123">-WhatIf</span></span>
<span data-ttu-id="ad30e-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad30e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad30e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad30e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad30e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad30e-126">CommonParameters</span></span>
<span data-ttu-id="ad30e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad30e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad30e-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad30e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad30e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad30e-129">INPUTS</span></span>

### <span data-ttu-id="ad30e-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="ad30e-130">None</span></span>

## <span data-ttu-id="ad30e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad30e-131">OUTPUTS</span></span>

### <span data-ttu-id="ad30e-132">Microsoft. Azure. Command. előfizetés. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ad30e-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="ad30e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad30e-133">NOTES</span></span>

## <span data-ttu-id="ad30e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad30e-134">RELATED LINKS</span></span>
