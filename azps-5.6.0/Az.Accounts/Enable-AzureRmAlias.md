---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: e99d7643fe67d4102e9f4eef7f9c10f131594948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008181"
---
# <span data-ttu-id="746a5-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="746a5-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="746a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="746a5-102">SYNOPSIS</span></span>
<span data-ttu-id="746a5-103">Engedélyezi az AzureRm előtag-aliasokat az Az-modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="746a5-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="746a5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="746a5-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="746a5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="746a5-105">DESCRIPTION</span></span>
<span data-ttu-id="746a5-106">Engedélyezi az AzureRm előtag-aliasokat az Az-modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="746a5-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="746a5-107">Ha a -Module van megadva, akkor csak a listában szereplő modulokhoz engedélyezettek az aliasok.</span><span class="sxs-lookup"><span data-stu-id="746a5-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="746a5-108">Ellenkező esetben az összes AzureRm-alias engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="746a5-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="746a5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="746a5-109">EXAMPLES</span></span>

### <span data-ttu-id="746a5-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="746a5-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="746a5-111">Engedélyezi az aktuális PowerShell-munkamenet összes AzureRm előtagját.</span><span class="sxs-lookup"><span data-stu-id="746a5-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="746a5-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="746a5-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="746a5-113">Engedélyezi az AzureRm-aliasokat az Az.Accounts modulban az aktuális folyamat és az aktuális felhasználó számára is.</span><span class="sxs-lookup"><span data-stu-id="746a5-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="746a5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="746a5-114">PARAMETERS</span></span>

### <span data-ttu-id="746a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746a5-115">-DefaultProfile</span></span>
<span data-ttu-id="746a5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="746a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="746a5-117">-Module</span><span class="sxs-lookup"><span data-stu-id="746a5-117">-Module</span></span>
<span data-ttu-id="746a5-118">Azt jelzi, hogy mely modulokhoz engedélyezi az aliasokat.</span><span class="sxs-lookup"><span data-stu-id="746a5-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="746a5-119">Ha nincs megadva egyik sincs megadva, az alapértelmezett beállítás az összes modul.</span><span class="sxs-lookup"><span data-stu-id="746a5-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="746a5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="746a5-120">-PassThru</span></span>
<span data-ttu-id="746a5-121">Ha meg van adva, a parancsmag az összes engedélyezett aliast visszaadja</span><span class="sxs-lookup"><span data-stu-id="746a5-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="746a5-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="746a5-122">-Scope</span></span>
<span data-ttu-id="746a5-123">Azt jelzi, hogy milyen hatókör-aliasokat kell engedélyezni.</span><span class="sxs-lookup"><span data-stu-id="746a5-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="746a5-124">Az alapértelmezett érték a "Helyi"</span><span class="sxs-lookup"><span data-stu-id="746a5-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746a5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="746a5-125">-Confirm</span></span>
<span data-ttu-id="746a5-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="746a5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="746a5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="746a5-127">-WhatIf</span></span>
<span data-ttu-id="746a5-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="746a5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="746a5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="746a5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="746a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746a5-130">CommonParameters</span></span>
<span data-ttu-id="746a5-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="746a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746a5-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="746a5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746a5-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="746a5-133">INPUTS</span></span>

### <span data-ttu-id="746a5-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="746a5-134">None</span></span>

## <span data-ttu-id="746a5-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="746a5-135">OUTPUTS</span></span>

### <span data-ttu-id="746a5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="746a5-136">System.String</span></span>

## <span data-ttu-id="746a5-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="746a5-137">NOTES</span></span>

## <span data-ttu-id="746a5-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="746a5-138">RELATED LINKS</span></span>
