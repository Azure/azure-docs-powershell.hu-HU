---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 6a530a0e20f3e69540320ad3eab8b8cc7f37b5af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162666"
---
# <span data-ttu-id="94de8-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="94de8-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="94de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94de8-102">SYNOPSIS</span></span>
<span data-ttu-id="94de8-103">Engedélyezi az AzureRm előtag-aliasokat az Az-modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="94de8-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="94de8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94de8-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94de8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94de8-105">DESCRIPTION</span></span>
<span data-ttu-id="94de8-106">Engedélyezi az AzureRm előtag-aliasokat az Az-modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="94de8-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="94de8-107">Ha a -Module van megadva, akkor csak a listában szereplő modulokhoz engedélyezettek az aliasok.</span><span class="sxs-lookup"><span data-stu-id="94de8-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="94de8-108">Ellenkező esetben az összes AzureRm-alias engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="94de8-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="94de8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94de8-109">EXAMPLES</span></span>

### <span data-ttu-id="94de8-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="94de8-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="94de8-111">Engedélyezi az aktuális PowerShell-munkamenet összes AzureRm előtagját.</span><span class="sxs-lookup"><span data-stu-id="94de8-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="94de8-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="94de8-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="94de8-113">Engedélyezi az AzureRm-aliasokat az Az.Accounts modulban az aktuális folyamat és az aktuális felhasználó számára is.</span><span class="sxs-lookup"><span data-stu-id="94de8-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="94de8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94de8-114">PARAMETERS</span></span>

### <span data-ttu-id="94de8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94de8-115">-DefaultProfile</span></span>
<span data-ttu-id="94de8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94de8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94de8-117">-Module</span><span class="sxs-lookup"><span data-stu-id="94de8-117">-Module</span></span>
<span data-ttu-id="94de8-118">Azt jelzi, hogy mely modulokhoz engedélyezi az aliasokat.</span><span class="sxs-lookup"><span data-stu-id="94de8-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="94de8-119">Ha nincs megadva egyik sincs megadva, az alapértelmezett beállítás az összes modul.</span><span class="sxs-lookup"><span data-stu-id="94de8-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="94de8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94de8-120">-PassThru</span></span>
<span data-ttu-id="94de8-121">Ha meg van adva, a parancsmag az összes engedélyezett aliast visszaadja</span><span class="sxs-lookup"><span data-stu-id="94de8-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="94de8-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="94de8-122">-Scope</span></span>
<span data-ttu-id="94de8-123">Azt jelzi, hogy milyen hatókör-aliasokat kell engedélyezni.</span><span class="sxs-lookup"><span data-stu-id="94de8-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="94de8-124">Az alapértelmezett érték a "Helyi"</span><span class="sxs-lookup"><span data-stu-id="94de8-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="94de8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94de8-125">-Confirm</span></span>
<span data-ttu-id="94de8-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="94de8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94de8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94de8-127">-WhatIf</span></span>
<span data-ttu-id="94de8-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="94de8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94de8-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94de8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94de8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94de8-130">CommonParameters</span></span>
<span data-ttu-id="94de8-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94de8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94de8-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94de8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94de8-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94de8-133">INPUTS</span></span>

### <span data-ttu-id="94de8-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="94de8-134">None</span></span>

## <span data-ttu-id="94de8-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94de8-135">OUTPUTS</span></span>

### <span data-ttu-id="94de8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="94de8-136">System.String</span></span>

## <span data-ttu-id="94de8-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94de8-137">NOTES</span></span>

## <span data-ttu-id="94de8-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94de8-138">RELATED LINKS</span></span>
