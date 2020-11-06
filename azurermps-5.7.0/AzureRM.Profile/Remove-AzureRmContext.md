---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: cb232bdebacfcb65cf3570854b14c28406d22b12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500472"
---
# <span data-ttu-id="aff7c-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="aff7c-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="aff7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aff7c-102">SYNOPSIS</span></span>
<span data-ttu-id="aff7c-103">Környezet eltávolítása az elérhető környezetek halmazból</span><span class="sxs-lookup"><span data-stu-id="aff7c-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aff7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aff7c-104">SYNTAX</span></span>

### <span data-ttu-id="aff7c-105">RemoveByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aff7c-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aff7c-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="aff7c-106">RemoveByName</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="aff7c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aff7c-107">DESCRIPTION</span></span>
<span data-ttu-id="aff7c-108">Azure-környezet eltávolítása a kontextusok halmazból</span><span class="sxs-lookup"><span data-stu-id="aff7c-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="aff7c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aff7c-109">EXAMPLES</span></span>

### <span data-ttu-id="aff7c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aff7c-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="aff7c-111">Az alapértelmezett nevű környezet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aff7c-111">Remove the context named default</span></span>

## <span data-ttu-id="aff7c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aff7c-112">PARAMETERS</span></span>

### <span data-ttu-id="aff7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff7c-113">-DefaultProfile</span></span>
<span data-ttu-id="aff7c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aff7c-114">The credentials, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff7c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aff7c-115">-Force</span></span>
<span data-ttu-id="aff7c-116">A környezet eltávolítása annak ellenére, hogy a defualt</span><span class="sxs-lookup"><span data-stu-id="aff7c-116">Remove context even if it is the defualt</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff7c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aff7c-117">-InputObject</span></span>
<span data-ttu-id="aff7c-118">Egy környezeti objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="aff7c-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aff7c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aff7c-119">-Name</span></span>
<span data-ttu-id="aff7c-120">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="aff7c-120">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: RemoveByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff7c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aff7c-121">-PassThru</span></span>
<span data-ttu-id="aff7c-122">Az eltávolított környezet visszaküldése</span><span class="sxs-lookup"><span data-stu-id="aff7c-122">Return the removed context</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff7c-123">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="aff7c-123">-Scope</span></span>
<span data-ttu-id="aff7c-124">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="aff7c-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff7c-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aff7c-125">-Confirm</span></span>
<span data-ttu-id="aff7c-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aff7c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff7c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aff7c-127">-WhatIf</span></span>
<span data-ttu-id="aff7c-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aff7c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aff7c-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aff7c-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff7c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff7c-130">CommonParameters</span></span>
<span data-ttu-id="aff7c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aff7c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff7c-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff7c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff7c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aff7c-133">INPUTS</span></span>

### <span data-ttu-id="aff7c-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="aff7c-134">None</span></span>

## <span data-ttu-id="aff7c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aff7c-135">OUTPUTS</span></span>

### <span data-ttu-id="aff7c-136">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="aff7c-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="aff7c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aff7c-137">NOTES</span></span>

## <span data-ttu-id="aff7c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aff7c-138">RELATED LINKS</span></span>

