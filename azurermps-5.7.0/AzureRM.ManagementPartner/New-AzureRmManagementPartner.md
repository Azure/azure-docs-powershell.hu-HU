---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393044
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
ms.openlocfilehash: 9a6d6d0d21a38ac5ff41460021287e0701de6057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500540"
---
# <span data-ttu-id="89aa5-101">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="89aa5-101">New-AzureRmManagementPartner</span></span>

## <span data-ttu-id="89aa5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="89aa5-103">A Microsoft Partner Network (MPN) AZONOSÍTÓját társítja az aktuális hitelesített felhasználóhoz vagy szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="89aa5-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89aa5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89aa5-104">SYNTAX</span></span>

```
New-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89aa5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89aa5-105">DESCRIPTION</span></span>
<span data-ttu-id="89aa5-106">A Microsoft Partner Network (MPN) AZONOSÍTÓját társítja az aktuális hitelesített felhasználóhoz vagy szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="89aa5-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="89aa5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="89aa5-107">EXAMPLES</span></span>

### <span data-ttu-id="89aa5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="89aa5-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="89aa5-109">Felügyeleti partner felvétele</span><span class="sxs-lookup"><span data-stu-id="89aa5-109">Add a management partner</span></span> 

## <span data-ttu-id="89aa5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89aa5-110">PARAMETERS</span></span>

### <span data-ttu-id="89aa5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89aa5-111">-DefaultProfile</span></span>
<span data-ttu-id="89aa5-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89aa5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89aa5-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="89aa5-113">-PartnerId</span></span>
<span data-ttu-id="89aa5-114">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="89aa5-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89aa5-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89aa5-115">-Confirm</span></span>
<span data-ttu-id="89aa5-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89aa5-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89aa5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89aa5-117">-WhatIf</span></span>
<span data-ttu-id="89aa5-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89aa5-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89aa5-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89aa5-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89aa5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89aa5-120">CommonParameters</span></span>
<span data-ttu-id="89aa5-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89aa5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89aa5-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89aa5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89aa5-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89aa5-123">INPUTS</span></span>

### <span data-ttu-id="89aa5-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="89aa5-124">None</span></span>

## <span data-ttu-id="89aa5-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89aa5-125">OUTPUTS</span></span>

### <span data-ttu-id="89aa5-126">Microsoft. Azure. Command. Resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="89aa5-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="89aa5-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89aa5-127">NOTES</span></span>

## <span data-ttu-id="89aa5-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89aa5-128">RELATED LINKS</span></span>

[<span data-ttu-id="89aa5-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="89aa5-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="89aa5-130">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="89aa5-130">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="89aa5-131">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="89aa5-131">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
