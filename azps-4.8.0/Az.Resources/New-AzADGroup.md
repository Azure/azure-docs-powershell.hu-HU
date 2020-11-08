---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025058"
---
# <span data-ttu-id="19b33-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="19b33-101">New-AzADGroup</span></span>

## <span data-ttu-id="19b33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19b33-102">SYNOPSIS</span></span>
<span data-ttu-id="19b33-103">Új Active Directory-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="19b33-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="19b33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19b33-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19b33-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19b33-105">DESCRIPTION</span></span>
<span data-ttu-id="19b33-106">Új Active Directory-csoport létrehozása Az alábbi engedélyek szükségesek:</span><span class="sxs-lookup"><span data-stu-id="19b33-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="19b33-107">Azure Active Directory-diagram</span><span class="sxs-lookup"><span data-stu-id="19b33-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="19b33-108">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="19b33-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="19b33-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="19b33-109">Microsoft Graph</span></span>
  - <span data-ttu-id="19b33-110">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="19b33-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="19b33-111">PrivilegedAccess. ReadWrite. AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="19b33-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="19b33-112">Példák</span><span class="sxs-lookup"><span data-stu-id="19b33-112">EXAMPLES</span></span>

### <span data-ttu-id="19b33-113">Példa 1: új HIRDETÉSCSOPORT létrehozása</span><span class="sxs-lookup"><span data-stu-id="19b33-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="19b33-114">Létrehoz egy új HIRDETÉSCSOPORTOT a "MyGroupDisplayName" névvel és a "MyGroupNick" levelezési felhasználónévvel.</span><span class="sxs-lookup"><span data-stu-id="19b33-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="19b33-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19b33-115">PARAMETERS</span></span>

### <span data-ttu-id="19b33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b33-116">-DefaultProfile</span></span>
<span data-ttu-id="19b33-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19b33-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19b33-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="19b33-118">-Description</span></span>
<span data-ttu-id="19b33-119">A csoport leírása.</span><span class="sxs-lookup"><span data-stu-id="19b33-119">The description for the group.</span></span>

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

### <span data-ttu-id="19b33-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="19b33-120">-DisplayName</span></span>
<span data-ttu-id="19b33-121">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="19b33-121">The display name for the group.</span></span>

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

### <span data-ttu-id="19b33-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="19b33-122">-MailNickname</span></span>
<span data-ttu-id="19b33-123">A csoport levelezési beceneve.</span><span class="sxs-lookup"><span data-stu-id="19b33-123">The mail nickname for the group.</span></span> <span data-ttu-id="19b33-124">Nem szerepelhet az @ jel.</span><span class="sxs-lookup"><span data-stu-id="19b33-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="19b33-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19b33-125">-Confirm</span></span>
<span data-ttu-id="19b33-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19b33-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19b33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19b33-127">-WhatIf</span></span>
<span data-ttu-id="19b33-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19b33-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19b33-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19b33-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19b33-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b33-130">CommonParameters</span></span>
<span data-ttu-id="19b33-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19b33-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b33-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="19b33-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b33-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19b33-133">INPUTS</span></span>

### <span data-ttu-id="19b33-134">System. String</span><span class="sxs-lookup"><span data-stu-id="19b33-134">System.String</span></span>

## <span data-ttu-id="19b33-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19b33-135">OUTPUTS</span></span>

### <span data-ttu-id="19b33-136">Microsoft. Azure. Command. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="19b33-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="19b33-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19b33-137">NOTES</span></span>

## <span data-ttu-id="19b33-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19b33-138">RELATED LINKS</span></span>
