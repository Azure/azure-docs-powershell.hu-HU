---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 24862931e19d0e8b8c7b8568aabb6f25cf65f9c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668262"
---
# <span data-ttu-id="2b792-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="2b792-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="2b792-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b792-102">SYNOPSIS</span></span>
<span data-ttu-id="2b792-103">Engedélyezi a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="2b792-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="2b792-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b792-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b792-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b792-105">DESCRIPTION</span></span>
<span data-ttu-id="2b792-106">Engedélyezi a AzureRm előtag-aliasát az as modulokhoz.</span><span class="sxs-lookup"><span data-stu-id="2b792-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="2b792-107">Ha-modult ad meg, csak a listában szereplő modulok lesznek engedélyezve az aliasok.</span><span class="sxs-lookup"><span data-stu-id="2b792-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="2b792-108">Egyéb esetekben az összes AzureRm-alias engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2b792-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="2b792-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2b792-109">EXAMPLES</span></span>

### <span data-ttu-id="2b792-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2b792-110">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="2b792-111">Az aktuális PowerShell-munkamenet összes AzureRm-előjavítását engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="2b792-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="2b792-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2b792-112">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="2b792-113">A AzureRm-aliasok engedélyezése az aktuális folyamat és az aktuális felhasználó esetében.</span><span class="sxs-lookup"><span data-stu-id="2b792-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="2b792-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b792-114">PARAMETERS</span></span>

### <span data-ttu-id="2b792-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b792-115">-DefaultProfile</span></span>
<span data-ttu-id="2b792-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b792-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b792-117">-Modul</span><span class="sxs-lookup"><span data-stu-id="2b792-117">-Module</span></span>
<span data-ttu-id="2b792-118">Meghatározza, hogy mely modulokat engedélyezze az aliasok.</span><span class="sxs-lookup"><span data-stu-id="2b792-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="2b792-119">Ha nincs megadva, az alapértelmezett érték az összes modul.</span><span class="sxs-lookup"><span data-stu-id="2b792-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="2b792-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b792-120">-PassThru</span></span>
<span data-ttu-id="2b792-121">Ha meg van adva, akkor a parancsmag az összes aliast visszaadja.</span><span class="sxs-lookup"><span data-stu-id="2b792-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="2b792-122">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="2b792-122">-Scope</span></span>
<span data-ttu-id="2b792-123">Azt jelzi, hogy milyen hatóköri aliasokat kell engedélyezni.</span><span class="sxs-lookup"><span data-stu-id="2b792-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="2b792-124">Az alapértelmezett érték a "helyi"</span><span class="sxs-lookup"><span data-stu-id="2b792-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="2b792-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b792-125">-Confirm</span></span>
<span data-ttu-id="2b792-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b792-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b792-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b792-127">-WhatIf</span></span>
<span data-ttu-id="2b792-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b792-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b792-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b792-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b792-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b792-130">CommonParameters</span></span>
<span data-ttu-id="2b792-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b792-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b792-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b792-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b792-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b792-133">INPUTS</span></span>

### <span data-ttu-id="2b792-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="2b792-134">None</span></span>

## <span data-ttu-id="2b792-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b792-135">OUTPUTS</span></span>

### <span data-ttu-id="2b792-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2b792-136">System.String</span></span>

## <span data-ttu-id="2b792-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b792-137">NOTES</span></span>

## <span data-ttu-id="2b792-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b792-138">RELATED LINKS</span></span>
