---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 50cb6a806522e8e8b0f3a792ad74e2543633f668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669406"
---
# <span data-ttu-id="f1899-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="f1899-101">New-AzADGroup</span></span>

## <span data-ttu-id="f1899-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1899-102">SYNOPSIS</span></span>
<span data-ttu-id="f1899-103">Új Active Directory-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1899-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="f1899-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1899-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1899-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1899-105">DESCRIPTION</span></span>
<span data-ttu-id="f1899-106">Új Active Directory-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1899-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="f1899-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1899-107">EXAMPLES</span></span>

### <span data-ttu-id="f1899-108">Példa 1 – új HIRDETÉSCSOPORT létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1899-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="f1899-109">Létrehoz egy új HIRDETÉSCSOPORTOT a "MyGroupDisplayName" névvel és a "MyGroupNick" levelezési felhasználónévvel.</span><span class="sxs-lookup"><span data-stu-id="f1899-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="f1899-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1899-110">PARAMETERS</span></span>

### <span data-ttu-id="f1899-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1899-111">-DefaultProfile</span></span>
<span data-ttu-id="f1899-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1899-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1899-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f1899-113">-DisplayName</span></span>
<span data-ttu-id="f1899-114">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="f1899-114">The display name for the group.</span></span>

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

### <span data-ttu-id="f1899-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="f1899-115">-MailNickname</span></span>
<span data-ttu-id="f1899-116">A csoport levelezési beceneve.</span><span class="sxs-lookup"><span data-stu-id="f1899-116">The mail nickname for the group.</span></span> <span data-ttu-id="f1899-117">Nem szerepelhet az @ jel.</span><span class="sxs-lookup"><span data-stu-id="f1899-117">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="f1899-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1899-118">-Confirm</span></span>
<span data-ttu-id="f1899-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1899-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1899-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1899-120">-WhatIf</span></span>
<span data-ttu-id="f1899-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1899-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1899-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1899-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1899-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1899-123">CommonParameters</span></span>
<span data-ttu-id="f1899-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1899-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1899-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1899-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1899-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1899-126">INPUTS</span></span>

### <span data-ttu-id="f1899-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f1899-127">System.String</span></span>

## <span data-ttu-id="f1899-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1899-128">OUTPUTS</span></span>

### <span data-ttu-id="f1899-129">Microsoft. Azure. Command. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="f1899-129">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="f1899-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1899-130">NOTES</span></span>

## <span data-ttu-id="f1899-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1899-131">RELATED LINKS</span></span>
