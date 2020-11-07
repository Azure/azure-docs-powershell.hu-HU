---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 5a640bf705040c3bb8ed0f7dc985693b2e57c873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680247"
---
# <span data-ttu-id="fa45e-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="fa45e-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="fa45e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa45e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa45e-103">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fa45e-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa45e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa45e-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa45e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa45e-105">DESCRIPTION</span></span>
<span data-ttu-id="fa45e-106">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fa45e-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="fa45e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fa45e-107">EXAMPLES</span></span>

### <span data-ttu-id="fa45e-108">Globális környezet törlése</span><span class="sxs-lookup"><span data-stu-id="fa45e-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="fa45e-109">Az összes fiók, előfizetés és hitelesítőadat-adat eltávolítása bármely PowerShell-munkamenethez</span><span class="sxs-lookup"><span data-stu-id="fa45e-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="fa45e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa45e-110">PARAMETERS</span></span>

### <span data-ttu-id="fa45e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa45e-111">-DefaultProfile</span></span>
<span data-ttu-id="fa45e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fa45e-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa45e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fa45e-113">-Force</span></span>
<span data-ttu-id="fa45e-114">Az összes felhasználó és csoport törlése a globális hatókörből figyelmeztetés nélkül</span><span class="sxs-lookup"><span data-stu-id="fa45e-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="fa45e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa45e-115">-PassThru</span></span>
<span data-ttu-id="fa45e-116">Sikert vagy kudarcot jelző érték visszaadása</span><span class="sxs-lookup"><span data-stu-id="fa45e-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="fa45e-117">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="fa45e-117">-Scope</span></span>
<span data-ttu-id="fa45e-118">Törölje a csak az aktuális PowerShell-munkamenet vagy az összes munkamenet környezetét.</span><span class="sxs-lookup"><span data-stu-id="fa45e-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa45e-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fa45e-119">-Confirm</span></span>
<span data-ttu-id="fa45e-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa45e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa45e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa45e-121">-WhatIf</span></span>
<span data-ttu-id="fa45e-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fa45e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa45e-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa45e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa45e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa45e-124">CommonParameters</span></span>
<span data-ttu-id="fa45e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa45e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa45e-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa45e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa45e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa45e-127">INPUTS</span></span>

### <span data-ttu-id="fa45e-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="fa45e-128">None</span></span>

## <span data-ttu-id="fa45e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa45e-129">OUTPUTS</span></span>

### <span data-ttu-id="fa45e-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa45e-130">System.Boolean</span></span>
<span data-ttu-id="fa45e-131">Igaz, ha a környezet sikeres volt, máskülönben hamis.</span><span class="sxs-lookup"><span data-stu-id="fa45e-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="fa45e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa45e-132">NOTES</span></span>

## <span data-ttu-id="fa45e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa45e-133">RELATED LINKS</span></span>

