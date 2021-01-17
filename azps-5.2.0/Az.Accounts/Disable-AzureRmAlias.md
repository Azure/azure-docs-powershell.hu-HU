---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367316"
---
# <span data-ttu-id="41497-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="41497-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="41497-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41497-102">SYNOPSIS</span></span>
<span data-ttu-id="41497-103">Letiltja az AzureRm előtag-aliasokat az Az modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="41497-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="41497-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41497-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41497-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41497-105">DESCRIPTION</span></span>
<span data-ttu-id="41497-106">Letiltja az AzureRm előtag-aliasokat az Az modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="41497-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="41497-107">Ha a -Module van megadva, akkor csak a listában szereplő modulokhoz lesznek letiltva az aliasok.</span><span class="sxs-lookup"><span data-stu-id="41497-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="41497-108">Ellenkező esetben az összes AzureRm-alias le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="41497-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="41497-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41497-109">EXAMPLES</span></span>

### <span data-ttu-id="41497-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="41497-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="41497-111">Letiltja az aktuális PowerShell-munkamenet összes AzureRm-előtagját.</span><span class="sxs-lookup"><span data-stu-id="41497-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="41497-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="41497-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="41497-113">Letiltja az AzureRm aliasokat az Az.Accounts modulban az aktuális folyamatra és az aktuális felhasználóra is.</span><span class="sxs-lookup"><span data-stu-id="41497-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="41497-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41497-114">PARAMETERS</span></span>

### <span data-ttu-id="41497-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41497-115">-DefaultProfile</span></span>
<span data-ttu-id="41497-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41497-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41497-117">-Module</span><span class="sxs-lookup"><span data-stu-id="41497-117">-Module</span></span>
<span data-ttu-id="41497-118">Azt jelzi, hogy mely modulokhoz tiltsa le az aliasokat.</span><span class="sxs-lookup"><span data-stu-id="41497-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="41497-119">Ha nincs megadva egyik sincs megadva, az alapértelmezett beállítás az összes engedélyezett modul.</span><span class="sxs-lookup"><span data-stu-id="41497-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="41497-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41497-120">-PassThru</span></span>
<span data-ttu-id="41497-121">Ha meg van adva, a parancsmag az összes letiltott aliast visszaadja</span><span class="sxs-lookup"><span data-stu-id="41497-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="41497-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="41497-122">-Scope</span></span>
<span data-ttu-id="41497-123">Azt jelzi, hogy milyen hatókör-aliasokat kell letiltani.</span><span class="sxs-lookup"><span data-stu-id="41497-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="41497-124">Az alapértelmezett érték a "Folyamat".</span><span class="sxs-lookup"><span data-stu-id="41497-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="41497-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41497-125">-Confirm</span></span>
<span data-ttu-id="41497-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="41497-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41497-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41497-127">-WhatIf</span></span>
<span data-ttu-id="41497-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="41497-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41497-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41497-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41497-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41497-130">CommonParameters</span></span>
<span data-ttu-id="41497-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41497-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41497-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41497-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41497-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41497-133">INPUTS</span></span>

### <span data-ttu-id="41497-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="41497-134">None</span></span>

## <span data-ttu-id="41497-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41497-135">OUTPUTS</span></span>

### <span data-ttu-id="41497-136">System.String</span><span class="sxs-lookup"><span data-stu-id="41497-136">System.String</span></span>

## <span data-ttu-id="41497-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41497-137">NOTES</span></span>

## <span data-ttu-id="41497-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41497-138">RELATED LINKS</span></span>
