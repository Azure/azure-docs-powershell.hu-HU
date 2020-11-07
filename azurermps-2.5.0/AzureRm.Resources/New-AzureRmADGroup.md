---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: fa9f708355e9c2fd4df530955db1d893e7591740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849486"
---
# <span data-ttu-id="0bba4-101">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="0bba4-101">New-AzureRmADGroup</span></span>

## <span data-ttu-id="0bba4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0bba4-102">SYNOPSIS</span></span>
<span data-ttu-id="0bba4-103">Új Active Directory-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="0bba4-103">Creates a new active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bba4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0bba4-104">SYNTAX</span></span>

```
New-AzureRmADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bba4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0bba4-105">DESCRIPTION</span></span>
<span data-ttu-id="0bba4-106">Új Active Directory-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="0bba4-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="0bba4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0bba4-107">EXAMPLES</span></span>

### <span data-ttu-id="0bba4-108">Példa 1 – új HIRDETÉSCSOPORT létrehozása</span><span class="sxs-lookup"><span data-stu-id="0bba4-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzureRmADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="0bba4-109">Egy új HIRDETÉSCSOPORTOT hoz létre a "MyGroupDisplayName" névvel és a levelek becenevevel " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="0bba4-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="0bba4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0bba4-110">PARAMETERS</span></span>

### <span data-ttu-id="0bba4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bba4-111">-DefaultProfile</span></span>
<span data-ttu-id="0bba4-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0bba4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bba4-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0bba4-113">-DisplayName</span></span>
<span data-ttu-id="0bba4-114">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="0bba4-114">The display name for the group.</span></span>

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

### <span data-ttu-id="0bba4-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="0bba4-115">-MailNickname</span></span>
<span data-ttu-id="0bba4-116">A csoport levelezési beceneve.</span><span class="sxs-lookup"><span data-stu-id="0bba4-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="0bba4-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0bba4-117">-Confirm</span></span>
<span data-ttu-id="0bba4-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0bba4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bba4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bba4-119">-WhatIf</span></span>
<span data-ttu-id="0bba4-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0bba4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bba4-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0bba4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bba4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bba4-122">CommonParameters</span></span>
<span data-ttu-id="0bba4-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0bba4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bba4-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bba4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bba4-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bba4-125">INPUTS</span></span>

### <span data-ttu-id="0bba4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0bba4-126">System.String</span></span>

## <span data-ttu-id="0bba4-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bba4-127">OUTPUTS</span></span>

### <span data-ttu-id="0bba4-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="0bba4-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="0bba4-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0bba4-129">NOTES</span></span>

## <span data-ttu-id="0bba4-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bba4-130">RELATED LINKS</span></span>
