---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327833"
---
# <span data-ttu-id="db66f-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="db66f-101">Clear-AzContext</span></span>

## <span data-ttu-id="db66f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db66f-102">SYNOPSIS</span></span>
<span data-ttu-id="db66f-103">Távolítsa el az Összes Azure-hitelesítő adatokat, fiókot és előfizetési információt.</span><span class="sxs-lookup"><span data-stu-id="db66f-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="db66f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db66f-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db66f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db66f-105">DESCRIPTION</span></span>
<span data-ttu-id="db66f-106">Távolítsa el az Azure-beli hitelesítő adatokat, fiókadatokat és előfizetési adatokat.</span><span class="sxs-lookup"><span data-stu-id="db66f-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="db66f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db66f-107">EXAMPLES</span></span>

### <span data-ttu-id="db66f-108">1. példa: Globális környezet egyértelművé</span><span class="sxs-lookup"><span data-stu-id="db66f-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="db66f-109">Távolítsa el az összes fiók-, előfizetés- és hitelesítőadat-információt bármely PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="db66f-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="db66f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db66f-110">PARAMETERS</span></span>

### <span data-ttu-id="db66f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db66f-111">-DefaultProfile</span></span>
<span data-ttu-id="db66f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="db66f-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db66f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="db66f-113">-Force</span></span>
<span data-ttu-id="db66f-114">Az összes felhasználó és csoport törlése a globális hatókörből rákérdezés nélkül</span><span class="sxs-lookup"><span data-stu-id="db66f-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="db66f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db66f-115">-PassThru</span></span>
<span data-ttu-id="db66f-116">Sikeres vagy sikertelenséget jelző értéket ad vissza</span><span class="sxs-lookup"><span data-stu-id="db66f-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="db66f-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="db66f-117">-Scope</span></span>
<span data-ttu-id="db66f-118">Csak az aktuális PowerShell-munkamenet környezetének vagy az összes munkamenetnek a környezetét törölje.</span><span class="sxs-lookup"><span data-stu-id="db66f-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="db66f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db66f-119">-Confirm</span></span>
<span data-ttu-id="db66f-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db66f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db66f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db66f-121">-WhatIf</span></span>
<span data-ttu-id="db66f-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db66f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db66f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db66f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db66f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db66f-124">CommonParameters</span></span>
<span data-ttu-id="db66f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db66f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db66f-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db66f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db66f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db66f-127">INPUTS</span></span>

### <span data-ttu-id="db66f-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="db66f-128">None</span></span>

## <span data-ttu-id="db66f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db66f-129">OUTPUTS</span></span>

### <span data-ttu-id="db66f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db66f-130">System.Boolean</span></span>

## <span data-ttu-id="db66f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db66f-131">NOTES</span></span>

## <span data-ttu-id="db66f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db66f-132">RELATED LINKS</span></span>
