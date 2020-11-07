---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: 5450939ba5d0dc2fb1ae6c475d51b6fc9187082c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679054"
---
# <span data-ttu-id="43c44-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="43c44-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="43c44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43c44-102">SYNOPSIS</span></span>
<span data-ttu-id="43c44-103">Előfizetés és fiók kiválasztása az Azure PowerShell-parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="43c44-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43c44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43c44-104">SYNTAX</span></span>

### <span data-ttu-id="43c44-105">Beviteli objektum (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43c44-105">Input Object (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43c44-106">Környezeti név</span><span class="sxs-lookup"><span data-stu-id="43c44-106">Context Name</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="43c44-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="43c44-107">DESCRIPTION</span></span>
<span data-ttu-id="43c44-108">Jelölje ki az Azure PowerShell-parancsmagokban a Target (vagy a fiók vagy bérlő) előfizetést.</span><span class="sxs-lookup"><span data-stu-id="43c44-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="43c44-109">A parancsmag után a jövőbeli parancsmagok a kijelölt környezetet fogják célozni.</span><span class="sxs-lookup"><span data-stu-id="43c44-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="43c44-110">Példák</span><span class="sxs-lookup"><span data-stu-id="43c44-110">EXAMPLES</span></span>

### <span data-ttu-id="43c44-111">1. példa: névvel ellátott környezet megcélzása</span><span class="sxs-lookup"><span data-stu-id="43c44-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="43c44-112">A következő Azure PowerShell-parancsmagok megcélzása az ügyfél, a bérlő és az előfizetés munkakörnyezetében.</span><span class="sxs-lookup"><span data-stu-id="43c44-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="43c44-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43c44-113">PARAMETERS</span></span>

### <span data-ttu-id="43c44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c44-114">-DefaultProfile</span></span>
<span data-ttu-id="43c44-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43c44-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43c44-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43c44-116">-InputObject</span></span>
<span data-ttu-id="43c44-117">Egy környezeti objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="43c44-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43c44-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43c44-118">-Name</span></span>
<span data-ttu-id="43c44-119">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="43c44-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c44-120">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="43c44-120">-Scope</span></span>
<span data-ttu-id="43c44-121">A környezeti változások hatókörét határozza meg, például a wheher módosítása csak a cusrrent folyamatra, illetve a felhasználó által indított összes munkamenetre érvényes.</span><span class="sxs-lookup"><span data-stu-id="43c44-121">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="43c44-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43c44-122">-Confirm</span></span>
<span data-ttu-id="43c44-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43c44-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43c44-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43c44-124">-WhatIf</span></span>
<span data-ttu-id="43c44-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43c44-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43c44-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43c44-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43c44-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c44-127">CommonParameters</span></span>
<span data-ttu-id="43c44-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43c44-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c44-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c44-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c44-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43c44-130">INPUTS</span></span>

### <span data-ttu-id="43c44-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="43c44-131">None</span></span>

## <span data-ttu-id="43c44-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43c44-132">OUTPUTS</span></span>

### <span data-ttu-id="43c44-133">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="43c44-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="43c44-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43c44-134">NOTES</span></span>

## <span data-ttu-id="43c44-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43c44-135">RELATED LINKS</span></span>

