---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADGroup.md
ms.openlocfilehash: 751b1b7daff59861b3f8e480b27dc4c88d35709d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495680"
---
# <span data-ttu-id="9cb0c-101">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="9cb0c-101">New-AzureRmADGroup</span></span>

## <span data-ttu-id="9cb0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cb0c-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb0c-103">Új Active Directory-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="9cb0c-103">Creates a new active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cb0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cb0c-104">SYNTAX</span></span>

```
New-AzureRmADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb0c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cb0c-105">DESCRIPTION</span></span>
<span data-ttu-id="9cb0c-106">Új Active Directory-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="9cb0c-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="9cb0c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9cb0c-107">EXAMPLES</span></span>

### <span data-ttu-id="9cb0c-108">Példa 1 – új HIRDETÉSCSOPORT létrehozása</span><span class="sxs-lookup"><span data-stu-id="9cb0c-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzureRmADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="9cb0c-109">Egy új HIRDETÉSCSOPORTOT hoz létre a "MyGroupDisplayName" névvel és a levelek becenevevel " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="9cb0c-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="9cb0c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cb0c-110">PARAMETERS</span></span>

### <span data-ttu-id="9cb0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb0c-111">-DefaultProfile</span></span>
<span data-ttu-id="9cb0c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb0c-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9cb0c-113">-DisplayName</span></span>
<span data-ttu-id="9cb0c-114">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-114">The display name for the group.</span></span>

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

### <span data-ttu-id="9cb0c-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="9cb0c-115">-MailNickname</span></span>
<span data-ttu-id="9cb0c-116">A csoport levelezési beceneve.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="9cb0c-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9cb0c-117">-Confirm</span></span>
<span data-ttu-id="9cb0c-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb0c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb0c-119">-WhatIf</span></span>
<span data-ttu-id="9cb0c-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb0c-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb0c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb0c-122">CommonParameters</span></span>
<span data-ttu-id="9cb0c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cb0c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb0c-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cb0c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb0c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cb0c-125">INPUTS</span></span>

### <span data-ttu-id="9cb0c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9cb0c-126">System.String</span></span>

## <span data-ttu-id="9cb0c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cb0c-127">OUTPUTS</span></span>

### <span data-ttu-id="9cb0c-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="9cb0c-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="9cb0c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cb0c-129">NOTES</span></span>

## <span data-ttu-id="9cb0c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cb0c-130">RELATED LINKS</span></span>
