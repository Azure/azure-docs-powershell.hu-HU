---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013033"
---
# <span data-ttu-id="b25b9-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="b25b9-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="b25b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b25b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b25b9-103">Letiltja a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="b25b9-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="b25b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b25b9-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b25b9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b25b9-105">DESCRIPTION</span></span>
<span data-ttu-id="b25b9-106">Letiltja a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="b25b9-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="b25b9-107">Ha-modul van megadva, csak a felsorolt modulok lesznek letiltva.</span><span class="sxs-lookup"><span data-stu-id="b25b9-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="b25b9-108">Máskülönben az összes AzureRm-alias le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="b25b9-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="b25b9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b25b9-109">EXAMPLES</span></span>

### <span data-ttu-id="b25b9-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b25b9-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="b25b9-111">Az aktuális PowerShell-munkamenet összes AzureRm-előjavítását letiltja.</span><span class="sxs-lookup"><span data-stu-id="b25b9-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="b25b9-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b25b9-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="b25b9-113">Letiltja a AzureRm aliasokat az aktuális folyamat és az aktuális felhasználó esetében.</span><span class="sxs-lookup"><span data-stu-id="b25b9-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="b25b9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b25b9-114">PARAMETERS</span></span>

### <span data-ttu-id="b25b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25b9-115">-DefaultProfile</span></span>
<span data-ttu-id="b25b9-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b25b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b25b9-117">-Modul</span><span class="sxs-lookup"><span data-stu-id="b25b9-117">-Module</span></span>
<span data-ttu-id="b25b9-118">Azt jelzi, hogy mely modulokat tiltsa le az aliasok.</span><span class="sxs-lookup"><span data-stu-id="b25b9-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="b25b9-119">Ha a none érték van megadva, az alapértelmezett érték az összes engedélyezett modul.</span><span class="sxs-lookup"><span data-stu-id="b25b9-119">If none are specified, default is all enabled modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25b9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b25b9-120">-PassThru</span></span>
<span data-ttu-id="b25b9-121">Ha meg van adva, akkor a parancsmag minden letiltott aliast visszaad</span><span class="sxs-lookup"><span data-stu-id="b25b9-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="b25b9-122">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="b25b9-122">-Scope</span></span>
<span data-ttu-id="b25b9-123">Azt jelzi, hogy a hatókör-aliasokat le kell tiltani.</span><span class="sxs-lookup"><span data-stu-id="b25b9-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="b25b9-124">Az alapértelmezett érték a "folyamat"</span><span class="sxs-lookup"><span data-stu-id="b25b9-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25b9-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b25b9-125">-Confirm</span></span>
<span data-ttu-id="b25b9-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b25b9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b25b9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b25b9-127">-WhatIf</span></span>
<span data-ttu-id="b25b9-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b25b9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b25b9-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b25b9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b25b9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25b9-130">CommonParameters</span></span>
<span data-ttu-id="b25b9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b25b9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25b9-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b25b9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25b9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b25b9-133">INPUTS</span></span>

### <span data-ttu-id="b25b9-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="b25b9-134">None</span></span>

## <span data-ttu-id="b25b9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b25b9-135">OUTPUTS</span></span>

### <span data-ttu-id="b25b9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b25b9-136">System.String</span></span>

## <span data-ttu-id="b25b9-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b25b9-137">NOTES</span></span>

## <span data-ttu-id="b25b9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b25b9-138">RELATED LINKS</span></span>
