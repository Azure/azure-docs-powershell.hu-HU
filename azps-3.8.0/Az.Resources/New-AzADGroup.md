---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 6496f2c65c5cfecb01ed68d0e47281fba72b7b63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014459"
---
# <span data-ttu-id="4707a-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="4707a-101">New-AzADGroup</span></span>

## <span data-ttu-id="4707a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4707a-102">SYNOPSIS</span></span>
<span data-ttu-id="4707a-103">Új Active Directory-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="4707a-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="4707a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4707a-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4707a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4707a-105">DESCRIPTION</span></span>
<span data-ttu-id="4707a-106">Új Active Directory-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="4707a-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="4707a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4707a-107">EXAMPLES</span></span>

### <span data-ttu-id="4707a-108">Példa 1 – új HIRDETÉSCSOPORT létrehozása</span><span class="sxs-lookup"><span data-stu-id="4707a-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="4707a-109">Létrehoz egy új HIRDETÉSCSOPORTOT a "MyGroupDisplayName" névvel és a "MyGroupNick" levelezési felhasználónévvel.</span><span class="sxs-lookup"><span data-stu-id="4707a-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="4707a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4707a-110">PARAMETERS</span></span>

### <span data-ttu-id="4707a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4707a-111">-DefaultProfile</span></span>
<span data-ttu-id="4707a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4707a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4707a-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4707a-113">-Description</span></span>
<span data-ttu-id="4707a-114">A csoport leírása.</span><span class="sxs-lookup"><span data-stu-id="4707a-114">The description for the group.</span></span>

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

### <span data-ttu-id="4707a-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4707a-115">-DisplayName</span></span>
<span data-ttu-id="4707a-116">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="4707a-116">The display name for the group.</span></span>

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

### <span data-ttu-id="4707a-117">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="4707a-117">-MailNickname</span></span>
<span data-ttu-id="4707a-118">A csoport levelezési beceneve.</span><span class="sxs-lookup"><span data-stu-id="4707a-118">The mail nickname for the group.</span></span> <span data-ttu-id="4707a-119">Nem szerepelhet az @ jel.</span><span class="sxs-lookup"><span data-stu-id="4707a-119">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="4707a-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4707a-120">-Confirm</span></span>
<span data-ttu-id="4707a-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4707a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4707a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4707a-122">-WhatIf</span></span>
<span data-ttu-id="4707a-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4707a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4707a-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4707a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4707a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4707a-125">CommonParameters</span></span>
<span data-ttu-id="4707a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4707a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4707a-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4707a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4707a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4707a-128">INPUTS</span></span>

### <span data-ttu-id="4707a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4707a-129">System.String</span></span>

## <span data-ttu-id="4707a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4707a-130">OUTPUTS</span></span>

### <span data-ttu-id="4707a-131">Microsoft. Azure. Command. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="4707a-131">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="4707a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4707a-132">NOTES</span></span>

## <span data-ttu-id="4707a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4707a-133">RELATED LINKS</span></span>
