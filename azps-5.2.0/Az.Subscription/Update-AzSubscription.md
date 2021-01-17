---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367918"
---
# <span data-ttu-id="a4b0c-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="a4b0c-101">Update-AzSubscription</span></span>

## <span data-ttu-id="a4b0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b0c-103">Azure-előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="a4b0c-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="a4b0c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a4b0c-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4b0c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a4b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b0c-106">Az **Update-AzSubscription** parancsmag frissíti az Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="a4b0c-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="a4b0c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a4b0c-107">EXAMPLES</span></span>

### <span data-ttu-id="a4b0c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a4b0c-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="a4b0c-109">Az előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="a4b0c-109">Updates the subscription</span></span>

## <span data-ttu-id="a4b0c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4b0c-110">PARAMETERS</span></span>

### <span data-ttu-id="a4b0c-111">-Művelet</span><span class="sxs-lookup"><span data-stu-id="a4b0c-111">-Action</span></span>
<span data-ttu-id="a4b0c-112">Az előfizetésen végre kell hajtanunk egy műveletet</span><span class="sxs-lookup"><span data-stu-id="a4b0c-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="a4b0c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4b0c-113">-AsJob</span></span>
<span data-ttu-id="a4b0c-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a4b0c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4b0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b0c-115">-DefaultProfile</span></span>
<span data-ttu-id="a4b0c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4b0c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4b0c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a4b0c-117">-Name</span></span>
<span data-ttu-id="a4b0c-118">Az előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="a4b0c-118">Name of the subscription</span></span>

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

### <span data-ttu-id="a4b0c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4b0c-119">-SubscriptionId</span></span>
<span data-ttu-id="a4b0c-120">Frissítend kell az előfizetésazonosítót</span><span class="sxs-lookup"><span data-stu-id="a4b0c-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="a4b0c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4b0c-121">-Confirm</span></span>
<span data-ttu-id="a4b0c-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a4b0c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4b0c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4b0c-123">-WhatIf</span></span>
<span data-ttu-id="a4b0c-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a4b0c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4b0c-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4b0c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4b0c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b0c-126">CommonParameters</span></span>
<span data-ttu-id="a4b0c-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b0c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b0c-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4b0c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b0c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4b0c-129">INPUTS</span></span>

### <span data-ttu-id="a4b0c-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="a4b0c-130">None</span></span>

## <span data-ttu-id="a4b0c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4b0c-131">OUTPUTS</span></span>

### <span data-ttu-id="a4b0c-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a4b0c-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="a4b0c-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a4b0c-133">NOTES</span></span>

## <span data-ttu-id="a4b0c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4b0c-134">RELATED LINKS</span></span>
