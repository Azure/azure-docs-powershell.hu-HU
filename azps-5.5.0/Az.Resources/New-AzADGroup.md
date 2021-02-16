---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153683"
---
# <span data-ttu-id="365c7-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="365c7-101">New-AzADGroup</span></span>

## <span data-ttu-id="365c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="365c7-102">SYNOPSIS</span></span>
<span data-ttu-id="365c7-103">Új Active Directory-csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="365c7-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="365c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="365c7-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="365c7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="365c7-105">DESCRIPTION</span></span>
<span data-ttu-id="365c7-106">Új Active Directory-csoportot hoz létre. Az alábbiakban a szükséges engedélyeket olvashatja:</span><span class="sxs-lookup"><span data-stu-id="365c7-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="365c7-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="365c7-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="365c7-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="365c7-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="365c7-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="365c7-109">Microsoft Graph</span></span>
  - <span data-ttu-id="365c7-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="365c7-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="365c7-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="365c7-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="365c7-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="365c7-112">EXAMPLES</span></span>

### <span data-ttu-id="365c7-113">1. példa: Új AD-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="365c7-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="365c7-114">Létrehoz egy új AD csoportot a "MyGroupDisplayName" névvel és a "MyGroupNick" becenévvel.</span><span class="sxs-lookup"><span data-stu-id="365c7-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="365c7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="365c7-115">PARAMETERS</span></span>

### <span data-ttu-id="365c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365c7-116">-DefaultProfile</span></span>
<span data-ttu-id="365c7-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="365c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="365c7-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="365c7-118">-Description</span></span>
<span data-ttu-id="365c7-119">A csoport leírása.</span><span class="sxs-lookup"><span data-stu-id="365c7-119">The description for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365c7-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="365c7-120">-DisplayName</span></span>
<span data-ttu-id="365c7-121">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="365c7-121">The display name for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365c7-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="365c7-122">-MailNickname</span></span>
<span data-ttu-id="365c7-123">A csoport e-mail-beceneve.</span><span class="sxs-lookup"><span data-stu-id="365c7-123">The mail nickname for the group.</span></span> <span data-ttu-id="365c7-124">Nem tartalmazhatja a @ jelet.</span><span class="sxs-lookup"><span data-stu-id="365c7-124">Cannot contain the @ sign.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365c7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="365c7-125">-Confirm</span></span>
<span data-ttu-id="365c7-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="365c7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="365c7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="365c7-127">-WhatIf</span></span>
<span data-ttu-id="365c7-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="365c7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="365c7-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="365c7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="365c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365c7-130">CommonParameters</span></span>
<span data-ttu-id="365c7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365c7-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="365c7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365c7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="365c7-133">INPUTS</span></span>

### <span data-ttu-id="365c7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="365c7-134">System.String</span></span>

## <span data-ttu-id="365c7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="365c7-135">OUTPUTS</span></span>

### <span data-ttu-id="365c7-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="365c7-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="365c7-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="365c7-137">NOTES</span></span>

## <span data-ttu-id="365c7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="365c7-138">RELATED LINKS</span></span>
