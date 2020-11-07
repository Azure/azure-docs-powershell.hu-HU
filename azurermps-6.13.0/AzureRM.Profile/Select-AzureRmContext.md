---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/select-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: 86d236a3601dfac9467b5da01cd297255ac98312
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673139"
---
# <span data-ttu-id="dbeed-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="dbeed-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="dbeed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dbeed-102">SYNOPSIS</span></span>
<span data-ttu-id="dbeed-103">Előfizetés és fiók kiválasztása az Azure PowerShell-parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="dbeed-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbeed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dbeed-104">SYNTAX</span></span>

### <span data-ttu-id="dbeed-105">SelectByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dbeed-105">SelectByInputObject (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbeed-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="dbeed-106">SelectByName</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="dbeed-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dbeed-107">DESCRIPTION</span></span>
<span data-ttu-id="dbeed-108">Jelölje ki az Azure PowerShell-parancsmagokban a Target (vagy a fiók vagy bérlő) előfizetést.</span><span class="sxs-lookup"><span data-stu-id="dbeed-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="dbeed-109">A parancsmag után a jövőbeli parancsmagok a kijelölt környezetet fogják célozni.</span><span class="sxs-lookup"><span data-stu-id="dbeed-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="dbeed-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dbeed-110">EXAMPLES</span></span>

### <span data-ttu-id="dbeed-111">1. példa: névvel ellátott környezet megcélzása</span><span class="sxs-lookup"><span data-stu-id="dbeed-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="dbeed-112">A következő Azure PowerShell-parancsmagok megcélzása az ügyfél, a bérlő és az előfizetés munkakörnyezetében.</span><span class="sxs-lookup"><span data-stu-id="dbeed-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="dbeed-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dbeed-113">PARAMETERS</span></span>

### <span data-ttu-id="dbeed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbeed-114">-DefaultProfile</span></span>
<span data-ttu-id="dbeed-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dbeed-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbeed-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbeed-116">-InputObject</span></span>
<span data-ttu-id="dbeed-117">Egy környezeti objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="dbeed-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbeed-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dbeed-118">-Name</span></span>
<span data-ttu-id="dbeed-119">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="dbeed-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbeed-120">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="dbeed-120">-Scope</span></span>
<span data-ttu-id="dbeed-121">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="dbeed-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="dbeed-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dbeed-122">-Confirm</span></span>
<span data-ttu-id="dbeed-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dbeed-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbeed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbeed-124">-WhatIf</span></span>
<span data-ttu-id="dbeed-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dbeed-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbeed-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dbeed-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbeed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbeed-127">CommonParameters</span></span>
<span data-ttu-id="dbeed-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dbeed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbeed-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbeed-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbeed-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbeed-130">INPUTS</span></span>

### <span data-ttu-id="dbeed-131">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="dbeed-131">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="dbeed-132">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dbeed-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="dbeed-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbeed-133">OUTPUTS</span></span>

### <span data-ttu-id="dbeed-134">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="dbeed-134">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="dbeed-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dbeed-135">NOTES</span></span>

## <span data-ttu-id="dbeed-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbeed-136">RELATED LINKS</span></span>
