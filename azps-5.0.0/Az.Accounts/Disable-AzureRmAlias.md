---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193980"
---
# <span data-ttu-id="8e16c-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="8e16c-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="8e16c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e16c-102">SYNOPSIS</span></span>
<span data-ttu-id="8e16c-103">Letiltja a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="8e16c-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="8e16c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e16c-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e16c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e16c-105">DESCRIPTION</span></span>
<span data-ttu-id="8e16c-106">Letiltja a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="8e16c-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="8e16c-107">Ha-modul van megadva, csak a felsorolt modulok lesznek letiltva.</span><span class="sxs-lookup"><span data-stu-id="8e16c-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="8e16c-108">Máskülönben az összes AzureRm-alias le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="8e16c-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="8e16c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8e16c-109">EXAMPLES</span></span>

### <span data-ttu-id="8e16c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8e16c-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="8e16c-111">Az aktuális PowerShell-munkamenet összes AzureRm-előjavítását letiltja.</span><span class="sxs-lookup"><span data-stu-id="8e16c-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="8e16c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8e16c-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="8e16c-113">Letiltja a AzureRm aliasokat az aktuális folyamat és az aktuális felhasználó esetében.</span><span class="sxs-lookup"><span data-stu-id="8e16c-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="8e16c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e16c-114">PARAMETERS</span></span>

### <span data-ttu-id="8e16c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e16c-115">-DefaultProfile</span></span>
<span data-ttu-id="8e16c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e16c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e16c-117">-Modul</span><span class="sxs-lookup"><span data-stu-id="8e16c-117">-Module</span></span>
<span data-ttu-id="8e16c-118">Azt jelzi, hogy mely modulokat tiltsa le az aliasok.</span><span class="sxs-lookup"><span data-stu-id="8e16c-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="8e16c-119">Ha a none érték van megadva, az alapértelmezett érték az összes engedélyezett modul.</span><span class="sxs-lookup"><span data-stu-id="8e16c-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="8e16c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e16c-120">-PassThru</span></span>
<span data-ttu-id="8e16c-121">Ha meg van adva, akkor a parancsmag minden letiltott aliast visszaad</span><span class="sxs-lookup"><span data-stu-id="8e16c-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="8e16c-122">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="8e16c-122">-Scope</span></span>
<span data-ttu-id="8e16c-123">Azt jelzi, hogy a hatókör-aliasokat le kell tiltani.</span><span class="sxs-lookup"><span data-stu-id="8e16c-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="8e16c-124">Az alapértelmezett érték a "folyamat"</span><span class="sxs-lookup"><span data-stu-id="8e16c-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="8e16c-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e16c-125">-Confirm</span></span>
<span data-ttu-id="8e16c-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e16c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e16c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e16c-127">-WhatIf</span></span>
<span data-ttu-id="8e16c-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e16c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e16c-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e16c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e16c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e16c-130">CommonParameters</span></span>
<span data-ttu-id="8e16c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e16c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e16c-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e16c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e16c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e16c-133">INPUTS</span></span>

### <span data-ttu-id="8e16c-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e16c-134">None</span></span>

## <span data-ttu-id="8e16c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e16c-135">OUTPUTS</span></span>

### <span data-ttu-id="8e16c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8e16c-136">System.String</span></span>

## <span data-ttu-id="8e16c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e16c-137">NOTES</span></span>

## <span data-ttu-id="8e16c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e16c-138">RELATED LINKS</span></span>
