---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: 6f3ff6868a34eefc9b7cd45cf371b6ef29dbf469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011998"
---
# <span data-ttu-id="ba1e2-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="ba1e2-101">Select-AzContext</span></span>

## <span data-ttu-id="ba1e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1e2-103">Előfizetés és fiók kiválasztása az Azure PowerShell-parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="ba1e2-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="ba1e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba1e2-104">SYNTAX</span></span>

### <span data-ttu-id="ba1e2-105">SelectByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba1e2-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba1e2-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="ba1e2-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="ba1e2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba1e2-107">DESCRIPTION</span></span>
<span data-ttu-id="ba1e2-108">Jelölje ki az Azure PowerShell-parancsmagokban a Target (vagy a fiók vagy bérlő) előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ba1e2-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="ba1e2-109">A parancsmag után a jövőbeli parancsmagok a kijelölt környezetet fogják célozni.</span><span class="sxs-lookup"><span data-stu-id="ba1e2-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="ba1e2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ba1e2-110">EXAMPLES</span></span>

### <span data-ttu-id="ba1e2-111">1. példa: névvel ellátott környezet megcélzása</span><span class="sxs-lookup"><span data-stu-id="ba1e2-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="ba1e2-112">A következő Azure PowerShell-parancsmagok megcélzása az ügyfél, a bérlő és az előfizetés munkakörnyezetében.</span><span class="sxs-lookup"><span data-stu-id="ba1e2-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="ba1e2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba1e2-113">PARAMETERS</span></span>

### <span data-ttu-id="ba1e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba1e2-114">-DefaultProfile</span></span>
<span data-ttu-id="ba1e2-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ba1e2-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba1e2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba1e2-116">-InputObject</span></span>
<span data-ttu-id="ba1e2-117">Egy környezeti objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="ba1e2-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba1e2-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba1e2-118">-Name</span></span>
<span data-ttu-id="ba1e2-119">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="ba1e2-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1e2-120">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="ba1e2-120">-Scope</span></span>
<span data-ttu-id="ba1e2-121">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="ba1e2-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1e2-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba1e2-122">-Confirm</span></span>
<span data-ttu-id="ba1e2-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba1e2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba1e2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba1e2-124">-WhatIf</span></span>
<span data-ttu-id="ba1e2-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba1e2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba1e2-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba1e2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba1e2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1e2-127">CommonParameters</span></span>
<span data-ttu-id="ba1e2-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba1e2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1e2-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba1e2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1e2-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba1e2-130">INPUTS</span></span>

### <span data-ttu-id="ba1e2-131">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ba1e2-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="ba1e2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba1e2-132">OUTPUTS</span></span>

### <span data-ttu-id="ba1e2-133">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ba1e2-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="ba1e2-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba1e2-134">NOTES</span></span>

## <span data-ttu-id="ba1e2-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba1e2-135">RELATED LINKS</span></span>
