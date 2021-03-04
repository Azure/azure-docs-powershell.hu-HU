---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 910453711e047f9be1694bed0c92c502694d8a6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930850"
---
# <span data-ttu-id="04373-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="04373-101">New-AzADGroup</span></span>

## <span data-ttu-id="04373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04373-102">SYNOPSIS</span></span>
<span data-ttu-id="04373-103">Új Active Directory-csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="04373-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="04373-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04373-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04373-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04373-105">DESCRIPTION</span></span>
<span data-ttu-id="04373-106">Új Active Directory-csoportot hoz létre. Az alábbiakban a szükséges engedélyeket olvashatja:</span><span class="sxs-lookup"><span data-stu-id="04373-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="04373-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="04373-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="04373-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="04373-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="04373-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="04373-109">Microsoft Graph</span></span>
  - <span data-ttu-id="04373-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="04373-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="04373-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="04373-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="04373-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04373-112">EXAMPLES</span></span>

### <span data-ttu-id="04373-113">1. példa: Új AD-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="04373-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="04373-114">Létrehoz egy új AD-csoportot a "MyGroupDisplayName" névvel és a "MyGroupNick" e-mail becenévvel.</span><span class="sxs-lookup"><span data-stu-id="04373-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="04373-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04373-115">PARAMETERS</span></span>

### <span data-ttu-id="04373-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04373-116">-DefaultProfile</span></span>
<span data-ttu-id="04373-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04373-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04373-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="04373-118">-Description</span></span>
<span data-ttu-id="04373-119">A csoport leírása.</span><span class="sxs-lookup"><span data-stu-id="04373-119">The description for the group.</span></span>

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

### <span data-ttu-id="04373-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="04373-120">-DisplayName</span></span>
<span data-ttu-id="04373-121">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="04373-121">The display name for the group.</span></span>

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

### <span data-ttu-id="04373-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="04373-122">-MailNickname</span></span>
<span data-ttu-id="04373-123">A csoport e-mail-beceneve.</span><span class="sxs-lookup"><span data-stu-id="04373-123">The mail nickname for the group.</span></span> <span data-ttu-id="04373-124">Nem tartalmazhatja a @ jelet.</span><span class="sxs-lookup"><span data-stu-id="04373-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="04373-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04373-125">-Confirm</span></span>
<span data-ttu-id="04373-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="04373-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04373-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04373-127">-WhatIf</span></span>
<span data-ttu-id="04373-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="04373-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04373-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04373-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04373-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04373-130">CommonParameters</span></span>
<span data-ttu-id="04373-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04373-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04373-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04373-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04373-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04373-133">INPUTS</span></span>

### <span data-ttu-id="04373-134">System.String</span><span class="sxs-lookup"><span data-stu-id="04373-134">System.String</span></span>

## <span data-ttu-id="04373-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04373-135">OUTPUTS</span></span>

### <span data-ttu-id="04373-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="04373-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="04373-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04373-137">NOTES</span></span>

## <span data-ttu-id="04373-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04373-138">RELATED LINKS</span></span>
